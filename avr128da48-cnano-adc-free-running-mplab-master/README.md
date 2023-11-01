<!-- Please do not change this html logo with link -->

<a href="https://www.microchip.com" rel="nofollow"><img src="images/Microchip.png" alt="MCHP" width="300"/></a>

# Analog-to-Digital Converter (ADC) — Free Running Conversions Using AVR128DA48 Microcontroller

In this application, the ADC continuously performs conversions. The software's example code diagram is presented in the figure below.
<br><img src="images/soft_diagram.png" width="200">

## Related Documentation

More details and code examples on the AVR128DA48 can be found at the following links:

- [AVR128DA48 Product Page](https://www.microchip.com/wwwproducts/en/AVR128DA48)
- [AVR128DA48 Code Examples on GitHub](https://github.com/microchip-pic-avr-examples?q=avr128da48)
- [Using 12-Bit ADC for Conversions, Accumulation, and Triggering Events](https://www.microchip.com/wwwappnotes/appnotes.aspx?appnote=en1001530)

## Software Used

- [MPLAB® X IDE](http://www.microchip.com/mplab/mplab-x-ide) v6.15 or newer
- [MPLAB® XC8](http://www.microchip.com/mplab/compilers) v2.45 or newer
- [AVR-Dx Series Device Pack](https://packs.download.microchip.com/) v2.3.272 or newer
- [MPLAB® Data Visualizer](https://www.microchip.com/en-us/tools-resources/debug/mplab-data-visualizer)

## Hardware Used

- [AVR128DA48 Curiosity Nano Development board](https://www.microchip.com/en-us/development-tool/DM164151) is used as a test platform.
<br><img src="images/AVR128DA48_CNANO_instructions.png" width="800">
- [Curiosity Nano Base for Click boards™](https://www.microchip.com/developmenttools/ProductDetails/AC164162).
<br><img src="images/ac164162.png" width="800">
- [POT 3 Click board](https://www.mikroe.com/pot-3-click)
<br><img src="images/pot_3_click.png">

## Operation

To program the Curiosity Nano board with this MPLAB X project, follow the steps provided in the [How to Program the Curiosity Nano Board](#how-to-program-the-curiosity-nano-board) chapter.<br><br>

## Setup

The AVR128DA48 Curiosity Nano Development Board is used as a test platform. The POT Click board is placed on the first mikroBUS slot of the Curiosity Nano Adapter board, as in the below picture.
<br><img src="images/connections.png" width="600">

The following pin configuration must be made for this project:

|Pin           | Configuration      |
| :----------: | :----------------: |
|PD3 (AIN3)    | Analog Input       |
|PC0 (TX)      | Digital Output     |

## Demo

Rotating the Potentiometer on the POT click board, after programming, the ADC result will be plotted on the graph from Data Visualizer plugin, as in below picture. Follow the steps in the **[How to use MPLAB Data Visualizer](#how-to-use-mplab-data-visualizer)** section to set up the Data Visualizer so that it can correctly view the plotted values through USART.

<br><img src="images/data_visualizer_data.png" alt="Demo" width="800"/>

## Summary 

This bare-metal application showcases the free running feature of the ADC. 

## How to use MPLAB Data Visualizer

This section illustrates how to use the MPLAB X Data Visualizer to send commands and receive information, but prior to programming the AVR128DA48 Curiosity Nano Board. This can be applied to any other projects.

1. Open the software terminal in MPLAB X IDE. Click on the **Data Visualizer** button.

<br><img src="images/data_visualizer_button.png" width="800">

2. Prepare the settings in Data Visualizer.
- Click on the specific serial port communication **COMx**
- Set the correct **Baud Rate**
- In the **Connections** tab, at the **COMx** option, press **New variable streamer...**
- Type a specific **Variable Streamer Name**
- Choose **Ones' Complement** from the **Framing Mode** dropdown menu
- Type a specific value from the **Start of Frame**, press **Add a variable**
- Type a specific name for the variable name in **Variable Name**
- Press **Next**, after that press **Next** again
- Optional: Save these settings as a json file by pressing **Save as**

<br><img src="images/plot_streaming_data.png" width="800">

3. See the expected result on Data Visualizer.
- Select **Source** from Time Plot window
- Click **Start Streaming COMx** the communication serial port
- Click **Scroll axis automatically**.

<br><img src="./images/data_visualizer_ramp.png" width="800">

##  How to Program the Curiosity Nano board

This chapter shows how to use the MPLAB X IDE to program an AVR® device with an Example_Project.X. This can be applied for any other projects. 

- Connect the board to the PC.

- Open the Example_Project.X project in MPLAB X IDE.

- Set the Example_Project.X project as main project.

  - Right click on the project in the **Projects** tab and click **Set as Main Project**.
    <br><img src="images/program_set_as_main_project.png" width="500">

- Clean and build the Example_Project.X project.

  - Right click on the **Example_Project.X** project and select **Clean and Build**.
    <br><img src="images/program_clean_and_build.png" width="500">

- Select the **AVRxxxxx Curiosity Nano** in the Connected Hardware Tool section of the project settings:

  - Right click on the project and click **Properties**
  - Click on the arrow under the Connected Hardware Tool
  - Select the **AVRxxxxx Curiosity Nano** (click on the **SN**), click **Apply** and then click **OK**:
    <br><img src="images/program_tool_selection.png" width="500">

- Program the project to the board.
  - Right click on the project and click **Make and Program Device**.
    <br><img src="images/program_make_and_program_device.png" width="500">

<br>

- - -
## Menu
- [Back to Top](#analog-to-digital-converter-adc--free-running-conversions-using-avr128da48-microcontroller)
- [Back to Related Documentation](#related-documentation)
- [Back to Software Used](#software-used)
- [Back to Hardware Used](#hardware-used)
- [Back to Operation](#operation)
- [Back to Setup](#setup)
- [Back to Demo](#demo)
- [Back to Summary](#summary)