# ![[project.png|30]] Proyecto XXXXX
### por Carlos Francisco Alvarez Salgado

---
## ![[job-description.png|30]] Descripción:

### [[Introducción]]
### [[Planteamiento del problema]]

### [[Justificación]]

### [[Hipótesis]]

## [[Objetivos de la investigación]]
- ### [[Objetivos de la investigación#Objetivo General|Objetivo General]]
- ### [[Objetivos de la investigación#Objetivos secundarios|Objetivos secundarios]]

### [[Tipo de investigación]]

### [[Marco Teórico]]

### [[Descripción de planeación y desarrollo del proyecto]]

### [[Propuesta de valor del proyecto]]

### [[Estudio de viabilidad para la implementación del prototipo]]

### [[Estudio de factibilidad técnica y financiera (Costos)]] para su producción e implementación

### [[Impacto]] social, ecológico, tecnológico y/o desarrollo sustentable

### [[Estrategia para la protección de la propiedad intelectual del prototipo]]

### [[Análisis de resultado]]

### [[Conclusiones]]

### [[Bibliografía]]

### [[Manual de Operación]]

### [[Manual de Instalación]]

### [[Cartel]]

### [[Presentación de proyecto]]


---
###  ![[project-management.png|25]] Actividad:

```dataviewjs
const trackerData = { 
	entries: [], 
	separateMonths: false, 
	showCurrentDayBorder: true,
	heatmapTitle: "Actividad en Bitácora", 
	//heatmapSubtitle: "Bitacoras del proyecto.", 
	} 
// Path to the folder with notes 
//const PATH_TO_YOUR_FOLDER = "Bitacora"; 

// Name of the parameter you want to see on this heatmap 
// const PARAMETER_NAME = 'bitacora'; 

// You need dataviewjs plugin to get information from your pages 
for(let page of dv.pages('"Bitacora"')){ 
	trackerData.entries.push({ 
		date: page.file.name, 
		//intensity: page[PARAMETER_NAME], 
		content: await dv.span(`[](${page.file.name})`) 
	}); 
} 

renderHeatmapTracker(this.container, trackerData);
```

```dataview
TABLE file.ctime AS Modificado, tags
FROM "Bitacora"
SORT file.name desc
```

---
### ![[experimentos/experimento.png|30]] Experimentos y pruebas

```dataview
TABLE file.mtime AS Modificado, tags 
FROM "experimentos"
```


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
### ![[research_book.png|30]] Referencias:


