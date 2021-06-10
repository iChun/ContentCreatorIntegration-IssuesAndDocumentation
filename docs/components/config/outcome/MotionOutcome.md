Motion Outcome
============= 

## Description

Adjust the motion of a set of entities This Outcome is Client-side only if `doOnPlayer` is set to `true`.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `motion`       |         Not seen in the Editor.        |
| *`target`*[^1] | String |      The target selector for the entities to affect.       |                 |
| *`amount`* | String |      The amount of motion to apply.       |                 |
| *`axis`* | String |      The axis to apply the motion to. Supports `x`, `y`, `z`.       |                 |
| `relative` | Boolean |      Should the motion applied be relative to the entity instead of absolute?       |                 |
| *`doOnPlayer`*[^1] | Boolean |      Apply this to just the player? Due to how Minecraft works, the player on the client has it's own motion and cannot be modified by the server.       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
[^1]: Either field is required for the Object to be valid.
