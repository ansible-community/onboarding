# Ansible Project Onboarding

Welcome to the Ansible ecosystem of projects! This document guides you 
through the steps to take to become part of the Ansible ecosystem.

# Why be part of the Ansible ecosystem
Being a part of the Ansible ecosystem means you are tapping into a large and
thriving community of passionate people working and volunteering in Ansible.

The major benefits of becoming part of the Ansible ecosystem include:

* A presence on docs.ansible.com/ecosystem for your project documentation,
 as well as being part of the official Ansible ReadTheDocs space.
* A presence on the (future) Ansible.com to introduce your project.
* Dedicated communications channels (chat and forum) to communicate with your
community and attract other community members to your project.



# Setting up your GitHub repository

The Ansible ecosystem projects exist in the following two GitHub repositories:

* ansible - Access is controlled by Red Hat
* ansible-community - Access is controlled by the community, 
under Red Hat sponsorship

We recommend most Ansible projects use the ansible-community GitHub repository.
Repository transfers are available if your project already exists somewhere else in GitHub.

For new projects, use the [project-template](https://github.com/ansible-community/project-template) to 
create a project with the default files.

## Other repository settings

* Open up issues and PRs for task tracking and community contributions.
* Disable the GitHub discussions. Use the 
[Ansible Community forum](https://forum.ansible.com/) for community and project discussions.
* Disable the repo wiki for project documentation. See the sections below on 
documentation and using the Ansible forum.

## Common files

*Note:* If you use the Ansible GitHub project template, these files are included
in the created repository.

All Ansible ecosystem projects MUST include the following files:

* [COPYING](https://github.com/ansible-community/onboarding/blob/main/COPYING) - 
If your project does not already have a license, we recommend
[GPLv3](https://www.gnu.org/licenses/gpl-3.0.txt).
* [CONTRIBUTING](https://github.com/ansible-community/onboarding/blob/main/CONTRIBUTING.md) - 
This can be the complete contributor details, if it is short. 
Otherwise, it can point to your project documentation which should include
 a Contributor guide. It also should include your Ansible Matrix chat channels and 
 [Ansible Community Forum](https://forum.ansible.com/) tags.
* [Code of Conduct](https://github.com/ansible-community/onboarding/blob/main/CODE-OF-CONDUCT.md) - 
MUST link to the [Ansible code of conduct](https://docs.ansible.com/ansible/devel/community/code_of_conduct.html). 
    Do not copy the CoC.
[DCO](https://github.com/ansible-community/onboarding/blob/main/DCO) - The Developer 
Certificate of Origin. Do not modify this text.
* [README.md](https://github.com/ansible-community/onboarding/blob/main/README.md) - 
A basic introduction to your project, communication channels, and so on.
It should include your matrix channel if your project has one, and  recommended forum tags,
with a link to the [Ansible Community Forum](https://forum.ansible.com/). 
You should not use the README.md for project documentation (user guide, for example),
 but instead set up a docsite. Even if the docsite is basic, it's a start others can
contribute to.

## Optional other steps
While not required, you should consider adding the following to your project repository:

  * Add a [SECURITY.md](https://github.com/ansible-community/onboarding/blob/main/SECURITY.md) 
  to let a security reporter know how to proceed.
  * Provide Issue and PR templates to improve the contributor experience.


# Creating your community space

Each Ansible ecosystem project should have ways to communicate and collaborate
 with community members. The following sections cover ways to interact
 and build your project community.

## Matrix
Our preferred chat option for Ansible projects is Matrix. Your matrix room name
should match your project name. You can set up your own matrix room or 
contact the community team in the forum to be officially added to the Ansible matrix space.
By doing so your project gets:

- Added to the Space (which functions as the directory)
- An ansible.com room alias
- The Admin bot to give you moderation/spam coverage
- A Matrix meetbot to help you create meeting summaries and logs, automatically posted to the forum
- (eventually) A room icon based on our template

Contact the community team in the forum to coordinate a new Matrix room for your project.

## Using the Ansible forum
Ansible introduced the [Ansible Community Forum](https://forum.ansible.com/).
This is a great place to interact with community members and grow your own project
community. We have a [set of videos](https://forum.ansible.com/t/discourse-video-demos/102)
 to help you learn how to use the forum, as well as 
 [some other tips](https://forum.ansible.com/tag/forum-tips). 

Reach out to the community team to request new tag(s) for your project in the forum.

## Working Groups
Not every project requires a working group. We advise projects to use
the Ansible forum and GitHub issues as much as possible
to be accessible to all timezones. 

A working group is your group of contributors, along with ways to coordinate
your work. This includes a tag or group for the forum and optionally a matrix room. 
 
Synchronous project meetings are an option and you can use the 
[Forum Events calendar](https://forum.ansible.com/c/events/8) to announce your meetings. 
Be aware that any real-time meetings will tend to exclude contributors not in or around the 
meeting timezone.

If you do decide to have a synchronous meeting, add your working group meeting 
time to the [shared Ansible ICS calender in GitHub](https://github.com/ansible/community/tree/main/meetings).

You can also include your meeting calendar and agenda in the forum. 
See [the DaWGs agenda](https://forum.ansible.com/t/documentation-working-group-agenda/153)
for one possible way to do this.

If you run meetings on Matrix, you can invite the Ansible Matrix bot(antsibot)
to autogenerate a meeting summary that is then posted in the forum
[Workflows and Logs](https://forum.ansible.com/c/workflow/15) category. We recommend that
that you edit the topic to add your project tag and the `meeting` tag to improve findability.

## Raise awareness about your project

Use the following communication options to let people know about your Ansible project:

 * Announce your project to The Bullhorn.
 * Ask the community team to announce your project in Mastodon.
 * Join the community WG meeting to announce your new project.


# Nurture and grow your community

* Use the communications options listed to keep people up to date on 
your community and project accomplishments. 
This includes Matrix, Bullhorn, and forum updates for:

    * New releases or changes
    * Requesting help
    * Kudos for community contributors
    * Any other ideas/accomplishments/calls for help for your project.

* Work in the community...decide in the community - The more your project 
team can engage in the open, the stronger your community will be. This includes
discussing issues, features, and in general, working as a team by default, 
in your matrix and forum areas. If possible, you can empower the community 
to help develop project roadmaps, for example. 
* Ask for help! Some people may not realize you are looking for help in areas
 if you do not ask. And specific asks/issues work better than generic calls for help.

# Creating your documentation

We have a [Documentation toolkit](./docs_toolkit.md) to help you design 
and publish your documentation to ReadTheDocs as part of the Ansible ecosystem.

# Project governance
These are suggestions on how to govern your projects for an inclusive community.

* Give trusted contributors merge rights.
* Enable CI in your github repo to automate testing/validation where possible.
* Discourage PR owners from merging their own PRs. Each PR should have 
one or more approvals before merging.
* Have a project roadmap!
