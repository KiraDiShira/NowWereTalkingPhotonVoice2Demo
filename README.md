# NowWereTalkingPhotonVoice2Demo

### 1 Create a Photon engine account

[Link](https://id.photonengine.com/account/signup)

### 2 Create a new Fusion application

[Link](https://dashboard.photonengine.com/app/create)

![Alt text](fusion.png "Optional title")

### 3 Get Fusion App Id

[Link](https://dashboard.photonengine.com/)

![Alt text](fusion2.png "Optional title")

### 4 Create a new Voice application

Like step 2, but *Select Photon SDK* value should be *VOICE*

### 5 Get Voice App Id

Like step 3

### 6 Setting Fusion and Voice App Ids in Unity

![Alt text](fusion3.png "Optional title")


![Alt text](fusion4.png "Optional title")

## Launch The Game

Go in the following Path:

\NowWereTalkingPhotonVoice2Demo\Assets\Photon\PhotonVoice\Demos\Fusion\DemoNetworkObject

The main scene is **Scene**.

You need to launch two instances and for each one you should click on **Start Shared Client**

At this point you should see two cube that can talk each other with voice.

## Random informations

The player is an instance of **NetworkObject** prefab: NowWereTalkingPhotonVoice2Demo\Assets\Photon\PhotonVoice\Demos\Fusion\DemoNetworkObject.
That prefab has a **Voice network object** component and a  **speaker** component in children.

The **Runner and Voice** prefab has a **Fusion voice client** component and also a recorder component as child.

In any client if you want to know if the local player is speaking you need something like this:

```player.VoiceNetworkObject.RecorderInUse.IsCurrentlyTransmitting```

Instead if you want to know if a remote player is speaking:

```player.VoiceNetworkObject.IsSpeaking```


