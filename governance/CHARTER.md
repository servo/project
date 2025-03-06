# Technical Charter (the "Charter") for Servo Project

*Adopted June 15, 2023*

This Charter sets forth the responsibilities and procedures for
technical contribution to, and oversight of, the Servo open source
project, which has been established as a project of Linux Foundation
Europe, a Belgian private stichting headquartered at Kunstlaan 56,
Brussels ("LF Europe"). All contributors (including
committers, maintainers, and other technical positions) and other
participants in the Project (collectively, "Collaborators") must comply
with the terms of this Charter.

## 1.  Mission and Scope of the Project

a.  The mission of the Project is to provide an independent, modular, embeddable web engine, which allows developers to deliver content and applications using web standards.

b.  The scope of the Project includes collaborative development under the Project License (as defined herein) supporting the mission, including documentation, testing, integration and the creation of other artifacts that aid the development, deployment, operation or adoption of the open source project.

## 2.  Technical Steering Committee

a.  The Technical Steering Committee (the "TSC") will be responsible for all technical oversight of the open source Project.

b.  The TSC voting members are as set forth within the [`servo/project` repository](https://github.com/servo/project/). The TSC may choose an alternative approach for determining the voting members of the TSC, and any such alternative approach will be documented in this repository. Any meetings of the Technical Steering Committee will be open to the public, and can be conducted electronically, via teleconference, or in person.

c.  The Project will involve Collaborators, Contributors and Maintainers. The TSC may adopt or modify roles so long as the roles are documented in the [`servo/project` repository](https://github.com/servo/project/).

d.  Participation in the Project through becoming a Collaborator, Contributor or Maintainer is open to anyone so long as they abide by the terms of this Charter.

e.  The TSC may (1) establish work flow procedures for the submission, approval, and closure/archiving of projects, (2) set requirements for the promotion of Collaborators to Contributor status or Contributors to Maintainer status, as applicable, and (3) amend, adjust, refine and/or eliminate the roles of Contributors, and Maintainers, and create new roles, and publicly document any TSC roles, as it sees fit.

f.  The TSC will annually elect a TSC Chair, who will preside over meetings of the TSC and will serve until their resignation or replacement by the TSC. The TSC Chair, or any other TSC member so designated by the TSC, will serve as the primary communication contact and any funding effort supporting the Project.

g.  Responsibilities: The TSC will be responsible for all aspects of oversight relating to the Project, which may include:

> i. coordinating the technical direction of the Project;
>
> ii.  approving project or system proposals (including, but not limited to, incubation, deprecation, and changes to a sub-project's scope);
>
> iii. organizing sub-projects and removing sub-projects;
>
> iv. creating sub-committees or working groups to focus on cross-project technical issues and requirements;
>
> v. appointing representatives to work with other open source or open standards communities;
>
> vi. establishing community norms, workflows, issuing releases, and security issue reporting policies;
>
> vii.  approving and implementing policies and processes for contributing (to be published in the [`servo/project` repository](https://github.com/servo/project/)) and coordinating with LF Europe to resolve matters or concerns that may arise as set forth in Section 7 of this Charter;
>
> viii. discussions, seeking consensus, and where necessary, voting on technical matters relating to the code base that affect multiple projects; and
>
> ix. coordinating any marketing, events, or communications regarding the Project.

## 3.  TSC Voting

a.  While the Project aims to operate as a consensus-based community, if any TSC decision requires a vote to move the Project forward, the voting members of the TSC will vote on a one vote per voting member basis.

b.  Quorum for TSC meetings requires at least fifty percent of all voting members of the TSC to be present. The TSC may continue to meet if quorum is not met but will be prevented from making any decisions at the meeting.

c.  Except as provided in Section 7.c. and 8.a, decisions by vote at a meeting require a majority vote of those in attendance, provided quorum is met. Decisions made by electronic vote without a meeting require a majority vote of all voting members of the TSC.

d.  In the event a vote cannot be resolved by the TSC, any voting member of the TSC may refer the matter to the Series Manager for assistance in reaching a resolution.

## 4.  Compliance with Policies

a.  Contributors will comply with the policies of LF Europe as may be adopted and amended by LF Europe, including, without limitation the policies listed at https://lfprojects.org/policies/.

b.  The TSC may adopt a code of conduct ("CoC") for the Project, which is subject to approval by LF Europe. In the event that a Project-specific CoC has not been approved, the LF Europe Code of Conduct listed at https://lfprojects.org/policies will apply for all Collaborators in the Project.

c.  When amending or adopting any policy applicable to the Project, LF Europe will publish such policy, as to be amended or adopted, on its web site at least 30 days prior to such policy taking effect; provided, however, that in the case of any amendment of the Trademark Policy or Terms of Use of LF Europe, any such amendment is effective upon publication on LF Europe's web site.

d.  All Collaborators must allow open participation from any individual or organization meeting the requirements for contributing under this Charter and any policies adopted for all Collaborators by the TSC, regardless of competitive interests. Put another way, the Project community must not seek to exclude any participant based on any criteria, requirement, or reason other than those that are reasonable and applied on a non-discriminatory basis to all Collaborators in the Project community.

e.  The Project will operate in a transparent, open, collaborative, and ethical manner at all times. The output of all Project discussions, proposals, timelines, decisions, and status should be made open and easily visible to all. Any potential violations of this requirement should be reported immediately to LF Europe.

## 5.  Community Assets

a.  LF Europe will hold title to all trade or service marks used by the Project ("Project Trademarks"), whether based on common law or registered rights. Project Trademarks will be transferred and assigned to LF Europe to hold on behalf of the Project. Any use of any Project Trademarks by Collaborators in the Project will be in accordance with the license from LF Europe and inure to the benefit of LF Europe.

b.  The Project will, as permitted and in accordance with such license from LF Europe, develop and own all Project GitHub and social media accounts, and domain name registrations created by the Project community.

c.  Under no circumstances will LF Europe be expected or required to undertake any action on behalf of the Project that is inconsistent with the tax-exempt status or purpose, as applicable, of the Joint Development Foundation or LF Europe.

## 6.  General Rules and Operations.

a.  The Project will:

> i. engage in the work of the Project in a professional manner consistent with maintaining a cohesive community, while also maintaining the goodwill and esteem of LF Europe and other partner organizations in the open source community; and
>
> ii. respect the rights of all trademark owners, including any branding and trademark usage guidelines.

## 7.  Intellectual Property Policy

a.  Collaborators acknowledge that the copyright in all new contributions will be retained by the copyright holder as independent works of authorship and that no contributor or copyright holder will be required to assign copyrights to the Project.

b.  Except as described in Section 7.c., all contributions to the Project are subject to the following:

> i. All new inbound code contributions to the Project must be made as follows:
>
> > 1.  contributions to the main Servo code base will be made under the Mozilla Public License, Version 2.0, available in the "LICENSE" file within the Project's code repository (the "Project License"); and
> >
> > 2.  contributions to subproject code bases that are not part of the main servo code base will be made under an open source license (approved as an open source license by the Open Source Initiative) that has been approved by the TSC.
>
> ii. All new inbound code contributions must also be accompanied by a Developer Certificate of Origin (http://developercertificate.org) sign-off in the source code system that is submitted through a TSC-approved contribution process which will bind the authorized contributor and, if not self-employed, their employer to the applicable license;
>
> iii. All outbound code will be made available under the Project License.
>
> iv.  Documentation will be received and made available by the Project under the Creative Commons Attribution 4.0 International License (available at http://creativecommons.org/licenses/by/4.0/).
>
> v. The Project may seek to integrate and contribute back to other open source projects ("Upstream Projects"). In such cases, the Project will conform to all license requirements of the Upstream Projects, including dependencies, leveraged by the Project. Upstream Project code contributions not stored within the Project's main code repository will comply with the contribution process and license terms for the applicable Upstream Project.

c.  The TSC may approve the use of an alternative license or licenses for inbound or outbound contributions on an exception basis. To request an exception, please describe the contribution, the alternative open source license(s), and the justification for using an alternative open source license for the Project. License exceptions must be approved by a two-thirds vote of the entire TSC.

d.  Contributed files should contain license information, such as SPDX short form identifiers, indicating the open source license or licenses pertaining to the file.

## 8.  Amendments

a.  This charter may be amended by a two-thirds vote of the entire TSC and is subject to approval by LF Europe.
