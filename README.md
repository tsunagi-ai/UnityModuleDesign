# UnityModuleDesign

## How to use PlantUML

### Generate UML diagrams

Copy and paste into: https://www.plantuml.com/plantuml/uml/SyfFKj2rKt3CoKnELR1Io4ZDoSa70000

### How to read UML

- Class Diagram: https://plantuml.com/class-diagram
- Sequence Diagram: https://plantuml.com/sequence-diagram

## Class Architecture

- This is design **NOT** to depend on GameEngine or specific language as much as possible.
- Design to be as abstract as possible. Doesn't depend on game genre.

![Class Architecture](classes.png)

### developer experience

#### Design GOAP components

create inheritance of...

- `Action` and its actual implementation
- `ConditionSet`
  - composed of `Condition`
- `State`

#### Run Tsunagi thinking

- Once developer-created `Character` runned `TsunagiBrain.StartThink()`, the TsunagiModule start infering, and give a list of `Action` as output.
  - Developers can specify when to think

## Sequences

### When Chat Sent

![ChatSequences](Sequences/Message.png)

### When taking Actions

![ActionSequences](Sequences/Action.png)
