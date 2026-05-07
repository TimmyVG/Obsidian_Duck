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

const pages = dv.pages("#Skill-Tree-Upgrade")

```dataviewjs
const pages = dv.pages("#Skill-Tree-Upgrade")

for (const p of pages) {

	const checkbox = document.createElement("input")
	checkbox.type = "checkbox"
	checkbox.checked = p.completed ?? false

	const label = document.createElement("span")
	label.textContent = " " + p.file.name

	const container = document.createElement("div")

	container.appendChild(checkbox)
	container.appendChild(label)

	dv.container.appendChild(container)
}

  
let total = 0  
  
for (const p of pages) {  
  
if (p.completed)  
total += p.maxLevel ?? 0  
}  
  
dv.paragraph(total)
```
