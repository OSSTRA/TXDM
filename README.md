# Travel Exchange Data Model (TXDM)
This project is intended for establishing a standard for the exchange of travel information between different systems. This is an evolving standard, everyone can collaborate.

# About
We at TXDM have noticed that there are no standardized ways on how to plan and execute travel. We set ourselves the goal to develop an open source ecosystem of solutions that supports people in creating, managing and executing their travel plans.

The first step to te creation of such a solution is to think about how data will be stored within our ecosystem. We're looking at the bigger picture first and asking ourselves how we can make our system exchange data with other systems.

**Feel free to submit pull requests**

# Concept

| title | responsibility| description |
|-------------|-------------|-------------|
|[Travel Place Objects (TPO)](#travel-place-objects-tpo)|Places| Depicting points of interest within a travel plan           |
|[Travel Movement Objects (TMO)](#travel-movement-objects-tmo)|Transportation| Depicting transportation within a travel plan           |
|[Travel Human Objects (THO)](#travel-human-objects-tho)|Participation | Depicting members of the travel plan, including responsibilities           |
|[Travel Booking Objects (TBO)](#travel-booking-objects-tbo)|Reservation Management| Depicting bookings and reservations           |
|[Travel Itinerary Objects (TIO)](#travel-itinerary-objects-tio)|Scheduling| Scheduling all other objects types to create a plan           |
|[Travel Redlining Objects (TRO)](#travel-redlining-objects-tro)|Reviewing| Add comments to all objects of the plan           |

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

**Example**
```javascript
{
}
```

| title | type | description |
|-------------|-----------|-------------|
|Title|String| |
|Properties|Dictionary| Dictionary of Properties|

### Metadata Model
| title | type| description |
|-------------|-------------|-------------|
|metadata:check_in_time|DateTime|            |
|metadata:check_out_time|DateTime|            |

### Facility Model
| title | type| description |
|-------------|-------------|-------------|
|facility:has_in_room_safe|Boolean|            |
|facility:has_giftshop|Boolean|            |
|facility:has_restaurant|Boolean|            |
|facility:has_bar|Boolean|            |
|facility:has_lounge|Boolean|            |
|facility:has_connecting_rooms|Boolean|            |
|facility:has_kids_area|Boolean|            |
|facility:has_wifi|Boolean|            |
|facility:has_disabled_accessibilty|Boolean|            |
|facility:has_in_room_kitchen|Boolean|            |
|facility:has_pillow_menu|Boolean|            |
|facility:has_room_temperature_control|Boolean|            |
|facility:has_business_centre|Boolean|            |
|facility:has_parking|Boolean|            |

### Services Model
| title | type| description |
|-------------|-------------|-------------|
|service:has_room_service|Boolean|            |
|service:has_shuttle|Boolean|            |
|service:has_loyality_program|Boolean|            |
|service:has_spa_services|Boolean|            |
|service:has_laundry_services|Boolean|            |
|service:has_express_checkin|Boolean|            |
|service:has_express_checkout|Boolean|            |
|service:has_late_checkout|Boolean|            |
|service:has_early_checkin|Boolean|            |
|service:has_babysitting_service|Boolean|            |
|service:has_24x7_service|Boolean|            |
|service:has_airport_transfer_service|Boolean|            |
|service:has_bike_rental_service|Boolean|            |
|service:has_car_rental_service|Boolean|            |
|service:has_boat_rental_service|Boolean|            |
|service:has_golf_rental_service|Boolean|            |
|service:has_valet_parking_service|Boolean|            |
|service:has_wakeup_call_service|Boolean|            |
|service:has_childcare_service|Boolean|            |
|service:has_currency_exchange_service|Boolean|            |
|service:has_room_service|Boolean|            |
|service:has_baggage_storage_service|Boolean|            |

### Policy Model
| title | type| description |
|-------------|-------------|-------------|
|policy:has_pet_friendly_policy|Boolean|            |
|policy:has_smoking_friendly_policy|Boolean|            |

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

**Example**
```javascript
{
}
```

### Train

### Car

### Boat

## Travel Human Objects (THO)

**Example**
```javascript
{
  properties: [
    {
      key: 'first_name',
      value: 'Max'
    },
    {
      key: 'last_name',
      value: 'Mustermann'
    },
    {
      key: 'date_of_birth',
      value: '2000-01-01'
    },
    {
      key: 'nationality',
      value: 'DE'
    }
  ]
}
```

### Common Attributes

| title | type| description |
|-------------|-------------|-------------|
|first_name|String|            |
|last_name|String|            |
|address||            |
|date_of_birth|Date|ISO 8601            |
|nationality|String|ISO 3166-1, Alpha-2 |

### Traveler

### Organizer

### Guide

### Driver

### Accommodation Manager

### Catering Coordinator

### Communication Liaison

### Photographer/Videographer

## Travel Booking Objects (TBO)

**Example**
```javascript
{
}
```

## Travel Itinerary Objects (TIO)

**Example**
```javascript
{
}
```

## Travel Redlining Objects (TRO)

**Example**
```javascript
{
}
```
