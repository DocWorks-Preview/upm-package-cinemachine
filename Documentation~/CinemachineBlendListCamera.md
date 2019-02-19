# Cinemachine Blend List Camera

The **Cinemachine Blend List Camera** component executes a sequence of blends or cuts among its child Virtual Cameras.

When the Blend List camera is activated, it executes its list of instructions, activating the first child Virtual Camera in the list, holding for a designated time, then cutting or blending to the next child, and so on. The Blend List camera holds the last Virtual Camera until Cinemachine Brain or Timeline deactivates the Blend List camera.

**Tip**: Use a Blend List Camera instead of  [Timeline](CinemachineTimeline.html) for simpler, automatic sequences.

## Properties:

| **Property:** | **Function:** |
|:---|:---|
| **Solo** | Toggles whether or not the Blend List camera is temporarily live. Use this property to get immediate visual feedback in the [Game view](https://docs.unity3d.com/Manual/GameView.html) to adjust the Virtual Camera. |
| **Game Window Guides** | Toggles the visibility of compositional guides in the Game view. This property applies to all Virtual Cameras. |
| **Save During Play** | Check to [apply the changes while in Play mode](CinemachineSavingDuringPlay.html).  Use this feature to fine-tune a Virtual Camera without having to remember which properties to copy and paste. This property applies to all Virtual Cameras. |
| **Priority** | The importance of this Blend List camera for choosing the next shot. A higher value indicates a higher priority. Cinemachine Brain chooses the next live Virtual Camera from all Virtual Cameras that are activated and have the same or higher priority as the current live Virtual Camera. This property has no effect when using a Virtual Camera with Timeline. |
| **Look At** | The default target GameObject that the children Virtual Camera move with. The Blend List camera uses this target when the child does not specify this target. May be empty if all of the children define targets of their own. |
| **Follow** | The default target GameObject to aim the Unity camera at. The Blend List camera uses this target when the child does not specify this target. May be empty if all of the children define targets of their own. |
| **Show Debug Text** | Check to display a textual summary of the live Virtual Camera and blend in the view. |
| **Enable All Child Cameras** | Check to activate all child cameras. This is useful if animating them in Timeline, but consumes extra resources. |
| **Instructions** | The set of instructions for enabling child cameras. |
