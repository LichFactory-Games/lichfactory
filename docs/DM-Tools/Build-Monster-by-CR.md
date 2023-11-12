---
share: false
cr: 9
date created: Thursday, November 2nd 2023, 4:27:02 pm
date modified: Sunday, November 12th 2023, 6:39:49 am
title: Build Monster by CR
---

### Monster CR: `INPUT[suggester(option(0), option(1/8), option(1/4), option(1/2), option(1), option(2), option(3), option(4), option(5), option(6), option(7), option(8), option(9), option(10), option(11), option(12), option(13), option(14), option(15), option(16), option(17), option(18), option(19), option(20), option(21), option(22), option(23), option(24), option(25), option(26), option(27), option(28), option(29), option(30)):cr]`

```js-engine
 // Access the "cr" value from the front matter
const crValue = context.metadata.frontmatter.cr; 

// Define data based on CR values
const data = {
  "0": {
    "Eqv Char Lvl": "< 1",
    "AC/DC": 10,
    "HP": "3 (2-4)",
    "Attack/Prof": "+2",
    "DPR": 2,
    "# of Attacks": 1,
    "Damage": "2 (1d4)",
    "Example Monster": "Commoner, rat, spider"
  },
  "1/8": {
    "Eqv Char Lvl": "< 1",
    "AC/DC": 11,
    "HP": "9 (7-11)",
    "Attack/Prof": "+3",
    "DPR": 3,
    "# of Attacks": 1,
    "Damage": "4 (1d6 + 1)",
    "Example Monster": "Bandit, cultist, giant rat"
  },
  "1/4": {
    "Eqv Char Lvl": "1",
    "AC/DC": 11,
    "HP": "13 (10-16)",
    "Attack/Prof": "+3",
    "DPR": 5,
    "# of Attacks": 1,
    "Damage": "5 (1d6 + 2)",
    "Example Monster": "Acolyte, skeleton, wolf"
  },
  "1/2": {
    "Eqv Char Lvl": "2",
    "AC/DC": 12,
    "HP": "22 (17-28)",
    "Attack/Prof": "+4",
    "DPR": 8,
    "# of Attacks": 2,
    "Damage": "4 (1d4 + 2)",
    "Example Monster": "Black bear, scout, shadow"
  },
  "1": {
    "Eqv Char Lvl": "3",
    "AC/DC": 12,
    "HP": "33 (25-41)",
    "Attack/Prof": "+5",
    "DPR": 12,
    "# of Attacks": 2,
    "Damage": "6 (1d8 + 2)",
    "Example Monster": "Dire wolf, specter, spy"
  },
  "2": {
    "Eqv Char Lvl": "5",
    "AC/DC": 13,
    "HP": "45 (34-56)",
    "Attack/Prof": "+5",
    "DPR": 17,
    "# of Attacks": 2,
    "Damage": "9 (2d6 + 2)",
    "Example Monster": "Ghast, ogre, priest"
  },
  "3": {
    "Eqv Char Lvl": "7",
    "AC/DC": 13,
    "HP": "65 (49-81)",
    "Attack/Prof": "+5",
    "DPR": 23,
    "# of Attacks": 2,
    "Damage": "12 (2d8 + 3)",
    "Example Monster": "Knight, mummy, werewolf"
  },
  "4": {
    "Eqv Char Lvl": "9",
    "AC/DC": 14,
    "HP": "84 (64-106)",
    "Attack/Prof": "+6",
    "DPR": 28,
    "# of Attacks": 2,
    "Damage": "14 (3d8 + 1)",
    "Example Monster": "Ettin, ghost"
  },
  "5": {
    "Eqv Char Lvl": "10",
    "AC/DC": 15,
    "HP": "95 (71-119)",
    "Attack/Prof": "+7",
    "DPR": 35,
    "# of Attacks": 3,
    "Damage": "12 (3d6 + 2)",
    "Example Monster": "Elemental, gladiator, vampire spawn"
  },
  "6": {
    "Eqv Char Lvl": "11",
    "AC/DC": 15,
    "HP": "112 (84-140)",
    "Attack/Prof": "+7",
    "DPR": 41,
    "# of Attacks": 3,
    "Damage": "14 (3d6 + 4)",
    "Example Monster": "Mage, medusa, wyvern"
  },
  "7": {
    "Eqv Char Lvl": "12",
    "AC/DC": 15,
    "HP": "130 (98-162)",
    "Attack/Prof": "+7",
    "DPR": 47,
    "# of Attacks": 3,
    "Damage": "16 (3d8 + 3)",
    "Example Monster": "Stone giant, young black dragon"
  },
  "8": {
    "Eqv Char Lvl": "13",
    "AC/DC": 15,
    "HP": "136 (102-170)",
    "Attack/Prof": "+7",
    "DPR": 53,
    "# of Attacks": 3,
    "Damage": "18 (3d10 + 2)",
    "Example Monster": "Assassin, frost giant"
  },
  "9": {
    "Eqv Char Lvl": "15",
    "AC/DC": 16,
    "HP": "145 (109-181)",
    "Attack/Prof": "+8",
    "DPR": 59,
    "# of Attacks": 3,
    "Damage": "22 (3d12 + 3)",
    "Example Monster": "Bone devil, fire giant, young blue dragon"
  },
  "10": {
    "Eqv Char Lvl": "16",
    "AC/DC": 17,
    "HP": "155 (116-194)",
    "Attack/Prof": "+9",
    "DPR": 65,
    "# of Attacks": 4,
    "Damage": "16 (3d8 + 3)",
    "Example Monster": "Stone golem, young red dragon"
  },
  "11": {
    "Eqv Char Lvl": "17",
    "AC/DC": 17,
    "HP": "165 (124-206)",
    "Attack/Prof": "+9",
    "DPR": 71,
    "# of Attacks": 4,
    "Damage": "18 (3d10 + 2)",
    "Example Monster": "Djinni, efreeti, horned devil"
  },
  "12": {
    "Eqv Char Lvl": "18",
    "AC/DC": 17,
    "HP": "175 (131-219)",
    "Attack/Prof": "+9",
    "DPR": 77,
    "# of Attacks": 4,
    "Damage": "19 (3d10 + 3)",
    "Example Monster": "Archmage, erinyes"
  },
  "13": {
    "Eqv Char Lvl": "19",
    "AC/DC": 18,
    "HP": "184 (138-230)",
    "Attack/Prof": "+10",
    "DPR": 83,
    "# of Attacks": 4,
    "Damage": "21 (4d8 + 3)",
    "Example Monster": "Adult white dragon, storm giant, vampire"
  },
  "14": {
    "Eqv Char Lvl": "20",
    "AC/DC": 19,
    "HP": "196 (147-245)",
    "Attack/Prof": "+11",
    "DPR": 89,
    "# of Attacks": 4,
    "Damage": "22 (4d10)",
    "Example Monster": "Adult black dragon, ice devil"
  },
  "15": {
    "Eqv Char Lvl": "> 20",
    "AC/DC": 19,
    "HP": "210 (158-263)",
    "Attack/Prof": "+11",
    "DPR": 95,
    "# of Attacks": 5,
    "Damage": "19 (3d10 + 3)",
    "Example Monster": "Adult green dragon, mummy lord, purple worm"
  },
  "16": {
    "Eqv Char Lvl": "> 20",
    "AC/DC": 19,
    "HP": "229 (172-286)",
    "Attack/Prof": "+11",
    "DPR": 101,
    "# of Attacks": 5,
    "Damage": "21 (4d8 + 3)",
    "Example Monster": "Adult blue dragon, iron golem, marilith"
  },
  "17": {
    "Eqv Char Lvl": "> 20",
    "AC/DC": 20,
    "HP": "246 (185-308)",
    "Attack/Prof": "+12",
    "DPR": 107,
    "# of Attacks": 5,
    "Damage": "22 (3d12 + 3)",
    "Example Monster": "Adult red dragon"
  },
  "18": {
    "Eqv Char Lvl": "> 20",
    "AC/DC": 21,
    "HP": "266 (200-333)",
    "Attack/Prof": "+13",
    "DPR": 113,
    "# of Attacks": 5,
    "Damage": "23 (4d10 + 1)",
    "Example Monster": "Demilich"
  },
  "19": {
    "Eqv Char Lvl": "> 20",
    "AC/DC": 21,
    "HP": "285 (214-356)",
    "Attack/Prof": "+13",
    "DPR": 119,
    "# of Attacks": 5,
    "Damage": "24 (4d10 + 2)",
    "Example Monster": "Balor"
  },
  "20": {
    "Eqv Char Lvl": "> 20",
    "AC/DC": 21,
    "HP": "300 (225-375)",
    "Attack/Prof": "+13",
    "DPR": 132,
    "# of Attacks": 5,
    "Damage": "26 (4d12)",
    "Example Monster": "Ancient white dragon, pit fiend"
  },
  "21": {
    "Eqv Char Lvl": "> 20",
    "AC/DC": 22,
    "HP": "325 (244-406)",
    "Attack/Prof": "+14",
    "DPR": 150,
    "# of Attacks": 5,
    "Damage": "30 (4d12 + 4)",
    "Example Monster": "Ancient black dragon, lich, solar"
  },
  "22": {
    "Eqv Char Lvl": "> 20",
    "AC/DC": 23,
    "HP": "350 (263-438)",
    "Attack/Prof": "+15",
    "DPR": 168,
    "# of Attacks": 5,
    "Damage": "34 (4d12 + 8)",
    "Example Monster": "Ancient green dragon"
  },
  "23": {
    "Eqv Char Lvl": "> 20",
    "AC/DC": 23,
    "HP": "375 (281-469)",
    "Attack/Prof": "+15",
    "DPR": 186,
    "# of Attacks": 5,
    "Damage": "37 (6d10 + 4)",
    "Example Monster": "Ancient blue dragon, kraken"
  },
  "24": {
    "Eqv Char Lvl": "> 20",
    "AC/DC": 23,
    "HP": "400 (300-500)",
    "Attack/Prof": "+15",
    "DPR": 204,
    "# of Attacks": 5,
    "Damage": "41 (6d10 + 8)",
    "Example Monster": "Ancient red dragon"
  },
  "25": {
    "Eqv Char Lvl": "> 20",
    "AC/DC": 24,
    "HP": "430 (323-538)",
    "Attack/Prof": "+16",
    "DPR": 222,
    "# of Attacks": 5,
    "Damage": "44 (6d10 + 11)",
    "Example Monster": ""
  },
  "26": {
    "Eqv Char Lvl": "> 20",
    "AC/DC": 25,
    "HP": "460 (345-575)",
    "Attack/Prof": "+17",
    "DPR": 240,
    "# of Attacks": 5,
    "Damage": "48 (6d10 + 15)",
    "Example Monster": ""
  },
  "27": {
    "Eqv Char Lvl": "> 20",
    "AC/DC": 25,
    "HP": "490 (368-613)",
    "Attack/Prof": "+17",
    "DPR": 258,
    "# of Attacks": 5,
    "Damage": "52 (6d10 + 19)",
    "Example Monster": ""
  },
  "28": {
    "Eqv Char Lvl": "> 20",
    "AC/DC": 25,
    "HP": "540 (405-675)",
    "Attack/Prof": "+17",
    "DPR": 276,
    "# of Attacks": 5,
    "Damage": "55 (6d10 + 22)",
    "Example Monster": ""
  },
  "29": {
    "Eqv Char Lvl": "> 20",
    "AC/DC": 26,
    "HP": "600 (450-750)",
    "Attack/Prof": "+18",
    "DPR": 294,
    "# of Attacks": 5,
    "Damage": "59 (6d10 + 26)",
    "Example Monster": ""
  },
  "30": {
    "Eqv Char Lvl": "> 20",
    "AC/DC": 27,
    "HP": "666 (500-833)",
    "Attack/Prof": "+19",
    "DPR": 312,
    "# of Attacks": 5,
    "Damage": "62 (6d10 + 29)",
    "Example Monster": "Tarrasque"
  }
};

// Use the "cr" value to look up data
const crData = data[crValue];

// Create a Markdown builder 
let markdownBuilder = engine.markdown.createBuilder();

// Check if the "cr" value exists in the front matter 
if (data[crValue]) { const crData = data[crValue];

const crText = "CR: ";
const crHeader = crText + crValue;

// Create a heading for the selected CR -- I just use the picker as heading but YMMV
// markdownBuilder.createHeading(2, crHeader);

// Render the data for the selected CR
for (const key in crData) {
markdownBuilder.createParagraph(`**${key}**: ${crData[key]}`);
}
} else {

// Display a message if the "cr" value is not found
markdownBuilder.createParagraph("CR value not found in the data.");
}

// Return the Markdown builder
return markdownBuilder;

```

> [!info|no-border]- License
> This work includes material taken from the [Lazy GM's 5e Monster Builder Resource Document](https://slyflourish.com/lazy_5e_monster_building_resource_document.html) written by Teos Abadía of [Alphastream.org](https://alphastream.org/), Scott Fitzgerald Gray of [Insaneangel.com](https://insaneangel.com/), and Michael E. Shea of [SlyFlourish.com](https://slyflourish.com/), available under a [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).