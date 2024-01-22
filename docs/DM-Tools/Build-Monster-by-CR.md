---
title: Build Monster by CR
date created: Thursday, November 2nd 2023, 4:27:02 pm
date modified: Sunday, December 10th 2023, 4:59:15 pm
share: false
cr: 9
mf: Cunning Action
---


## Monster CR: `INPUT[suggester(option(0), option(1/8), option(1/4), option(1/2), option(1), option(2), option(3), option(4), option(5), option(6), option(7), option(8), option(9), option(10), option(11), option(12), option(13), option(14), option(15), option(16), option(17), option(18), option(19), option(20), option(21), option(22), option(23), option(24), option(25), option(26), option(27), option(28), option(29), option(30)):cr]`

```js-engine

const mb = engine.getPlugin('obsidian-meta-bind-plugin').api;
const signal = mb.createSignal(undefined)

// Register to listen for changes in the 'mf' property
component.register(mb.listenToMetadata(signal, context.file.path, ['cr']))

// Define data based on CR values
const crBuild = {
"0": {
  "Eqv Char Lvl": "< 1",
  "AC/DC": 10,
  "HP": "3 (2-4)",
  "Attack/Prof": "+2",
  "DPR": 2,
  "# of Attacks": 1,
  "Damage": "2 (1d4)",
  "Example Monster": "[[Commoner]], [[rat]], [[spider]]",
  "One Line Stat Block": "CR 0 | AC/DC 10 | HP 3 (2-4) | Atk/Prof +2 | DPR 2 | # Atks 1 | Dmg 2 (1d4)"
},
"1/8": {
  "Eqv Char Lvl": "< 1",
  "AC/DC": 11,
  "HP": "9 (7-11)",
  "Attack/Prof": "+3",
  "DPR": 3,
  "# of Attacks": 1,
  "Damage": "4 (1d6 + 1)",
  "Example Monster": "[[Bandit]], [[cultist]], [[giant-rat]]",
  "One Line Stat Block": "CR 1/8 | AC/DC 11 | HP 9 (7-11) | Atk/Prof +3 | DPR 3 | # Atks 1 | Dmg 4 (1d6 + 1)"
},
"1/4": {
  "Eqv Char Lvl": "1",
  "AC/DC": 11,
  "HP": "13 (10-16)",
  "Attack/Prof": "+3",
  "DPR": 5,
  "# of Attacks": 1,
  "Damage": "5 (1d6 + 2)",
  "Example Monster": "[[Acolyte]], [[skeleton]], [[wolf]]",
  "One Line Stat Block": "CR 1/4 | AC/DC 11 | HP 13 (10-16) | Atk/Prof +3 | DPR 5 | # Atks 1 | Dmg 5 (1d6 + 2)"
},
"1/2": {
  "Eqv Char Lvl": "2",
  "AC/DC": 12,
  "HP": "22 (17-28)",
  "Attack/Prof": "+4",
  "DPR": 8,
  "# of Attacks": 2,
  "Damage": "4 (1d4 + 2)",
  "Example Monster": "[[Black bear]], [[scout]], [[shadow]]",
  "One Line Stat Block": "CR 1/2 | AC/DC 12 | HP 22 (17-28) | Atk/Prof +4 | DPR 8 | # Atks 2 | Dmg 4 (1d4 + 2)"
},
"1": {
  "Eqv Char Lvl": "3",
  "AC/DC": 12,
  "HP": "33 (25-41)",
  "Attack/Prof": "+5",
  "DPR": 12,
  "# of Attacks": 2,
  "Damage": "6 (1d8 + 2)",
  "Example Monster": "[[Dire-wolf]], [[specter]], [[spy]]",
  "One Line Stat Block": "CR 1 | AC/DC 12 | HP 33 (25-41) | Atk/Prof +5 | DPR 12 | # Atks 2 | Dmg 6 (1d8 + 2)"
},
"2": {
  "Eqv Char Lvl": "5",
  "AC/DC": 13,
  "HP": "45 (34-56)",
  "Attack/Prof": "+5",
  "DPR": 17,
  "# of Attacks": 2,
  "Damage": "9 (2d6 + 2)",
  "Example Monster": "[[Ghast]], [[ogre]], [[priest]]",
  "One Line Stat Block": "CR 2 | AC/DC 13 | HP 45 (34-56) | Atk/Prof +5 | DPR 17 | # Atks 2 | Dmg 9 (2d6 + 2)"
},
"3": {
  "Eqv Char Lvl": "7",
  "AC/DC": 13,
  "HP": "65 (49-81)",
  "Attack/Prof": "+5",
  "DPR": 23,
  "# of Attacks": 2,
  "Damage": "12 (2d8 + 3)",
  "Example Monster": "[[Knight]], [[mummy]], [[werewolf]]",
  "One Line Stat Block": "CR 3 | AC/DC 13 | HP 65 (49-81) | Atk/Prof +5 | DPR 23 | # Atks 2 | Dmg 12 (2d8 + 3)"
},
"4": {
  "Eqv Char Lvl": "9",
  "AC/DC": 14,
  "HP": "84 (64-106)",
  "Attack/Prof": "+6",
  "DPR": 28,
  "# of Attacks": 2,
  "Damage": "14 (3d8 + 1)",
  "Example Monster": "[[Ettin]], [[ghost]]",
  "One Line Stat Block": "CR 4 | AC/DC 14 | HP 84 (64-106) | Atk/Prof +6 | DPR 28 | # Atks 2 | Dmg 14 (3d8 + 1)"
},
"5": {
  "Eqv Char Lvl": "10",
  "AC/DC": 15,
  "HP": "95 (71-119)",
  "Attack/Prof": "+7",
  "DPR": 35,
  "# of Attacks": 3,
  "Damage": "12 (3d6 + 2)",
  "Example Monster": "[[Elemental]], [[gladiator]], [[vampire-spawn]]",
  "One Line Stat Block": "CR 5 | AC/DC 15 | HP 95 (71-119) | Atk/Prof +7 | DPR 35 | # Atks 3 | Dmg 12 (3d6 + 2)"
},
"6": {
  "Eqv Char Lvl": "11",
  "AC/DC": 15,
  "HP": "112 (84-140)",
  "Attack/Prof": "+7",
  "DPR": 41,
  "# of Attacks": 3,
  "Damage": "14 (3d6 + 4)",
  "Example Monster": "[[Mage]], [[medusa]], [[wyvern]]",
  "One Line Stat Block": "CR 6 | AC/DC 15 | HP 112 (84-140) | Atk/Prof +7 | DPR 41 | # Atks 3 | Dmg 14 (3d6 + 4)"
},
"7": {
  "Eqv Char Lvl": "12",
  "AC/DC": 15,
  "HP": "130 (98-162)",
  "Attack/Prof": "+7",
  "DPR": 47,
  "# of Attacks": 3,
  "Damage": "16 (3d8 + 3)",
  "Example Monster": "[[Stone-giant]], [[young-black-dragon]]",
  "One Line Stat Block": "CR 7 | AC/DC 15 | HP 130 (98-162) | Atk/Prof +7 | DPR 47 | # Atks 3 | Dmg 16 (3d8 + 3)"
},
"8": {
  "Eqv Char Lvl": "13",
  "AC/DC": 15,
  "HP": "136 (102-170)",
  "Attack/Prof": "+7",
  "DPR": 53,
  "# of Attacks": 3,
  "Damage": "18 (3d10 + 2)",
  "Example Monster": "[[Assassin]], [[frost-giant]]",
  "One Line Stat Block": "CR 8 | AC/DC 15 | HP 136 (102-170) | Atk/Prof +7 | DPR 53 | # Atks 3 | Dmg 18 (3d10 + 2)"
},
"9": {
  "Eqv Char Lvl": "15",
  "AC/DC": 16,
  "HP": "145 (109-181)",
  "Attack/Prof": "+8",
  "DPR": 59,
  "# of Attacks": 3,
  "Damage": "22 (3d12 + 3)",
  "Example Monster": "[[Bone-devil]], [[fire-giant]], [[young-blue-dragon]]",
  "One Line Stat Block": "CR 9 | AC/DC 16 | HP 145 (109-181) | Atk/Prof +8 | DPR 59 | # Atks 3 | Dmg 22 (3d12 + 3)"
},
"10": {
  "Eqv Char Lvl": "16",
  "AC/DC": 17,
  "HP": "155 (116-194)",
  "Attack/Prof": "+9",
  "DPR": 65,
  "# of Attacks": 4,
  "Damage": "16 (3d8 + 3)",
  "Example Monster": "[[Stone-golem]], [[young-red-dragon]]",
  "One Line Stat Block": "CR 10 | AC/DC 17 | HP 155 (116-194) | Atk/Prof +9 | DPR 65 | # Atks 4 | Dmg 16 (3d8 + 3)"
},
"11": {
  "Eqv Char Lvl": "17",
  "AC/DC": 17,
  "HP": "165 (124-206)",
  "Attack/Prof": "+9",
  "DPR": 71,
  "# of Attacks": 4,
  "Damage": "18 (3d10 + 2)",
  "Example Monster": "[[Djinni]], [[efreeti]], [[horned-devil]]",
  "One Line Stat Block": "CR 11 | AC/DC 17 | HP 165 (124-206) | Atk/Prof +9 | DPR 71 | # Atks 4 | Dmg 18 (3d10 + 2)"
},
"12": {
  "Eqv Char Lvl": "18",
  "AC/DC": 17,
  "HP": "175 (131-219)",
  "Attack/Prof": "+9",
  "DPR": 77,
  "# of Attacks": 4,
  "Damage": "19 (3d10 + 3)",
  "Example Monster": "[[Archmage]], [[erinyes]]",
  "One Line Stat Block": "CR 12 | AC/DC 17 | HP 175 (131-219) | Atk/Prof +9 | DPR 77 | # Atks 4 | Dmg 19 (3d10 + 3)"
},
"13": {
  "Eqv Char Lvl": "19",
  "AC/DC": 18,
  "HP": "184 (138-230)",
  "Attack/Prof": "+10",
  "DPR": 83,
  "# of Attacks": 4,
  "Damage": "21 (4d8 + 3)",
  "Example Monster": "[[Adult-white-dragon]], [[storm-giant]], [[vampire]]",
  "One Line Stat Block": "CR 13 | AC/DC 18 | HP 184 (138-230) | Atk/Prof +10 | DPR 83 | # Atks 4 | Dmg 21 (4d8 + 3)"
},
"14": {
  "Eqv Char Lvl": "20",
  "AC/DC": 19,
  "HP": "196 (147-245)",
  "Attack/Prof": "+11",
  "DPR": 89,
  "# of Attacks": 4,
  "Damage": "22 (4d10)",
  "Example Monster": "[[Adult-black-dragon]], [[ice-devil]]",
  "One Line Stat Block": "CR 14 | AC/DC 19 | HP 196 (147-245) | Atk/Prof +11 | DPR 89 | # Atks 4 | Dmg 22 (4d10)"
},
"15": {
  "Eqv Char Lvl": "> 20",
  "AC/DC": 19,
  "HP": "210 (158-263)",
  "Attack/Prof": "+11",
  "DPR": 95,
  "# of Attacks": 5,
  "Damage": "19 (3d10 + 3)",
  "Example Monster": "[[Adult-green-dragon]], [[mummy-lord]], [[purple-worm]]",
  "One Line Stat Block": "CR 15 | AC/DC 19 | HP 210 (158-263) | Atk/Prof +11 | DPR 95 | # Atks 5 | Dmg 19 (3d10 + 3)"
},
"16": {
  "Eqv Char Lvl": "> 20",
  "AC/DC": 19,
  "HP": "229 (172-286)",
  "Attack/Prof": "+11",
  "DPR": 101,
  "# of Attacks": 5,
  "Damage": "21 (4d8 + 3)",
  "Example Monster": "[[Adult-blue-dragon]], [[iron-golem]], [[marilith]]",
  "One Line Stat Block": "CR 16 | AC/DC 19 | HP 229 (172-286) | Atk/Prof +11 | DPR 101 | # Atks 5 | Dmg 21 (4d8 + 3)"
},
"17": {
  "Eqv Char Lvl": "> 20",
  "AC/DC": 20,
  "HP": "246 (185-308)",
  "Attack/Prof": "+12",
  "DPR": 107,
  "# of Attacks": 5,
  "Damage": "22 (3d12 + 3)",
  "Example Monster": "[[Adult-red-dragon]]",
  "One Line Stat Block": "CR 17 | AC/DC 20 | HP 246 (185-308) | Atk/Prof +12 | DPR 107 | # Atks 5 | Dmg 22 (3d12 + 3)"
},
"18": {
  "Eqv Char Lvl": "> 20",
  "AC/DC": 21,
  "HP": "266 (200-333)",
  "Attack/Prof": "+13",
  "DPR": 113,
  "# of Attacks": 5,
  "Damage": "23 (4d10 + 1)",
  "Example Monster": "[[Demilich]]",
  "One Line Stat Block": "CR 18 | AC/DC 21 | HP 266 (200-333) | Atk/Prof +13 | DPR 113 | # Atks 5 | Dmg 23 (4d10 + 1)"
},
"19": {
  "Eqv Char Lvl": "> 20",
  "AC/DC": 21,
  "HP": "285 (214-356)",
  "Attack/Prof": "+13",
  "DPR": 119,
  "# of Attacks": 5,
  "Damage": "24 (4d10 + 2)",
  "Example Monster": "[[Balor]]",
  "One Line Stat Block": "CR 19 | AC/DC 21 | HP 285 (214-356) | Atk/Prof +13 | DPR 119 | # Atks 5 | Dmg 24 (4d10 + 2)"
},
"20": {
  "Eqv Char Lvl": "> 20",
  "AC/DC": 21,
  "HP": "300 (225-375)",
  "Attack/Prof": "+13",
  "DPR": 132,
  "# of Attacks": 5,
  "Damage": "26 (4d12)",
  "Example Monster": "[[Ancient-white-dragon]], [[pit-fiend]]",
  "One Line Stat Block": "CR 20 | AC/DC 21 | HP 300 (225-375) | Atk/Prof +13 | DPR 132 | # Atks 5 | Dmg 26 (4d12)"
},
"21": {
  "Eqv Char Lvl": "> 20",
  "AC/DC": 22,
  "HP": "325 (244-406)",
  "Attack/Prof": "+14",
  "DPR": 150,
  "# of Attacks": 5,
  "Damage": "30 (4d12 + 4)",
  "Example Monster": "[[Ancient-black-dragon]], [[lich]], [[solar]]",
  "One Line Stat Block": "CR 21 | AC/DC 22 | HP 325 (244-406) | Atk/Prof +14 | DPR 150 | # Atks 5 | Dmg 30 (4d12 + 4)"
},
"22": {
  "Eqv Char Lvl": "> 20",
  "AC/DC": 23,
  "HP": "350 (263-438)",
  "Attack/Prof": "+15",
  "DPR": 168,
  "# of Attacks": 5,
  "Damage": "34 (4d12 + 8)",
  "Example Monster": "[[Ancient-green-dragon]]",
  "One Line Stat Block": "CR 22 | AC/DC 23 | HP 350 (263-438) | Atk/Prof +15 | DPR 168 | # Atks 5 | Dmg 34 (4d12 + 8)"
},
"23": {
  "Eqv Char Lvl": "> 20",
  "AC/DC": 23,
  "HP": "375 (281-469)",
  "Attack/Prof": "+15",
  "DPR": 186,
  "# of Attacks": 5,
  "Damage": "37 (6d10 + 4)",
  "Example Monster": "[[Ancient-blue-dragon]], [[kraken]]",
  "One Line Stat Block": "CR 23 | AC/DC 23 | HP 375 (281-469) | Atk/Prof +15 | DPR 186 | # Atks 5 | Dmg 37 (6d10 + 4)"
},
"24": {
  "Eqv Char Lvl": "> 20",
  "AC/DC": 23,
  "HP": "400 (300-500)",
  "Attack/Prof": "+15",
  "DPR": 204,
  "# of Attacks": 5,
  "Damage": "41 (6d10 + 8)",
  "Example Monster": "[[Ancient-red-dragon]]",
  "One Line Stat Block": "CR 24 | AC/DC 23 | HP 400 (300-500) | Atk/Prof +15 | DPR 204 | # Atks 5 | Dmg 41 (6d10 + 8)"
},
"25": {
  "Eqv Char Lvl": "> 20",
  "AC/DC": 24,
  "HP": "430 (323-538)",
  "Attack/Prof": "+16",
  "DPR": 222,
  "# of Attacks": 5,
  "Damage": "44 (6d10 + 11)",
  "Example Monster": "",
  "One Line Stat Block": "CR 25 | AC/DC 24 | HP 430 (323-538) | Atk/Prof +16 | DPR 222 | # Atks 5 | Dmg 44 (6d10 + 11)"
},
"26": { 
	"Eqv Char Lvl": "> 20", 
	"AC/DC": 25, 
	"HP": "460 (345-575)", 
	"Attack/Prof": "+17", 
	"DPR": 240, 
	"# of Attacks": 5, 
	"Damage": "48 (6d10 + 15)", 
	"Example Monster": "", 
	"One Line Stat Block": "CR 26 | AC/DC 25 | HP 460 (345-575) | Atk/Prof +17 | DPR 240 | # Atks 5 | Dmg 48 (6d10 + 15)" 
},
"27": {
  "Eqv Char Lvl": "> 20",
  "AC/DC": 25,
  "HP": "490 (368-613)",
  "Attack/Prof": "+17",
  "DPR": 258,
  "# of Attacks": 5,
  "Damage": "52 (6d10 + 19)",
  "Example Monster": "",
  "One Line Stat Block": "CR 27 | AC/DC 25 | HP 490 (368-613) | Atk/Prof +17 | DPR 258 | # Atks 5 | Dmg 52 (6d10 + 19)"
},
"28": {
  "Eqv Char Lvl": "> 20",
  "AC/DC": 25,
  "HP": "540 (405-675)",
  "Attack/Prof": "+17",
  "DPR": 276,
  "# of Attacks": 5,
  "Damage": "55 (6d10 + 22)",
  "Example Monster": "",
  "One Line Stat Block": "CR 28 | AC/DC 25 | HP 540 (405-675) | Atk/Prof +17 | DPR 276 | # Atks 5 | Dmg 55 (6d10 + 22)"
},
"29": {
  "Eqv Char Lvl": "> 20",
  "AC/DC": 26,
  "HP": "600 (450-750)",
  "Attack/Prof": "+18",
  "DPR": 294,
  "# of Attacks": 5,
  "Damage": "59 (6d10 + 26)",
  "Example Monster": "",
  "One Line Stat Block": "CR 29 | AC/DC 26 | HP 600 (450-750) | Atk/Prof +18 | DPR 294 | # Atks 5 | Dmg 59 (6d10 + 26)"
},
"30": {
  "Eqv Char Lvl": "> 20",
  "AC/DC": 27,
  "HP": "666 (500-833)",
  "Attack/Prof": "+19",
  "DPR": 312,
  "# of Attacks": 5,
  "Damage": "62 (6d10 + 29)",
  "Example Monster": "[[Tarrasque]]",
  "One Line Stat Block": "CR 30 | AC/DC 27 | HP 666 (500-833) | Atk/Prof +19 | DPR 312 | # Atks 5 | Dmg 62 (6d10 + 29)"
}

};

function onCrUpdate(crValue) {

let markdownBuilder = engine.markdown.createBuilder();

    if (crBuild[crValue]) {
        const crData = crBuild[crValue];

        // Create a heading for the selected CR
        // Uncomment below line if you want a heading
        // markdownBuilder.createHeading(2, `CR ${crValue}`);

        // Render the data for the selected CR
        for (const key in crData) {
            markdownBuilder.createParagraph(`**${key}**: ${crData[key]}`);
        }
    } else {
        markdownBuilder.createParagraph("CR value not found in the data.");
    }

    return markdownBuilder;
}

// Create a js engine reactive component
const reactive = engine.reactive(onCrUpdate, signal.get())
// Tell the component to rerender when the metadata cache changes
signal.registerListener({
    callback: (v) => reactive.refresh(v),
})

return reactive;

```

