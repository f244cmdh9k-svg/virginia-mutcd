# Virginia MUTCD v11.0 Codex Skill

Use `virginia-mutcd` to review Virginia traffic-control questions and plans against the January 2026 Virginia MUTCD.

## Skillset

| Workflow | What it helps you do |
| --- | --- |
| [Authority and applicability](references/capabilities/authority.md) | Identify the governing authority and edition, and interpret standards, guidance, options, and support. |
| [Official MUTCD requests](references/capabilities/official-requests.md) | Choose a path for an official interpretation, experimentation, a rule change, or interim approval. |
| [Permanent signs](references/capabilities/sign-review.md) | Check sign selection, sizing, placement, and maintenance. |
| [Horizontal-curve warnings](references/capabilities/curve-warning.md) | Evaluate advisory-speed evidence and screen warning devices using Table 2C-4. |
| [Pavement markings](references/capabilities/marking-review.md) | Review center lines, edge lines, no-passing zones, and retroreflectivity maintenance. |
| [Permanent lane-reduction tapers](references/capabilities/lane-reduction.md) | Calculate a taper from the applicable speed and offset, and identify related markings. |
| [Pedestrian crossings](references/capabilities/pedestrian-crossing.md) | Screen uncontrolled crossings and evaluate candidate beacons and other treatments. |
| [Traffic signal warrants](references/capabilities/signal-warrants.md) | Check applicable warrants and identify the evidence needed to justify a new signal. |
| [Signal design and operations](references/capabilities/signal-design.md) | Review signal faces, phasing, timing, detection, and accessibility. |
| [Driving automation](references/capabilities/automation.md) | Review traffic-control device uniformity, visibility, and serviceability. |
| [Work zones](references/capabilities/work-zone.md) | Identify the governing temporary traffic control manual for the project. |
| [School areas](references/capabilities/school-area.md) | Review walking routes, school crossings, signs, and speed zones. |
| [Rail and light rail crossings](references/capabilities/grade-crossing.md) | Prepare a diagnostic review of track clearance, storage, and signal preemption. |
| [Bicycle facilities](references/capabilities/bicycle-facility.md) | Review signs, markings, turn-lane conflicts, shared-use path crossings, and detection. |

## Add to Codex

The repository is public and available to clone or download from GitHub. If `virginia-mutcd` already appears in your skill picker, go to [Use the skill](#use-the-skill).

### Install from a ZIP

1. Download and extract the ZIP. Use [Source code (zip) from the latest release](https://github.com/f244cmdh9k-svg/virginia-mutcd/releases/latest) for a fixed version, or [download the current main branch](https://github.com/f244cmdh9k-svg/virginia-mutcd/archive/refs/heads/main.zip).
2. Rename the extracted folder to `virginia-mutcd`. Move it to your personal Codex skills folder. Create the parent folder if needed.
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
