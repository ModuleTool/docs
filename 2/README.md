# Low level solution

## DB structure

![db strcuture](db_structure.png)

### Service Specification

+ Expectation
    + id  
    + description  
    + role: customer, manager

+ Requirement
    + id
    + description
    + input: DataModel
    + output: DataModel


+ DataModel
    + id
    + language: php, js, python
    + name: domain, url, host, 
    + type: file, class, function, url
    + format: json, html, yaml, text, string, integer, bool    


+ Documentation
    + Expectation_id: one
    + Requirement_id: many


+ Component
    + id  
    + type: file, class, function, url
    + input: DataModel
    + output: DataModel
    + comments
    + autor



### Implementation

+ Implementation
    + id
    + Documentation_id: one
    + Component_id: many
    + Stage: prototype, local, test, production

+ Deployment
    + input_value: DataValue
    + output_value: DataValue
    + input_type: DataModel
    + output_type: DataModel
    + Component_id: Component
    + Environment_id: Environment
    


  
### Environment

+ Environment
  + id
  + type: local, remote, vm  
  + configuration: docker, docker-comopse
  + volume
  + service
  + Stage: prototype, local, test, production

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