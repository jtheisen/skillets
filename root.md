Skillets are small skill-like files that are hosted in this repo and meant to selectively be downloaded and maintained.

All skillet files are in the skillet folder:

List:
https://api.github.com/repos/jtheisen/skillets/contents/skillets

Individual skillet:
https://raw.githubusercontent.com/jtheisen/skillets/refs/heads/main/skillets/<name>.md

This file has the url:
https://raw.githubusercontent.com/jtheisen/skillets/refs/heads/main/root.md

You should download some of these and maintain them according to the following rules.

## Cross-skillet modes

- agentsmd vs file
  - global(ly): The user-wide AGENTS.md file of your agent harness
  - local(ly): The AGENTS.md or AGENTS.override.md file of the current workspace

- public vs private
  - public: We use AGENTS.md and store skillets in <workspace>/skillets (default)
  - private: We use AGENTS.override.md and manage skillets in <workspace>/.agents/skillets

## Per-skillet home

Skillets can be maintained
- in the respective file at the path specified earlier (file, default) or
- in the AGENTS.md of the configured mode under an appropriate section (agentsmd)
  (make a section "skillets" with subsections for each skillet - this file
  itself is also maintained there as "root", see below under bootrap)

Select agentsmd only if the skillet file itself says so in the frontmatter or you
are asked to with the keyword "agentsmd".

## Workflow

When you read this file either through the skillet skill invocation or by being directly asked
to, a list of terms can be given: global, local, public, private, update and a number of skillet names.

If a mode is given, this means you should select the corresponding mode.

If "update" is given, you are asked to locally maintained skillets against their upstream
source and update them locally. This includes both file and agentsmd skillets, as well
as the upstream version of this file.

Unknown words are skillet names mean you're asked to bring in the respective skillets.

### Boostrap

When you have no recollection of anything about "skillets", you're in bootstrap. Treat this
file as a skillet named "root" in agentsmd mode and update the respective AGENTS.md so
further chats don't need to read it again.

Also directly record
- the selected cross-skillet mode and
- where the default AGENTS.md and the skillets live locally
- a list of the maintained skillets with
  - their name,
  - their path (for a file-home),
  - their "apply" (from the frontmatter)

### Update

If you have a recollection of "skillets", then an AGENTS.md already contains the bootstrapped
information. You are reading a copy and longer need to check the upstream source unless asked to.

If the skillet skill is invoked with the "update" keyword it means you are asked to, see above.

### Using skillets

Use skillets during other work if and only if the "apply" matches or you're explicitly asked to.
