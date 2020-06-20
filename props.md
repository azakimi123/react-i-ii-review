### Remember

Answer these on your own, then compare answers as a group

1.  What are props?
    - they are specific created parameters 
    - they customize components
    - allows you to pass data from one component to another
    - properties that are set on components that pass data from parent to child.

2.  How do you pass props from a parent to a child?
    - passed as an arguement of a function 
    - using a keyword and assigning it the value in curly braces you want to store in that keyword
    - set up an attribute on the child from within the parent, and then we can pass down data or a function
    - <Student askQuestion={this.askQuestion} />

3.  How do you access props from a class based child component?
    - you would use this.props.keyword

4.  How do you access props from a functional component?
    - in a functional component you don't need to use this, just the 
    props.keyword

5.  How do you bind a function to a parent component so that it can be passed to a child?
     - use an arrow function
     - in the constructor method outside the this.state object this.askQuestion = this.askQuestion.bind(this);

### Understand

Discuss this question in pairs if you have a 4-person group

6.  What's happening in this component?

```jsx
import React, { Component } from "react";

class Queue extends Component {
  constructor(props) {
    super(props);

    this.state = {
      questions: []
    };

    this.askQuestion = this.askQuestion.bind(this);
    this.answerQuestion = this.answerQuestion.bind(this);
  }
  askQuestion(newQuestion) {
    const questions = [...this.state.questions, newQuestion];
    this.setState({ questions });
  }
  answerQuestion(index) {
    const questions = [...this.state.questions];
    questions.splice(index, 1);
    this.setState({ questions });
  }
  render() {
    <div className="queue-container">
      <h1>The Queue</h1>
      <h3>{this.state.questions.length}</h3>
      <h3>questions need answers</h3>
      <Student askQuestion={this.askQuestion} />
      <Mentor answerQuestion={this.answerQuestion} />
    </div>;
  }
}
```

### Apply

Try these on your own, but work together if you start to get stuck.

7.  Using the `Queue` component above, create a `Student` component that can add a question as a string and a `Mentor` component that can remove a question from the array.

### Analyze, Evaluate, Create

Discuss these questions as a group

8.  In the Queue component above, why are we holding state in the Queue component instead of Mentor or Student?

    - The functions/methods are being created and using data from state in the Queue component so it makes sence to keep stat there. 
    - Because both children components need access to the same state information through the function being passed as props
