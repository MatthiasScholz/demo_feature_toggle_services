# Flipt

- https://flipt.io

## Usage

```
make up
make test
make down
```

## Features

- REST API
- GRPC
- UI
- A/B Testing

- Simple
- Prometheus
- OpenTracing

### Evaluation

> Evaluation is the process of sending requests to the Flipt server
> to process and determine
> if that _request matches_ any of your _segments_, and 
> if so which _variant_ to _return_.

- https://flipt.io/docs/concepts/#evaluation

#### Entities

> Evaluation works by uniquely identifying each thing that you want to compare against
> your segments and flags.
> We call this an __entity_ in the Flipt ecosystem.
> 
> More often than not this will be a user,
> but we didn’t want to make any assumptions on how your application works,
> which is why entity was chosen.
> 
> For Flipt to successfully determine which bucket your entities fall into,
> it must have a way to uniquely identify them.
> 
> This is the _entityId_ and it is a simple string.
> It’s up to you what that entityId is.

- https://flipt.io/docs/concepts/#entities

### REST API Client

> You can use swagger-codegen to generate client code
> in your preferred language from the OpenAPI v2 specification linked above.

- https://flipt.io/docs/integration/#rest-clients

## Evaluation

### Pros

- easy to setup
- good documentation
- lean ui
- flexible

### Cons

- complexity due to different concepts

### Untested

- how to do time based toggling? -> possible with Segments
  - Segment -> Comparison Type: Number -> Operator: >= -> Value: date, time as number
    - (https://www.epochconverter.com);
  - Property Naming Convention: e.g. `ToggleAfter`
  - -> Error prone, potential for mistake - time has to be send by the service, time zones have to match.
  - -> Number hard to read as human
