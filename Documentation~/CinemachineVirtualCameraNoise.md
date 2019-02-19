# Noise properties

Use Noise properties in a Virtual Camera to simulate camera shake. Cinemachine includes a **Basic Multi Channel Perlin** component, which adds Perlin noise to the movement of the Virtual Camera. **Perlin noise** is a technique to compute random movement with a natural behavior.

![Choosing the Basic Multi Channel Perlin component to add camera noise](Images/CinemachineBasicMultiChannelPerlin_5c6c12dddd83130d44febdef.png)

The Basic Multi Channel Perlin component applies a noise profile. A noise profile is an Asset that defines the behavior of noise over time. Cinemachine includes a few noise profile assets. You can [edit these and create your own](CinemachineNoiseProfiles.html).

To apply noise:

1. Select your Virtual Camera in the [Scene](https://docs.unity3d.com/Manual/UsingTheSceneView.html) view or [Hierarchy](https://docs.unity3d.com/Manual/Hierarchy.html) window.

2. In the [Inspector](https://docs.unity3d.com/Manual/UsingTheInspector.html), use the  **Noise** drop-down menu to choose **Basic Multi Channel Perlin**.

3. In **Noise Profile**, choose an existing profile asset or [create your own profile](CinemachineNoiseProfiles.html).

4. Use **Amplitude Gain** and **Frequency Gain** to fine-tune the noise.

## Properties

| **Property:** | **Function:** |
|:---|:---|
| **Noise Profile** | The noise profile asset to use.|
| **Amplitude Gain** | Gain to apply to the amplitudes defined in the noise profile. Use 1 to use the amplitudes defined in the noise profile. Setting this to 0 mutes the noise. Tip: Animate this property to ramp the noise effect up and down.|
| **Frequency Gain** | Factor to apply to the frequencies defined in the noise profile. Use 1 to use the frequencies defined in the noise profile. Use larger values to shake the camera more rapidly. Tip: Animate this property to ramp the noise effect up and down. |



