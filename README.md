# Travel Exchange Data Model (TXDM)
This project is intended for establishing a standard for the exchange of travel information between different systems. This is an evolving standard, everyone can collaborate.

# About
We at TXDM have noticed that there are no standardized ways on how to plan and execute travel. We set ourselves the goal to develop an open source ecosystem of solutions that supports people in creating, managing and executing their travel plans.

The first step to te creation of such a solution is to think about how data will be stored within our ecosystem. We're looking at the bigger picture first and asking ourselves how we can make our system exchange data with other systems.

**Feel free to submit pull requests**

# Concept

| title | responsibility| description |
|-------------|-------------|-------------|
|Travel Place Objects (TPO)|Places| Depicting points of interest within a travel plan           |
|Travel Movement Objects (TMO)|Transportation| Depicting transportation within a travel plan           |
|Travel Human Objects (THO)|Participation | Depicting members of the travel plan, including responsibilities           |
|Travel Reservation Objects (TRO)|Reservation Management| Depicting bookings and reservations           |
|Travel Itinerary Objects (TRO)|Scheduling| Scheduling all other objects types to create a plan           |
|Travel Redlining Objects (TRO)|Reviewing| Add comments to all objects of the plan           |

# Implementation

## Position
Travelling in it's core is changing position for various reasons. Therefore, positions and the act of changing positions are a crucial element to consider when creating a standardized data exchange format for travel plans. Accurate and precise representation of positions help in trip planning, navigating unfamiliar places, and keeping track of the journey's progress, while acknowledging that travel is about changing locations.

In the real world, some objects are static, meaning that they don't move or change position, such as buildings, monuments, or other fixed structures. In contrast, other objects are dynamic, meaning that they can have changing locations over time, such as vehicles, boats or abstract things like travelling markets.

### Fixed Position
Some objects within a travel plan are static, such as landmarks, museums and others.

#### Coordinates
We have decided to utilize **World Geodetic System 1984 (WGS 84)** as the permanent system for referencing coordinates.

| title | type | description |
|-------------|-----------|-------------|
|geodetic latitude|Double|             |
|geodetic longitude|Double|             |
|height / height bounding box|Double|             |

#### Area
| title | type | description |
|-------------|-----------|-------------|
|points|Array| Array of type coordinate            |

### Dynamic Position
Some objects within a travel plan have dynamic locations, such as a motor home, ships or even travelling markets.

For dynamic objects, we need to use more advanced data structures that are able to represent the object's changing location over time. For example, we can use a track history data structure to store the position of a object at different points in time.

| title | type | description |
|-------------|-----------|-------------|
|timestamp|DateTime|             |
|fixedPosition|Fixed Position|Either Coordinate or Area             |

## Travel Place Objects (TPO)
Within a travel plan, there is a vast amount of objects covered. Places can be for accomodation, transportation or just for plain reference.

The Travel Object Model (TO) features minimal shared attributes and an type-specific amount of spezialiced attributes. The interpretation of the Type shall be solely dependent on the specialized attributed choosen.

| title | type | description |
|-------------|-----------|-------------|
|Title|String| |
|Properties|Dictionary| Dictionary of Properties|

### Location Properties

#### Stationary
#### Moving

### Accomodation

#### Hotel
#### Car
#### Motorhome
#### Homestay
#### Ryokan

### Restaurant

### Museum

### Activitity

### Reference Point

### Note

## Travel Movement Objects (TMO)
When talking about travel, we are talking about changing position to see/experience places. 

### Train

### Car

### Boat

## Travel Human Objects (THO)

### Common Attributes

| title | type| description |
|-------------|-------------|-------------|
|first_name|String|            |
|last_name|String|            |
|address||            |
|date_of_birth|Date|            |
|nationality|String|ISO 3166-1, Alpha-2 |

### Traveler

### Organizer

### Guide

### Driver

### Accommodation Manager

### Catering Coordinator

### Communication Liaison

### Photographer/Videographer

## Travel Reservation Objects (TRO)

## Travel Itinerary Objects (TRO)

## Travel Redlining Objects (TRO)
