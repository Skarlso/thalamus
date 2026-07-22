<!--
# SPDX-FileCopyrightText: Copyright 2026 SAP SE or an SAP affiliate company and cobaltcore-dev contributors
#
# SPDX-License-Identifier: Apache-2.0
-->

# OCM Single Component

## Building

Running from the repository root:

```sh
ocm add component-version \
  --constructor ocm-single-component/component-constructor.yaml \
  --working-directory . \
  --repository <target>
```

## Before Deployment

In order for ocm to be able to apply and create RGDs, you need extend its service account with the necessary RBAC.
To do that, simply apply the [custom-rbac.yaml](deploy/custom-rbac.yaml) file.

```
kubectl apply -f ./deploy/custom-rbac.yaml
```

Next, you need to create the `thalamus` namespace.

```
kubectl create ns thalamus
```

Lastly, `ocm add component-version` adds all components in `private` mode initially. For a demo, instead of configuring
credentials, for now, it's easier to simply go through the created component version objects and make them public.

There are ~11 components currently, so this is a bit cumbersome by hand. Here is a handy little script:

```bash

```

## Deployment

```sh
kubectl apply -f ocm-single-component/deploy/bootstrap.yaml
kubectl apply -f ocm-single-component/deploy/instance.yaml
```

## Image Localization

Every referenced component declares its container images as `ociImage`
resources with an `ociArtifact` access, digest-pinned at build time. The single
RGD resolves each image through a `Resource` object
(`additionalStatusFields: oci: resource.access.toOCI()`, dependency images via
`referencePath`) and feeds registry, repository and digest into the
HelmRelease values.

Without copied resources the access points upstream and `toOCI()` resolves the
upstream image, digest-pinned. After a transfer with `--copy-resources` the
access is rewritten to the target registry and the same RGD deploys the
localized images unchanged.

Charts without a dedicated digest value (node-feature-discovery, external-dns,
open-webui, agentgateway, the gpu-operator deployment itself) get the combined
`repository:tag@digest` reference smuggled through their tag field; container
runtimes resolve such references by digest.

Deliberately not localized: the NVIDIA driver image (the operator appends an
OS suffix to the tag at runtime, so the default tag is not a pullable
artifact), license-gated or hardware-conditional gpu-operator images (vgpu,
kata, vfio, standalone dcgm), and subcharts disabled by our values (grafana,
node-exporter, ollama, pipelines, tika, terminals).