NOTE: As can be seen in how the Actions are formatted, the name and the description have to be unique and the description in quotations. If one or the other are the same and another action, only one set will show. If the description doesn't have quotes, sometimes the whole statblock will disappear.

`dice: 1d10+2`


```statblock
name: Name
size: Small
type: Fiend
subtype: ,
alignment: Chaotic Evil
ac: 9
hp: 20000
hit_dice: string
speed: string
stats: [12, 14, 2, number, number, number]
saves:
  - <ability-score>: number
skillsaves:
  - <skill-name>: number
damage_vulnerabilities: string
damage_resistances: string
damage_immunities: string
condition_immunities: string
senses: string
languages: string
cr: 4
spells:
  - <description>
  - <spell level>: <spell-list>
traits:
  - name: <trait-name>
    desc: <trait-description>
  - ...
actions:
  - name: Attack Type 1
    desc: "trait-description1"
  - name: Attack Type 2
    desc: "trait-description2"
  - name: Attack Type 3
    desc: "trait-description3"
legendary_actions:
  - name: <legendary_actions-name>
    desc: <legendary_actions-description>
  - ...
bonus_actions:
  - name: <trait-name>
    desc: <trait-description>
  - ...
reactions:
  - name: <reaction-name>
    desc: <reaction-description>
  - ...
```



```statblock
monster: Goblin
```

```statblock
monster: Adult Blue Dracolich
```

