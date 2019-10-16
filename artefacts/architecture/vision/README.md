![Foosus Logo](../../../images/foosus.png)
# Architecture Vision

Project Geo-Aware FooSus (*working title*)
Client: Foosus

*Note: On hiring a replacement Architect this document WILL require tailoring to suit a the context and available information around the project at that time.*


# Table of Contents

1. Purpose of this Document
1. Problem Description
1. Detailed Objectives
1. Environment and Process Models
1. Actors and their Roles and Responsibilities

# Purpose of this Document

This document provides a partially completed summary of the changes to the enterprise required for successful deployment of the Target State Architecture (TSA) for a Geo-Aware, and future-proofed, Foosus platform. 

This Architecture Vision should provide key stakeholders and the leadership team with a *formally agreed outcome*. Early agreement on the outcome, prior to experimentation within the team, enables the architects and owners of our platfrom to focus on the steps necessary to validate feasibility and the TSA being fit for purpose. 

This document is intended to provide a _summary_ version of the architecture to be realised through investment in the accompanying Archiectural Statement of Work. 

# Problem Description

Foosus’ legacy platform has reached a critical point, where it is no longer supports planned business growth. Development teams are fully invested in fire-fighting and keeping it running, which has slowed down our ability to deliver new features and remain competitive within a new and unpredictable market.

We wish to keep the existing platform in maintance mode and restructure the teams to deliver an architected platform allowing the platform to grow in line with our business vision of supporting *local* markets. Sign-ups represent a key metric to our investors and can only be recovered through the aglity to innovate rapidly and experiment with variants of existing product offerings.

Our business objective is to rapidly and itteratively release an new product which co-exists with can initially co-exist with the existing platform before replacing it.

The goal of this project is to put in place the architectural constraints and direction to keep iterating rapidly towards our business goals.

The problem is further elaborated in the High Level Functional Requirements brief produced by the CIO and CPO, which stands in for a request for architectural work.

## Stake Holder Specific Constraints and Issues to be Addressed

### Rate of User Registrations

*Stake holders:* CEO, Ash Callum and Jo Kumar, CFO
Foosus's current consortium of investors are measuring our value in terms of our ability to maintain a positive rate of new user sign ups.

Expanding into local markets and providing geo-targetting are seen as critical factors in reaching a broader range of users. 

Any architecture should be designed to scale with planned increases in our customer base.

### Innovating within the Boundaries of an Enterprise Architecture 
*Stake holders:*  CIO, CPO, CFO

Foosus's legacy platform has support our operations but needs to be updated to support business growth plans. While preserving a sense of ownership in every engineer and partner involved in creating the new platform, there need to be clear boundaries to ensure that every increment is considered in terms of its impact towards providing the required business capabilities and supporting Foosus' future growth.

### Supporting Rapid Technical Innovation and Experimentation
*Stake holders:* CMO, CIO, CPO, CFO

The current market is one where our direct competitors are rapidly gaining advantages through pivoting in response to new learnings. Learning has to be at the heart of our target state architecture, as this has previously been bolted onto solutions in a way which resulted in greater instability and technical debt.

The platform should be designed with extensibility and feature customisation in mind.

### Visibility of Platform

*Stake holders*: CMO, CPO, Operations Lead

There is no clarity of how the current platform behaves technically, nor how our platform is performing from a business perspective. Any insights currently require analysis of logs and spreadsheets, before business intelligence can be sought.

We require an architecture design to provide real time insights and views of the
the platform health both technically and commercially.

### Improving Foosus' Market Reputation Through Stability

The Foosus brand needs to be be bolstered by reducing user visible outages. This includes:
* Processes to reduce the risk of releasing failing or poor quality solutions
* The ability to release new versions of our platform without impacting the user through outages.

3AM releases seemed to work when our users were primarily in one geographic region, however we should no longer depend on this.

# Detailed Objectives

The purpose of this section is to describe the detailed objectives that need to be fulfilled by Foosus' target state architecture.

We want to drive Foosus' marketing campaigns in a number of major cities, with the confidence that our platform will remain usable, responsive and deliver a first class customer experience. In order to achieve this we need to architect a solution and governance process which helps us deliver the business' current set of goals and overall vision.

# Environment and Process Models
The purpose of this section is to outline the environment and process models that are in scope for Foosus' target state architecture.

## Business processes that are in scope for the vision
* Customer facing search and ordering of consumables.

## Business and technology environment in scope for the vision
* Foosus web application and other Software assets (services)
* Runtime infrastructure
* Development infrstructure and processes


## Users who interact with the business process
* Food Suppliers will provide Foosus with an inventory of available foods
* Consumers will find foods and order foods
* Food Suppliers will receive orders
* Foosus Finance team will receive payment

## Information flows for the business processes

See [organisational value stream map](../../organisation/value-stream-map) for the current flows. 
*TODO: New flows to be defined by the New Architect.*

# Actors and their Roles and Responsibilities

This section describes the system users/actors in scope for Foosus' target state architecture. System actors/users are those users who interact with a system. They can be human or a system/computer.


## Human Actors and Roles

* Consumer - buyer
* Food Supplier - seller
* Customer Fulfillment Team Representative - customer facing
* Developer - implementer
* Finance Team Member - invoicing

## Computer Actors and Roles

* Inventory Systems
* Order Systems
* Search Systems
* Invoicing Systems


## Responsibilities

* Invoicing Systems must ensure that Food Suppliers are invoiced for a commission as all payment is made directly on delivery.

# Architure Model
This section describes the target state architecure principles and boundaries.

## High Level Diagram

*TODO: TO BE COMPLETED BY NEW ARCHITECT *

## Requirements that map to the target architecture
See [Geo-aware Food Sourcing - High Level Business Requirements Brief](../request-for-architectural-work/)

## Constraints that impact the target architecture
See stake-holder constraints above.

## Principles that impact the target architecture
### Principles to Be Reflected During a Process of Lean Architecture

#### Overarching Principles
* Feedback and learning driven decisions
* Making choices which support Long Term objectives.
* Accepting mistakes occur
* Ensuring we architect to fail fast and improve.

#### Business Principles
* Support business innovation and agility through extensibility
* Support brand reputation through stability


#### Data Principles
* Always model as though you don't have the full picture yet.
* Always protect personally identifiable data
* Design for either data access or mutability depending on the problem
* Apply consistency depending on the scenario to best statisfy the business need. (Don't assume that all data has to be immediately or even eventually consistent) 
* Reflect the domain model within an appropriate bounded context.

#### Application Principles
* Single responsibility and loose coupling of applications.
* Design open and extensible interfaces into systems, which you can easily iterate on.
* Apply a *consumer contract driven* approach where interfaces between systems reflect only the data and operation required for them to integrate.
* Avoid cyclical dependencies between systems.


#### Technology Principles

* Make choices which are open and convenient to change. 
* Build vs buy choices should be reasoned and always considered.
* Technology choices should align with the capability and fit to the business.
* Support releasing software as soon as possible.
* Ensure that all architecture components are designed to be easy to catalogue and not lose track of.
* Prefer and predictability and repeatability over non-determinism

# Target State Vision

* Decomissioned legacy platform
* Developer Experience friendly platform which aids developers in fulfilling new business requirements in congruence with longer-term business and technical roadmaps.


