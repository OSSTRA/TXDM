# TXDM
This project is intended for establishing a standard for the exchange of travel information between different systems. This is an evolving standard, everyone can collaborate.

**Feel free to submit pull requests**

# Position
In the real world, some objects are static, meaning that they don't move or change position, such as buildings, monuments, or other fixed structures. In contrast, other objects are dynamic, meaning that they can have changing locations over time, such as vehicles, boats or abstract things like travelling markets.

## Fixed Position
### Coordinates
- geodetic latitude
- geodetic longitude
- height / height bounding box
- geographic coordinate reference system

### Area
- points[]

## Dynamic Position
For dynamic objects, we need to use more advanced data structures that are able to represent the object's changing location over time. For example, we can use a track history data structure to store the position of a object at different points in time.

- timestamp
- fixedPosition

# Places
## Accomodation
### Stationary Accomodation
### Moving Accomodation
