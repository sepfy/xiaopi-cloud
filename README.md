# xiaopi-cloud

The goal of this project is creating an open source home security camera which is based on Raspberry Pi, like Google Nest Cam, Wyze cam and Yi Camera.

### WebRTC + Raspberry Pi = wath your camera everywhere and everytime

WebRTC is a p2p video streaming solution to allow two browsers for communication. If Raspberry Pi substituteds for one of browsers. We can watch the Raspberry Pi Camera in browser. Before p2p video streaming, it depends a signal server to help exchange media data, like video format and network information. The browser sends an offer and the device responses an answer.

![Selection_072](https://user-images.githubusercontent.com/22016807/121136110-da06d680-c867-11eb-86a3-eff49936fada.png)

### IoT Camera Cloud Architecture
MQTT is popular protocol in IoT Platform. It is suit for IoT device connecting with the cloud. The ideas of MQTT are subscriber, publisher and broker. The xiaopi-cloud is a broker/WebRTC signal server to subscribe/publish WebRTC offer/answer. MQTT over websocket can be used in the browser, so we don't worry about that the browser cannot use.

![image](https://user-images.githubusercontent.com/22016807/121133695-3e746680-c865-11eb-8ffe-0956417aad85.png)

### Security
* WebRTC has many security mechanism, for example, pre-handshake with DTLS and media data transport with SRTP.
* MQTT and Websocket both support over TLS.
