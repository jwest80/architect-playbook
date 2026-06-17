# Markdown Diagram Examples

Use markdown-native diagrams for quick iteration. Move polished or tool-generated diagrams into [images](images/) when needed.

## Mermaid Flowchart

```mermaid
flowchart LR
    User[User] --> App[.NET API]
    App --> KeyVault[Azure Key Vault]
    App --> Database[(Database)]
    App --> Monitor[Application Insights]
```

## Mermaid Sequence Diagram

```mermaid
sequenceDiagram
    participant User
    participant App as .NET API
    participant Bus as Message Bus
    participant Worker

    User->>App: Submit request
    App->>App: Validate command
    App->>Bus: Publish event
    Bus->>Worker: Deliver event
    Worker->>Worker: Process asynchronously
    Worker-->>Bus: Complete message
```

## Simple C4-Style Text Diagram

```text
System Context

[Customer]
    -> uses
[Web Application]
    -> calls
[Orders API]
    -> stores data in
[Orders Database]
    -> publishes events to
[Message Bus]
```

## Referencing PNG or SVG Images

Place exported images in `docs/diagrams/images`.

```markdown
![Container deployment diagram](images/container-deployment.png)
![Service interaction diagram](images/service-interaction.svg)
```

