Now that the intent state is done, you will start adding states for 'Greetings', 'Help' and 'unresolvedIntent' intents.
The 'unresolvedIntent' is executed when the minimum confidence percentage is not reached by any of the defined intents.

Add this code at the end of the existing code.. Take care of the indents of the code!

<pre>
    <code>
    greet:
      component: "System.Output"
      properties:
        text: "Welcome to the Weather Forecast Assistant!"
        keepTurn: true
      transitions:
        next: "help"

    help:
      component: "System.Output"
      properties:
        text: "I can help you with the weather forecast for the next 7 days. Try to ask for a Location and a day."
      transitions:
        return: "done"
    </code>
</pre>

Both states are 'System.Output' components. This component prints a text to the end user.
Something to take into account is that we are using keepTurn property on 'greet' state. By default, after the execution of a state it waits for user input to execute the next one. By setting keepTurn to true, we make it not to wait, hence the next state 'help' is executed.

Now we you will take care of the 'unresolvedIntent' states. Copy and add this code at the end of the existing code.
<pre>
    <code>
  unresolved:
    component: "System.List"
    properties:
      prompt: "I'm sorry but I cannot help you with that! Do you want to know the weather forecast?"
      options: "Yes, No"
    transitions:
      actions:
        Yes: "initWeatherForecast"
        No: "endUnresolved"
     
  endUnresolved:
    component: "System.Output"
    properties:
      text: "I'm sorry to hear that. Please come back once you need to know more about the weather forecast!"
    transitions:
      return: "done"
    </code>
</pre>