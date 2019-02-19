# Blending between Virtual Cameras

Use blending properties to specify how the Cinemachine Brain component performs a blend between virtual cameras.

A Cinemachine blend is not a fade, wipe, or dissolve. Rather, Cinemachine Brain performs a smooth animation of the position, rotation, and other settings of the Unity camera from one Virtual Camera to the next.

For blends between specific Virtual Cameras, use the **Custom Blends** list in the Cinemachine Brain component. Use the **Default Blend** property in Cinemachine Brain to specify blends between Virtual Cameras that do not have custom blends.

![Custom Blends list in Cinemachine Brain](Images/CinemachineCustomBlends_5c6c12dedd83130d44febdfa.png)

The **From** and **To** settings are name-based, not references. This means that Cinemachine finds cameras by matching their names to the settings. They are not linked to specific GameObjects.

Use the name \*\*ANY CAMERA\*\* to blend from or to any Virtual Camera.

## Properties:

| **Property:** || **Function:** |
|:---|:---|:---|
| **From** || The name of the Virtual Camera to blend from. Use the name \*\*ANY CAMERA\*\* to blend from any Virtual Camera. This property is available only for custom blends. |
| **To** || The name of the Virtual Camera to blend to. Use the name \*\*ANY CAMERA\*\* to blend to any Virtual Camera. This property is available only for custom blends. |
| **Style Default Blend** || Shape of the blend curve. |
| | _Cut_ | Zero-length blend. |
| | _Ease In Out_ | S-shaped curve, giving a gentle and smooth transition. |
| | _Ease In_ | Linear out of the outgoing Virtual Camera, and ease into the incoming Virtual Camera. |
| | _Ease Out_ | Ease out of the outgoing Virtual Camera, and blend linearly into the incoming Virtual Camera. |
| | _Hard In_ | Ease out of the outgoing Virtual Camera, and accelerate into the incoming Virtual Camera. |
| | _Hard Out_ | Accelerate out of the outgoing Virtual Camera, and ease into the incoming Virtual Camera. |
| | _Linear_ | Linear blend. mechanical-looking. |
| | _Custom_ | Custom blend curve. Allows you to draw a custom blend curve. |
| **Time** || Duration (in seconds) of the blend. |


