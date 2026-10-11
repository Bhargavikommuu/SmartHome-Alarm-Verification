# SmartHome-Alarm-Controller — Verification Using UVM

.Project Overview
The Smart Home Alarm Controller is a hardware security system designed to monitor multiple sensor zones, process keypad PIN authentication, manage alarm conditions, and provide software access through an AHB interface.
This project focuses on functional verification of the Smart Home Alarm Controller using **SystemVerilog and Universal Verification Methodology (UVM)**. The verification environment generates stimulus, observes DUT responses, checks expected behavior, and identifies functional bugs.

.Objectives

- Verify sensor detection and alarm activation.
- Verify keypad PIN authentication, invalid attempts, lockout, and recovery.
- Verify AHB register read and write operations.
- Verify alarm priority and status reporting.
- Identify design bugs through directed verification scenarios.
- Develop a reusable, modular UVM testbench.

.Tools and Technologies

- SystemVerilog
- UVM 1.2
- Synopsys VCS
- EDA Playground
- AHB-Lite protocol

. UVM Testbench Architecture

The verification environment contains the following components:

- Sequences: Generate stimulus for sensor, keypad, and AHB operations.
- Sequencers: Control the flow of sequence items to drivers.
- Drivers: Apply transactions to the DUT interfaces.
- Monitors: Observe DUT interface activity and publish transactions.
- Agents: Group the driver, monitor, and sequencer where applicable.
- Reference Model: Maintains expected behavior for comparison.
- Scoreboard and Checkers: Check observed behavior against expected results.
- Environment: Integrates the verification components.
- Tests: Configure and execute individual verification scenarios.
- Testbench Top: Connects the DUT, interfaces, and UVM environment.

.Verification Scenarios

.AHB Verification

- Register access and default-value checks
- Register read/write and readback checks
- Entry and exit delay configuration
- VERSION register readback
- Zone configuration and alarm-status access
- AHB error and protocol scenarios, where implemented

.Keypad Verification

- Valid PIN acceptance
- Invalid PIN rejection
- Multiple invalid PIN attempts
- Keypad lockout verification
- Reset and recovery behavior

.Sensor and Alarm Verification

- Sensor activation and deactivation
- Sensor qualification and debounce behavior
- Alarm activation and latching
- Multiple-zone scenarios
- Alarm-priority verification

.Bug Detection

The verification environment is intended to identify functional issues such as:

- Incorrect entry and exit delay register behavior
- Incorrect VERSION register readback
- Keypad failure-count and lockout behavior
- Sensor debounce behavior
- Alarm-priority comparison issues

Actual bug status and simulation results should be documented using the corresponding test logs and observed DUT behavior.

.Contributions

My primary contribution to this team project focused on:

- Developing AHB verification sequences and tests
- Verifying register read/write operations
- Developing keypad verification scenarios
- Checking valid and invalid PIN responses
- Verifying lockout and recovery behavior
- Analyzing simulation logs and investigating functional mismatches

Sensor verification was also part of the team's overall verification effort.

.Run the Project

The project is available on EDA Playground:

[Open Smart Home Alarm Controller — EDA Playground](https://www.edaplayground.com/x/vsjT)

Open the playground, select the appropriate simulator and UVM settings, and run the required test.
 Learning Outcomes

- Practical experience with SystemVerilog and UVM
- Understanding of UVM agents, sequences, drivers, and monitors
- AHB register-level verification
- Functional checking using reference models and scoreboards
- Debugging and reporting RTL functional issues

 Project Information

Project: Smart Home Alarm Controller — Verification using UVM

Languages: SystemVerilog

Methodology: UVM 1.2

Simulator: Synopsys VCS

**Platform:** EDA Playground
