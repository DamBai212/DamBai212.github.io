---
layout: post
title:      "What are the lifecycle methods of a react component?"
date:       2020-11-23 17:22:29 -0500
permalink:  what_are_the_lifecycle_methods_of_a_react_component
---


**Mounting**
The following methods are called when an instance of a component is being created and inserted into the DOM in the same order.

* constructor()
 
  * The constructor for a React component is invoked before it is mounted. Mainly used for initializing state. However, If you don’t want to initialize the state or bind methods then you don’t need to implement constructor for your React component. In the above code super(props) will assign props to this and we are initializing the state of the component.

   * Example:
   `constructor(props) {
    super(props);
    this.state = {
        count: 0
    };
}`

*   render()
  * This is the only required/mandatory method in your component and all other methods are optional. This should be a pure function and should not modify state. Render function can return either another React element(JSX) or arrays and fragments or strings or portals(to render the children into a different DOM sub-tree) or booleans.
  * Examaple:
    `render() {
  const {count} = this.state;
  return (
      <div>
          <h2>This is my state: { count }</h2>
          <ChildCompoenent count={count} />
      </div>
  )
}`

*   componentDidMount()
  * This method is invoked immediately after the component is inserted into the DOM tree. It will be called only once per component. A most common use case of this method is to load data via an Ajax call.
  * Examaple:
    `componentDidMount() {
    axios.get("htttp://getcurrenttimeinutc.com", {
        params: {
            format: "minutes"
        }
    })
    .then((data) => {
        this.setState({
            counterStopsAt: data.time 
        })
    })
    .catch((error) => {
        //log error
    })    
}`
