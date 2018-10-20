# Serverless Architecture for Node apps

## Better Names

* FaaS (Functions as a Service)
* Cloud Functions
* Lambda Functions

## DevOps & Architecture

Serverless takes care of scalability and availability. Is it a new architectural model in writing server-side applications. We're moving from IaaS (infrastructure as a service) to FaaS (functions as a service).

As a new architectural model, you can focus on building apps. No need to worry about Docker. Use existing FaaS or write your own FaaS. Event-driven, where events can be almost anything. The line between an API and a FaaS can be very hazy. We shift our thinking to fire an event with params to invoke a FaaS.

### Events

* message (queue)
* http call
* fs or db monitor
* inbound email
* Alexa

## FaaS

Pratik Patel seems pretty happy with OpenWhisk.
Gives lose coupling with tight cohesion, if you architect it with the following maxims:

* kep it small (do a unit of work)
  * this will keep latency low, due to fast startup
* make it single purpose
* keep it short running
  * you get charged for CPU x RAM
* keep it stateless
  * store that nonsense in a in-memory database (like Redis)
* Can be sync or async
  * async for long-running code and can call repeatedly for same result
* Can be invoked through a very wide range of events
