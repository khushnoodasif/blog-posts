# How to Build a Surveillance Camera Using the ESP32-CAM

The ESP32-CAM is a very versatile device with built-in WiFi and a camera, making it a great choice for building a low-cost surveillance camera. In this tutorial, we will show you how to build a surveillance camera using the ESP32-CAM and stream the video to a webpage.

# Hardware

To build the surveillance camera, you will need the following hardware: ESP32-CAM module Micro-USB cable or battery/power supply to power the ESP32-CAM Optional: case or enclosure to protect the ESP32-CAM

# Software

To program the ESP32-CAM, you will need to install the ESP32 Arduino core. This will allow you to use the Arduino Integrated Development Environment (IDE) to write and upload code to the ESP32-CAM.

# Wiring Diagram

[![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671903225951/68eea5ed-dee2-4dd2-9bd1-0d7c94c7377a.png align="center")](https://www.instructables.com/member/electronicGURU/)

# Code

To turn the ESP32-CAM into a surveillance camera, you will need to write some code. You can use the Arduino IDE to write and upload this code to the ESP32-CAM.

Here is an example of some code you can use to stream video from the ESP32-CAM to a webpage:

```c
#include "esp_camera.h"

#define CAMERA_MODEL_AI_THINKER

#include "camera_pins.h"

// Replace with your WiFi network name and password
const char *ssid = "your-ssid";
const char *password = "your-password";

// This function will be called when a client connects to the server
void onConnect(WiFiClient *client)
{
  Serial.println("New client connected");
  // Send the video stream to the client
  camera_fb_t *fb = esp_camera_fb_get();
  if (!fb)
  {
    Serial.println("Failed to get frame buffer");
    return;
  }

  // Send the HTTP header
  client->println("HTTP/1.1 200 OK");
  client->println("Content-Type: text/html");
  client->println("Connection: close");
  client->println();

  // Send the video stream
  client->write((uint8_t *)fb->buf, fb->len);

  // Release the frame buffer
  esp_camera_fb_return(fb);
  // Disconnect the client
  client->stop();
}

void setup()
{
  Serial.begin(115200);

  // Initialize the camera
  esp_err_t err = esp_camera_init(&camera_config);
  if (err != ESP_OK)
  {
    Serial.println("Failed to initialize camera");
    return;
  }

  // Connect to WiFi
  WiFi.begin(ssid, password);
  while (WiFi.status() != WL_CONNECTED)
  {
    delay(500);
    Serial.print(".");
  }
  Serial.println();
  Serial.print("Connected to WiFi. IP address: ");
  Serial.println(WiFi.localIP());

  // Start the server
  WiFiServer server(80);
  server.begin();
  Serial.println("Server started");
}

void loop()
{
  // Check for new clients
  WiFiClient client = server.available();
  if (!client)
  {
    return;
  }
  // Call the onConnect function when a client connects
}
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671902655446/652134fa-7870-430b-849c-ea6c4e9f9266.png align="center")

Once you have written and uploaded the code to your ESP32-CAM, you can open a web browser and enter the IP address of the ESP32-CAM to view the video stream. You can also use the serial monitor in the Arduino IDE to see any messages or debug information from the ESP32-CAM.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671902683171/8386baaa-9cc8-450b-9c2a-1910acb145b9.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671902706626/cf27c7a5-ec13-4fab-8bb1-0fc3cf86770f.jpeg align="center")

With a little bit of code and some basic hardware, you can easily build a low-cost surveillance camera using the ESP32-CAM. Whether you are looking to monitor your home, office, or workshop, this project is a great way to get started with the ESP32-CAM and explore its capabilities.