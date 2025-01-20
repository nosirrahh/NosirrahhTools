# AddressablesTools

...

## Installation
1. Open your Unity project.
2. Add the package via the Package Manager:
   ```
   https://github.com/nosirrahh/NosirrahhTools.git?path=Assets/NosirrahhTools/AddressablesTools/
   ```

## How to Use

Check if an asset exists.
```csharp
AddressablesHelper.Instance.Exists<AudioClip> (
    "asset_path",
    (status) =>
    {
        Debug.Log (status);
    }
);
```

Load an asset.
```csharp
AddressablesHelper.Instance.Load (
    "asset_path",
    (AsyncOperationStatus status, AudioClip loadedAsset) =>
    {
        Debug.Log ($"Load completed with status: {status}.");
        Debug.Log ($"If the status is AsyncOperationStatus.Succeeded your asset will be available in 'loadedAsset' field.");
    }
);
```