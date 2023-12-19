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
