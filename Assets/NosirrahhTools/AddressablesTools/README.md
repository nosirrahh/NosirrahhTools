# AddressablesTools

...

## Dependencies

Before installing this package, make sure the following dependencies are pre-installed in your Unity project:

- [Addressables](https://docs.unity3d.com/Packages/com.unity.addressables@2.3/manual/index.html) (```com.unity.addressables```) - Version ```1.0.0``` or higher
- [CoreTools](../CoreTools/README.md) (```com.nosirrahh.coretools```) - Version ```1.0.0``` or higher

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