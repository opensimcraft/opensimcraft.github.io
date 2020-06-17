---
layout: page
title: Open Source Motion Simulation
---

The [OpenSimCraft community](https://github.com/opensimcraft) is focused on
open source hardware and software that is designed around the [SimCraft
motion simulation
methodology](https://www.simcraft.com/simcraft-method-of-motion-simulation-realistic-physicsbased-simulator-physicsmatter/).
The SimCraft methodology claims to mirror how Earth physics works, using up
to [six degrees of motion
freedom](https://www.simcraft.com/6-degrees-of-freedom-full-motion-roll-pitch-yaw-surge-sway-heave/),
in order to provide a more natural simulation experience.

## Hardware vs Software
The SimCraft motion simulation methodoloy is not proprietary technology,
however the SimCraft company's software/firmware and actuator hardware
implementation is.

The OpenSimCraft community is currently focused on open-sourcing existing
simulator "cockpit" designs (sim rigs) that will work with motion kits from
SimCraft. These motion kits include both hardware, firmware and PC software
used in conjunction with a piece of simulation software running on a computer
(for example, a racing simulator PC software). The OpenSimCraft community is
free to develop its own open source motion kits as well.

## License
OpenSimCraft hardware designs are licensed under the [CERN Open Hardware
License (OHL)](https://cern-ohl.web.cern.ch/), specifically [CERN-OHL-S
(strongly reciprocal)](https://ohwr.org/cern_ohl_s_v2.txt). CERN-OHL-S was
chosen because of its strong reciprocity requirement. The OpenSimCraft
community encourages innovation and encourages individuals to experiment. The
OpenSimCraft community and the CERN-OHL-S license do not prohibit commercial
entities from selling or supporting sim rigs / cockpits that utilize the
community's designs. However, any changes or alterations to the designs must
be made publicly available per the CERN-OHL-S terms and conditions.

## Repositories
Each repository in the OpenSimCraft organization should contain either all of
the source for a complete sim rig, or should only contain source for a set of
components that add another degree of motion freedom to an existing design.

Examples:

* `8020-1dof` is a repository that contains an entire cockpit design made of
  80/20 extruded t-slot aluminum that can implement 1 degree of motion freedom
* `8020-2dof` is the same, but is a complete design implementing 2 degrees of
  motion freedom
* `8020-3rd-dof` is a repository that describes how construct the necessary
  components to add or modify `8020-2dof` to add a third degree of motion
  freedom

TODO: define a repository naming standard

## Required Contents
Each repository must have:

* A CAD file in a format that can be opened by [FreeCAD](https://www.freecadweb.org/)

  TODO: specify additional requirements or design standards for CAD files

* A bill of materials (BOM) in a [LibreOffice
  Calc](https://www.libreoffice.org/) spreadsheet describing the list of
  components required

  TODO: define a standard which includes the 80/20 manufacturer codes

* A README.md file that describes the design and whether or not it is a
  complete cockpit or an additional component/system for an existing cockpit

  TODO: define a standard README layout for design repositories
