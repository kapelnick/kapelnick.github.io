## Tech Writing Interview Exercise

Source for [AsyncAPI document](https://github.com/quetzalliwrites/6-Figure-Tech-Writer-Resource-Hub/blob/main/interview-prep/writing-prompts/asyncapi-document-writing-prompt.md#technical-writing-interview-exercise-asyncapi-document)

[Application link](https://tally.so/r/3yEezB)

### Raw Text
An AsyncAPI file document or document file is basically a thing you have to create for some kind of Event-Driven API. It's a file that like defines different, totally important components of the API which of course is not REST, just to be clear, because it's events-based which means not synchronous... asynchronous is the opposite of synchronous FYI. You gotta use JSON, or YAML, but no funny business with YAML extensions, just plain YAML that matches JSON-like capabilities exactly; don't get creative.

AsyncAPI (the document thing) defines stuff for your Event-Driven—super important, super fancy—API. This document later gets turned into readable code stuff (not by magic, by machines) so it can be used for generating more docs, for validating all the incoming or outgoing or floating around somewhere messages sent by your Example_App, or possibly to apply some "policies" (whatever that means) to the events in the API before they go to, like, a broker? And don't ask about brokers; it's not that kind of broker, nothing to do with Wall Street.

Now, you have the ultimate in machine-readable API docs! Machines everywhere (robots? who knows?) can parse this stuff like it's no big deal. What will they do with it? Endless things. Or nothing at all.

Confused yet, or is that only me?


### Transformation
An AsyncAPI file is used for event-driven APIs. It defines the components of an API.

*Note that the API is not a REST API, due to the event being asynchronous

To do so, you must use JSON or YAML. It is recommended that YAML matches JSON-like syntax.

The AsyncAPI file is in turn transformed into code, to generate more docs to validate incoming and outgoing messages sent by your application

It is also used to apply "policies" to the events in the API before they are sent to the application
