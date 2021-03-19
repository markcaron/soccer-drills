# Soccer Drills

Collecting and open sourcing soccer drills (particularly one's I've found useful) for youth soccer coaches everywhere.

[See the drills](drills)

## Usage

Anyone is free to use these drills and practice plans provided they adhere to the [Attribution-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0) license associated with this repository.

Perhaps at some point an application could be developed (within this repo or elsewhere) to consume these drills.

## Contributing

I'd love for other coaches to contribute to this repository of drills.

Therefore, it's necessary to ensure we're using the same format: [Markdown](https://www.markdownguide.org/basic-syntax/) with YAML front matter (as a schema). If you're not familiar with either, they're [easy to learn](https://learn-the-web.algonquindesign.ca/topics/markdown-yaml-cheat-sheet/) and human readable.

### Template

Use the `_template.md` in `/drills/` to start you off on the right (or left) foot.

### YAML Schema

| Property | Meaning        | Value Type | Possible Values |
| :---     | :---           | :---       | :---            |
| `title:`  | Name of drill  | string     | _Any_           |
| `type:`   | Type of drill  | string     | `Warm-up`, `Tactical`, `Technical`, `Physical`, `Game` |
| `ages:`   | Age range      | string     | `All`, `U6`, `U7`, etc., or range like `U6-U8`   |
| `level:`  | Level of skill | string     | `All`,<br>`Initial` (U6–U8),<br>`Basic` (U9-U12),<br>`Intermediate` (U13 & U14),<br>`Advanced` (U15–U18),<br>`Professional` |
| `skills:` | Skills taught  | list of categories | _See skills category list below_  |
| `setup:`  | Drill steup    | nested object | `duration:`, `cones:`, `pinnies:`, `balls:`, `players:`, `area:`  |
| setup/`duration:` | Time in minutes | time duration | _Any_ (for example: `5`) |
| setup/`cones:` | Number of cones | number | _Any_ (for example: `4`) |
| setup/`goals:` | Number of goals | number | _Any_ (for example: `1`) |
| setup/`pinnies:` | Pinnies required | string | `yes`, `no`, `optional` |
| setup/`balls:` | Number of balls | nested object | `min:` and `max:` (numbers) |
| setup/`players:` | Number of balls | nested object | `min:` and `max:` (numbers) |
| setup/`area:` | Area of play required | nested object | `min:` and `max:` (strings, e.g. `10 x 10` as measured in yards |
| `desc:`  | Description of drill | string | _Any_           |

**Example:**

```yaml
---
title: Passing & Communication Square
type: Warm-up
ages: All
level: All
skills:
  - passing
  - communication
  - dribbling
  - ball control
  - receiving
  - turning
  - change of direction
  - identifying space
  - providing support
  - conditioning
  - ice breaker
setup:
  duration: 10
  cones: 8
  pinnies: optional
  balls:
    min: 4
    max: 10
  players:
    min: 8
    max: 20
  area:
    min: 10 x 10
    max: 20 x 20
desc: Simple passing warm-up for all ages that combines passing, communication, dribbling, turning & receiving, and finding open teammates.
---
```

### Skills Categories

The current skills categories used in the YAML schema are as follows:

- awareness
  - attacking
  - change of direction
  - defending
  - identifying space
  - providing support
- ball control
  - dribbling
  - receiving
  - turning
- communication
- conditioning
- finishing
- goalkeeping
  - goalkeeping basics
  - goalkeeping conditioning
  - goalkeeping distribution
  - goalkeeping diving
  - goalkeeping reflexes
  - goalkeeping situational
- ice breaker
- passing
- strength building
