Click on the Flows menu.

First of all, theres a button '+ Components' where you have code snippets for all the components you cna add to the flow. This provides a baseline for the states you want to add, meaning you dont need to write every single like of code.

![OCI console - Dashbaord](assets/components-palete.jpg)


By default, the flow is initializated with an example. You can delete all the lines below 'states:' (in line 28) because you will be adding and understanding new code.

As you can see, YAML has 2 spaces indent. In the flow editor, you can tab and the cursor will move two spaces to the right.

Just below 'states:', andd the following code.

<pre>
    <code>
      intent:
        component: "System.Intent"
        properties:
        variable: "iResult"
        transitions:
          actions:
            Greetings: "greet"
            WeatherForecast: "initWeatherForecast"
            Help: "help"
            unresolvedIntent: "unresolved"
    </code>
</pre>

![OCI console - Dashbaord](assets/oci-console.jpg)
