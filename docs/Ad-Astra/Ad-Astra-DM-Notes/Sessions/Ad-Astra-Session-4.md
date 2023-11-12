```dataview 
>> TASK 
>> FROM "Ad Astra/Ad Astra DM Notes/Sessions/Session TODOs"
>> WHERE !completed 
>> GROUP BY meta(section).subpath
>> ```