#### Other Features

Give any custom monster impactful features and attacks that make sense for their place in the game. When a monster feature deals damage, choose a damage type appropriate to the creature's physiology, theme, or story. A creature channeling magical power might deal acid, cold, fire, lightning, force, poison, psychic, necrotic, radiant, or thunder damage. A creature making use of spines, spikes, or projectiles might deal bludgeoning, piercing, or slashing damage.

## Monster Feature: `INPUT[suggester(option(Damaging Blast), option(Damage Reflection), option(Misty Step), option(Knockdown), option(Restraining Grab), option(Damaging Burst), option(Cunning Action), option(Damaging Aura), option(Energy Weapons), option(Damage Transference)):mf]`


```js-engine
const mb = engine.getPlugin('obsidian-meta-bind-plugin').api;

const signal = mb.createSignal(undefined)
// Register to listen for changes in the 'mf' property
component.register(mb.listenToMetadata(signal, context.file.path, ['mf']))

// Define the monster features and their descriptions
const featuresData = {
  "Damaging Blast": "This creature has one or more single-target ranged attacks using the attack bonus and damage calculated above, and which deal damage of an appropriate type.",
  "Damage Reflection": "Whenever a creature within 5 feet of this creature hits them with a melee attack, the attacker takes damage in return of a type appropriate to the creature. The damage dealt is equal to half the damage of one of this creature's attacks. If you give a creature this feature, give them one less attack than normal.",
  "Misty Step": "As a bonus action, this creature can teleport up to 30 feet to an unoccupied space they can see.",
  "Knockdown": "When this creature hits a target with a melee attack, the target must succeed on a Strength saving throw or be knocked prone.",
  "Restraining Grab": "When this creature hits a target with a melee attack, the target is grappled (escape DC based on this creature's Strength or Dexterity modifier). While grappled, the target is restrained.",
   "Damaging Burst": "As an action, this creature can create a burst of energy, magic, spines, or some other effect in a 10-foot-radius sphere, either around themself or at a point within 120 feet. Each creature in that area must make a Dexterity, Constitution, or Wisdom saving throw (your choice, based on the type of burst). On a failure, a target takes damage of an appropriate type equal to half this creature's total damage per round. On a success, a target takes half as much damage.", 
   "Cunning Action": "On each of their turns, this creature can use a bonus action to take the Dash, Disengage, or Hide action.", 
   "Damaging Aura": "Each creature who starts their turn within 10 feet of this creature takes damage of a type appropriate to the creature. The damage dealt is equal to half the damage of one of this creature's attacks. If you give a creature this feature, give them one less attack than normal.", 
   "Energy Weapons": "The creature's weapon attacks deal extra damage of an appropriate type. You can add this damage on top of the creature's regular damage output to give them a combat boost, or you can replace some of the creature's normal weapon damage with this energy damage.", 
   "Damage Transference": "When this creature takes damage, they can transfer half or all of that damage (your choice) to a willing creature within 30 or 60 feet of them. This feature is particularly good for boss monsters."
};

function onFrUpdate(featureName) {
  // Create a Markdown builder
  let markdownBuilder = engine.markdown.createBuilder();

  // Check if the feature name exists and has a description
  if (featuresData[featureName]) {
    const featureDescription = featuresData[featureName];

    // Render the description for the selected feature
    markdownBuilder.createParagraph(featureDescription);
  } else {
    // Display a message if the feature name is not found
    markdownBuilder.createParagraph("Feature description not found.");
  }

  // Return the Markdown builder
  return markdownBuilder;
}

// Create a js engine reactive component
const reactive = engine.reactive(onFrUpdate, signal.get())
// Tell the component to rerender when the metadata cache changes
signal.registerListener({
    callback: (v) => reactive.refresh(v),
})

return reactive;

```


> [!info|hover]- License  
> This work includes material taken from the [Lazy GM's 5e Monster Builder Resource Document](https://slyflourish.com/lazy_5e_monster_building_resource_document.html) written by Teos Abadía of [Alphastream.org](https://alphastream.org/), Scott Fitzgerald Gray of [Insaneangel.com](https://insaneangel.com/), and Michael E. Shea of [SlyFlourish.com](https://slyflourish.com/), available under a [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).
