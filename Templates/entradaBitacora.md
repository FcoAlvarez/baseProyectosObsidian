---
tipoEntrada: bitacora

---

Tags: #SeedAndForget
## Bitácora: {{Date:DD-MMM-YYYY}}

### Por hacer:

### Pendientes para hoy:
```dataviewjs
dv.taskList(dv.pages().file.tasks 
  .where(t => !t.completed)
  .where(t => t.text.includes("{{date:YYYY-MM-DD}}")))
```

## Referencias