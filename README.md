# COS — Career Operating System

<p align="center">
  <img src="https://img.shields.io/badge/status-Concept%20%2F%20MVP%20Planning-yellow" alt="Project Status">
  <img src="https://img.shields.io/badge/license-MIT-blue" alt="License">
  <img src="https://img.shields.io/badge/product-Career%20Operating%20System-purple" alt="Product">
  <img src="https://img.shields.io/badge/AI-Augmented-brightgreen" alt="AI Augmented">
</p>

<p align="center">
  <strong>A personal operating system for planning, navigating, and managing your career.</strong>
</p>

<p align="center">
  Plan your goals. Build your skills. Manage your applications. Track your progress.
  Turn your career journey into an actionable roadmap.
</p>

---

## Project Status

> **Current Status: Concept / Product Discovery / MVP Planning**

COS is currently in the product discovery and architecture planning stage.

The repository is being established before implementation begins in order to document the product vision, requirements, user journeys, domain model, architecture, and development roadmap.

The initial goal is to build a functional MVP that helps users transform an uncertain career journey into a structured, measurable, and actionable plan.

---

# Overview

**COS (Career Operating System)** is a career planning and management platform designed to help people navigate complex career journeys.

Traditional job trackers focus primarily on applications.

COS takes a broader approach.

It treats a career as a long-term journey involving:

- Career goals
- Skills
- Learning
- Projects
- Applications
- Networking
- Interviews
- Professional development
- Personal milestones
- Career transitions

The objective is not simply to answer:

> **"What jobs have I applied for?"**

COS aims to answer:

> **"Where am I in my career journey, where do I want to go, and what should I do next?"**

---

# Problem Statement

Career development is often fragmented across multiple tools.

A person may use:

- LinkedIn for professional networking
- Job boards for applications
- Spreadsheets for application tracking
- Notion or similar tools for planning
- Online courses for learning
- GitHub for projects
- Documents for CV versions
- Calendars for interviews
- Separate notes for career goals

This fragmentation makes it difficult to maintain a coherent view of the overall career journey.

COS aims to bring these elements together into a single structured system.

---

# Product Vision

COS is designed around four core principles.

### 1. Structure

Transform broad career ambitions into structured goals, milestones, roadmaps, and actionable tasks.

### 2. Visibility

Provide users with a clear overview of their current career position, progress, strengths, weaknesses, and outstanding objectives.

### 3. Context

Connect career goals, skills, learning, projects, applications, and professional development.

### 4. Intelligence

Use AI to analyse structured information within the system and provide contextual recommendations.

The AI should **augment the user's decision-making rather than replace it**.

For more information, see:

- [`docs/vision.md`](docs/vision.md)
- [`docs/user-personas.md`](docs/user-personas.md)

---

# Core Product Question

COS is built around three fundamental questions:

### Where am I?

Understand the user's current career position, skills, experience, projects, qualifications, and professional activity.

### Where do I want to go?

Define career goals, target roles, desired skills, milestones, and long-term objectives.

### What should I do next?

Convert the gap between the current state and desired state into actionable tasks, learning objectives, projects, applications, and milestones.

---

# Core Product Loop

COS is designed around a continuous career-development lifecycle:

```text
Current State
      ↓
Career Goal
      ↓
Skills / Experience Gap
      ↓
Roadmap
      ↓
Actions
      ↓
Progress
      ↓
Updated Current State
      └──────────────────────↺
```

The objective is to create a continuous feedback loop in which users can reassess their position, update their goals, and adapt their plans as their careers develop.

---

# Target Users

COS is intended to support multiple career stages.

## Students

Students preparing to enter the professional world.

Potential needs:

- Career exploration
- Skills assessment
- Learning roadmaps
- Project planning
- CV preparation
- Internship tracking
- First job applications

## Graduates

Recent graduates transitioning from education into employment.

Potential needs:

- Job-search planning
- Portfolio development
- Application tracking
- Interview preparation
- Skills gap analysis
- Professional networking

## Career Changers

Professionals transitioning into a new career or industry.

Potential needs:

- Transferable skills identification
- Skills-gap analysis
- Reskilling plans
- Career roadmaps
- Application management
- Progress tracking

## Established Professionals

Professionals seeking advancement or a change in direction.

Potential needs:

- Career progression planning
- Promotion preparation
- Professional development
- Networking
- Certifications
- Long-term career planning

## Freelancers & Entrepreneurs

Potential future users managing a transition toward independent work.

Potential needs:

- Business goals
- Client acquisition
- Skills development
- Revenue milestones
- Project tracking

Detailed persona definitions are documented in:

[`docs/user-personas.md`] (docs/user-personas.md)

---

# Core Product Areas

The long-term COS ecosystem may consist of several interconnected modules.

## COS Core

The central career management system.

Responsible for:

- User profiles
- Career goals
- Career roadmaps
- Milestones
- Tasks
- Progress tracking

