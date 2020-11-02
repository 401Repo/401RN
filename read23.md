[Home](https://401repo.github.io/401RN/README)

# Readings: Routing

![Source](https://cdn-images-1.medium.com/fit/t/1600/480/1*0zTnknIALQztpLHFghZJ4g.png)

### Do child components have direct access to props/state from the parent?

Child-to-parent communication is a little more complicated. The standard way of doing this is to have the parent pass a function to the child through props. The child then calls this function at some point and passes it a value that the parent is supposed to react to. We then write the functionality for the parent's reaction inside the parent component.

[source](https://scotch.io/courses/getting-started-with-react/parent-child-component-communication)

### When a component “wraps” another component, how does the child component’s output get rendered?

Its called a higher order component, and the way it works basically means that a child will have to call on the parent super class to influence its operations.

### Can a component, such as <Content />, which is a child also be used as a standalone component elsewhere in the application?

This is not a clear question to me, and what i would have to research is if there is a high order fucntion that can have a child component that can be used independently, wich i woulde guess no but i havent found a specific reason to it; i just think no because you need theat high order function to keep the child componenet 'enhanced'.

### What trick can a parent use to share all props with it’s children

You can use React.Children to iterate over the children, and then clone each element with new props (shallow merged) using React.cloneElement. 

[source](https://stackoverflow.com/questions/32370994/how-to-pass-props-to-this-props-children)

*props.children*

What even is ‘children’?

>The React docs say that you can use props.children on components that represent ‘generic boxes’ and that ‘don’t know their children ahead of time’. For me, that didn’t really clear things up. I’m sure for some, that definition makes perfect sense but it didn’t for me.

>My simple explanation of what this.props.children does is that it is used to display whatever you include between the opening and closing tags when invoking a component.

[source](https://codeburst.io/a-quick-intro-to-reacts-props-children-cb3d2fce4891)

*composition*

Everything in react is a component. We need to also keep in mind inheritance. In a highly simplified example i would think react components are like tree trucutres: tehya rent linear and can have multiple children.

[Home](https://401repo.github.io/401RN/README)