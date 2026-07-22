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

## Deployment

```sh
kubectl apply -f ocm-single-component/deploy/bootstrap.yaml
kubectl apply -f ocm-single-component/deploy/instance.yaml
```
