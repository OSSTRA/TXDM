## Travel Place Objects (TPO)
Within a travel plan, there is a vast amount of objects covered. Places can be for accomodation, transportation or just for plain reference.

The Travel Object Model (TO) features minimal shared attributes and an type-specific amount of spezialiced attributes. The interpretation of the Type shall be solely dependent on the specialized attributed choosen.

### Base Type Reference - Travel Object (TO)
Always be aware about that concrete implementations are alwas to be implemented in the Travel Object (TO) context to ensure support of functionalities.

**Reference:** [Travel Object (TO) Reference](https://github.com/OSSTRA/TXDM/blob/main/docs/Travel%20Object%20TO.md)

### Example
```javascript
 {
    "Attributes": [
        {
            "key": "metadata:capacity",
            "value": 5
        },
        {
            "key": "f acility:has_disabled_accessibilty",
            "value": true
        }
    ],
    "Tags": [] //see datatag implementation
 }
```

## Concept
//insert diagram of sub classes here

## Attributes

All attributes that can be attached to this implementation. Attributes are to be assigned based on the [Travel Object (TO) Reference](https://github.com/OSSTRA/TXDM/blob/main/docs/Travel%20Object%20TO.md).

## Shared Attributes
These attributes are valid for all sub types of Travel Place Objects (TPO).

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

## Location Properties

### Accomodation

#### Hotel
Attributes which are only assignable to Hotels.

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
Accomodation can also temporary exist in the form a a car, which is an example for a non-static place.

Attributes which are only assignable to Cars.

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
Accomodation can also exist in the form a a motor home, which is an example for a non-static place.

Attributes which are only assignable to Motor Homes.

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

Attributes which are only assignable to Homestays.

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

#### Metadata Model
| title | type| description |
|-------------|-------------|-------------|

#### Facility Model
| title | type| description |
|-------------|-------------|-------------|

#### Services Model
| title | type| description |
|-------------|-------------|-------------|

#### Policy Model
| title | type| description |
|-------------|-------------|-------------|

### Museum

#### Metadata Model
| title | type| description |
|-------------|-------------|-------------|

#### Facility Model
| title | type| description |
|-------------|-------------|-------------|

#### Services Model
| title | type| description |
|-------------|-------------|-------------|

#### Policy Model
| title | type| description |
|-------------|-------------|-------------|

### Activitity

#### Metadata Model
| title | type| description |
|-------------|-------------|-------------|

#### Facility Model
| title | type| description |
|-------------|-------------|-------------|

#### Services Model
| title | type| description |
|-------------|-------------|-------------|

#### Policy Model
| title | type| description |
|-------------|-------------|-------------|

### Reference Point
For storage of reference points. These places do only exist for reference (e.g. orientation, taking photos, navigation, ..) and are not easily referencable (e.g. by name, address) in real life.

Reference points are generally to be identified with coordinates.

#### Metadata Model
| title | type| description |
|-------------|-------------|-------------|

#### Facility Model
| title | type| description |
|-------------|-------------|-------------|

#### Services Model
| title | type| description |
|-------------|-------------|-------------|

#### Policy Model
| title | type| description |
|-------------|-------------|-------------|