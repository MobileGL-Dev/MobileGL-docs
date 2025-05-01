# MobileGL  
*(Work-in-Progress | Early Development Phase)*  

**A Cross-Platform OpenGL Implementation for Mobile Devices**  
*Powered by Modern Graphics Backends (OpenGL ES, Vulkan, etc.)*  

---

## Overview  
**MobileGL** is an **OpenGL-compatible implementation** designed for mobile platforms, enabling OpenGL applications to run on modern graphics APIs like **OpenGL ES, Vulkan, etc.** through a modular system. Unlike traditional OpenGL, MobileGL decouples the frontend (GL API/state) from the rendering backend via a **MobileGL-RHI**, allowing developers to target multiple platforms with minimal changes.  

**⚠️ Note**: This project is in **early development**. Core components and APIs are incomplete.  

---

## Architecture  
MobileGL is structured into these key layers:  

### 1. **GL Frontend**  
*An OpenGL API Emulator*  
- **Goal**: Provide a **strict OpenGL-compatible interface** for applications, including state machine operations.  
- **Features**:  
  - Accepts standard OpenGL commands.
  - Tracks and reports OpenGL state (context, bound resources, etc.).
  - Translates GL commands into backend-agnostic RHI operations.

### 2. **MobileGL-RHI**  
*A Cross-API Command Abstraction | Platform-Specific Implementations*
- **Goal**: Serve as an intermediate layer to serialize, optimize, and dispatch rendering commands to any backend.  
- **Features**:  
  - Unified APIs of rendering commands (draw calls, textures, shaders).
  - Acts as a bridge between high-level rendering logic and specific backend commands.
  - No reliance on any particular GL state; can integrate effortlessly with any engine or program.

### 3. **MobileGL-State**  
*A Generic OpenGL State Machine*  
- **Goal**: Convert Accurately track and emulate the OpenGL state machine.  
- **Features**:  
  - Context state management (e.g., textures, buffers, shaders).
  - State validation to mimic OpenGL error semantics.
  - Backend-agnostic design for integration with any programs.

---

## Project Status

| Component                           | Progress             |
|-------------------------------------|----------------------|
| **OpenGL State Manager (MG_State)** | 🚧 Early Development | 
| **Abstraction Layer (MG_RHI)**      | 🔜 Coming Soon       | 
| **MG_RHI: OpenGL ES Backend**       | ⏳ Pending RHI        | 
| **MG_RHI: Vulkan**                  | 🚧 Planned           | 
| **MG_RHI: Metal**                   | ❓ Future             |