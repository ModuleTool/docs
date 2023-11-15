# Low level solution

## DB structure

This diagram uses classDiagram to provide a visual representation of your data model and the relationships between entities. Each class has its attributes listed and relationships are represented by lines with varying types of connectors to indicate the nature of the relationship (e.g., composition, association).

![db strcuture](db_structure.png)


### Specification

+ Expectation
    + id  
    + description  
    + role: customer, manager

+ Requirement
    + id
    + description

+ DataModel
    + id
    + language: php, js, python
    + name: domain, url, host, 
    + type: file, class, function, url
    + format: json, html, yaml, text, string, integer, bool    





### Implementation

+ Documentation
    + Expectation_id: one
    + Requirement_id: many
    + Description
    + input: DataModel
    + output: DataModel

+ Component
    + id  
    + type: file, class, function, url
    + input: DataModel
    + output: DataModel
    + comments
    + autor


+ Implementation
    + id
    + Documentation_id: one
    + Component_id: many
    + Stage: prototype, local, test, production



### Iteration

+ Deployment
    + input_value: DataValue
    + output_value: DataValue
    + input_type: DataModel
    + output_type: DataModel
    + Component_id: Component
    + Environment_id: Environment
    
+ Environment
    + id
    + type: local, remote, vm  
    + configuration: docker, docker-comopse
    + volume
    + service
    + Stage: prototype, local, test, production


## Monitoring

 + Logs
    + id
    + Deployment_id
    + SQL
    + URI
    + PARAMS
    + description



## Iteration
```php
try{
    // component
}catch e {
    // logs messages
}
```