## COS Job Tracker

Application and recruitment management.

Potential functionality:

- Job opportunities
- Applications
- Application stages
- Companies
- Contacts
- Interviews
- Follow-ups
- Rejections
- Offers

## COS Skills

Skills and competency management.

Potential functionality:

- Technical skills
- Soft skills
- Skill levels
- Target skills
- Skills gaps
- Learning objectives
- Evidence and projects associated with skills

## COS Learning

Personal learning and development management.

Potential functionality:

- Learning objectives
- Courses
- Certifications
- Study plans
- Learning resources
- Progress tracking
- Skill acquisition

## COS Portfolio

Professional evidence management.

Potential functionality:

- Projects
- GitHub repositories
- Portfolio items
- Certifications
- Achievements
- Case studies
- Professional documentation

## COS Coach

AI-assisted career guidance.

The AI layer could analyse structured career data and provide contextual recommendations.

Examples:

	"Your target roles commonly require Docker, but your current skills profile does not include it. Consider adding a Docker project to your roadmap."

	"Your application activity is high, but your interview conversion rate is low. Consider prioritising interview preparation."

	"Your GitHub contains several relevant projects, but your portfolio does not currently highlight them."

The objective is career intelligence, not generic chatbot functionality.

---

# AI Philosophy

COS is not intended to be another generic LLM interface or chatbot wrapper.

The product should be built around structured data and workflows first.

AI should operate on the user's career context.

The guiding principle is:

	Structured data first. AI second.

Conceptually:

```text
                    ┌──────────────────┐
                    │   User Goals     │
                    └────────┬─────────┘
                             │
                    ┌────────▼─────────┐
                    │   COS Domain     │
                    │      Model       │
                    └────────┬─────────┘
                             │
                    ┌────────▼─────────┐
                    │ Structured Data  │
                    └────────┬─────────┘
                             │
       ┌─────────────────────┼─────────────────────┐
       │                     │                     │
   Skills                 Projects            Applications
       │                     │                     │
       └─────────────────────┼─────────────────────┘
                             │
                    ┌────────▼─────────┐
                    │ Intelligence     │
                    │     Layer        │
                    └────────┬─────────┘
                             │
                    ┌────────▼─────────┐
                    │ Recommendations  │
                    └──────────────────┘
```
AI should:

- Analyse career context
- Identify potential skills gaps
- Highlight patterns
- Suggest actions
- Assist with planning
- Provide contextual recommendations

AI should not:

- Make career decisions on behalf of users
- Replace professional judgement
- Generate recommendations without relevant context
- Become the primary purpose of the application

---

# What COS Is Not

COS is not intended to be:

- A recruitment agency
- A job board
- A replacement for LinkedIn
- A generic AI chatbot
- A generic project-management application
- A standalone CV generator
- A learning platform
- An automated career decision-maker

COS is a personal career management and planning system.

---

# MVP Scope

The first version of COS will deliberately focus on the fundamental career-planning workflow.

## Initial MVP

The MVP should allow a user to:

1. Create a career profile.
2. Define a career goal.
3. Create a roadmap toward that goal.
4. Define milestones.
5. Create actionable tasks.
6. Track progress.
7. Review their current career position.

The MVP should validate the core COS product loop before expanding into more complex functionality.

## Post-MVP Candidates

Potential future functionality includes:

- Job application tracking
- Skills management
- Learning management
- Portfolio management
- AI career analysis
- Skills-gap analysis
- CV analysis
- LinkedIn analysis
- GitHub integration
- Job-market analysis
- Interview preparation
- Calendar integration
- External service integrations

These features are subject to product validation and are not commitments for the initial MVP.

---

# Conceptual Architecture

COS will be designed around a domain-driven application model in which career information is represented as structured entities and relationships.

At a conceptual level:
```text
┌─────────────────────┐
│        User         │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│   COS Application   │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│   Career Domain     │
│       Model         │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ Structured Career   │
│       Data          │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ Intelligence Layer  │
│      (Future)       │
└─────────────────────┘
```
The concrete technical architecture and technology choices will be documented separately once the MVP requirements and domain model have been defined.

---

# Potential Domain entities

The initial domain model is expected to include entities such as:
```text
User
 │
 ├── Career Goals
 │
 ├── Roadmaps
 │    ├── Milestones
 │    └── Tasks
 │
 ├── Skills
 │
 ├── Learning Plans
 │
 ├── Projects
 │
 ├── Job Opportunities
 │    └── Applications
 │
 ├── Companies
 │
 ├── Contacts
 │
 ├── Interviews
 │
 └── Achievements
```

This is a preliminary conceptual model and will be refined during the requirements and domain-modelling phases.

---

# Technology

The final production technology stack has not yet been formally selected.

Potential technologies under consideration include:

## Backend

- Java
- Spring Boot
- REST APIs

