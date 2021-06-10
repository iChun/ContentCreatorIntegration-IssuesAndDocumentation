Commonly Asked How To's
=======================

## How to Set up CCI

![](./images/faq/judge.png) There's like, a giant [Getting Started section](../../gettingstarted/) to help you out with that.
<br />
<br />


## How to do Math (in CCI)

I can't help you pass your third grade Math, but CCI has a `ArithmeticCondition` to do most mathematical functions you may need. Takes two values and a function.

<br />

## How to get a random Mob for spawning

Check out `RandomStringCondition`. You can list all the Mob types to spawn there. Alternatively, have a list of Outcomes, with a `weight` each, CCI will only pick one when triggering that Config Event.

<br />

## How to give Outcomes a random chance

Use a `ConditionalOutcome` with a `RandomCondition`. Set the chance in `RandomCondition` and the pass and/or fail Outcome in `ConditionalOutcome` and you're all set.

<br />

## How to spawn one mob per raider

Use a `RepeatOutcome` that triggers your entity spawning Outcome. Set `times` to `$amount` and the RepeatOutcome will trigger your spawning Outcome the number of times `$amount` is set to.

<br />

## How to stop mobs from spawning at my feet or in the wall

Use a `TwoHighSpaceCondition`. That will give you (absolute) coordinates where you can spawn entities where there is a (customisable) set height of air blocks, with a solid block to stand on.

<br />

## How to convert messages that break JSON formatting

There is a `JsonSafeCondition` made just for this. Message goes in, JSON-safe messsage pops out. Use this for your `tellraw` or your spawners. Bear in mind that this doesn't prevent Variable Insertion from breaking the message (when you send it in a `CommandOutcome`) anyway, check [here](../../advanced/variableinsertion/) on instructions on how to disable Variable Insertion.
