# OpenZT2 Project Roadmap

## 0. Foundational Decisions

### Engine Architecture
- [ ] **Decision**: Custom engine vs COTS (Unity/Unreal) vs FOSS (Godot/Bevy/raylib)
  - Trade-offs: Control vs development speed vs community familiarity
  - Consider: Godot (GDScript/C#, strong 3D, MIT), Bevy (Rust, ECS, modern), custom (full control, huge effort)
- [ ] **Decision**: Primary programming language (C++, Rust, C#, GDScript)
- [ ] **Decision**: Build system (CMake, Cargo, Meson, engine-native)
- [ ] **Decision**: Graphics API abstraction (Vulkan, OpenGL, wgpu, engine-native)
- [ ] **Decision**: Audio backend (OpenAL, miniaudio, FMOD, engine-native)

### Project Infrastructure
- [ ] Set up CI/CD pipeline (GitHub Actions)
- [ ] Configure linting/formatting standards
- [ ] Create contribution guidelines (CONTRIBUTING.md)
- [ ] Set up issue templates and PR templates
- [ ] Create development environment documentation
- [ ] Establish coding standards document
- [ ] Set up automated testing framework

### Legal & Community
- [ ] Document clean-room reverse engineering procedures
- [ ] Establish asset provenance tracking system
- [ ] Create Discord/Matrix community server
- [ ] Set up project website/documentation site

---

## 1. Reverse Engineering & Decompilation

### File Format Analysis
- [ ] Document .ztd package format (ZIP-based container)
- [ ] Document .bfm/.bfa model/animation formats
- [ ] Document .tga/.dds texture formats and conventions
- [ ] Document .xml configuration schemas (animals, objects, biomes)
- [ ] Document .lua script integration points
- [ ] Document .uca/.ucs animation controller formats
- [ ] Document save file format (.z2s)
- [ ] Document scenario/challenge file formats

### Engine Behavior Analysis
- [ ] Map original game's entity-component architecture
- [ ] Document AI behavior trees and pathfinding algorithms
- [ ] Reverse engineer guest/animal need systems
- [ ] Document terrain system (heightmaps, textures, biomes)
- [ ] Analyze rendering pipeline and shader behavior
- [ ] Document physics/collision systems
- [ ] Map UI framework and widget system
- [ ] Document sound system and 3D audio positioning

### Tools Development
- [ ] Create .ztd extractor/packer tool
- [ ] Create .bfm/.bfa model viewer/converter
- [ ] Create XML schema validator
- [ ] Build save file parser/editor
- [ ] Create asset dependency mapper

---

## 2. Engine Development

### Core Systems
- [ ] Implement application lifecycle management
- [ ] Create window management and input handling
- [ ] Implement resource/asset management system
- [ ] Create entity-component system (or chosen architecture)
- [ ] Implement scene graph / spatial partitioning
- [ ] Create event/messaging system
- [ ] Implement serialization framework

### Rendering
- [ ] Implement 3D model loading (target: .bfm compatibility)
- [ ] Implement skeletal animation system
- [ ] Create terrain rendering system
- [ ] Implement water rendering with reflections
- [ ] Create foliage/vegetation system
- [ ] Implement dynamic lighting and shadows
- [ ] Create particle system
- [ ] Implement LOD (Level of Detail) system
- [ ] Add post-processing pipeline
- [ ] Implement UI rendering system
- [ ] Support 4K and ultrawide resolutions

### Audio
- [ ] Implement 3D positional audio
- [ ] Create ambient soundscape system
- [ ] Implement music playback with crossfading
- [ ] Add animal vocalization system
- [ ] Create UI sound effects system

### Physics & Simulation
- [ ] Implement collision detection
- [ ] Create pathfinding system (NavMesh or grid-based)
- [ ] Implement terrain collision
- [ ] Add ragdoll physics (optional/stretch)

### Platform Support
- [ ] Windows build and packaging
- [ ] Linux build and packaging (AppImage, Flatpak)
- [ ] Steam Deck verification and optimization
- [ ] macOS build (stretch goal)
- [ ] Controller input support

---

## 3. Game Systems Implementation

### Zoo Management
- [ ] Implement zoo boundaries and expansion system
- [ ] Create financial/economy system
- [ ] Implement guest simulation (needs, pathfinding, satisfaction)
- [ ] Create staff simulation (zookeepers, maintenance, tours)
- [ ] Implement research/unlock progression system
- [ ] Create award/achievement system

### Animal Systems
- [ ] Implement animal needs (hunger, thirst, rest, enrichment, space)
- [ ] Create animal behavior state machines
- [ ] Implement breeding and genetics system
- [ ] Create aging and lifespan system
- [ ] Implement animal interactions (social, territorial)
- [ ] Create adoption/release mechanics
- [ ] Implement animal escapes and capture

### Construction & Placement
- [ ] Implement fencing system with multiple types
- [ ] Create terrain modification tools
- [ ] Implement path/walkway placement
- [ ] Create building placement system
- [ ] Implement foliage/decoration placement
- [ ] Create exhibit design validation

### Biomes & Environments
- [ ] Implement biome system (temperature, humidity)
- [ ] Create weather system
- [ ] Implement day/night cycle
- [ ] Create seasonal variation (optional)

### Campaigns & Scenarios
- [ ] Implement scenario objective system
- [ ] Create tutorial framework
- [ ] Support custom scenario creation
- [ ] Implement challenge/timed modes

### UI/UX
- [ ] Create main menu system
- [ ] Implement in-game HUD
- [ ] Create animal/object info panels
- [ ] Implement build menus and toolbars
- [ ] Create photo mode
- [ ] Implement guest/animal first-person view
- [ ] Create settings/options menus

---

## 4. Media Collation & Asset Pipeline

### Original Asset Extraction
- [ ] Extract and catalog all base game models
- [ ] Extract and catalog expansion pack assets (Marine Mania, African Adventure, etc.)
- [ ] Extract all textures and create format conversion pipeline
- [ ] Extract all audio files and catalog
- [ ] Extract all XML definitions and schemas
- [ ] Extract all Lua scripts from official content

### Asset Organization
- [ ] Create asset database/registry
- [ ] Implement tagging system (biome, era, expansion, type)
- [ ] Document asset dependencies and relationships
- [ ] Create asset preview generator
- [ ] Build searchable asset browser

### Format Conversion
- [ ] Create .bfm to modern format converter (glTF, FBX)
- [ ] Create texture upscaling pipeline (optional AI enhancement)
- [ ] Create audio format standardization pipeline
- [ ] Build batch conversion tools

---

## 5. New Media Generation

### Visual Assets
- [ ] Create/commission new UI artwork
- [ ] Design new icons and interface elements
- [ ] Create loading screens and promotional art
- [ ] Design new animal models (stretch goal)
- [ ] Create terrain textures and materials

### Audio Assets
- [ ] Create new music tracks (or license compatible music)
- [ ] Record new ambient soundscapes
- [ ] Create UI sound effects
- [ ] Generate animal vocalizations (or source from libraries)

### Marketing & Documentation
- [ ] Complete trailer video production
- [ ] Create screenshots and promotional materials
- [ ] Write user documentation/manual
- [ ] Create video tutorials
- [ ] Design project branding materials

---

## 6. Mod Support Framework

### Legacy Mod Compatibility
- [ ] Implement .ztd mod loading
- [ ] Create compatibility layer for original mod formats
- [ ] Test with popular community mods
- [ ] Document compatibility status per mod
- [ ] Create mod troubleshooting guide

### Lua Scripting
- [ ] Integrate Lua interpreter
- [ ] Design and document modding API
- [ ] Create API reference documentation
- [ ] Implement sandboxing for mod security
- [ ] Create example mods and templates

### Mod Development Tools
- [ ] Create mod SDK/development kit
- [ ] Build mod packaging tool
- [ ] Create mod validator/linter
- [ ] Implement hot-reload for mod development
- [ ] Create modding documentation and tutorials

### Mod Distribution
- [ ] Design mod manifest format
- [ ] Implement mod versioning system
- [ ] Create mod dependency resolution
- [ ] Support mod.io or similar platform integration

---

## 7. Mod Manager Integration

### Built-in Manager
- [ ] Create mod browser/discovery UI
- [ ] Implement mod enable/disable functionality
- [ ] Create load order management
- [ ] Implement mod conflict detection
- [ ] Create mod update checking system
- [ ] Add one-click mod installation

### External Manager Support
- [ ] Document integration points for external managers
- [ ] Support Nexus Mods integration (if applicable)
- [ ] Support Steam Workshop (if on Steam)
- [ ] Create mod list export/import

---

## 8. Quality & Polish

### Testing
- [ ] Create automated unit test suite
- [ ] Implement integration tests
- [ ] Create performance benchmarks
- [ ] Establish compatibility test matrix
- [ ] Implement crash reporting system

### Performance
- [ ] Profile and optimize rendering
- [ ] Optimize simulation for large zoos
- [ ] Implement asset streaming
- [ ] Add graphics quality presets
- [ ] Optimize for Steam Deck battery life

### Accessibility
- [ ] Implement colorblind modes
- [ ] Add UI scaling options
- [ ] Create subtitle/caption system
- [ ] Support screen readers (where feasible)
- [ ] Add input remapping

### Localization
- [ ] Design localization system
- [ ] Extract and organize translatable strings
- [ ] Support community translations
- [ ] Implement RTL language support

---

## 9. Distribution & Release

### Packaging
- [ ] Create installer for Windows
- [ ] Package for Linux (AppImage, Flatpak, .deb)
- [ ] Prepare Steam release (if pursuing)
- [ ] Create itch.io release
- [ ] Prepare GOG release (if pursuing)

### Documentation
- [ ] Write installation guide
- [ ] Create troubleshooting FAQ
- [ ] Document system requirements
- [ ] Write modding guide
- [ ] Create developer documentation

### Community
- [ ] Set up bug tracker workflow
- [ ] Create feature request process
- [ ] Establish release cadence
- [ ] Plan alpha/beta testing program

---

## Milestone Targets

### M0: Foundation
- Engine decision made
- Build system working
- Window opens with basic rendering

### M1: Asset Loading
- Can load and display original .ztd assets
- Basic 3D rendering working
- Model viewer functional

### M2: Terrain & Navigation
- Terrain rendering
- Camera controls
- Basic pathfinding

### M3: Entity Simulation
- Animals can be placed
- Basic needs simulation
- Guests can navigate

### M4: Playable Alpha
- Core gameplay loop functional
- Basic UI implemented
- Save/load working

### M5: Mod Support Alpha
- Legacy mods can load
- Lua scripting functional
- Mod manager operational

### M6: Beta Release
- Feature complete
- Polish and optimization
- Community testing

### M7: Release
- Stable 1.0 release
- Full documentation
- Distribution channels active
