---
share: true
tags:
  - foundry
  - macros
date created: Tuesday, October 17th 2023, 4:00:55 pm
date modified: Saturday, November 4th 2023, 5:12:18 pm
---


# Macro Commands

Macros are an exciting part of any virtual tabletop. In Foundry Virtual Tabletop, you will find that macros are as versatile, powerful, and simple as you want them to be. With the right macros, you can speed up your game, automate the unwieldy, and even do things that would normally require use of Add-on Modules. Best of all, macros are easily shared among users, allowing you to pick and choose your own tailored experience in Foundry Virtual Tabletop!

Macros are pre-written commands in Foundry Virtual Tabletop that when used, execute their commands. Macros can be created and accessed through the macro toolbar located on the bottom of the Foundry window. This article will introduce you to two types of macros: 

- **Chat Macros:** Simple and easy to use, chat macros post pre-defined chat messages to the chat log when executed. All users can execute chat macros by default.
- **Script Macros:** Complex and powerful macros which leverage the FVTT API through plain JavaScript to perform functions as simple or as advanced as you can imagine.

## The Macros UI

![Macro Hotbar](https://foundryvtt.s3.us-west-2.amazonaws.com/website-media-dev/user_671/screen/macro-hotbar-2021-02-03.jpg)

The Macro Hotbar is located at the bottom of the game interface. See the legend below for explanations of each element.

The sections of the macro bar are as follows:

#### Macro Hotbar

The Macro Hotbar gives instant keypress access to 10 quick Macros, which can be used to send chat messages or perform scripted API actions. Primarily used by advanced users. Some systems provide the ability to drop items or actors onto the macro bar to generate a macro for quick use. The macro hotbar has four macro pages that users can switch between, giving them up to four different pages of macro layouts for convenience. These can be cycled by using the up and down indicators on the right of the macro bar ( and ).

#### Macro Directory

The Macro Directory () provides access to all macros that have been created which you have permission to view, use, or edit. From inside this directory you can create new macros by clicking the **Create Macro** button, which will open the macro creation dialog, allowing you to set a name and select the type of macro you want to create.

You can also use the **Create Folder** button to create a folder in this directory. Macros can be dragged to and from folders to organize macros as desired. Clicking the Create Macro icon () on the folder itself will open the macro creation dialog, allowing you to create a new macro that will automatically be placed into that folder.

Folders can be edited by right clicking them and selecting "Edit Folder," the resulting dialog allows you to set the name and color of the folder as you see fit. You can also configure the permissions of the folder to decide what level of user can see and use the macros within. This uses the same permission guidelines found in the [Users and Permissions](https://foundryvtt.com/article/users/ "Users and Permissions") article. You can also export all the macros in a folder to an unlocked compendium, create a new rolltable with the macros in the folder as the possible results, remove the folder (this places the macros back into the directory itself), or delete the folder and all items within it.

## Creating, Using, and Sharing Macros

Macros can be created by clicking on an empty slot in the macro bar, and typing out the relevant information. If your Game System supports it, macros can also be created by dragging and dropping an item from an actor sheet to the Hotbar. In addition, existing macros stored in a compendium or in the Macros Directory can be dragged to the macro hotbar for convenience.

#### Executing Macros

Macros can be used by clicking on them in the macro bar, pressing the corresponding number key on your keyboard, or by entering `/macro The Macro's Name` in the chat box. You can also execute a macro from its configuration window by pressing the Execute button at the bottom.

#### Sharing Macros

Macros can be shared in several different ways in Foundry Virtual Tabletop. The easiest method is to copy and paste the macro text. This is as simple as sharing it on Discord, hosting it on a text-pasting website, or putting it in a macro repository- the community wiki has one hosted [here](https://foundryvtt.wiki/en/basics/Macros).

In the Macros Directory, a single Macro can be exported to a JSON file and re-imported in a different World. Lastly, Macros can also be stored in a compendium, which can be shared among users via a Module.

### Creating Chat Macros

Chat macros are, as indicated by the name, macros that will utilize chat when executed. They are simpler to create, but do not have all of the capabilities that a script macro does.

A chat macro can involve a simple dice command like `/r 1d100` linking a document in chat`@Document[Document Name Here]` (where `Document` is the Type for that Document like `Actor`), or displaying pre-written text or an image using HTML tags.

Chat macros work the same as typing a message in chat, and anything you can type into the chat entry field can be entered here. For more information on chat syntax and the possible actions a user can do within the chat entry field, see [Chat Messages](https://foundryvtt.com/article/chat/ "Chat Messages")

#### Example Chat Macros

```
/r 1d6#which of my players is the next victim?
```

```
/roll {4d6kh3, 4d6kh3, 4d6kh3, 4d6kh3, 4d6kh3, 4d6kh3}#Rolling for DND5e Ability Scores. Don't forget to click to expand the message!
```

```
<em><u>Singing:</u>
There once was a ship that put to sea,
and the name of the ship was the <b>Billy o' Tea!</b>
The winds blew hard, her bow dipped down
Blow, me bully boys, blow!</em>
```

```
<h2>Foundry VTT is AWESOME!</h2>
<img src="https://foundryvtt.s3.us-west-2.amazonaws.com/website-media-dev/user_1/asset/fvtt-community-content-anvil-2020-09-16.png" width="100%"/>
```

### What Are Script Macros?

Script macros are more complicated, but powerful commands that can interact with the Foundry JavaScript API. Script macros are limited only by your imagination and the functions available to JavaScript. Users can perform any task using a script macro that their User role and permissions settings allow for them to take. For example, script macros could automatically consume character resources, roll dice checks, toggle conditions, or change Token appearance.

As script macros are more powerful than chat macros, a Gamemaster can choose to disable script macros for players via the permissions system, which is found in the Configure Settings menu under the Game Settings tab.

#### Using Arguments in Macros and Returning Values

Some values are available directly in Macros without passing them in. For example, if a Token is selected the variables `actor` and `token` will both be populated with the values from the selected Token. Macros can also have arguments passed to them programmatically or through the chat box. Arguments that are passed into a macro are available in the `scope` variable in your Macro. For example, if you pass in the argument `id` it will be available at `scope.id`. Before we learn how to pass arguments let's create an example macro that uses an argument and returns a value. It's name will be "Get Actor" and it's ID is "kIuGflzokbwdwla5":

	

`const character = game.actors.get(scope.id); console.log(character); return character;`

	

#### Pass Arguments to Macros Programmatically and Get Their Return Value

This example demonstrates how to get a Macro by it's ID (the demonstration Macro we created above) and then execute it with the argument `id` passed to it. We then capture the return value in the `Actor` variable.

	

`// Get the Macro by it's ID const macro = game.macros.get("kIuGflzokbwdwla5"); // Execute the Macro and pass the 'id' argument in via an object and capture the return value in 'actor' const character = await m.execute({id: "G9CLr70iR4k2pl5l"});` 

	

#### Pass Arguments to Macros From the Chat Box

This example demonstrates how to call a macro from the chat box (the demonstration Macro we created above) and then execute it with the argument `id` passed to it like so:`/macro Get Actor id=G9CLr70iR4k2pl5l`

#### Example Script Macros

##### Scene Wall and Light Duplicator

```javascript
const source = game.scenes.get("9293Opb8eFtD0BxO");

const wallData = source.walls.map(i=>i.toObject())
const lightData = source.lights.map(i=>i.toObject())

await canvas.scene.createEmbeddedDocuments("Wall", wallData)
await canvas.scene.createEmbeddedDocuments("AmbientLight", lightData)
```

##### Emergency Campaign Resolver

```javascript
//Rocks Fall, everyone dies.

const targets = []
game.user.targets.forEach(i => {
	const name = i.name;
	targets.push(name);
})

if (targets.length === 0) {targets = "no one, this time"}

const roll = await new Roll(`8d10+100`).roll();
console.log(this.roll)

const results_html = `<h2>Cave In!</h2>
The cave collapses from above, dealing <a class="inline-result"><i class="fas fa-dice-d20"></i>${roll.total}</a> damage to <strong>${targets}</strong>.`

ChatMessage.create({
	user: game.user._id,
	speaker: ChatMessage.getSpeaker({token: actor}),
	content: results_html
});
```

## API References

While anything within the [Foundry VTT API](https://foundryvtt.com/api/) can be used within a Macro, to interact with Macros themselves, you will primarily use the following API concepts:

- The [Macro Document](https://foundryvtt.com/api/classes/client.Macro.html "Macro Document")
- The [Macros Collection](https://foundryvtt.com/api/classes/client.Macros.html "Macros Collection")
- The [MacroDirectory Setup Application](https://foundryvtt.com/api/classes/client.MacroDirectory.html "MacroDirectory Setup Application")

#### Foundry Virtual Tabletop

[Software License](https://foundryvtt.com/article/license "Software License")[Privacy Policy](https://foundryvtt.com/article/privacy-policy "Privacy Policy")[Terms of Service](https://foundryvtt.com/article/terms-of-service "Privacy Policy")[Partnerships](https://foundryvtt.com/article/partnerships "Partnerships")[Branding Guide](https://foundryvtt.com/article/branding "Branding and Content Kit")[Employment Opportunities](https://foundryvtt.com/article/employment "Employment Opportunities")[Contact Us](https://foundryvtt.com/contact-us/ "Contact Us")

Foundry Virtual Tabletop © Copyright 2023, Foundry Gaming, LLC. All rights reserved.