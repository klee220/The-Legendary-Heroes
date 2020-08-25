# CS 100 Programming Project
## To large to upload to git
download of the repo here
  https://mega.nz/folder/WTIRmKra#ICKPAaNiTEzpEkubSbCh0w

## Project details
Project Name: The Legendary Heroes

Group Members: Karina Lee (klee220@ucr.edu), Samiha Kibria (skibr001@ucr.edu), Michael Risher (mrish001@ucr.edu)

App: A RPG style game in the vein of old Final Fantasy games.

In this game, the user will be put into battle against various enemies. Each type of enemy will have different amounts of HP, MP, and attack points. The user will be able to select an action, either magic, or attack, in each of their turns in battle. The goal of the game is to win the battles. The development will focus on the development of the gameplay mechanics and the implementation of design patterns.

This project is important as it allows the group members to create a project that can be used in portfolios and to gain experience in the development of a game, as our group members are looking towards graduation and finding internships. The team wishes to learn about and familiarize with tools and the process that is currently used in the industry today. With COVID-19 and everyone experiencing self-quarantine, it is important for our group to learn something valuable for our future and, at the same time, create something that could be used as entertainment to bring joy during these difficult times.

Tools: The team will use Unreal Engine, a game engine, as it uses C++ script, and it is a standard used currently in the industry.

I/O: Input will be keyboard inputs "a", "s", and the directional keys. Output will be as follows: "a" accepts, "s" will cancel, and directional keys will give movement to the character.

## UML Diagram for project
Image of uml diagram

## UML description
In our game, we will be using three design patterns: visitor, decorator, and abstract factory.

The client uses the abstract Character class to create a Player, and the abstract factory pattern to create enemies. Player and Enemy both inherit from RPGCharacter.

For the abstract factory pattern, the EnemyFactory class is the abstract factory. From this, the concrete factory BP_EnemyFactory is derived which constructs RPGCharacterEnemy.

The Character objects have an Action. We use the decorator pattern to implement Action and its subclasses. AbstractAction is the abstract component class, which defines the interface for the objects that can have responsibilities added to them. Action is our concrete component, which defines an object that can have responsibilities added. ActionDecorator is our abstract decorator, which defines an interface that implements the abstract Action’s interface. Attack, Fire, Water, and Lightning are our concrete decorators, which extend ActionDecorator and add responsibilities to Action.

For the visitor pattern, we have a concrete visitor Visitor_Actor that derives from the abstract visitor class. The Visitor_actor works as a timer to trigger battles. When it visits anything that isn't a ThirdPerson.BP it triggers a battle for the player.

## Test Cases
When the left key is pressed, the character moves left.

When the right key is pressed, the character moves right.

When the up key is pressed, the character moves up.

When the down key is pressed, the character moves down.

When “a” is pressed, a selection is made.

The user may select one of the following actions for each of their turns in battle: attack, fire, stream, lightning.

When the user chooses attack, MP does not decrease, and the character inflicts 1 damage point to the enemy.

When the user casts a fire spell, MP decreases by 3 and the character inflicts 3 damage point to the enemy.

When the user casts a stream spell, MP decreases by 1 and the character inflicts 1 damage points to the enemy.

When the user casts a lightning spell, MP decreases by 5 and the character inflicts 5 damage points to the enemy.

When “s” is pressed, the selection is canceled.

A battle is initiated within 30 seconds.

In battle, players are ordered by speed.

The user will have two allies.

The user will face between one and four enemies, which may be any of the following types: wolf, goblin, orc, and troll.

The wolf has the following stats: 100-125 hp, 5 attack, 5 defense, 5 resistance, and 5-10 speed points.

The goblin has the following stats: 75-100 hp, 5 attack, 5 defense, 5-10 resistance, and 5-10 speed points.

The orc has the following stats: 75-100 hp, 5-10 attack, 5 defense, 5 resistance, and 0-5 speed points.

The troll has the following stats: 75-100 hp, 5 attack, 5-10 defense, 5 resistance, and 0-5 speed points.
