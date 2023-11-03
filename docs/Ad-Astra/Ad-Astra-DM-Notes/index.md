```dataview
>> TABLE WITHOUT ID
>>	embed(art) AS "Art",
>>     "<span style='display: block; border-bottom: 2px solid var(--text-accent); text-align: center; margin-bottom: 5px;'>" + link(file.link, Title) + " (lvl" + (level) + " " + (class) + ")" + "</span>" AS Title,
>>	 (":fas_person: ") + pronouns AS "Pronouns",
>>	(":rif_git_repository: ") + ancestry AS "Ancestry",
>>	(":rif_heart: ") + condition AS "Condition",
>>	(":fas_globe_americas: ") + link(location, location) AS "Location"
>> WHERE type = "pc" AND !contains(condition, "Dead")
>>SORT file.name asc
>>```