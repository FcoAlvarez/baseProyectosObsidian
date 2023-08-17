# ![[project.png|30]] Proyecto XXXXX
### por Carlos Francisco Alvarez Salgado

---

## ![[job-description.png|30]] Descripción:


---
##  ![[lista.png|30]] Pendientes:
```tasks
not done
sort by created
sort by priority
group by filename
group by heading
```


---

## ![[documentacion.png|30]] Documentación:



---
###  ![[project-management.png|25]] Actividad:

```dataviewjs
dv.span("Actividad en Bitácora") /* optional ⏹️💤⚡⚠🧩↑↓⏳📔💾📁📝🔄📝🔀⌨️🕸️📅🔍✨ */
const calendarData = {
    year: 2023,  // (optional) defaults to current year
    colors: {    // (optional) defaults to green
        blue:        ["#8cb9ff", "#69a3ff", "#428bff", "#1872ff", "#0058e2"], // first entry is considered default if supplied
        green:       ["#c6e48b", "#7bc96f", "#49af5d", "#2e8840", "#196127"],
        red:         ["#ff9e82", "#ff7b55", "#ff4d1a", "#e73400", "#bd2a00"],
        orange:      ["#ffa244", "#fd7f00", "#dd6f00", "#bf6000", "#9b4e00"],
        pink:        ["#ff96cb", "#ff70b8", "#ff3a9d", "#ee0077", "#c30062"],
        orangeToRed: ["#ffdf04", "#ffbe04", "#ff9a03", "#ff6d02", "#ff2c01"]
    },
    showCurrentDayBorder: true, // (optional) defaults to true
    defaultEntryIntensity: 4,   // (optional) defaults to 4
    intensityScaleStart: 10,    // (optional) defaults to lowest value passed to entries.intensity
    intensityScaleEnd: 100,     // (optional) defaults to highest value passed to entries.intensity
    entries: [],                // (required) populated in the DataviewJS loop below
}

//DataviewJS loop
for (let page of dv.pages('"Bitacora"')) {
    //dv.span("<br>" + page.file.name) // uncomment for troubleshooting
    calendarData.entries.push({
        date: page.file.name,     // (required) Format YYYY-MM-DD
        //intensity: page.exercise, // (required) the data you want to track, will map color intensities automatically
        //content: "🏋️",           // (optional) Add text to the date cell
        color: "green",          // (optional) Reference from *calendarData.colors*. If no color is supplied; colors[0] is used
    })
}

renderHeatmapCalendar(this.container, calendarData)
```

---
### ![[experimentos/experimento.png|30]] Experimentos y pruebas

```dataview
TABLE file.mtime AS Modificado, tags 
FROM "experimentos"
```

---
### ![[research_book.png|30]] Referencias:


