## Componentn based architecture

## Why Is this Important
when deploying websites a library can be used to speed the process and add more functionality to a website with less time, this is important as when in the field im sure we wont be given 5 days to write a basic website, this allows us to use industry tools and pre debugged librarys to innact significant overhaul to our product in a streamlined manner

## What is a “component”?
> A component is a modular, portable, replaceable, and reusable set of well-defined functionality that encapsulates its implementation and exporting it as a higher-level interface.

## What are the characteristics of a component?
- The software system is decomposed into reusable, cohesive, and encapsulated component units.

- Each component has its own interface that specifies required ports and provided ports; each component hides its detailed implementation.

- A component should be extended without the need to make internal code or design modifications to the existing parts of the component.

- Depend on abstractions component do not depend on other concrete components, which increase difficulty in expendability.

- Connectors connected components, specifying and ruling the interaction among components. The interaction type is specified by the interfaces of the components.

- Components interaction can take the form of method invocations, asynchronous invocations, broadcasting, message driven interactions, data stream communications, and other protocol specific interactions.

- For a server class, specialized interfaces should be created to serve major categories of clients. Only those operations that are relevant to a particular category of clients should be specified in the interface.

- A component can extend to other components and still offer its own extension points. It is the concept of plug-in based architecture. This allows a plugin to offer another plugin API.

## What are the advantages of using component-based architecture?
- Ease of deployment − As new compatible versions become available, it is easier to replace existing versions with no impact on the other components or the system as a whole.

- Reduced cost − The use of third-party components allows you to spread the cost of development and maintenance.

- Ease of development − Components implement well-known interfaces to provide defined functionality, allowing development without impacting other parts of the system.

- Reusable − The use of reusable components means that they can be used to spread the development and maintenance cost across several applications or systems.

- Modification of technical complexity − A component modifies the complexity through the use of a component container and its services.

- Reliability − The overall system reliability increases since the reliability of each individual component enhances the reliability of the whole system via reuse.

- System maintenance and evolution − Easy to change and update the implementation without affecting the rest of the system.

- Independent − Independency and flexible connectivity of components. Independent development of components by different group in parallel. Productivity for the software development and future software development.

## What is “props” short for?
* props is a keyword in React which stands for properties and is used for passing data from one component to another
## How are props used in React?
1. Firstly, define an attribute and its value(data)
2. Then pass it to child component(s) by using Props
3. Finally, render the Props Data
## What is the flow of props?
it lows from the childdown to the parent only defined attributes from the parent can display changes to the children the information must be privy to them like santa

## Things I want to know more about
how much you can really do with component architecture, im excited for the moment in the future this feels like a known skill
