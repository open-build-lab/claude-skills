# Claude Skills

Skills that teach Claude how to do a specific job. Each folder here is one skill.

## scout-master

Helps Scouts BSA (Scouting America) Scoutmasters plan troop meetings, PLC agendas, campouts, Scoutmaster conferences (with questions for every rank), advancement and Eagle timelines, youth leadership training (ILST), open houses, Courts of Honor (including training the MC), and parent emails, all while following Youth Protection and safety rules.

Once it's installed, just ask Claude something like *"Plan next Thursday's troop meeting on knots"* or *"Write the parent email for our October campout"*. Claude uses the skill on its own.

**Make it yours:** fill in `scout-master/references/my-troop.md` with your troop's details (meeting night, patrols, traditions) so Claude's plans fit your troop.

## How to install

### Claude app (claude.ai or the desktop app)

1. Download this repository from [github.com/open-build-lab/claude-skills](https://github.com/open-build-lab/claude-skills) and find the `scout-master` folder.
2. Zip the folder, so you have `scout-master.zip` with `SKILL.md` inside the `scout-master` folder.
3. In Claude, go to **Settings > Capabilities**, find **Skills**, and choose **Upload skill**.
4. Pick `scout-master.zip`, then make sure the skill is turned on.

### Quickest way (any agent that supports skills)

```bash
npx skills add open-build-lab/claude-skills
```

### Claude Code

Copy the folder into your personal skills folder:

```bash
mkdir -p ~/.claude/skills
cp -R scout-master ~/.claude/skills/
```

Or, to get updates automatically when you `git pull`, link it instead of copying:

```bash
ln -s "$(pwd)/scout-master" ~/.claude/skills/scout-master
```

Start a new Claude Code session, and the skill is ready.

## What's inside a skill

```
scout-master/
├── SKILL.md            the main instructions (Claude reads this first)
└── references/         extra detail Claude reads only when it needs it
    ├── meetings.md
    ├── outings.md
    ├── advancement.md
    ├── scoutmaster-conference.md
    ├── communication.md
    ├── youth-leadership-training.md
    ├── open-house-recruiting.md
    ├── court-of-honor.md
    ├── safety.md
    └── my-troop.md     your troop's details (optional)
```

Note: Scouting rules and rank requirements change over time. Always check the current Guide to Safe Scouting, Scouts BSA Handbook, or Scoutbook for exact rules.
