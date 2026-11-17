# Virginia MUTCD v11.0 Codex Skill

Use `virginia-mutcd` to review Virginia traffic-control questions and plans against the January 2026 Virginia MUTCD. The skill covers fourteen workflows, including source applicability, signing and markings, signal warrants, school areas, grade crossings, bicycle facilities, and work-zone manual selection.

## Add to Codex

The repository is public and available to clone or download from GitHub. If `virginia-mutcd` already appears in your skill picker, go to [Use the skill](#use-the-skill).

### Install from a ZIP

1. [Download the ZIP](https://github.com/f244cmdh9k-svg/virginia-mutcd/archive/refs/heads/main.zip) and extract it.
2. Rename the extracted `virginia-mutcd-main` folder to `virginia-mutcd`. Move it to your personal Codex skills folder. Create the parent folder if needed.
   - Windows destination is `%USERPROFILE%\.agents\skills\virginia-mutcd`.
   - macOS and Linux destination is `~/.agents/skills/virginia-mutcd`.
   - For a single project, use `.agents/skills/virginia-mutcd` inside that project's root.
3. Check that `SKILL.md`, `references/`, and `resources/` sit directly inside `virginia-mutcd`.
4. In Codex, select `$virginia-mutcd` and add your request. Restart Codex if the skill doesn't appear. [Codex local skill locations and discovery](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills).

### Install with Git

Clone the full repository into your personal skills directory so the workflows and source locator are available in every local project.

#### Windows PowerShell

```powershell
$skills = Join-Path $env:USERPROFILE '.agents/skills'
New-Item -ItemType Directory -Force -Path $skills | Out-Null
git clone --branch main https://github.com/f244cmdh9k-svg/virginia-mutcd.git (Join-Path $skills 'virginia-mutcd')
```

#### macOS or Linux

```sh
mkdir -p "$HOME/.agents/skills"
git clone --branch main https://github.com/f244cmdh9k-svg/virginia-mutcd.git "$HOME/.agents/skills/virginia-mutcd"
```

## Use the skill

In a local Codex chat, type `$virginia-mutcd` and select the skill when it appears. Add your request after the mention. In Codex CLI or the IDE extension, you can also use `/skills` to find it. [OpenAI skill invocation guide](https://learn.chatgpt.com/docs/build-skills#how-chatgpt-and-codex-use-skills).

Try one of these prompts:

```text
$virginia-mutcd Draw an R2-1 SPEED LIMIT 45 sign for illustration and cite the applicable Virginia MUTCD table.
```

```text
$virginia-mutcd Review the signing and pavement markings for this two-lane VDOT urban collector. The posted limit is 45 mph, the traveled way is 22 ft wide, and ADT is 4,200. Cite the controlling provisions and flag missing inputs.
```

```text
$virginia-mutcd Screen this proposed pedestrian crossing. Review the attached plan and counts, cite the applicable provisions, and list the field checks still needed.
```

For a project review, provide the route or locality, maintaining agency, roadway class, lane layout, posted speed, applicable counts, and any relevant plans or measurements. Ask for the finding, provision, evidence, and open issues. Use the VDOT Road Design Manual for geometric design criteria and the Virginia Work Area Protection Manual for temporary traffic control details. Confirm the controlling edition, official figures and project facts before using findings in design or approval. [VDOT Road Design Manual](https://www.vdot.virginia.gov/doing-business/technical-guidance-and-support/technical-guidance-documents/road-design-manual/) · [Official Virginia incorporation register](https://law.lis.virginia.gov/admincode/title24/agency30/chapter315/section9999/).

## Update your copy

For a Git clone, run `git pull --ff-only` inside the installed `virginia-mutcd` folder. For a ZIP installation, download and extract the latest archive and replace the installed folder with the updated copy.

## Included references

- [Skill entry and workflow list](SKILL.md)
- [Source locator](resources/source-locator.md)
- [Glossary](references/glossary.md)
- [Decision summary](references/cheatsheet.md)
