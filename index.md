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

## Part Naming / Numbers / SKUs
In general, a distinct part, whether it is something ordered directly from a
manufacturer, machined from scratch, or something in between, needs a
distinct part number within the community. By having a unique registry of
parts, the OpenSimCraft community will be able to re-use things across many
differet projects.

TODO: define a part numbering scheme
TODO: figure out a part registry

## Required Contents
Each repository must have:

* [FreeCAD] is the CAD tool that the community is
  using, along with the
  [Assembly4](https://github.com/Zolko-123/FreeCAD_Assembly4) add-on. See the
  CAD section for additional details on requirements.

* A bill of materials (BOM) in a [LibreOffice
  Calc](https://www.libreoffice.org/) spreadsheet describing the list of
  components required

  TODO: define a standard which includes the 80/20 manufacturer codes

* A README.md file that describes the design and whether or not it is a
  complete cockpit or an additional component/system for an existing cockpit

  TODO: define a standard README layout for design repositories

## FreeCAD Requirements
All designs should be created with [FreeCAD].
Since designs should be made up of unique parts, FreeCAD files should either
contain a single part, or only a logical assembly of several individual
parts. Ultimately, a cockpit design may be an assembly of assemblies, with
their constituent parts.

For example, if you have four 80/20 T-slot extrusions that make a square
assembly, each individual extrusion should be a part, and the square assembly
should only contain linked parts for each of the extrusions. There should not
be additional sketches, bodies, or other non-linked-parts in the assembly. If
you needed a fastener, or an additional extrusion, or any other random
widget, you would want a separate file that contains that part, and link it
in the parent assembly.

The [Assembly4](https://github.com/Zolko-123/FreeCAD_Assembly4) add-on is
used to help manage part linking and part relationships. While it is not an
official add-on, files will open and can be modified even without it.

FreeCAD and Assembly4 require unique names for linked parts in an assembly.
When adding multiple instances of the same part to an assembly, use a hyphen
followed by an English letter suffix, starting with `-A`, and increment for
each instance of the part. If you have more than 26 instances of the same
part, you would circle to the top of the alphabet and continue with two
letters. So, you would have `-Y`, `-Z`, and then `-AA` followed by `-AB`, and
so on and so forth.


[FreeCAD]: https://FreeCAD.Org