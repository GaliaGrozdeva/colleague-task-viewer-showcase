# Colleague Task Viewer Showcase

This repository presents the concept and workflow of a role-based task and client-information viewer for accounting-office employees.

> This is a public showcase repository.  
> It does not contain production code, client data, databases, credentials or internal business logic.

## Purpose

Accounting offices often rely on informal communication channels such as phone calls, Viber messages, scattered notes and verbal reminders to coordinate work between team members.

The Colleague Task Viewer is designed to replace that fragmented communication with a structured task exchange workflow inside the accounting office.

Each employee sees only the clients, deadlines and tasks assigned to them.

## Core idea

The main Accounting Desktop Assistant remains the central control system.

The Colleague Task Viewer is a lightweight local application for employees. It receives structured task data from the main system and allows the employee to review assigned work, return statuses, ask questions and provide updates.

The exchange is designed to be controlled, traceable and role-based.

## Key workflow areas

### Role-based client visibility

Each employee sees only the clients for which they are responsible.

Client data is read-only in the colleague application. Employees do not create or modify the main client registry.

### Automatic task import

Tasks created in the main system are exported to the colleague application.

After import, the colleague receives a mandatory pop-up notification for new tasks. The notification must be acknowledged, helping reduce the risk of missed assignments.

### Status exchange

The colleague can return task statuses such as:

- in progress;
- problem;
- ready for review.

The colleague can also add a question or note.

These updates are sent back to the main system, where the manager can review and respond.

### Structured communication loop

A manager’s response becomes a new update for the colleague.

This replaces scattered Viber messages, phone calls and informal reminders with a structured task history connected to the client and task.

### Local notes and operational support

The colleague application can maintain local notes, local paths and operational shortcuts without modifying the main system.

### Excel export

Operational boards can be exported to Excel for review, printing or internal control.

## Integration model

The system uses file-based JSON exchange between the main Accounting Desktop Assistant and the Colleague Task Viewer.

The colleague application does not directly access or modify the main database.

This keeps the main system as the source of truth while allowing employees to work in a simplified interface.

## Safety principles

- each employee sees only assigned clients;
- client master data is read-only;
- no direct write access to the main database;
- local tasks stay local;
- status updates are exchanged through controlled files;
- imports and exports use validation and backups;
- new tasks require acknowledgement.

## Business value

The system helps accounting-office teams:

- reduce missed tasks;
- improve accountability;
- separate responsibilities by client;
- reduce phone/Viber interruptions;
- keep task communication connected to the client;
- provide managers with structured status feedback;
- support distributed or multi-employee office workflows.

## Current status

Internal working system under active development and testing.

This public repository is a showcase only. Production code, real client data, local databases and internal exchange files are private.

## Development approach

The application is designed around daily accounting-office team coordination:

1. define who is responsible for which clients;
2. export only relevant tasks to each employee;
3. notify the employee about new work;
4. collect status updates and questions;
5. return updates to the main system;
6. preserve traceability and review.
