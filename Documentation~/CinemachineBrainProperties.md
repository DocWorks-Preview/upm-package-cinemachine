# Setting Cinemachine Brain properties

The Cinemachine Brain is a component in the Unity camera itself. Cinemachine Brain monitors all active Virtual Cameras in the Scene. It chooses the next Virtual Camera to control the Unity camera. It also controls the [cut or blend](CinemachineBlending.html) from the current Virtual Camera to the next.

To add a Cinemachine Brain component to a Unity camera, do **one** of the following:

* [Add a Virtual Camera](CinemachineSetUpVCam.html), or other Cinemachine object, to your Scene. Unity adds a Cinemachine Brain component to the Unity camera for you if there isn’t one already.

* [Add](https://docs.unity3d.com/Manual/UsingComponents.html) a Cinemachine Brain component to the Unity camera yourself.

**Tip**: You can also control Virtual Cameras from [Timeline](CinemachineTimeline.html). Timeline overrides the decisions that Cinemachine Brain makes.

Cinemachine Brain holds the following key properties:

* **Blend Settings**: A list that defines how to blend from one Virtual Camera to another.  For example, add an item to the list for a 4 second blend from vcam1 to vcam2 then add another item for a 1 second blend from vcam2 back to vcam1. If a blend between two cameras isn’t defined, Cinemachine Brain uses its default blend.

* **Layer Filter**:  Cinemachine Brain uses only those Virtual Cameras that pass the culling mask of the Unity camera.  You can set up [split-screen environments](CinemachineMultipleCameras.html) by using the culling mask to filter layers.

* **Event Dispatching**:  Cinemachine Brain fires events when it changes shot. It fires an event when a Virtual Camera goes live. It also fires an event when it cuts from one Virtual Camera to another. Use the latter event to reset temporal post effects.

![Cinemachine Brain, a component in the Unity camera](Images/CinemachineBrain_5c6c12dedd83130d44febdf7.png)

## Properties:

| **Property:** || **Function:** |
|:---|:---|:---|
| **Show Debug Text** || Check to display a textual summary of the live Virtual Camera and blend in the view. |
| **Show Camera Frustum** || Check to display the frustum of the camera in the Scene view. |
| **Ignore Time Scale** || Check to make the Virtual Cameras respond in real time to user input and damping, even if the game is running in slow motion. |
| **World Up Override** || The Y axis of the specified GameObject defines the worldspace up vector for Virtual Cameras. Use this property in top-down game environments. Set to None to use the worldspace Y axis. Setting this appropriately is important to avoid gimbal-lock in extreme up/down conditions. |
| **Update Method** || When to update the position and rotation of the Virtual Cameras.  |
| | _Fixed Update_ | Synchronize Virtual Camera update with the Physics module, in FixedUpdate. |
| | _Late Update_ | In MonoBehaviour LateUpdate. |
| | _Smart Update_ | Update each virtual camera according to how its target is updated. This is the recommended setting. |
| **Default Blend** || The blend to use when you haven’t explicitly defined a blend between two Virtual Cameras. |
| | _Cut_ | Zero-length blend. |
| | _Ease In Out_ | S-shaped curve, giving a gentle and smooth transition. |
| | _Ease In_ | Linear out of the outgoing shot, and easy into the incoming. |
| | _Ease Out_ | Easy out of the outgoing shot, and linear into the incoming. |
| | _Hard In_ | Easy out of the outgoing, and hard into the incoming. |
| | _Hard Out_ | Hard out of the outgoing, and easy into the incoming. |
| | _Linear_ | Linear blend. Mechanical-looking. |
| | _Custom_ | Custom blend curve. Draw the curve you want. |
| **Custom Blends** || The asset that contains custom settings for blends between specific Virtual Cameras in your Scene. |
| **Create Asset** || Create an asset containing a [list of custom blends](CinemachineBlending.html) between Virtual Cameras.  |
| **Camera Cut Event** || This event fires when a Virtual Camera goes live and there is no blend.  |
| **Camera Activated Event** || This event fires when a Virtual Camera goes live. If a blend is involved, then the event fires on the first frame of the blend. |

