---
layout: page
title: Open Source Motion Simulation
---

The [OpenSimCraft community](https://github.com/opensimcraft) is focused on
open source hardware and software that is designed around the SimCraft motion
simulation methodology. The SimCraft methodology claims to mirror how Earth
physics works, using up to six degrees of motion freedom, in order to provide
a more natural simulation experience. The SimCraft motion simulation
methodology is described more in detail on the [SimCraft company website](https://www.simcraft.com/simcraft-method-of-motion-simulation-realistic-physicsbased-simulator-physicsmatter/).

## Hardware vs Software
The SimCraft motion simulation methodoloy is not proprietary technology,
however the SimCraft company's software implementation is.

The OpenSimCraft community is currently focused on open-sourcing existing
simulator "cockpit" designs that will work with motion kits from SimCraft.
These motion kits include both hardware and software used in conjunction with
a piece of simulation software running on a computer (for example, a racing
simulator PC software). The OpenSimCraft community is free to develop
its own open source motion kits as well.

## License
OpenSimCraft hardware designs are licensed under the [CERN Open Hardware License (OHL)](https://ohwr.org).

## Repositories
Each repository in the OpenSimCraft organization should contain either all of the source for a complete cockpit, or should only contain source for a set of components that add another degree of motion freedom to an existing design.

Examples:

* `8020-1dof` is a repository that contains an entire cockpit design made of 80/20 extruded t-slot aluminum that can implement 1 degree of motion freedom
* `8020-2dof` is the same, but is a complete design implementing 2 degrees of motion freedom
* `8020-3rd-dof` is a repository that describes how construct the necessary components to add or modify `8020-2dof` to add a third degree of motion freedom

No naming convention has been identified at this time.

## Required Contents
Each repository must have:

* A CAD file in a format that can be opened by [FreeCAD](https://www.freecadweb.org/)
* A bill of materials (BOM) in a [LibreOffice Calc](https://www.libreoffice.org/) spreadsheet describing the list of components required
* A README.md file that describes the design and whether or not it is a complete cockpit or an additional component/system for an existing cockpit
