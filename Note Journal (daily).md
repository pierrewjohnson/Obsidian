---
lieu:
banner: "![[banners-18.jpg]]"
---
<%*
const title = tp.file.title;
const today = moment(title, "YYYY-MM-DD");
const yesterday = today.clone().subtract(1, 'd');
const tomorrow = today.clone().add(1, 'd');
const yesterdayLink = yesterday.format("YYYY-MM-DD");
const tomorrowLink = tomorrow.format("YYYY-MM-DD");
const todayFormatted = today.format("YYYY-MM-DD");
const currentDayOfYear = today.format("DDDo");
const currentYear = today.format("[An ]YYYY");
const currentWeek = today.format("gggg-[W]ww");
const weekNumber = today.format("WW");
const currentMonth = today.format("YYYY-[M]MM");
const monthName = today.format("MMMM");
const creationDate = tp.file.creation_date("dddd Do MMMM YYYY");
-%>
```widgets
type: clock
format: "24hr"
hideSeconds: true
```
Journal du <% creationDate %>, le <% currentDayOfYear %> jour de l'[[<% currentYear %>]].

[[/0. JOURNAL/<% yesterday.format("YYYY/MM") %>/<% yesterdayLink %>|⏮️]] — <% todayFormatted %> — [[/0. JOURNAL/<% tomorrow.format("YYYY/MM") %>/<% tomorrowLink %>|⏭]] - 📆 [[0. JOURNAL/Planning/<% currentWeek %>|Semaine <% weekNumber %>]] du mois de [[0. JOURNAL/Planning/<% currentMonth %>|<% monthName %>]]

---
#### 📅 Journal perso

##### :luc_bookmark: Priorités

##### Hier ou Jours passés 
<% tp.file.cursor() %>
##### :luc_sunrise: Ce matin - ㏂

##### :luc_sunset: Cet après-midi et ce soir - ㏘

##### :luc_pencil: Notes
- 

##### :luc_flag_triangle_right:Accomplissements 

##### 👐 Gratitude et/ou 🚥 Difficultés

##### :luc_anchor: Utile


#### 📝 Notes créées aujourd'hui

 > [!info]+ Généré automatiquement

```dataview

List FROM "" WHERE file.cday = date("<%tp.date.now('YYYY-MM-DD')%>") SORT file.ctime asc

```

