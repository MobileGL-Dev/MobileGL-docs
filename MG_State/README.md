*(Work-in-Progress | In Development)*  

**A Generic OpenGL State Machine**  

---

## Overview  
**MobileGL-State** (*MG_State*) is a modular OpenGL state machine emulator designed to replicate the behavior of OpenGL contexts. It provides accurate tracking and validation of OpenGL states (e.g., textures, buffers, shaders).  

**⚠️ Note**: This component is **in development**.

---

## Features  

### **State Tracking**  
- Emulates OpenGL state variables.
- Toggles and validates state transitions.  

### **Error Emulation**  
- Mimics OpenGL error codes.
- Validates API calls against the current state.

### **Backend-Agnostic**  
- No dependency on specific backends.

### **Integration-Ready**  
- Lightweight API for embedding into custom engines or tools.  
- Already compatible with **MobileGL** for backend command translation.  

---

## Component Status

| Components                      | Progress                          | Note                                                                                      |
|---------------------------------|-----------------------------------|-------------------------------------------------------------------------------------------|
| GL Error                        | ✅ Implemented                    | BufferState, VertexArrayState and ProgramState need more error checks                     |
| GL Global Rendering State       | ℹ️ Simple implementation          |                                                                                           |
| Texture                         | ℹ️ Simple implementation          |                                                                                           |
| Buffer                          | ℹ️ Simple implementation          | VBO, EBO & Copy Write Buffers implemented; others coming soon                             |
| Vertex Array                    | ℹ️ Simple implementation          |                                                                                           |
| Shader & Program                | ☑️ Nearly complete implementation |                                                                                           |
| Framebuffer                     | ℹ️ Simple implementation          |                                                                                           |
| Others...                       | ⏳ Coming Soon                    |                                                                                           |
