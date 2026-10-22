# SCADALattice

A modular SCADA platform for monitoring and controlling simulated physical processes.

Course: Information Security of Infrastructure Systems, Faculty of Technical Sciences, University of Novi Sad.

## Scope

- Create SCADA projects with tags, HMI screens, alarms, and access permissions.
- Build HMI screens and bind visual elements to process signals.
- Connect independent process models through a Simulator SDK.
- Record telemetry, trends, commands, alarms, and security events.

## Architecture

The specification requires Clean Architecture and SOLID principles. Process models integrate through a stable SDK; adding a simulator must not require changes to the SCADA core, tag service, or HMI logic.

## Specification

[Technical specification (PDF, Serbian)](docs/SCADALattice_Tehnicka_specifikacija.pdf)

The PDF defines the requirements, acceptance tests, and reference scenario. Application code has not been added yet.
