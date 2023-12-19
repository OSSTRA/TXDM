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

## Concept

| title | responsibility| description |
|-------------|-------------|-------------|
|[Travel Place Objects (TPO)](#travel-place-objects-tpo)|Places| Depicting points of interest within a travel plan           |
|[Travel Movement Objects (TMO)](#travel-movement-objects-tmo)|Transportation| Depicting transportation within a travel plan           |
|[Travel Human Objects (THO)](#travel-human-objects-tho)|Participation | Depicting members of the travel plan, including responsibilities           |
|[Travel Booking Objects (TBO)](#travel-booking-objects-tbo)|Reservation Management| Depicting bookings and reservations           |
|[Travel Itinerary Objects (TIO)](#travel-itinerary-objects-tio)|Scheduling| Scheduling all other objects types to create a plan           |
|[Travel Redlining Objects (TRO)](#travel-redlining-objects-tro)|Reviewing| Add comments to all objects of the plan           |


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

#### Common Attributes

##### Metadata Model
| title | type| description |
|-------------|-------------|-------------|
|metadata:capacity|Integer| How many people can the place fit?          |

##### Facility Model
| title | type| description |
|-------------|-------------|-------------|
|facility:has_giftshop|Boolean|            |
|facility:has_restaurant|Boolean|            |
|facility:has_bar|Boolean|            |
|facility:has_lounge|Boolean|            |
|facility:has_kids_area|Boolean|            |
|facility:has_wifi|Boolean|            |
|facility:has_disabled_accessibilty|Boolean|            |
|facility:has_business_centre|Boolean|            |
|facility:has_parking|Boolean|            |

##### Services Model
| title | type| description |
|-------------|-------------|-------------|
|service:has_baggage_storage_service|Boolean|            |

##### Policy Model
| title | type| description |
|-------------|-------------|-------------|
|policy:has_pet_friendly_policy|Boolean|            |
|policy:has_smoking_friendly_policy|Boolean|            |

##### Location Properties

### Accomodation

#### Hotel
##### Metadata Model
| title | type| description |
|-------------|-------------|-------------|
|metadata:check_in_time|DateTime|            |
|metadata:check_out_time|DateTime|            |

##### Facility Model
| title | type| description |
|-------------|-------------|-------------|
|facility:has_in_room_safe|Boolean|            |
|facility:has_connecting_rooms|Boolean|            |
|facility:has_kids_area|Boolean|            |
|facility:has_in_room_kitchen|Boolean|            |
|facility:has_pillow_menu|Boolean|            |
|facility:has_room_temperature_control|Boolean|            |

##### Services Model
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

##### Policy Model
| title | type| description |
|-------------|-------------|-------------|


#### Car

##### Metadata Model
| title | type| description |
|-------------|-------------|-------------|
|metadata:owner|Travel Human Object|            |

##### Facility Model
| title | type| description |
|-------------|-------------|-------------|

##### Services Model
| title | type| description |
|-------------|-------------|-------------|

##### Policy Model
| title | type| description |
|-------------|-------------|-------------|

#### Motorhome

##### Metadata Model
| title | type| description |
|-------------|-------------|-------------|
|metadata:owner|Travel Human Object|            |

##### Facility Model
| title | type| description |
|-------------|-------------|-------------|

##### Services Model
| title | type| description |
|-------------|-------------|-------------|

##### Policy Model
| title | type| description |
|-------------|-------------|-------------|

#### Homestay

##### Metadata Model
| title | type| description |
|-------------|-------------|-------------|
|metadata:owner|Travel Human Object|            |

##### Facility Model
| title | type| description |
|-------------|-------------|-------------|

##### Services Model
| title | type| description |
|-------------|-------------|-------------|

##### Policy Model
| title | type| description |
|-------------|-------------|-------------|

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
