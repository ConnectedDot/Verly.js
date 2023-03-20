# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## v1.3.0 - 13-07-2019

### Added
- ***AngleStick Class*** - AngleStick is a angle join which will prevent points from bending at certain degrees, helpfull for making ragdolls
- Entity.js - **addAngleStick**
- Utils.js - **radians, degrees**
- Vector.js - **angle, angle2, rotateBy**
- Verly.js - **setDPI()** function which will improve the rendering in mobile devices
- **Added Basic Unit Testing**

## v1.2.1 - 11-07-2019

### Added

- better landing page
- improved examples

### Fixed

- bug in clamp function

## v1.2.0 - 08-07-2019

### Added

- Hidden Sticks with hidden parameter to Stick class
- Setters API for easy use of Point and Stick constructors
- Method chaining for Point and Stick
- with setters api we can create customized Entity easily. `entity.addPoint(0, 0).pin().setRadius()`

### Fixed

- clamp function wrong parameter bug
- fixed development webpack environment

## v1.1.4 05-07-2019

### Fixed

- independent internal rendering engine
- multiple instance of verly.js was causing global var collisions (WIDTH, HEIGHT, CTX)

### Changed

- Entity.js Class now expects two arguments (iteration, verlyInstance) because previously we used global variables to keep track of WIDTH, HEIGHT and ctx which was casing some problems
- When extending Entity class we have to do super(iteration, verlyInstance)
- Point.js Class's render, constrain, update methods now expects verlyInstance and ctx variables to be passed.
