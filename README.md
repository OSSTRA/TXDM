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

The standard has been split in so-called **Travel Objects (TO)**, which each are responsible for indidual functions of travel planning. None of these elements is required, allowing the creation and exchange of Travel Data in various stages of the Travel Planning Life Cycle.

## Concept

```mermaid
graph TD;
    subgraph Generic Object Models;
    BASE[Travel Object TO];
    end;
    subgraph Specific Object Models;
    BASE[Travel Object TO];
     BASE<-. implements .->TRO[Travel Redlining Objects TRO];
    BASE-->TIO[Travel Itinerary Object TIO];
    BASE-->TPO[Travel Place Object TPO];
    BASE-->TMO[Travel Movement Object TMO];
    BASE-->THO[Travel Human Object THO]
    BASE-->TBO[Travel Booking Object TBO]
    TIO<-- schedulable-->TPO;
    TIO<-- schedulable-->TMO;
    TIO<-- schedulable-->THO;
    TMO<-- bookedable -->TBO;
    THO<-- bookedable -->TBO;
    TPO<-- bookedable -->TBO;
    end;
    click BASE "https://github.com/OSSTRA/TXDM/blob/main/Travel%20Object%20TO.md"
    click TRO "https://github.com/OSSTRA/TXDM/blob/main/Travel%20Redlining%20Objects%20(TRO).md"
    click TIO "https://github.com/OSSTRA/TXDM/blob/main/Travel%20Itinerary%20Objects%20(TIO).md"
    click TPO "https://github.com/OSSTRA/TXDM/blob/main/Travel%20Place%20Objects%20(TPO).md"
    click TMO "https://github.com/OSSTRA/TXDM/blob/main/Travel%20Movement%20Objects%20(TMO).md"
    click THO "https://github.com/OSSTRA/TXDM/blob/main/Travel%20Human%20Objects%20(THO)"
    click TBO "https://github.com/OSSTRA/TXDM/blob/main/Travel%20Booking%20Objects%20(TBO).md"
```

| title | responsibility| description |
|-------------|-------------|-------------|
|[Travel Place Objects (TPO)](#travel-place-objects-tpo)|Places| Depicting points of interest within a travel plan           |
|[Travel Movement Objects (TMO)](#travel-movement-objects-tmo)|Transportation| Depicting transportation within a travel plan           |
|[Travel Human Objects (THO)](#travel-human-objects-tho)|Participation | Depicting members of the travel plan, including responsibilities           |
|[Travel Booking Objects (TBO)](#travel-booking-objects-tbo)|Reservation Management| Depicting bookings and reservations           |
|[Travel Itinerary Objects (TIO)](#travel-itinerary-objects-tio)|Scheduling| Scheduling all other objects types to create a plan           |
|[Travel Redlining Objects (TRO)](#travel-redlining-objects-tro)|Reviewing| Add comments to all objects of the plan           |

## Glossary
