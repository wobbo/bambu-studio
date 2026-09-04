# Bambu Studio for Debian 13 GNOME

This repository contains my Debian 13 AMD64 build of **Bambu Studio 2.8.2.61**, with a small set of Linux/GNOME changes that I use on my own Debian GNOME system.

<img width="320" height="180" alt="Bambu_Studio_2026-09-04_17-13-11" src="https://github.com/user-attachments/assets/83151333-c8f9-4dae-bdc9-72f3c6b75946" /> <img width="320" height="180" alt="Bambu_Studio_2026-09-04_17-13-46" src="https://github.com/user-attachments/assets/84bec2af-73bc-4c9c-bf71-e0754d17de29" />

The main goal is to make Bambu Studio feel more like a normal native GNOME application under Wayland. I fixed several window-management issues, including moving and resizing the window, maximize/restore behaviour, the startup splash screen and some of the behaviour while Bambu Studio is starting.

I also changed the Linux startup so that OpenGL initialization is delayed until the 3D view is actually needed. Together, these changes make startup and general window behaviour noticeably better on my Debian 13 GNOME system.

## Why a native Debian package?

There is already a Flatpak version of Bambu Studio, but for my own system I prefer a normal Debian `.deb` package.

The goal of this build is to use the Debian system directly as much as practical, including its GTK/GNOME environment, graphics stack, drivers and other system components, instead of running Bambu Studio through the additional Flatpak runtime and sandbox layer.

For me this gives better integration with Debian and GNOME, and makes the application behave more like software installed directly from the operating system.

This package includes:

- Debian 13 AMD64 integration
- GNOME Wayland window fixes
- Native window moving and edge resizing
- Improved maximize and restore behaviour
- Improved startup splash behaviour
- Deferred OpenGL initialization during startup
- GNOME Software / AppStream metadata
- All Bambu Studio language resources

The optional proprietary **Bambu Network Plugin is not included**.

This is an independent Debian build based on the official open-source Bambu Studio project and is not an official Bambu Lab Debian package.

---




![image](https://user-images.githubusercontent.com/106916061/179006347-497d24c0-9bd6-45b7-8c49-d5cc8ecfe5d7.png)
# BambuStudio
Bambu Studio is a cutting-edge, feature-rich slicing software.  
It contains project-based workflows, systematically optimized slicing algorithms, and an easy-to-use graphic interface, bringing users an incredibly smooth printing experience.

Prebuilt Windows, macOS 64-bit and Linux releases are available through the [github releases page](https://github.com/bambulab/BambuStudio/releases/).

Bambu Studio is based on [PrusaSlicer](https://github.com/prusa3d/PrusaSlicer) by Prusa Research, which is from [Slic3r](https://github.com/Slic3r/Slic3r) by Alessandro Ranellucci and the RepRap community.

See the [wiki](https://github.com/bambulab/BambuStudio/wiki) and the [documentation directory](https://github.com/bambulab/BambuStudio/tree/master/doc) for more information.

# What are Bambu Studio's main features?
Key features are:
- Basic slicing features & GCode viewer
- Multiple plates management
- Remote control & monitoring
- Auto-arrange objects
- Auto-orient objects
- Hybrid/Tree/Normal support types, Customized support
- multi-material printing and rich painting tools
- multi-platform (Win/Mac/Linux) support
- Global/Object/Part level slicing parameters

Other major features are:
- Advanced cooling logic controlling fan speed and dynamic print speed
- Auto brim according to mechanical analysis
- Support arc path(G2/G3)
- Support STEP format
- Assembly & explosion view
- Flushing transition-filament into infill/object during filament change

# How to compile
Following platforms are currently supported to compile:
- Windows 64-bit, [Compile Guide](https://github.com/bambulab/BambuStudio/wiki/Windows-Compile-Guide)
- Mac 64-bit, [Compile Guide](https://github.com/bambulab/BambuStudio/wiki/Mac-Compile-Guide)
- Linux, [Compile Guide](https://github.com/bambulab/BambuStudio/wiki/Linux-Compile-Guide)
  - currently we only provide linux appimages on [github releases](https://github.com/bambulab/BambuStudio/releases) for Ubuntu/Fedora, and a [flathub version](https://flathub.org/apps/com.bambulab.BambuStudio) can be used for all the linux platforms

# Report issue
You can add an issue to the [github tracker](https://github.com/bambulab/BambuStudio/issues) if **it isn't already present.**

# License
Bambu Studio is licensed under the GNU Affero General Public License, version 3. Bambu Studio is based on PrusaSlicer by PrusaResearch.

PrusaSlicer is licensed under the GNU Affero General Public License, version 3. PrusaSlicer is owned by Prusa Research. PrusaSlicer is originally based on Slic3r by Alessandro Ranellucci.

Slic3r is licensed under the GNU Affero General Public License, version 3. Slic3r was created by Alessandro Ranellucci with the help of many other contributors.

The GNU Affero General Public License, version 3 ensures that if you use any part of this software in any way (even behind a web server), your software must be released under the same license.

The bambu networking plugin is based on non-free libraries. It is optional to the Bambu Studio and provides extended networking functionalities for users.
By default, after installing Bambu Studio without the networking plugin, you can initiate printing through the SD card after slicing is completed.

