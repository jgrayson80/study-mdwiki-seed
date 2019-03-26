# ASCP 2019 Study Guide

Based on August 2018 content guidline and reading list

## Test to link

[Navigation](navigation.md)

Well that worked

## Mermaid incorporation test

### Flowchart

```mermaid
graph LR
    A --> B
    B --> C
    C --> D
    C --> E
```

## Plant UML incorporation test

```puml
@startuml
start
if (condition A) then (yes)
  :Text 1;
elseif (condition B) then (yes)
  :Text 2;
  stop
elseif (condition C) then (yes)
  :Text 3;
elseif (condition D) then (yes)
  :Text 4;
else (nothing)
  :Text else;
endif
stop
@enduml
```