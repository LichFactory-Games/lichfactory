```dataview
>> TABLE WITHOUT ID
>>     "<span style='display: block; border-bottom: 2px solid var(--text-accent); text-align: center; margin-bottom: 10px;'>" + link(file.link, Title) + "</span>" AS Title,
>>  embed(art)  AS "Art",
>>	(":luc_person_standing: ") + leader AS "Leader",
>>	(":fas_home: ") + link(base, base) AS "Home Base",   
>>	(":fas_church: ") + religion AS "Religion",  
>>	(":luc_timer:")  + status as "Current Status"  
>> WHERE (type = "group" OR type = "faction") OR (contains(tags, "ermis") AND contains(tags, "faction"))
>> SORT file.name asc
>>```