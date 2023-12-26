## Travel Object (TO)
This data standard is based among a base concept - the 'Travel Object (TO)'. This data structure contains metadata for base functionality offered by this data exchange standard. 

### Functionality
#### Versioning
Keeping track of all changes executed in a travel plan to allow a transparent overview about data evolution.

#### Tagging
Allowing to include tags in the data allows to depict data evolution in a way that is understandable by humans.

### Concept


```mermaid
classDiagram
Wrapper -- Version
Tag -- Version
Version -- TravelObject
TravelObject -- Attribute
TravelObject -- Tag
Tag <-- VersionTag
Tag <-- DataTag
    class Wrapper{
      +Guid Guid
      +Guid CurrentVersion
      +VersionObject[] Versions
    }
    class Version{
      +Guid Guid
      +DateTime Modified
      +String ModifiedBy
      +Tag[] Tags
      +TravelObject Data
    }
    class Tag{
        +Guid Guid
        +Title Title
    }
    class TravelObject{
        +Attribute[] Attributes
        +Tag[] Tags
    }
    class Attribute{
        +String Key
        +Object Value
    }
    note for Version "Versioning Implementation"
    note for Tag "Tagging Implementation"
    note for TravelObject "Can be any type of 'Travel X Object' (TXO)"
    note for Attribute "Needs to be compatible with choosen 'Travel X Object' (TXO), select from catalogue"
```
