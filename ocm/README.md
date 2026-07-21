<!--
# SPDX-FileCopyrightText: Copyright 2026 SAP SE or an SAP affiliate company and cobaltcore-dev contributors
#
# SPDX-License-Identifier: Apache-2.0
-->

# OCM Components

These mirror whatever is in helmfile.yaml.gotmpl for now.

## Building

Running from root:

```sh
# transfer the main component
ocm add component-version \
  --constructor ocm/component-constructor.yaml \
  --working-directory . \
  --repository <target>
```

Alternatively, everything can be defined in a single constructor file.

Right now, the RGD contains hardcoded values yaml data, but in a real environment we would leverage HelmRelease's
ability to layer helm value file applies like this:

```yaml
spec:
  valuesFrom:
    - kind: ConfigMap
      name: prod-env-values
      valuesKey: values-prod.yaml
    - kind: Secret
      name: prod-tls-values
      valuesKey: crt
      targetPath: tls.crt
      optional: true
    - kind: ConfigMap
      name: app-config-source
      valuesKey: application.yml
      targetPath: 'externalConfig.application\.yml.content'
      literal: true
```

https://fluxcd.io/flux/components/helm/helmreleases/#values

Whatever imperative approach exists would hence deal with applying and setting up the right configmap values for the
selected environment. The ConfigMAp would not live as a resource in the component it's an expected cog piece.

ACTUALLY.

Expose the configurable options in the RGD as parameters and the Instance would be where the configuration lives.

```yaml
apiVersion: kro.run/v1alpha1
kind: Thalamus
metadata:
  name: thalamus
  namespace: thalamus
spec:
  version: "0.1.0"
  repository:
    baseUrl: http://registry:5000
    type: OCIRegistry
  insecureRegistry: true
  externalDns:
    enabled: false
  openWebui:
    enabled: true
```

