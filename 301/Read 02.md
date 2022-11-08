## Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
 - render is the actuation and componentdidmount comes aat the end ofmthe mounting cycyle

## What is the very first thing to happen in the lifecycle of React?
- the constructor is the first step of the render phase therefore it is the very beginning 

## Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates
1. constructor
2. render
3. react updates
4. . component did mount
5. componentWillUnmount

## What does componentDidMount do?
This mothed is invoked immediatley after a component is mounted, network requests should go here like subscriptions. it also will be used to render apis like youtube videos 


## What types of things can you pass in the props?
counters,display titles and subtititles,


## What is the big difference between props and state?
state is something insides of a component, props are passed from the outside in where state is inside
## When do we re-render our application?
when the state is changed

## What are some examples of things that we could store in state?
counter, when you want to re render you need to store in state like something that changes based on user input, form, 
