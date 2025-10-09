# Servo Governance

The Servo project is governed by the **Technical Steering Committee (TSC)**, who are responsible for technical oversight of the project as laid out in the [**charter**](CHARTER.md). The project follows a [Consensus Seeking](https://en.wikipedia.org/wiki/Consensus-seeking_decision-making) decision making model.

The TSC meets in public, and meetings are announced with an issue on this repository. All [meeting minutes are published here](tsc/README.md).

The TSC can form subcommittees for detailed discussion of issues. Currently there are no active subcommittees.

The TSC has the following rules:
* **Maximum size**: Servo TSC maximum size would be **20 people**. We don't limit the number of people from the same organization in the TSC.
* **Vote limit**: When there's a decision by vote at a meeting, the maximum valid votes per organization is 1/3 of those in attendance, provided quorum is met. When there's a decision made by electronic vote, the maximum valid votes per organization is 1/3 of all voting members of the TSC.
  * E.g. Right now there are 17 members on the TSC, and 6 are from Igalia. If there's an electronic vote only 5 votes from Igalia would be valid.

Servo is a [Linux Foundation Europe Project](https://linuxfoundation.eu/en/projects).

The Servo project stablishes three levels of collaboration as described below.

## Contributors

People that are collaborating in the project development and have permissions to run try jobs and triage issues adding the correct labels.

### Current Members

Current **Contributors** are listed in [the `CONTRIBUTORS.md` file](CONTRIBUTORS.md).

### Requirements

To be recognized with **Contributor** status, a community member must demonstrate a significant number of nontrivial code contributions which would benefit from access to try jobs, or consistent nontrivial participation in issue reporting and triage.

### Nomination

A **Maintainer** requests the addition of a new **Contributor** in the private *Maintainers* channel in Zulip, listing the number of nontrival contributions by that person. A person may also request that a **Maintainer** nominates them and vouch for them. If no objections are raised within one week, the person is added to the **Contributors** team. Additionally, if four other maintainers express support after at least two days have elapsed then there is no need to wait out the remaining time.

### Removal

People will be removed from this team after six months of no activity. A majority of **Maintainers** can also vote to remove a **Contributor**.

## Maintainers

People that can review, approve and merge contributions to the Servo project.

### Current Members

Current **Maintainers** are listed in [the `MAINTAINERS.md` file](MAINTAINERS.md).

### Requirements

To be recognized with **Maintainer** status, a community member must demonstrate expertise in at least one area of Servo (usually via multiple code contributions or technical investigations in a particular crate or subcomponent) and perform several code reviews of nontrivial PRs with an existing reviewer shadowing.

For some of our subprojects of Servo, it useful to have a group with maintainer permissions for a subset of our repositories. To add or remove a **Maintainer** in these cases, we'll create a separated team ("repo Maintainers") and follow a similar nomination process.

### Nomination

A **Maintainer** has to nominate a person listing the main highlights of their work and their number of contributions in the private *Maintainers* channel in Zulip. Two more **Maintainers** must support the proposal. If no objections are raised within one week, the person is added to the **Maintainers** team.

### Removal

People will be removed from this team after one year of no activity. A majority of **Maintainers** can also vote to remove a **Maintainer**.

## Technical Steering Committee Members

People that have voting power in the governing body.

### Current Members

Current **TSC Members** are listed in [the `TSC-MEMBERS.md` file](TSC-MEMBERS.md).

### Requirements

To be recognized as **TSC Member**, a community member must demonstrate commitment and understanding of the Servo project by having participated as a Maintainer for a significant amount of time.

The TSC can also nominate *Invited Experts* who are not working directly on Servo in a technical way, but can provide insight and help with coordination. The nomination process is the same as for other **TSC Members**.

### Nomination

A **TSC Member** nominates a person in the private *TSC* channel in Zulip explaining the reasons and main highlights of their participation in the project. A majority of the **TSC Members** must approve the addition. If the vote succeeds and no objections are raised within one week, the person is added to the **TSC Members** team.

### Removal

People will be removed from this team after one year of no activity, and would be recognized as **Emeritus TSC Members**. A majority of **TSC Members** can also vote to remove a **TSC Member**.

## Administrators

This is a smaller group of people group of people (maximum 5) that have administrator permissions in the Servo organization and repositories. Administrators are also assigned [ownership](https://github.com/orgs/servo/people?query=role%3Aowner) of the Servo GitHub organization.

In addition, as long as [Linux Foundation Europe](https://github.com/LF-Europe) hosts the project, it is also included in the list of administrators as well.

### Requirements

To be assigned **Administrator** status, a community member must have been a **TSC Member** for a significant amount of time and have the trust of the Servo community.

### Nomination

If there's an available administrator slot, a **TSC Member** can nominate a new administrator in the private *TSC* Zulip channel. The nomination should explain why that person should become **Administrator**. A majority of the **TSC Members** must approve the addition. If the vote succeeds and no objections are raised within one week, the person is added to the **Administrators** team.

### Removal

Administrators can be removed in several ways:
 - They are automatically removed after one year of inactivity.
 - A majority of the **TSC** can vote to remove an **Administrator**.
 - Any **Administrator** can choose to step down by sending a message to the private *TSC* Zulip channel.

