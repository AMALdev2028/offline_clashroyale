# OfflineClanRoyale

An offline mobile game combining Clash Royale-style arena battles with Clash of Clans base-building mechanics, featuring Bluetooth P2P multiplayer without internet requirements.

## Features

- **Arena Battles**: Real-time card-based combat in Clash Royale-style arenas
- **Base Building**: Collect and upgrade buildings, troops, and defenses
- **Offline Multiplayer**: Bluetooth P2P connectivity for local group matches
- **Deterministic Sync**: Lockstep networking for consistent multiplayer experience
- **Cross-Platform**: Android and iOS support via Unity
- **Free to Play**: No monetization, completely free game

## Technical Architecture

### Core Systems
- **BluetoothManager**: Handles device discovery, connection, and data transmission
- **GameStateManager**: Manages deterministic game state and synchronization
- **LockstepNetwork**: Implements deterministic lockstep networking
- **CardSystem**: Deck building and card management
- **BaseSystem**: Building placement and resource management

### Multiplayer Features
- **In-App Hosting**: One device acts as match server
- **Host Migration**: Automatic host transfer if primary host disconnects
- **Lobby System**: Local matchmaking and player management
- **Deterministic Sync**: Input-based synchronization with rollback support

## Setup Instructions

### Prerequisites
- Unity 2022.3 LTS or newer
- Android SDK (for Android builds)
- Xcode (for iOS builds, macOS only)

### Installation
1. Clone this repository
2. Open the project in Unity
3. Install required packages via Package Manager:
   - Input System
   - TextMeshPro
   - Universal Render Pipeline
4. Configure platform-specific settings in Project Settings

### Building
- **Android**: File > Build Settings > Android > Build
- **iOS**: File > Build Settings > iOS > Build (requires macOS)

## Project Structure

```
Assets/
├── Scripts/
│   ├── Core/           # Core game systems
│   ├── Networking/     # Bluetooth and multiplayer
│   ├── UI/            # User interface components
│   ├── Cards/         # Card system and deck management
│   └── Base/          # Base building mechanics
├── Prefabs/           # Reusable game objects
├── Scenes/            # Game scenes
├── Art/               # Original artwork
└── Audio/             # Game audio assets
```

## Development Guidelines

### Legal Considerations
- Use only original artwork and audio
- Avoid copying Supercell's exact mechanics, names, or visual style
- Create unique IP while maintaining similar game feel

### Performance Optimization
- Optimize for mobile battery life
- Minimize Bluetooth data transmission
- Use efficient rendering for mobile GPUs

### Testing
- Test on multiple Android devices
- Test on multiple iOS devices
- Verify Bluetooth connectivity across platforms
- Test host migration scenarios

## License

This project is free to use and modify. Please ensure all assets are original or properly licensed.
