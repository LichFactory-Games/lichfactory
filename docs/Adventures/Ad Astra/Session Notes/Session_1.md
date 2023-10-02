```dataview
>TABLE WITHOUT ID 
>art AS "Art",
>(file.link) AS "PC",
>ancestry AS "Ancestry",
>class AS "Class"
>FROM "Adventures/Ad Astra/The Party"
>WHERE type = "pc"
>SORT file.name ASC
>```