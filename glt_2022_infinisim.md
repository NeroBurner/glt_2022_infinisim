---
marp: true
theme: gaia
---

# InfiniSim

- ommiting restructures restructures of the InfiniSim project, it's confusing enough on its own

---

## The beginnings

- I've got a PineTime, and I'm loving it!
- I want to hack on the PineTime, but I'm afraid I'm destroying it
- Let's write a Simulator to check my changes before killing my beloved watch

And so the journey began

---

## LVGL

https://github.com/lvgl/lvgl

> **About**
> Powerful and easy-to-use embedded GUI library with many widgets, advanced visual effects (opacity, antialiasing, animations) and low memory requirements (16K RAM, 64K Flash).

---

## lv_sim

Need LVGL simulator ... found one: [lvgl/lv_sim_eclipse_sdl ](https://github.com/lvgl/lv_sim_eclipse_sdl)

> **About**
> PC simulator project for LVGL embedded GUI Library. Recommended on Linux and Mac.

---

## First Screen

- Something easy
- little dependencies
- `Paddle.h`!

```cpp
Paddle(DisplayApp* app, Pinetime::Components::LittleVgl& lvgl);
```

```
src/displayapp/DisplayApp.h    -> sim/displayapp/DisplayApp.h
src/displayapp/DisplayApp.cpp  -> sim/displayapp/DisplayApp.cpp
src/displayapp/LittleVGL.h     -> sim/displayapp/LittleVGL.h
src/displayapp/LittleVGL.cpp   -> sim/displayapp/LittleVGL.cpp
```


---

## Emscripten WebAssembly

2022-02-24: https://github.com/InfiniTimeOrg/InfiniSim/pull/6
