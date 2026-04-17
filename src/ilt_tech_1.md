# ILT tech 1

## SDLC

- Problem Definition
- Design & Architecture
- Implementation
- Testing & Validation
- Deployment & Monitoring

### SDLC Phase 1: Planning

- project foundation
  the bedrock of any successful software development initiative.
- goal alignment
  focuses on gathering core project goals, objectives, and specific requirements.
- resource strategy

### SDLC Phase 2: Feasibility Analysis

- project viability
- technical & cost
- risk analysis

### SDLC Phase 3: System Design

- Blueprint Creation

  transform project requirements into a clear technical blueprint for a development.

- Specifications

  focuses on high-level architecture and detailed design specifications.

- Ui Design

  includes user interface (UI) design to ensure the application is user-friendly.

### SDLC Phase 4: Implementation

- Development Phase

  also known as the development phase where the actual coding takes place.

- System Transformation

  transforms the system design and blueprints into a functional application.

- Best Practices

  requires strict adherence to standards to ensure code is efficient, secure and
  maintainable.

### SDLC Phase 5: Testing

- Performance & Usability

  crucial for generating performance and usability feedback through real-world scenarios.

- Quality Assurance

  reveals defects, bugs and quirks before the software reaches users.

- Testing Methods

  utilizes various methods like automated, unit, integration and system testing.

### SDLC Phase 6: Deployment

- Software Release

  releasing the tested software to end users as the final stage of the
  development cycle.

- Beta Testing

  may include a beta-testing phase or pilot launch to a select group of users
  for feedback.

- Deployment Strategy

  involves choosing the right strategy, such as cloud-based or on-premise infrastructure.

### SDLC Phase 7: Maintenance

- Post Deployment

  the ongoing phase after the software is deployed to end users.

- Support & Updates

  focuses on providing continous support to address issues and apply updates.

- Evolving Relevance

  the stage where new features can finally be added to keep the software relevant.

## Problem Definition & Scope Management

- MVP Mindset

- User Segmentation

- Explicit Exclusions

## Why Learning Plans Fail

Three recurring patterns and how we'll fix them together.

- Goals Are Too Big

  ambitious targets without breakdown > overwhelm > never start.

- Generic Schedule

  doesn't match personal rhythms > falls apart in the first week.

- Progress Isn'T Measured

  no feedback loop > motivation drops > stops halfway through.

## What You'll Build

- Goal Management

  break big goals into 25-90 minutes tasks that are actionable.

- Weekly Calendar

  your schedule is built around your availability, not a generic template.

- Ai Coach

  study suggestions + rationale: not autopilot, you still make the decisions.

- Progress Tracker

  weekly snapshots, performance trends, and nudges when you start to go off track.

## AI assists. You decide

set goal > ai suggests > review > accept or reject > save task

## Design Principle

every step involves human decision-making. ai never acts on its own.

- Human-In-The-Loop

  all ai actions require explicit user confirmation before being saved.

- Explainability

  every suggestion includes a rationale that can be read and evaluated.

- Privacy-First

  only the user_id alias is sent to the LLM, not the name or email.

## Scope: MVP Vs Nice-To-Have Vs Out-Of-Scope

| MVP                                            | Nice-to-Have                    | Out-of-Scope                      |
| ---------------------------------------------- | ------------------------------- | --------------------------------- |
| auth, profile, goal settings                   | adaptive learning               | native mobile app                 |
| task crud                                      | study streaks \* micro coaching | cross timezon multi calendar sync |
| ai task breakdown + rationale + accept/reject  | content recommendations         | deep LMS integration              |
| calendar view + weekly plan                    | performance nudges              | -                                 |
| progress tracker + weekly snapshot             | -                               | -                                 |
| observabilty: logging, metrics, error handling | -                               | -                                 |
| minimal test coverage + ai audit log           | -                               | -                                 |

## 5 Layer Architecture

| layer             | tech                                        | detail                                 |
| ----------------- | ------------------------------------------- | -------------------------------------- |
| frontend (client) | react (vite)                                | components, routing, state             |
| backend (api)     | node.js (express/hapi)                      | auth, crud, ai orchestration           |
| db                | postgresql + redis(opt)                     | -                                      |
| ai                | gemini API                                  | task breakdown + rationale generations |
| observabilty      | pino logs, prom-client metrics, audit table | -                                      |

## Layered Architecture

understanding the data flow

### Separation Of Concerns

software is divided into distinct layers, each with specific responsibilities
(UI, Business Logic, Data storage).

### Predictable Data Flow

data travels sequentially between layers (client <> server <> database/external
apis)

How Data Flows

- Create Goal

  define goal, availability, request ai

- Assemble Context

  combine goal, availability, tasks

- LLM & Validate

  send to model and check schema

- Show & Accept

  present suggestions

### Code Quality & Observability From Day 1

> "if you can't monitor it, you can't maintain it."

these standards must be applied from the beginning to facilitate debugging and stability

- Validation

  ensuring data integrity from the moment it enters the system.

- Error Handling

  graceful degradation and clear feedback loop for debugging.

- Observabilty

  real-time insights into system health and performance.

### Secrets Management - The Golden Rule

user `.env.example` as a secure template. never commit `.env` to Git

Application credentials (such as API key, database password) must be strictly
protected and injected into the environment, not hardcoded into the source code.

### Architectural Mindset & ADR

Architecture Decision Record (ADR)

a snapshot of a specific decision, capturing why it was made and the context
around it.

- Reasoning Matter Most

  _why_ you chose it is more important than _what_ you chose.

- No Perfect Architecture

  everything in software engineering is a series of _trade-offs_.

### Definition Of Done - Capstone Complete

- Functional Application

  auth, goals/tasks, calendar view and progress tracking work end-to-end

- Ai Suggestion Engine

  task breakdown + rationale + accept/reject flow fully functional

- Production Ready

  deployed to production, observabilty active, test coverage >= 50%

- Docs + Career Assets

  readme, problem framing, cv updated, pitch video, github documented.

### Stick to the MVP

- Target Graduation

  focus on the MVP column to ensure your project is completed on time

- Nice-To-Have Features

  consider these as a bonus. Work on them `ONLY` if the MVP is 100% complete
