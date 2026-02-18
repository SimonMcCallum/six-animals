# Six-Animal Model

A group collaboration framework by **Dr. Simon McCallum** that uses six animal avatars to represent beneficial behaviours in team projects. Built on McClelland's Three Needs Theory and Self-Determination Theory (SDT).

**Website:**[sixanimals.co.nz](https://sixanimals.co.nz)

## The Six Animals

| Animal | Role | Core Behaviour | Primary Need | SDT Focus |
|--------|------|----------------|--------------|-----------|
| **Bear** | Visionary/Leader | Speaks when nobody else speaks; articulates vision and makes decisions | Achievement (nAch) | Competence |
| **Cat** | Cynic/Risk Manager | Identifies what could go wrong; questions assumptions and flags risks | Power (nPow) | Autonomy |
| **Owl** | Process Manager | Ensures meetings move forward; tracks progress and forces decisions | Power (nPow) | Autonomy |
| **Puppy** | Enthusiast | Supports every idea; maintains positive energy and spots opportunities | Affiliation (nAff) | Relatedness |
| **Rabbit** | Facilitator | Makes sure everyone has what they need; communicates with stakeholders | Achievement (nAch) | Competence |
| **Wolf** | Manager/Pack Leader | Tells the Bear to "shut up"; ensures everyone is participating | Affiliation (nAff) | Relatedness |

### Simon Agent (Supervisor)

The **Simon agent** is a meta-level pedagogue/supervisor that sits above the six animal roles. It analyses conversation to identify which animal someone is playing, coaches role performance, and facilitates effective group collaboration. Simon operates as the "guide on the side" rather than a seventh group member.

## Theoretical Foundation

The model combines two psychological frameworks:

**McClelland's Three Needs Theory:**
- **nAch (Achievement)** — Drive to succeed and receive performance feedback
- **nPow (Power)** — Drive to influence, control, and make decisions
- **nAff (Affiliation)** — Drive to belong, connect, and maintain relationships

**Self-Determination Theory (SDT)** mapped to Te Ao Maori:
- **Agency / Mana motuhake** — Feeling in control of your own goals
- **Competence / Pumanawa** — Feeling effective and capable
- **Relatedness / Manaaki** — Feeling connected to others and community

For collectivist cultures (Maori, Pasifika, and others), these three elements are interconnected and cannot be developed in isolation.

## How It Works

1. **Role Selection** — Each group member chooses an animal that resonates with their interaction style
2. **Group Formation** — Teams are formed with six different animals, ensuring diversity of perspective
3. **Rapid Storming** — Pre-defined roles reduce power struggles and accelerate through Tuckman's storming phase
4. **Psychological Safety** — The animal personas provide a buffer from personal criticism (feedback targets the role, not the person)
5. **Fair Distribution** — Every member has defined responsibilities, preventing free-riding

### Multi-classing Rules

Some animals can combine roles; others cannot:

| Combination | Allowed? | Reason |
|-------------|----------|--------|
| Bear + Wolf | No | Cannot both lead and manage participation simultaneously |
| Cat + Puppy | No | Cannot be both critical and enthusiastic simultaneously |
| Wolf + Puppy | Yes | Combines participation management with encouragement |
| Owl + Cat | Yes | Combines process control with risk awareness |
| Owl + Rabbit | Yes | Combines progress tracking with resource facilitation |

## Using as Claude Code Skills

These animal agents are designed to work as [Claude Code skills](https://docs.anthropic.com/en/docs/claude-code). Each can be invoked as a slash command to apply that animal's perspective to your work.

### Installation

**Option 1: Project-level skills (this repo)**

Clone the repo and the skills in `skills/` are available when working within this project:

```bash
git clone https://github.com/user/six-animals.git
cd six-animals
# Skills are available as /bear-agent, /cat-agent, etc.
```

**Option 2: Copy to your project**

Copy the `.claude/skills/` directory into any project:

```bash
cp -r six-animals/.claude/skills/ your-project/.claude/skills/
```

**Option 3: Personal skills (all projects)**

Copy to your home directory for global availability:

```bash
cp -r six-animals/.claude/skills/ ~/.claude/skills/
```

### Available Commands

| Command | What it does |
|---------|-------------|
| `/bear-agent` | Apply visionary/leader perspective — strategic direction and decision-making |
| `/cat-agent` | Apply risk manager perspective — identify what could go wrong |
| `/owl-agent` | Apply process manager perspective — track progress and force decisions |
| `/puppy-agent` | Apply enthusiast perspective — find opportunities and encourage ideas |
| `/rabbit-agent` | Apply facilitator perspective — identify resource needs and remove blockers |
| `/wolf-agent` | Apply pack leader perspective — monitor participation and build cohesion |
| `/simon-agent` | Analyse conversation for animal behaviours, coach role performance, diagnose group dynamics |

### Using with Claude.ai Projects

The content of each `SKILL.md` file can be added directly as project instructions in Claude.ai. Copy the markdown content (after the frontmatter) into your project's custom instructions.

## Project Structure

```
six-animals/
├── .claude/
│   └── skills/           # Claude Code skill discovery directory
│       ├── bear-agent/
│       ├── cat-agent/
│       ├── owl-agent/
│       ├── puppy-agent/
│       ├── rabbit-agent/
│       ├── wolf-agent/
│       └── simon-agent/
├── skills/                # Canonical skill definitions
│   ├── bear-agent/SKILL.md
│   ├── cat-agent/SKILL.md
│   ├── owl-agent/SKILL.md
│   ├── puppy-agent/SKILL.md
│   ├── rabbit-agent/SKILL.md
│   ├── wolf-agent/SKILL.md
│   └── simon-agent/SKILL.md
├── docs/                  # Teaching evidence and methodology
│   └── Teaching Evidence Portfolio - Wellington.md
├── LICENSE
└── README.md
```

## Evidence of Effectiveness

> "the 'team roles' were super useless, especially in comparison to the animal roles last year which were great."
> — Student feedback, COMP313, 2019

The animal avatars have been used in university courses at Victoria University of Wellington and NTNU Norway since approximately 2011. Student feedback consistently shows preference for the animal role system over traditional team roles, with benefits including faster group formation, fairer work distribution, and improved psychological safety.

## License

CC-BY-SA-4.0 — Dr. Simon McCallum

## Author

**Dr. Simon McCallum** — Senior Lecturer, Victoria University of Wellington / Te Herenga Waka. Teaching game development, human-computer interaction, and software engineering with a focus on student agency, social constructivism, and culturally responsive pedagogy.
