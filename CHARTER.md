<!--
SPDX-FileCopyrightText: Copyright 2026 SAP SE or an SAP affiliate company and cobaltcore-dev contributors

SPDX-License-Identifier: Apache-2.0
-->

# Technical Charter for Thalamus

**Adoption Date:** August 21, 2026
**Organization:** Linux Foundation Europe

This Technical Charter (the "Charter") sets forth the responsibilities and procedures for technical contribution to, and oversight of, the Thalamus open source project (the "Project"), which has been established as a project of Linux Foundation Europe. Linux Foundation Europe has agreed to act as the "Sponsoring Organization" for the Project. All community participants must adhere to the policies and procedures of Linux Foundation Europe, as may be adopted and amended from time to time.

## 1. Mission

The mission of Thalamus is to provide a vendor-neutral, Kubernetes-native inference service for sovereign LLM deployments, ensuring that model weights, prompts, and context remain protected and within the deployment perimeter. 
Thalamus integrates natively with CobaltCore, Greenhouse, and the broader NeoNephos ecosystem, and supports Nvidia, AMD, and Intel infrastructure.

## 2. Technical Steering Committee

**2.1** The Technical Steering Committee (the "TSC") is responsible for all technical oversight of the Project.

**2.2** The TSC voting members are initially as listed in the OWNERS.md file within the Project repository. The TSC may choose an alternative approach for determining the voting membership of the TSC, and any such alternative approach will be documented in the OWNERS.md file.

**2.3** At the inception of the Project, the Sponsoring Organization will appoint the initial TSC voting members. If the Technical Advisory Council (TAC) of Linux Foundation Europe has adopted a Project Lifecycle Policy ("Lifecycle Policy"), the TSC will manage the Project in compliance with that policy.

**2.4** Any meetings of the TSC are intended to be open to the public and may be conducted electronically, via teleconference, or in person.

**2.5** TSC projects generally will involve contributors, code owners, and a TSC. The TSC may adopt or modify roles so long as the roles are documented in the CONTRIBUTING.md file.

**2.6** Responsibilities of the TSC include:
- Coordinating the technical direction of the Project;
- Approving project or system proposals and releases;
- Organizing sub-projects and removing sub-projects;
- Creating sub-committees or working groups to focus on cross-project technical issues;
- Appointing representatives to work with other open source or open standards communities;
- Establishing community norms, workflows, issuing releases, and security issue reporting policies;
- Approving and implementing policies and processes for contributing;
- Discussing, seeking consensus, and where necessary, voting on technical matters relating to the code base;
- Coordinating with the Sponsoring Organization on any marketing, events, or communications regarding the Project.

## 3. TSC Voting

**3.1** While the Project aims to operate as a consensus-based community, if any TSC decision requires a vote to move the Project forward, the voting members of the TSC will vote on a one-vote-per-member basis.

**3.2** Quorum for TSC meetings requires at least fifty percent of all TSC voting members to be present. The TSC may continue to meet if quorum is not met, but will be prevented from making any decisions requiring a vote at the meeting.

**3.3** Except as provided in Section 6.3 and Section 7, decisions by vote at a meeting require a majority vote of those in attendance, provided quorum is met. Decisions made by electronic vote without a meeting require a majority vote of all TSC voting members.

**3.4** In the event a vote cannot be resolved by the TSC, any voting member of the TSC may refer the matter to the TAC for assistance in reaching a resolution.

## 4. Compliance with Policies

**4.1** Contributors will comply with the policies of Linux Foundation Europe as may be adopted and amended from time to time. Such policies include the Linux Foundation Antitrust Policy available at [https://www.linuxfoundation.org/antitrust-policy/](https://www.linuxfoundation.org/antitrust-policy/).

**4.2** The TSC will adopt a written Code of Conduct ("CoC") for the Project, which may be (i) the Code of Conduct for the Project developed and adopted by the TSC, or (ii) the Code of Conduct made available by the Sponsoring Organization for use by its Projects. The Project will comply with the CoC. In the event that the TSC has not adopted a CoC, the Linux Foundation Europe Code of Conduct will apply. The current CoC for Thalamus is the [SAP Open Source Code of Conduct](https://github.com/SAP/.github/blob/main/CODE_OF_CONDUCT.md).

**4.3** When amending or adopting any policy applicable to the Project, Linux Foundation Europe will publish such policy, as to be inclusive of all Project participants.

**4.4** All participants must allow open participation from any individual or organization meeting the requirements for contributing under this Charter, regardless of competitive interests. Put another way, the Project community must not seek to exclude any participant based on any criteria, requirement, or reason other than those that are reasonable and applied on a non-discriminatory basis to all participants in the Project community.

**4.5** The Project will operate in a transparent, open, collaborative, and ethical manner at all times. The output of all Project discussions, proposals, timelines, decisions, and status will be made publicly available. Any decisions made by electronic vote will be publicly published.

## 5. Community Assets

**5.1** Linux Foundation Europe will hold title to all trade or service marks used by the Project ("Project Trademarks"), whether based on common law or registered rights. Project Trademarks will be transferred and assigned to Linux Foundation Europe to hold on behalf of the Project. Any use of any Project Trademarks by participants in the Project will be in accordance with the license from Linux Foundation Europe and inure to the benefit of Linux Foundation Europe.

**5.2** The Project will, as permitted and in accordance with such license from Linux Foundation Europe, develop and own all Project GitHub and social media accounts, and domain name registrations created by the Project community.

**5.3** Under no circumstances will Linux Foundation Europe be expected or required to undertake any action on behalf of the Project that is inconsistent with the tax-exempt status or purpose, if any, of the Sponsoring Organization.

## 6. Intellectual Property Policy

**6.1** Participants acknowledge that the copyright in all new contributions will be retained by the copyright holder as independent works of authorship and that no contributor is required to assign copyrights to the Project.

**6.2** Except as described in Section 6.3, all contributions to the Project are subject to the following:
- All new inbound code contributions to the Project must be made using the Apache License, Version 2.0 (available at [https://www.apache.org/licenses/LICENSE-2.0](https://www.apache.org/licenses/LICENSE-2.0)) (the "Project License").
- All new inbound code contributions must also be accompanied by a Developer Certificate of Origin ([https://developercertificate.org](https://developercertificate.org)) sign-off in the source code system that is submitted through to the TSC-approved contribution process for the Project.
- All outbound code will be made available under the Project License.
- Documentation will be received and made available by the Project under the Creative Commons Attribution 4.0 International License (available at [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)).
- The TSC may approve the use of an alternative license or licenses for inbound or outbound contributions on an exception basis. To request an exception, please describe the contribution, the alternative open source license(s), and the justification for using an alternative open source license for the Project. License exceptions must be approved by a two-thirds vote of the entire TSC.
- Contributed files should contain license information, such as SPDX short form identifiers, indicating the open source license or licenses pertaining to the file.

**6.3** The TSC is permitted to allow larger inbound contributions of existing open source projects, provided that any such contribution is licensed under an open source license that is approved by the Open Source Initiative (OSI).

## 7. Amendments

This Charter may be amended by a two-thirds vote of the entire TSC and is subject to approval by Linux Foundation Europe.
