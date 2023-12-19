## Generic Object Models (GOM)

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
