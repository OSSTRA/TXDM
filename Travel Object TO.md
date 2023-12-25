```mermaid
classDiagram
TravelObject <|-- VersionObject
    class TravelObject{
      +Guid Guid
      +Guid CurrentVersion
      +Version[] Versions
    }
    class VersionObject{
      +Guid Guid
      +DateTime Modified
      +String ModifiedBy
      +Object Data
    }
```
