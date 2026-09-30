A dark cyberpunk mercenary-management strategy game where you recruit and equip a crew, take dangerous contracts, manage money, heat and retaliation, and build your operation into a legendary criminal outfit without getting wiped out.

## Overview

**MERC_OS** is a single-player browser game built entirely in HTML, CSS and JavaScript.

You run a freelance mercenary cell operating across a hostile cyberpunk city. Every contract can earn credits, reputation and experience, but success also draws attention. As your operation grows, you will have to balance profit against crew injuries, stress, salaries, law-enforcement heat and retaliation from rival crews and corporations.

There is no backend, account system or installation process required. The entire game runs locally in the browser.

## Features

- **Crew management** with multiple operative roles:
  - Infiltrator
  - Netrunner
  - Solo
  - Techie
  - Fixer
  - Medic
- **Combat, Tech and Stealth** skill systems
- **Health, stress, morale, XP and leveling**
- **Equipment and loadouts** with weapons, cyberware, armor and utility gear
- **Procedurally generated contracts** with different clients, districts, risks, rewards and expiration dates
- **Mission planning** with 1–3 operatives and projected success odds
- **Black market** for purchasing equipment
- **Recruitment system** for expanding the crew
- **Safehouse upgrades** that increase crew capacity
- **Security upgrades** that reduce the danger of hostile events
- **Heat system** representing law-enforcement attention
- **Retaliation system** representing hostile pressure from gangs, rivals and corporations
- **Random events and crises**, including ambushes, raids, cyberattacks, law-enforcement sweeps and shakedowns
- **Intel system** that can improve mission planning and help resolve dangerous situations
- **Daily salaries and operating costs**
- **Dynamic city map** with multiple districts and danger levels
- **In-game field manual / guide**
- **Autosave and manual save/load**
- **Responsive desktop, tablet and mobile layouts**
- **No external framework or backend required**

## Objective

Your goal is to achieve **Legend Status**.

To win, you must simultaneously reach:

- **100 Reputation**
- **¥75,000 in liquid credits**

The campaign has no fixed turn limit.

You lose if:

- Your credits fall below **-¥5,000**, or
- Every member of your crew reaches **0 health**

## Core Gameplay Loop

1. Review available contracts.
2. Compare their risk, reward, duration and required primary skill.
3. Select one to three suitable operatives.
4. Equip your crew for the mission.
5. Review the projected success chance.
6. Execute the contract.
7. Collect rewards, reputation and experience — or deal with the consequences of failure.
8. Treat injuries and manage stress.
9. Buy better equipment and recruit specialists.
10. Upgrade and secure your safehouse.
11. Manage heat and retaliation before your growing reputation brings increasingly dangerous enemies to your door.

The central tension is simple:

> The more successful your operation becomes, the more dangerous it becomes to remain successful.

## Crew

Every operative has three core skills:

| Skill | Used for |
| --- | --- |
| **Combat** | Assaults, defense, firefights and violent recovery operations |
| **Tech** | Hacking, drones, electronics and cyber intrusion |
| **Stealth** | Infiltration, theft, extraction and low-signature operations |

Crew members also have:

- Health
- Stress
- Level
- XP
- Salary
- Role
- Equipment

Operatives become unavailable for deployment when their condition becomes too poor.

Each successful deployment contributes to long-term progression, while higher-level operatives become more effective — and more expensive.

## Equipment

Equipment is divided into four slots:

- Weapon
- Cyber
- Armor
- Utility

Each item provides bonuses to one or more statistics.

An operative can carry only one item from each slot at a time. Equipping another item in the same slot replaces the previous one.

Equipment can be purchased through the **Black Market**.

## Contracts

Contracts are dynamically generated and include:

- Client
- District
- Risk rating
- Primary skill
- Tags
- Reward
- Mission duration
- Expiration date

Risk ranges from low-level street work to extremely dangerous corporate operations.

Harder missions generally offer greater rewards and reputation gains, but also expose your crew to greater injury, stress, heat and retaliation.

Contracts expire as time passes, so the available job market continually changes.