## Frontend

- Angular
- TypeScript
- HTML5
- CSS

## Data

- MySQL
- PostgreSQL

## Infrastructure

- Docker
- GitHub Actions
- Linux
- Cloud hosting

## AI

- LLM APIs
- Retrieval-Augmented Generation (RAG)
- Embeddings
- Vector databases

Technology decisions will be made after the product requirements and domain model have been sufficiently defined.

---

# Development Philosophy

COS will be developed using an iterative product-development approach.

The development process will emphasise:

- Requirements before implementation
- User-centred design
- Clear domain modelling
- Separation of concerns
- Testable components
- RESTful API design
- Secure authentication
- Maintainable code
- Automated testing
- Documentation
- Version control
- Continuous integration

The project will follow an Agile-inspired workflow using:

- Epics
- User stories
- Tasks
- Backlog management
- Iterative sprints
- Product validation

---

# Documentation

Project documentation will be maintained alongside the implementation.

Current documentation:
| Document                                         | Purpose                                    | Status     |
| ------------------------------------------------ | ------------------------------------------ | ---------- |
| [`docs/vision.md`](docs/vision.md)               | Product vision and philosophy              | ✅ Complete |
| [`docs/user-personas.md`](docs/user-personas.md) | Primary user personas and jobs-to-be-done  | ✅ Complete |
| `docs/product-requirements.md`                   | Functional and non-functional requirements | 🚧 Planned |
| `docs/domain-model.md`                           | Domain entities and relationships          | 🚧 Planned |
| `docs/architecture.md`                           | Technical architecture                     | 🚧 Planned |
| `docs/roadmap.md`                                | Product and development roadmap            | 🚧 Planned |

Planning documentation will be maintained under:
planning/

Design and visual documentation will be maintained under:
designs/

---

# Development Roadmap

## Phase 0 — Product Discovery

 - Define initial product concept
 - Define product vision
 - Define target users
 - Define initial user personas
 - Define core product philosophy
 - Define functional requirements
 - Define non-functional requirements
 - Define user stories
 - Define MVP scope
 - Create domain model
 - Define technical architecture
 
## Phase 1 — Foundation

 - Repository and project structure
 - Development environment
 - Application architecture
 - Database design
 - Authentication
 - User profile
 - Career goals
 
## Phase 2 — Career Planning

 - Career roadmaps
 - Milestones
 - Tasks
 - Skills
 - Progress tracking
 - Dashboard
 
## Phase 3 — Job Search

 - Companies
 - Job opportunities
 - Applications
 - Application pipeline
 - Contacts
 - Interviews
 
## Phase 4 — Intelligence

 - AI career analysis
 - Skills-gap analysis
 - Personalised recommendations
 - CV analysis
 - Career roadmap suggestions
 
## Phase 5 — Integrations

Potential integrations:

 - GitHub
 - Calendar
 - Job boards
 - Learning platforms
 - Microsoft ecosystem

---

# COS Ecosystem

COS may eventually evolve into a broader ecosystem of structured personal operating systems.

## Career Operating System

COS

	Manage your career journey.

## Writer Operating System

Writer OS

	Manage your creative writing journey.

Potential Writer OS functionality includes:

- Character management
- Character relationships
- Plot management
- Story structures
- Chapters and scenes
- Story timelines
- Worldbuilding
- Locations
- Factions
- Plot threads
- Continuity tracking
- Story analysis
- AI-assisted story analysis
- Visual story planning

An Excalidraw-based or compatible visual whiteboard may eventually provide a canvas for connecting story elements visually.

Writer OS is considered a future product within the COS ecosystem and is outside the initial COS MVP.

Both products share the same philosophy:

	Structure first. Intelligence second.
	
---

# Security & Privacy

Career information can be highly personal.

Future development will therefore prioritise:

- Secure authentication
- Password hashing
- Authorisation
- Input validation
- Secure API design
- Secrets management
- Data minimisation
- Appropriate protection of user career information

AI integrations should avoid unnecessary exposure of sensitive user data.

Specific security architecture will be documented before production deployment.

---

# License

This project is currently intended to use the MIT License unless otherwise specified.

Copyright © 2026 Stephen Nicholas Jones De Giorgi.

---

# Author

Stephen Nicholas Jones De Giorgi

Full-Stack Developer | Web Applications | Automation | AI

[`https://github.com/L0cksat`] (GitHub)
[`www.linkedin.com/in/stephen-nicholas-jones-de-giorgi-50668449`] (LinkedIn)
[`https://stephennicholasjones.com`] (Portfolio)

---

# Project Philosophy

COS is based on a simple idea:

	A career should be managed as a journey, not just a collection of job applications.

The goal is to give people the structure, visibility, context, and intelligence they need to make deliberate decisions about their professional future.

	Turn uncertainty into structure. Turn structure into action. Turn action into measurable progress.