---
share: true
date created: Sunday, October 22nd 2023, 7:51:59 am
date modified: Sunday, October 29th 2023, 3:19:20 pm
---

<%*  
const tfile = tp.file.find_tfile("Campaign/Campaign Mainpage")  
const charLevel = Number(app.metadataCache.getFileCache(tfile).frontmatter.level)  
const tsessions = Number(app.metadataCache.getFileCache(tfile).frontmatter.sessions)  
const nsessions = tsessions + 1  
await app.fileManager.processFrontMatter(tfile, (frontmatter) => {frontmatter["sessions"] += 1;})  
await tp.file.move("Campaign/Notes/Sessions/Session "+nsessions)  
%><%"---"%>  
tags: Campaign, Session  
session: <%* tR += nsessions %>  
characters: PC1, PC2, PC3, PC4  
level: <%* tR += level %>  
<%"---"%>

# Session <%* Tr += Nsessions %>

```button
name Session Date
type line(2) template
action Insert - Session Date
remove true
```

^button-sessionDate

## Characters

| Character | Pronunciation | Class | Player | Race |
| --------- | ------------- | ----- | ------ | ---- |


**Known Languages:**

### Prior Session Recap: [[Session <%* tR += tsessions %>|Session <%* tR += tsessions %>]]
> ![[Session <%* tR += tsessions %> #Session Summary|no-h no-link clean]]

## Strong Start

## Session Summary
- [I]  
- [+] Session Recording: [[Audio - Session <%* tR += nsessions %>.flac|Audio - Session <%* tR += nsessions %>.flac]]
