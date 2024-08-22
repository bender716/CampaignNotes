In my version of this, I have used the following link to create a nice documentation here, but as I do not have permissions to copy at present, I will leave you with a link to the original page and the links Nicole has referenced.
https://nicolevanderhoeven.com/blog/20210809-dnd-obsidian-player/

[Getting Things Done](https://gettingthingsdone.com/) methodology Obsidian [Completed Area plugin](https://github.com/DahaWong/obsidian-completed-area) 

[Obsidian Dataview plugin](https://github.com/blacksmithgu/obsidian-dataview)
[Advanced Tables plugin](https://github.com/tgrosinger/advanced-tables-obsidian) 
[Outliner plugin](https://github.com/vslinko/obsidian-outliner) 
[Dice Roller plugin](https://github.com/valentine195/obsidian-dice-roller).
### Creating new pages

```
---
type: 
location: [Neverwinter]
world: "Forgotten Realms"
campaign: "[campaign_name]"
date: 2021-06-23
---
```
 [Obsidian Leaflet](https://github.com/valentine195/obsidian-leaflet-plugin)
 [Obsidian Timelines plugin](https://github.com/Darakah/obsidian-timelines) to create order of events pages by using this code in the timeline page:

````markdown
```timeline
fr
\```
````

(without the backtick) and this for every event that I want to include:

```markdown
---
date: [2021-06-23]
tags: [timeline, fr]
---
<span 
	  class='ob-timelines' 
	  data-date='1443-00' 
	  data-title='Xionerys is born' 
	  data-class='orange' 
          data-img = 'assets/xionerys.jpg' 
	  data-type='range' 
	  data-end='1443-00'> 
	Xionerys is born in Calimshan.
</span>
```

### Publish

