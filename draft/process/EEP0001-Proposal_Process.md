    EEP: 0001
    Title: Proposal Process
    Author: Alex Batlin
    Type: Process
    Category: N/A
    Status: Draft
    Created: 2017-05-29
    Requires: N/A
    Replaces: N/A

# What is an EEP?

EEP stands for Enterprise Ethereum Proposal. EEPs are inspired by [EIPs](https://github.com/ethereum/EIPs). An EEP is nothing but a text file, with an accompanying GitHub issue used for discussions about the text file.

EEPs are used to describe a wide range of artifacts e.g. design specifications, working groups, process guides, templates etc. They should provide concise problem, rationale and solution statements. EEPs should be managed within an existing or new working group. The EEP author is responsible for building consensus within the community and documenting dissenting opinions.

Because EEPS are maintained as text files in a versioned repository, an EEPs revision history is not maintained in the document itself, but rather as repository metadata. When the proposal is shared outside the repository, it is advisable to also include document repository metadata.

# EEP Rationale

EEPs are intended to be the primary mechanism for proposing new features, new working groups, and new processes, for collecting community input on an issue, and for documenting the design decisions that have gone into Enterprise Ethereum. 

# EEP Issue

Every proposal starts with a new issue. Each issue has a unique number, and that number should be used when creating the EEP text file i.e. the issue number sets the EEP number. The issue should contain just a brief proposal summary, and a link to the EEP text file, once that is created. Do not put too much info into the issue body, as you will then need to reconcile the issue body and the EEP text file, which should be the canonical text.

Issues can also be created to add to an existing draft document i.e. multiple issues are being resolved in a single EEP. In which case reference in the issue an existing EEP file. If the issue proposes to make a change to an adopted EEP, then it should reference the adopted EEP and a new EEP file that will replace the adopted one. 

# EEP Group

Each EEP is managed by a working group. Each working group has a dedicated branch to work on. Once the group is ready to submit the work to a governance body, a pull request is created. Working group creation, like everything else, is managed as an EEP. To see the list of approved working groups and their branches, check out the EEPs. Some example groups and their branches:

* **process** - branch managed by Process Working Group
* **groups** - branch managed by Groups Working Group
* **misc** - branch managed by Misc Working Group, responsible for reviewing proposals that do not fit existing groups

# EEP Status

Each EEP has a status. Status is a function of the repository root sub-folder, which the EEP resides under e.g. if you wish to set EEP status to draft, save the file under ${branch}/EEPs/draft folder, and if you wish to promote it to accepted, move the file to ${branch}/EEPs/accepted.

* **draft** - EEPs that are open for consideration
* **accepted** - EEPs that are planned for immediate adoption
* **final** - EEPs that have been adopted
* **deferred** - EEPs that are planned for some future adoption
* **obsolete** - EEPs that have been replaced
* **rejected** - EEPs thta have been rejected

# EEP Type

Each EEP has a type. Type is a function of the status sub-folder, which the EEP resides under e.g. if you wish to set EEP type to process, save the file under ${branch}/EEPs/${status}/process folder. Currently defined types are:

* **ethereum** - proposals that effect Ethereum itself
* **network** - proposals that effect EEA network
* **process** - EEP process related proposals
* **groups** - working group formation proposals
* **templates** -  proposals that effect document templates
* **misc** - any other proposal that does not fit in above and does not warrent update to this EEP

# EEP File

An EEP is nothing but a [Markdown](https://help.github.com/categories/writing-on-github/).md text file. Each EEP file is created in response to a new GitHub issue, which determines the EEPs number and is used to discuss the EEP.

An EEP should follow this naming format, using grep-like conventions: EEP[0-9]{4}-[a-zA-Z_]+\\.md e.g. EEP0001-Proposal_Process.md. The EEP 4 digit reference number is based on the GitHub issue that was raised to propose the EEP. Image files should be included in a subdirectory for that EIP. The file itself shoud be saved under this folder structure: ${branch}/EEPs/${status}/{$type}.

# EEP Template

Each EEP type shoud use a predefined template in the template type folder e.g. a process EEP should use the process template EEP.

# EEP Work Flow

All proposals and changes are managed as EEPs. Change to this document should be managed as an EEP. Creation of new working groups, new templates, new processes etc. are all managed via EEPs.

The EEP process begins when someone submits an new issue in GitHub. If there is no existing EEP for the issue, then a new draft EEP should be created. If the issue referenced an existing yet to be adopted EEP, then changes can be made to the draft EEP. If the issue proposes a change to an adopted EEP, then a new EEP should be created that replaces the current EEP, and once adopted, the old EEP should be set to obsolete.

It is highly recommended that an issue contains a single key proposal or a new idea. The more focused the issue, the more successful it tends to be. An EEP may include changes from multiple issues, but again, the more focused the EEP, the better.

The EEP should be managed within a specific working group e.g. this EEP is managed by process working group. Each group has it's own branch, and it's own set of branch managers, resposible for accepting new pull requests from sub-branches. It is up to the submitter to self-select the most approporiate working group when raising a new issue, by applying a label to the issue that matches the branch name. If no group seems appropriae, the misc group should be selected. Depending on the outcome of the issue review, a new working group may be created, with it's own new EEP, to work on the issue.

The master branch represents EEA's official document set, and has it's own set of managers listed later on. If the working group wants their documents to be considered official, they need to submit a new pull request for the master branch and work with the master branch managers to have it merged in.

The branch manager reserves the right to reject EEPs if they appear too unfocused or too broad. If in doubt, split your EEP into several well-focused ones.

Each EEP must have a champion - someone who writes the EEP using the style and format described below, shepherds the discussions in the appropriate forums, and attempts to build community consensus around the idea.

Vetting an idea publicly as an issue discussion before going as far as writing an EEP is meant to save the potential author time. Asking the EEA community first if an idea is original helps prevent too much time being spent on something that is guaranteed to be rejected based on prior discussions (searching the Internet does not always do the trick). It also helps to make sure the idea is applicable to the entire community and not just the author. Just because an idea sounds good to the author does not mean it will work for most people in most areas where Ethereum is used.

Once the champion has asked the EEA community whether an idea has any chance of acceptance, a draft EEP should be presented as as a new pull request from working group sub-branch. Later on, the working group branch manager will submit a master branch pull request to review the EEP with the top level governance body. This gives the author a chance to continuously edit the draft EEP for proper formatting and quality. This also allows for further public comment and the author of the EEP to address concerns about the proposal.

The branch manager should not unreasonably deny an EEP pull request. Reasons for denying an EEP may include duplication of effort, being technically unsound, not providing proper motivation or addressing backwards compatibility, or not in keeping with the EEA philosophy. For an EEP to be accepted it must meet certain minimum criteria. It must have clear and complete description of the proposal. The proposal must represent a net improvement. 

Once an EEP has been accepted, the implementations must be completed. When the implementation is complete and accepted by the community, the status will be changed to “Final”. Implementation could be in form document e.g. process, code, or both.

An EEP can also be assigned status “Deferred”. The EEP champion can assign the EEP this status when no progress is being made on the EEP. Once an EEP is deferred, the EEP champion can re-assign it to draft status.

An EEP can also be “Rejected”. Perhaps after all is said and done it was not a good idea. It is still important to have a record of this fact.

EEPs can also be superseded by a different EEP, rendering the original obsolete.

# EEP Branch Manager Responsibilities

- Read the EEP to check if it ready: sound and complete. The ideas must make technical sense, even if they don't seem likely to be accepted. The title should accurately describe the content. EEP should be chedcked for language (spelling, grammar, sentence structure, etc.), markup (Github flavored Markdown), code style.
- If the EEP isn't ready, the editor will send it back to the author for revision, with specific instructions.
- Once the EEP is ready for the repository, the branch manager will accept the corresponding pull request

# EEP Master Branch Managers

- Alex Batlin
- Bob Summerwill