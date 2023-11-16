# ModuleTool Implementation


How to build and develop complex applications in the form of a network of managed services at the DNS level?


The idea is to have an automation layer to create tested services. (AI/ML is not able to make it so efficient)
The important thing about this solution is to focus on the format and type of input and output data and only then on the component itself.
This makes reuse possible, since the interface must be standardized, just as we do in APIs, but here we operate on the object form first.


Hypermodular solutions are using component-based architecture to create working service. In the current state of the project, I am implementing a simple SQL database to show with simple examples how we can build a web application based on open source code and/or chatgpt generated code. it's not about creating one service, but an entire ecosystem on DNS in automation way. Here's a little more on: 

+ Tool for managing service-based components 


it sounds like, just microservice provides an endpoint via a protocol. Hypermodularity is a way of creating an ecosystem of services, a network map of all components.


## How it works

in one sentence:  If We: Define Expectation - > Requirements -> Data Type Definition -> Prepare Example Data Values for Test purpose  ===> We can looking for existing Component OR generate him ===> Start with Stage: prototyping & after Successful Deployment -> Checking  expected data -> IF data on Output are correct Go to the stage: Test if not go to the Stage=prototyping ....



### Interface

User can work on terminal with command line and markdown editor for documentation purposes
+ markdown documentation for Model Data describing
+ markdown for Expactation and requirement description with examples Data on Data model with values

### Data, SQL DB

+ TestData
    + DataModel
    + DataValue

### Sourcecode

+ Logic
    + Component
    + Environment

### Test Iteration


### Environment, Infrasttructure



### Production Iteration



### Tools:

+ planShell
+ plainEdit



## DB structure

![db_structure3](/db_structure3.png)




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
    + Expectation: one
    + Requirement: many
    + TestData: many
    + Description: string    

+ Component
    + id  
    + type: file, class, function, url
    + input: DataModel
    + output: DataModel
    + comments: string
    + license: string
    + autor: string


+ DataValue
    + id
    + type
    + value
    + format

      
+ TestData
    + id
    + input_value: DataValue
    + output_value: DataValue
    + input_type: DataModel
    + output_type: DataModel



### Iteration


+ Environment
    + id
    + type: local, remote, vm  
    + configuration: docker, docker-comopse
    + volume
    + service
    + Stage: prototype, local, test, production

      
+ Deployment
    + id    
    + Documentation: one
    + Component: many
    + Environment: many     
    + Stage: prototype, local, test, production
    
      
## Monitoring

 + Logs
    + id
    + Deployment: one
    + Message
    


## Iteration



```php
$moduleList = []; // from files
$testModuleList = []; // from Readme
$codeList = []; // from files

// select component by DataModule
array findComponentByDataModule(codeList, testModuleList){
    $sourcecodeList = [];
    foreach(){
        
        $component = new Component($lang, $soucrecode, $input, $output)
        if (component->data->input === testModuleList->input) &&
           (component->data->output === testModuleList->output)
        {
            $componentList[] = $component;
        }
    }
    return $componentList
}

// test selected component
foreach(componentList as $component){
    $test_input = get_from_file("")
    $test_output = get_from_file("")
    
    iteration(DataModel $test_input, DataModel $test_output, $component);
}

function iteration(DataModel $test_input, DataModel $test_output, $component)
{
    DataModel function testComponent(DataModel $input, Component $component) {
        $component->language;
        $component->sourcecode;
        $component->input = $input;
        try{
            $result = new runComponent($component);
            new Logs(serialize($test_input), serialize($test_output), serialize(testComponent), str($e->getMessage()))
            return DataModel $result->output;
        }catch e {
            // logs Component messages
            new Logs(serialize($test_input), serialize($test_output), serialize(testComponent), str($e->getMessage()))
        }
        return DataModel(); // empty, error logs
    }
    
    bool function testDataOuptut(DataModel $test_output, DataModel $real_output){
        throw Exception('NotEqual')
        return true
    }
    
    try{
        // data preparation
        $test_input = new DataModel(type,value)
        $test_output = new DataModel(type,value)
        // test component        
        $real_output = testComponent($component, $test_input)
        // test output
        testDataOuptut($test_output, $real_output)
    }catch e {
        // logs Data messages
        new Logs(serialize($test_input), serialize($test_output), serialize(testComponent), str($e->getMessage()))
    }
}
```

----

```php

class TestData(
    private input;
    private output;

    function __construct(input, output){
        $this->input = input;
        $this->output = output;
    }
)

DataModel function testComponent($input) {
    return $output;
}

bool function testDataOuptut(DataModel $test_output, DataModel $real_output){
    return 
}

try{
    // data
    $data = new TestData(
            new DataModel(type,value)
            new DataModel(type,value)
        )
    $test_input = new DataModel(type,value)
    // component
    #$output = Component($data->input)
    $output = Component($test_input)

    DataComparasion$output
}catch e {
    // logs messages
}

try{
    // data
    $data = new TestData(
            new DataModel(type,value)
            new DataModel(type,value)
    )
    $test_input = new DataModel(type,value)
    // component    
    $output = Component($test_input)

    DataComparasion$output
}catch e {
    // logs messages
}


```


---

+ [edit](https://github.com/ModuleTool/docs/edit/main/3/README.md)
+ [git](https://github.com/ModuleTool/docs/)
