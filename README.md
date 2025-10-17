# AtmosphericEnergizersChange

A BepInEx mod for MycoPunk that changes Atmospheric Energizers ammo regeneration behavior.

## Description

This mod modifies the Atmospheric Energizers weapon so that instead of refilling the magazine clips, they now refill the ammunition reserves. This provides a more balanced ammo regeneration mechanic without ovely filling the active magazine.

The mod uses Harmony to patch the `SwarmGun.OnActiveUpdate` method with a prefix that handles ammo regeneration directly into stored ammo reserves, bypassing the original magazine refill logic.

## Getting Started

### Dependencies

* MycoPunk (base game)
* [BepInEx](https://github.com/BepInEx/BepInEx) - Version 5.4.2403 or compatible
* .NET Framework 4.8

### Building/Compiling

1. Clone this repository
2. Open the solution file in Visual Studio, Rider, or your preferred C# IDE
3. Build the project in Release mode

Alternatively, use dotnet CLI:
```bash
dotnet build --configuration Release
```

### Installing

**Option 1: Via Thunderstore (Recommended)**
1. Download and install using the Thunderstore Mod Manager
2. Search for "AtmosphericEnergizersChange" under MycoPunk community
3. Install and enable the mod

**Option 2: Manual Installation**
1. Ensure BepInEx is installed for MycoPunk
2. Copy `AtmosphericEnergizersChange.dll` from the build folder
3. Place it in `<MycoPunk Game Directory>/BepInEx/plugins/`
4. Launch the game

### Executing program

The mod runs automatically when you launch the game. Once loaded, Atmospheric Energizers will refill ammunition reserves instead of magazine clips when the weapon's auto-regeneration conditions are met (weapon hasn't fired in 1 second, has bullets in the air, and regeneration interval has elapsed).

## Help

* **Mod not working?** Ensure you've installed the correct version of BepInEx and that the DLL is placed in the right plugins folder
* **Incompatibility issues?** This mod uses Harmony patches. If you have other mods that modify SwarmGun ammo behavior, conflicts may occur
* **Logs:** Check the BepInEx console for any error messages on startup

## Authors

* Sparroh
* funlennysub (original mod template)
* [@DomPizzie](https://twitter.com/dompizzie) (README template)

## License

* This project is licensed under the MIT License - see the LICENSE.md file for details
