# AudioTools

...

## Installation
1. Open your Unity project.
2. Add the package via the Package Manager:
   ```
   https://github.com/nosirrahh/NosirrahhTools.git?path=Assets/NosirrahhTools/AudioTools/
   ```

## How to Use

Define which IAudioLoader will be used to load audios.
```csharp
AudioManager.Instance.SetAudioLoader (new AddressablesAudioLoader ());
```

Play an audio.
```csharp
AudioManager.Instance.PlayAudio ("audio_path");
```

Play an audio with optional parameters.
```csharp
AudioManager.Instance.PlayAudio ("audio_path", volume: 1F,  loop: true);
```

Use an AudioProfile to play an audio.
```csharp
AudioProfile myAudioProfile = new AudioProfile ()
{
    volume = 0.5F,
    mute = false
};

AudioManager.Instance.PlayAudio ("audio_path", volume: myAudioProfile.volume, mute: myAudioProfile.mute);
```