## City Districts

The city contains several operational zones:

- **Neon Row** — clubs and vice
- **Black Harbor** — docks and smuggling
- **Corporate Spire** — heavily secured megacorporate territory
- **Undercity** — gang-controlled territory
- **Old Grid** — markets and ruins

Districts have different baseline danger levels.

The city map can also be used to filter contracts geographically.

## Heat & Retaliation

### Heat

Heat represents how much attention your operation is receiving from law enforcement.

High heat makes continued operations more dangerous and contributes to hostile incidents.

You can reduce heat by temporarily laying low instead of constantly accepting contracts.

### Retaliation

Retaliation represents pressure from rival crews, gangs and corporations.

Successful high-profile operations can increase retaliation and trigger hostile responses such as:

- Crew ambushes
- Safehouse raids
- Network intrusions
- Law-enforcement sweeps
- Rival shakedowns

These events require decisions and may force you to sacrifice money, intel, reputation or crew safety.

Upgrading safehouse security reduces both crisis frequency and potential damage.

## Safehouse

Your safehouse is the operational center of the crew.

Available actions include:

- **Clinic** — heal operatives and reduce stress
- **Lay Low** — reduce pressure while allowing time to pass
- **Safehouse Upgrade** — increase crew capacity and passive recovery
- **Security Hardening** — reduce hostile-event frequency and damage
- **Intel Broker** — purchase intelligence for future operations

Safehouse tier also determines the maximum size of your crew.

## Economy

Credits are needed for:

- Crew salaries
- Safehouse upkeep
- Security
- Equipment
- Recruitment
- Medical treatment
- Intel
- Emergency responses

Time matters because salaries and operating expenses are deducted as days pass.

Expanding too quickly can therefore be just as dangerous as failing missions.

## Saving

MERC_OS automatically stores campaign data in the browser using `localStorage`.

It also includes manual **Save** and **Load** controls in the header.

Your campaign normally survives page refreshes and browser restarts as long as the site's local browser storage is not cleared.

> Saves are local to the browser and origin where the game is running. A save created on one computer, browser profile or domain does not automatically transfer to another.

## Running the Game

No build process is required.

### Option 1 — Open Locally

Download the HTML file and open it directly in a modern browser.

### Option 2 — Run a Local Web Server

For example, with Python:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

### Option 3 — GitHub Pages

Because MERC_OS is a fully static browser game, it can be hosted directly on GitHub Pages.

1. Add the game HTML file to a GitHub repository.
2. Rename it to `index.html`.
3. Open **Settings → Pages**.
4. Select the branch containing the file.
5. Save the Pages configuration.
6. Open the generated GitHub Pages URL.

No server-side code is required.

## Controls

The game is primarily mouse/touch driven.

Header controls:

| Control | Action |
| --- | --- |
| `▣` | Save campaign |
| `↻` | Load campaign |
| `?` | Open the field manual |

Most gameplay actions are performed by clicking crew members, contracts, districts, equipment or management options.

## Technology

MERC_OS intentionally has a minimal technical footprint:

- HTML5
- CSS3
- Vanilla JavaScript
- Browser `localStorage`

There are no required:

- JavaScript frameworks
- Package managers
- Databases
- Backend servers
- User accounts
- Build tools

## Responsive Design

The interface adapts to smaller displays.

On wide screens, MERC_OS uses a three-column command-center layout. At smaller widths, panels reorganize into fewer columns and eventually stack vertically for mobile-sized displays.

The game can therefore be deployed as a static web application while remaining playable across desktop and smaller screens.

## Project Structure

The current version can operate as a single-file application:

```text
merc-os/
├── index.html
└── README.md
```

All interface styling, game data and game logic are contained inside the HTML file.

## Status

MERC_OS is a playable single-player browser game with a complete campaign loop, persistent saves, crew progression, procedural contracts, resource management and escalating hostile events.

It is designed as a compact standalone game rather than a server-based MMO.

## License

No license is currently specified.

If this project is published publicly, add a `LICENSE` file defining how others may use, modify and redistribute the project.
