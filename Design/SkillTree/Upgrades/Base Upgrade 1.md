---
tags:
  - Skill-Tree
  - Skill-Tree-Upgrade
Max-Level: 5
Type:
  - Active
---

```dataviewjs
const dmg =  dv.current()["Max-Level"]

const crit = 0.25  
  
dv.paragraph(dmg * (1 + crit))
dv.paragraph(dmg + dv.page("Base Upgrade 1")["Max-Level"])
```
```dataview

TABLE
FROM #Skill-Tree-Upgrade 

```

