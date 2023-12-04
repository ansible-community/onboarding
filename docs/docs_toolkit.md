# Documenting your project

This section helps you add documentation to your Ansible project or improve your existing documentation.
The onboarding [project-template](https://github.com/ansible-community/project-template)
in GitHub gives you the scaffolding files to start your documentation effort. 

## Creating new documentation projects

Ansible projects starting a new documentation effort should follow these guidelines:

* Markdown is simple, ubiquitous, and familiar to most contributors. For these reasons
 the Ansible community team recommends markdown as the format for documentation.
* [mkdocs](https://www.mkdocs.org/getting-started/) is the recommended tool for building 
the documentation from markdown.
* [ReadtheDocs](https://readthedocs.org/) is the recommended place to publish documentation
 for Ansible projects.
* The [Ansible style guide](https://docs.ansible.com/ansible/latest/dev_guide/style_guide/index.html) 
is available to help ensure your project is well-written and follows technical documentation guidelines.

Follow these steps to set up your documentation if you do not use the GitHub project-template:

1. Create a ``/docs`` directory in your project repository. 
2. Follow the proposed [documentation structure](https://github.com/ansible-community/project-template/tree/main/docs)
 from the project-template to ensure you include all the important guides common
to all projects.
3. Add a [`mkdocs.yml`](https://github.com/ansible-community/project-template/blob/main/mkdocs.yml) to
 your project root directory and modify the `nav` section to match your proposed navigation/set of guides.
4. Create [``.readthedocs.yml``](https://github.com/ansible-community/project-template/blob/main/.readthedocs.yaml) in your project root directory.
5. Coordinate with the [Ansible community team](https://docs.ansible.com/ansible/latest/community/communication.html#forum) to set up automated publishing and to have your documentation added to the Ansible ecosystem page.

   
## Fundamentals of creating documentation


[Diataxis](https://diataxis.fr/) includes a good set of guidelines on how to write different types of documentation. The next sections summarize this information for quick reference.

### Tutorials / Getting Started guides
We tend to call these Getting Started guides. They are a quick introduction to 
the new user (or developer) to help them get something done. The focus is on 
doing. The [Ansible Getting Started Guide](https://) is a good example of this. 
Tutorials should use numbered steps (procedures). We'll cover procedures in the How-to guides section.

### Explanations/concepts
Explanations or concepts describe the 'what and the why'. 

See Red Hat's [concept explanation](https://github.com/redhat-documentation/modular-docs/blob/main/modular-docs-manual/files/TEMPLATE_CONCEPT_concept-explanation.adoc)
for further details, but keep in mind it uses asciidoc, not markdown.

### How-to guides/procedures

How-to guides are what most of your readers use. 

They should focus on what are called 'user stories'. User stories help you transform 
what is a development/product feature into something a user or developer wants to achieve.

`as a <type of user> I want <some goal> so that <some reason>`

For example, this guide fulfills the following user story:

`As a project developer, I want to ensure my project matches the Ansible project recommendations`
`so that I can ensure a smooth onboarding to the Ansible ecosystem`
    
You should write these procedures as a series of steps with an introduction sentence.
    
To watch your favorite sports team:

1. Search for what TV or streaming service televises it.
2. Subscribe to that service.
3. Set a calendar reminder so you do not forget the game.
  
    
See Red Hat's [procedure explanation](https://github.com/redhat-documentation/modular-docs/blob/main/modular-docs-manual/files/TEMPLATE_PROCEDURE_doing-one-procedure.adoc) 
for further details, but keep in mind it uses asciidoc, not markdown.
    
### Reference

References are the facts--lists, tables, and so on. Your readers refer to these
 to help them with items such as what kind of parameters or options are available
  and so on. [Ansible modules](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/copy_module.html#ansible-collections-ansible-builtin-copy-module)
  are an example of reference material.

See Red Hat's [reference explanation](https://github.com/redhat-documentation/modular-docs/blob/main/modular-docs-manual/files/TEMPLATE_REFERENCE_reference-material.adoc)
for further details, but keep in mind it uses asciidoc, not markdown.

## Types of guides to include in Ansible projects

**NOTE** A guide may only be one page if that is all that is needed for your project.

Your project likely needs the following types of documentation:

* Installation
* Getting started
* Configuration/CLI reference
* User guide
* Contributor or developer guide


### Installation uide
This is how to install your project. It should be procedure-focused and include:

- Installing
- Uninstalling
- Upgrading 

Your installation guide may need to refer to a configuration page in the References
 section for initial setup.

Consider including procedures for more than one OS/environment if your 
project supports this.

### Getting started
This guide acts as a tutorial for the reader. It should cover a simple scenario
 that the reader can follow to get their first 'thing done'. This is the 
 'Hello World' for your project.

See the [Ansible Getting Started](https://docs.ansible.com/ansible/latest/getting_started/index.html)
 for a good example.

### References

Your documentation should include the following reference sections:

**Configuration**
This covers any required configuration files.
See [Ansible configuration](https://docs.ansible.com/ansible/latest/reference_appendices/config.html) for an example. 
Consider if your project can autogenerate the configuration from code as the best way
 to keep documentation and code in sync.

**CLI reference**
If your project includes a CLI, this reference sectoin should go into more detail than the man page provides.
The command reference should be autogenerated from code if possible.

**Porting guide/changelogs**
All projects should include changelogs and a porting guide to assist your users as they upgrade 
to newer versions of your project. See the [Ansible collections changelog guidelines](https://docs.ansible.com/ansible/latest/community/collection_development_process.html#sts=Creating%20changelog%20fragments%EF%83%81)
for a good example of how to do this.

**Roadmap**
You should consider having a project roadmap so contributors and users of your project can see what 
is coming in future releases.

### User Guide
This is where you want to really think not just about what features your project provides,
 but what problems it solves. These are your 'How To' pages. Again, consider those user stories:

`as a <type of user> I want <some goal> so that <some reason>`

Think of all your features as like elements in a plane's cockpit. Your reference 
material will describe each button, switch, and display panel.

What your User guide does is tell the user how to fly the plane:

- Taking off
- Landing
- Engaging autopilot for a good cross-country nap

Something else a good User guide has? Validation or troubleshooting help. 
What to do if you are landing your plane and the landing gear won't engage?

So a generic user story/use case will have the following topics:

* What is this use case and why would the reader want to use it?
* A numbered procedure that takes the reader step by step to apply this use case.
* Troubleshooting/verifying the end result (if applicable).

**NOTE** - a user story/use case should not list every possible option a reader could use. 
That detail should be in a reference section, or in a follow-on procedure.


### Contributor guide
As these are open source projects, you want to give your potential contributors
an easy entry into your project. Keep in mind contributors can go beyond code contributions. 

Your contributor guide should include:
- Reference to the [Ansible code of conduct](https://docs.ansible.com/ansible/latest/community/code_of_conduct.html). 
- Communication channels you use (matrix, forum tags)
- How to set up their development environment
- Where your issues/PRs are tracked, and so on.

