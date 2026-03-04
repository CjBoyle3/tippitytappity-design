# tippitytappity-design

tippitytappity is a program to practice typing


## Data model

```mermaid
classDiagram
  User <|-- UserStats
  class User{ 
        - name: string
        - email: string
        - password: string
        + ign: string
        + login(user: string, pass: string) boolean
        + get_email() string
  }
  class UserStats{
        + topScores vector~float~
        + bestAccuracy: float
        + strength: (character: char, accuracy: float) 
        + weakness (character: char, accuracy: float) 
  }
  UserStats <|-- history
  class History{
        + bestTime: string
        + averageTime: string
        + averageAccuracy: string
        + averageWPM: string
```
