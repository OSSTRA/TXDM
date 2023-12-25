```mermaid
classDiagram
TravelObject -- VersionObject
TraveTags -- VersionObject
    class TravelObject{
      +Guid Guid
      +Guid CurrentVersion
      +VersionObject[] Versions
    }
    class VersionObject{
      +Guid Guid
      +DateTime Modified
      +String ModifiedBy
      +Tags[] Tags
      +TravelObjectImplementation Data
    }
    class TravelTags{
        +Guid Guid
        +Title Title
    }
```
