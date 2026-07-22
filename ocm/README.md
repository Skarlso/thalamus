<!--
# SPDX-FileCopyrightText: Copyright 2026 SAP SE or an SAP affiliate company and cobaltcore-dev contributors
#
# SPDX-License-Identifier: Apache-2.0
-->

# OCM Separate Components

These mirror whatever is in helmfile.yaml.gotmpl for now.

## Building

Running from root, building blocks first, then the root:

```sh
# add the main components first
ocm add component-version \
  --constructor ocm/component-constructor.yaml \
  --working-directory . \
  --repository <target>

# and then you can add the root component that bundles the existing things
ocm add component-version \
  --constructor ocm/root-component-constructor.yaml \
  --working-directory . \
  --repository <target>
```
