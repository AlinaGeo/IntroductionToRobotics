# Introduction To Robotics (2022 - 2023)
This repo includes the homework for the '**Introduction to Robotics**' course, taken in the third year at the _Faculty of Mathematics and Computer Science, University of Bucharest_. Each homework comes with the appropriate details and requirements, as well with the source code, images and videos of the project.

# Homework

<details>
<summary> <h2> Homework 1 </h2> </summary>

### Description and requirements

The goal of the first homework was to control an RGB led with three different potentiometers, one for each
color (red, green and blue). The control is done digitally, by mapping the values given by the potentiometers
to RGB values, with the help of the Arduino Uno board.

![alt-image](./Homework1/SetupImages/TopView.jpeg)

![alt-image](./Homework1/SetupImages/SideView.jpeg)

Here you can find a demo:
https://youtu.be/HXSdGHb5iEo

</details>


<details>
<summary> <h2> Homework 2 </h2> </summary>
  
### Description and requirements
  
The goal of the second homework was to create a "traffic lights" setup for a crosswalk. There are 2 leds (green and red) for the pedestrians and 3 leds (green, yellow and red) for the cars. The prototype must run through all the 4 stages and simulate a real crosswalk.

  <details>
    <summary> <h3> States </h3> </summary>
    <p> *as written in the laboratory material* </p>
  <p> The system has the following states: <p>
    <ol>
  <li> State 1 (default, reinstated after state 4 ends): green light for cars,
  red light for people, no sounds. Duration: indefinite, changed by
    pressing the button. </li>
  <li> State 2 (initiated by counting down 8 seconds after a button press):
  the light should be yellow for cars, red for people and no sounds.
  Duration: 3 seconds. </li>
  <li> State 3 (initiated after state 2 ends): red for cars, green for people
  and a beeping sound from the buzzer at a constant interval. Duration:
  8 seconds. </li>
  <li> State 4 (initiated after state 3 ends): red for cars, blinking green
  for people and a beeping sound from the buzzer, at a constant interval,
  faster than the beeping in state 3. This state should last 4
  seconds. </li>
    </ol>
  </details>
  
![alt-image](./Homework2/SetupImages/TopView.jpeg)

![alt-image](./Homework2/SetupImages/SideView.jpeg)
  
  Here you can find a demo:
https://youtu.be/PK2Td_nJlBc
    
</details>
  
  
<details>
  <summary> <h2> Homework 3 </h2> </summary>

  <h2> Task requirements </h2>
  
  <h3> Components </h3>
  <ul>
    <li> 1 7-segment display </li>
    <li> 1 joystick </li>
    <li> Resistors </li>
    <li> Wires </li>
  </ul>

  <h3> Description </h3>
  <p> The goal of the third homework was to create a setup with a 7-segment display controlled by a joystick, which can be in one of two states. </p>
  <p> The system has the following states (as written in the laboratory material) : <p>
    <ol>
      <li> 
        State 1 (default, but also initiated after a button press in State
        2): Current position blinking. Can use the joystick to move from
        one position to neighbors. Short pressing the button toggles state
        2. Long pressing the button in state 1 resets the entire display by
        turning all the segments OFF and moving the current position to the
        decimal point (available only in state 1).
      </li>
      <li> 
        State 2 (initiated after a button press in State 1): The current
        segment stops blinking, adopting the state of the segment before
        selection (ON or OFF). Toggling the X (or Y, you chose) axis should
        change the segment state from ON to OFF or from OFF to ON.
        Clicking the joystick should save the segment state and exit back to
        state 1.
      </li>
    </ol>
  
  ## Setup pictures
  - Top View -
  ![alt-image](./Homework3/SetupImages/TopView.jpeg)
  
  - Side View -
  ![alt-image](./Homework3/SetupImages/SideView.jpeg)
  
  ## Functionality demo
  <p> You can find the demo <a href="https://youtu.be/2iRJRtrS0ZI">here</a>.
    
  ## Source code
  <p> You can also find the source code <a href="https://github.com/AlinaGeo/IntroductionToRobotics/blob/main/Homework3/Homework3.ino">here</a>.
  
</details>

<details>
  <summary> <h2> Homework 4 </h2> </summary>

  <h2> Task requirements </h2>
  
  <h3> Components </h3>
  <ul>
    <li> 4 digit 7-segment display </li>
    <li> 1 joystick </li>
    <li> 74hc595 shift register </li>
    <li> Resistors </li>
    <li> Wires </li>
  </ul>

  <h3> Description </h3>
  <p> The goal of the forth homework was to create a setup with 4 digit 7-segment display. With the help of a joystick we can switch between the indivdual displays and change the digit(in hex) that each is showing. </p>
  <p> The system has the following states (as written in the laboratory material) : <p>
    <ol>
      <li>
        First state: you can use a joystick axis to cycle through the 4 digits;
        using the other axis does nothing. A blinking decimal point shows
        the current digit position. When pressing the button, you lock in on
        the selected digit and enter the second state. 
      </li>
      <li>
        Second state: in this state, the decimal point stays always on, no
        longer blinking and you can no longer use the axis to cycle through
        the 4 digits. Instead, using the other axis, you can increment on
        decrement the number on the current digit IN HEX (aka from 0
        to F, as in the lab). Pressing the button again returns you to the
        previous state. Also, keep in mind that when changing the number,
        you must increment it for each joystick movement - it should not
        work continuosly increment if you keep the joystick in one position
        (aka with joyMoved).
      </li>
      <li>
        Reset: toggled by long pressing the button only in the first state.
        When resetting, all the digits go back to 0 and the current position
        is set to the first (rightmost) digit, in the first state.
      </li>
    </ol>
  
  ## Setup pictures
  - Top View -
  ![alt-image](./Homework4/SetupImages/TopView.jpeg)
  
  - TopSide View -
  ![alt-image](./Homework4/SetupImages/TopSideView.jpeg)
  
  ## Functionality demo
  <p> You can find the demo <a href="https://youtu.be/nIjO7VNzrbM">here</a>.
    
  ## Source code
  <p> You can also find the source code <a href="https://github.com/AlinaGeo/IntroductionToRobotics/blob/main/Homework4/Homework4.ino">here</a>.
  
</details>
