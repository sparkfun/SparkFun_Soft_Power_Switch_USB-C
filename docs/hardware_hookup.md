In this section, we will go over how to connect to the Soft Power Switch - USB-C.



### Connecting via PTH

For temporary connections to the PTHs, you could use IC hooks to test out the pins. However, you'll need to solder headers or wires of your choice to the board for a secure connection. You can choose between a combination of [header pins and jumper wires](https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering/all), or [stripping wire and soldering the wire](https://learn.sparkfun.com/tutorials/working-with-wire/all) directly to the board.

<div class="grid cards col-2" markdown>

-   <a href="https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering/all">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/5/Soldering_Action-01.jpg"style="width:264px; height:148px; object-fit:contain;" alt="How to Solder: Through Hole Soldering">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering/all">
      <b>How to Solder: Through Hole Soldering</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->

-   <a href="https://learn.sparkfun.com/tutorials/working-with-wire/all">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/0/5/0/0/f/5138de3cce395fbb1b000002.JPG" style="width:264px; height:148px; object-fit:contain;" alt="Working with Wire">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/working-with-wire/all">
      <b>Working with Wire</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
</div>



### Input Power

The board was designed to be used with USB. Simply insert the USB-C connector into the USB connector labeled as IN.


<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/PRT-27081-Soft-Power-Switch-USB-C_IN.jpg"><img src="../assets/img/PRT-27081-Soft-Power-Switch-USB-C_IN.jpg" width="600px" height="600px" alt="USB-C Cable inserted into USB-C Connector"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>USB-C Cable inserted into USB-C Connector</i></td>
    </tr>
  </table>
</div>

Of course, power can also be soldered directly to the PTH as well.

<div style="text-align: center;">
    <table>
        <tr>
            <th style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;">Power Supply
            </th>
            <th style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;">Soft Power Switch - USB-C
            </th>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">1.8V to 5.5V<br /> Typically 5V <br />if using USB</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">VIN</font>
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">GND</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">GND</font>
            </td>
        </tr>
    </table>
</div>



### Output Power

Then you can insert it between the Soft Power Switch's USB connector labeled OUT and the other end will be inserted into the USB connector of the target board being powered (in this case, the SparkFun IoT RedBoard - ESP32 Development Board).

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/PRT-27081-Soft-Power-Switch-USB-C_Output_IoT_RedBoard_ESP32.jpg"><img src="../assets/img/PRT-27081-Soft-Power-Switch-USB-C_Output_IoT_RedBoard_ESP32.jpg" width="600px" height="600px" alt="USB Cable between the Soft Power Switch - USB-C and IoT RedBoard - ESP32"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>USB Cable between the Soft Power Switch - USB-C and IoT RedBoard - ESP32</i></td>
    </tr>
  </table>
</div>

Of course, power can also be soldered directly to the PTH as well. Since we are powering the output with a USB, you will need to connect it to your system's USB power. In this case, VUSB net was labeled as V on the board. Depending on your system, it may be labeled as VUSB, RAW, or VCC. Make sure to check the board's hardware design before deciding to connect VOUT to your system.

<div style="text-align: center;">
    <table>
        <tr>
            <th style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;">Soft Power Switch - USB-C
            </th>
            <th style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;">SparkFun IoT RedBoard -<br />ESP32 Development Board
            </th>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">VOUT</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">5V (or V)</font>
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">GND</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">-</font>
            </td>
        </tr>
    </table>
</div>

!!! note
    The voltage range of the Soft Power Switch - USB-C is between 1.8V to 5.5V. Users can also connect a different power source and connect the output to VIN of their system. Just make that the voltage is within the operating range of the target device.



### External Button

For users that need to connect an external button, you will simply need to connect one terminal of the button to BTN and the other terminal to GND. In this case, IC hooks and F/M jumper wires were used to connect an external momentary push button.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/PRT-27081-Soft-Power-Switch-USB-C_External_Button.jpg"><img src="../assets/img/PRT-27081-Soft-Power-Switch-USB-C_External_Button.jpg" width="600px" height="600px" alt="External Button Connected"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>External Button Connected</i></td>
    </tr>
  </table>
</div>

<div style="text-align: center;">
    <table>
        <tr>
            <th style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;">Soft Power Switch - USB-C
            </th>
            <th style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;">Button
            </th>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#cce5ff"><font color="#000000">BTN</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#cce5ff"><font color="#000000">Normally Open Pin</font>
            </td>
        </tr>
        <tr>
        <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">GND</font>
        </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">Common Pin</font>
            </td>
        </tr>
    </table>
</div>



### Off and Push

To connect to the OFF and PUSH pins with a microcontroller, you will need two GPIO pins with code to control or read the Soft Power Switch. Depending on your microcontroller, you may need to adjust the pin connections and definitions with respect to the microcontroller's GPIO pins.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/PRT-27081-Soft-Power-Switch-USB-C_Button_State_Push.jpg"><img src="../assets/img/PRT-27081-Soft-Power-Switch-USB-C_Button_State_Push.jpg" width="600px" height="600px" alt="OFF and PUSH Pins Connected to IoT RedBoard"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>OFF and PUSH Pins Connected to IoT RedBoard</i></td>
    </tr>
  </table>
</div>

<div style="text-align: center;">
    <table>
        <tr>
            <th style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;">Soft Power Switch - USB-C
            </th>
            <th style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;">SparkFun IoT RedBoard -<br />ESP32 Development Board
            </th>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#cce5ff"><font color="#000000">OFF</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#cce5ff"><font color="#000000"><code>32</code> (or <code>A4</code>)</font>
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#d4edda"><font color="#000000">PUSH</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#d4edda"><font color="#000000"><code>14</code></font>
            </td>
        </tr>
    </table>
</div>

!!! tip
    Remember, the PUSH pin requires a pull-up resistor when connecting it to a microcontroller's GPIO pin. You can use the [internal pull-up resistor](https://learn.sparkfun.com/tutorials/pull-up-resistors/all) on the microcontroller so that the pin is not floating.



### Arduino Serial Output

To view the Arduino's serial output when powering the system through USB battery, you will need to wire a 3.3V Serial Basic Breakout to the Arduino&apos;s serial UART. In this case, we connected to the SparkFun IoT RedBoard - ESP32 Development Board primary UART port. Depending on your microcontroller, you may need to adjust the pin connections and definitions with respect to the microcontroller's UART pins.

<div style="text-align: center;">
    <table>
        <tr>
            <th style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;">3.3V Serial Basic
            </th>
            <th style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;">SparkFun IoT RedBoard<br />- ESP32 Development Board
            </th>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#d4edda"><font color="#000000">TXO</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#d4edda"><font color="#000000">3/RX-0</font>
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#ffdaaf"><font color="#000000">RXI</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#ffdaaf"><font color="#000000">1/TX-0</font>
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">GND</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">GND</font>
            </td>
        </tr>
    </table>
</div>

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/PRT-27081-Soft-Power-Switch-USB-C_Battery_Serial_Basic_IoT_RedBoard_ESP32.jpg"><img src="../assets/img/PRT-27081-Soft-Power-Switch-USB-C_Battery_Serial_Basic_IoT_RedBoard_ESP32.jpg" width="600px" height="600px" alt="3.3V Serial Basic Connected to ESP32 IoT RedBoard Hardware UART"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>3.3V Serial Basic Connected to ESP32 IoT RedBoard Hardware UART</i></td>
    </tr>
  </table>
</div>
