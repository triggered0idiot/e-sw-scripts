# Setting up a checkpoint.
<i><span style="color:FireBrick; font-size:10px;">Need help? Come to the Envy & Spite Discord server at <a href="https://discord.gg/RY8J67neJ9">https://discord.gg/RY8J67neJ9</a>!</span></i>

# Beginning

<b>Checkpoints are usually over looked in levels However , They play an essential part in how levels are played, as dying and starting all over isnt fun.</b>

# Actual usage

<b>Alright lets explain 1 thing, Checkpoints can crash your game.</b>

*But you may be wondering why?*

Well thats due to you having a checkpoint which contains a room/gameobject that has another checkpoint under it.

So lets firstly drag Checkpoint_0 into our scene and we can see some fields, Mainly `Rooms` and `Rooms to Inherit` , but what does this all mean? Well basically, `Rooms` is what gets saved when the scene is loaded, This isnt usually recommended but its there.

>[!CAUTION]
>Checkpoints mustn't be parented. They must be outside of everything.

<img src="https://coolboi21.github.io/Rude-Docs/Tutorials/Beginner/assets/creating-checkpoints-checkpoint-settings.png" alt="checkpoint settings" width="50%" height="50%" >

Now `Rooms to Inherit` is what you mainly want to be using, the stuff you assign to it will be saved once you HIT the checkpoint not during the start of the map, Additionally, if you are using this for encounters, Assign the `Stuff` gameobject here

Last but not least we have two things left, `To Activate`'s list and `Doors to Unlock`'s list, these are rather simple:

- `To Activate` - Is a field where once the player hits the checkpoint, the gameobject in the field gets activated.
	- This is pretty useful for optimization because it allows big sections of levels to be disabled up until you reach them.
	
- `Doors to Unlock` - Is a really important field, as it unlocks previously locked doors from if you were in a wave and you died, wouldnt be nice if you died during a encounter and the door was still locked and you couldnt get in.
