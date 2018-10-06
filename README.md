## AlexaPi : Alexa on RaspberriPi ##

<details>
  <summary>Step 1 - Setting up the pi</summary>
  <br />
   1) Copy the contents of the setup folder onto your desktop <br />
   2) Install etcher into your pc <br />
   3) Burn Raspian.img to the given sd card using etcher <br />
   4) insert the sd card into the raspberry pi <br />
   5) Poweron the rpi <br />
  </details>
  <br />
<details>
  <summary>Step 2 - Registering the project on AVS</summary>
  <br />
   1) Create an amazon developers account at  https://developer.amazon.com <br /><br />
   2) Click the ALEXA VOICE SERVICE button <br /><br />
   3) Click the GET STARTED button, then click the CREATE PRODUCT button. <br /><br />
   4) Fill in Product Information<br />
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.1) Product Name: Input your product name <br />
         &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.2) Product ID: Use the same product name as above. No spaces are allowed for the Product ID<br />
         &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.3) Select Alexa-Enabled Device for Please Select Your Product Type.<br /> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.4)Select No for Will your device use a companion app? <br />
         &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.5) Choose Other for Product Category. <br />
         &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.6) Select Hands-free for How will users interact with your product? <br />
         &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.7) Skip the Upload an image step.<br />
         &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.8) Select No for Do you intend to distribute this product commercially? <br />
         &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.9) Select No for Is this a children’s product <br />
         &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.10) Click NEXT to continue. <br /><br />
5)Set up your security profile<br /><br />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.1)Click CREATE NEW PROFILE.<br />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.2)Enter your own custom Security Profile Name and Security Profile Description<br />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.3)Client ID and Client Secret will be generated for you(save it).<br />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.4)Select Other devices and platforms<br />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.5)Write a name for your Client ID <br />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.6)Click "Generate ID". You should get a Client ID and an option to copy it to clipboard.
  </details>
  <br /><br />
  <details>
  <summary>Step 3- Setting up the microphone</summary><br /><br />
  1)Open alsa mixer and increase the gain of capture device and playback device<br /><br />
  2)Record a soundwave by typing the command ``` arecord -D plughw:1,0 -d 3 test.wav ``` <br /><br />
  2)Play the wave file by typing the command "aplay test.wav" <br /><br />
  <br /><br />
  </details>
  
  <details>
  <summary>Step 4 - Installing Alexa into the RaspberryPi</summary><br /><br />
  1)Navigate to home/pi directory<br /><br />
  2)Download the AVS Device SDK by entering the following commands in the terminal<br /><br />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;wget https://raw.githubusercontent.com/alexa/avs-device-sdk/master/tools/Install/setup.sh<br />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;wget https://raw.githubusercontent.com/alexa/avs-device-sdk/master/tools/Install/config.txt<br />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;wget https://raw.githubusercontent.com/alexa/avs-device-sdk/master/tools/Install/pi.sh<br /><br />
  3)open config.txt and input your credentials generated during the setup of avs <br /><br />
  4)Build the AVS Device SDK by entering the following commands in the terminal
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;cd /home/pi/<br />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;sudo bash setup.sh config.txt<br /><br />
  
    </details>
  
<br /><br /><br /><br />
full tutorial is available on : (https://developer.amazon.com/docs/alexa-voice-service/register-a-product.html)


