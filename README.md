# PlantUML styles for Event Storming

## Getting started

At the top of your PlantUML `.puml` file, you need to include the `styles.puml` file found in the `root` of this repo.

After you have included `styles.puml` you can use the defined macro definitions for the Event Storming elements: `ContextBoundary`, `Command`, `DomainEvent`, `Policy`, `Actor`, `Aggregate`, `ReadModel`, and `ExternalSystem`.

## Example

```csharp
@startuml
!include styles.puml

title Example components for Event Storming

ContextBoundary(CTX, "Description context boundary") {
    Command(C, "Command", "Some command")
    DomainEvent(DE, "Domain event", "Some domain event")
    Policy(PO, "Policy", "Some policy")
    Actor(A, "Actor", "Some actor")
    Aggregate(AG, "Aggregate", "Some aggregate")
    ReadModel(RM, "Read model", "Some read model")
    ExternalSystem(ES, "External system", "Some external system")
}

ContextBoundary(CTX2, "Without description context boundary") {
    Command(C2, "Command")
    DomainEvent(DE2, "Domain event")
    Policy(PO2, "Policy")
    Actor(A2, "Actor")
    Aggregate(AG2, "Aggregate")
    ReadModel(RM2, "Read model")
    ExternalSystem(ES2, "External system")
}

@enduml
```

![Preview](preview.png)