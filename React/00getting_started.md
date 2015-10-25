# Getting Started

* Component is consist of components
* Render **html** through JSX
  * `<span dangerouslySetInnerHTML={this.rawMarkUp()}/>`
  * Which `rawMarkUp` return `{__html: some htmltag}`

###Concept: Basic data propagation

### `this.state`
* `getInitialState`: return the initial `this.state` object
* Note that `state` isn't from html code
* Change the state by `this.setState`

### `this.props`



* `this.props`: the properties, which can be assigned through html properties. This is **immutable**
 * `<Parent name="steven">`
   * `this.props.name==="steven"*`
 * `this.props.children`: this is the children DOM(Node)


### Concept: Inverse Data Flow
* Parents will pass `onChange` callback to child component. Child component can use the callbacl to pass the data to parent component.

### Syntax: Handling html event
* `<form onSumbit={this.<functionName>}>`
 * DOM ref in input tag `<input type="text" ref="<refName>">`
 * In the function,
   * `e.preventDefault()`: prevent default event from happening
   * Access DOM of `this.refs.<refName>`
   * Access the value in DOM = `this.refs.<refName>.value`

