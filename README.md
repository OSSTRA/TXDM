# Travel Exchange Data Model (TXDM)
This project is intended for establishing a standard for the exchange of travel information between different systems. This is an evolving standard, everyone can collaborate.

# Overview
We at OSSTRA have noticed that there are no standardized ways on how to plan and execute travel.

The goal of this project is to simplify and speed up data transfer between participants in the vacation planning industry.

We believe that the solution is to establish an industry standard data exchange format between data creators, processors and users. Together, we will try to achieve this goal by establishing common data models within this project so anybody can make use of them.

**Feel free to submit pull requests**

# Current State
This project just started. Please register your interest in the dicussion forum.

I am looking for people to contribute to the project. Together, we will continuing to define the architecture and implementation. Please participate in the open issues.

Any code in the repo is in active development, please do thorough testing and verification before implementing for production use.

# Background

## Background to the problem

The vacation planning industry is primarily made up from big corporations providing accomodations, tech companies proving booking services, small companies offering packaged tours and small actors executing individual vacation planning services.

Every step of the vacation planning lifecycle is currently more or less isolated and unconnected. Planning is done in Excel, Booking is done on Booking Platforms, Communication to Participants is individually prepared. 

### Motivation and goals

The motivation is to stop the usage of sub-optimal tools for vacation planning and to introduce an open solution for individuals and small businesses to use to create vacaiton iterinaries.

# Implementation

The standard has been split in so-called **Travel Objects (TO)**, whicha re each responsible for indivuals function within travel planning.

## Concept

| title | responsibility| description |
|-------------|-------------|-------------|
|[Travel Place Objects (TPO)](#travel-place-objects-tpo)|Places| Depicting points of interest within a travel plan           |
|[Travel Movement Objects (TMO)](#travel-movement-objects-tmo)|Transportation| Depicting transportation within a travel plan           |
|[Travel Human Objects (THO)](#travel-human-objects-tho)|Participation | Depicting members of the travel plan, including responsibilities           |
|[Travel Booking Objects (TBO)](#travel-booking-objects-tbo)|Reservation Management| Depicting bookings and reservations           |
|[Travel Itinerary Objects (TIO)](#travel-itinerary-objects-tio)|Scheduling| Scheduling all other objects types to create a plan           |
|[Travel Redlining Objects (TRO)](#travel-redlining-objects-tro)|Reviewing| Add comments to all objects of the plan           |

## Glossary
