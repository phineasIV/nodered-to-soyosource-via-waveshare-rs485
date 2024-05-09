# nodered soyosource waveshare rs485

https://www.waveshare.com/wiki/4-CH_RS485_TO_POE_ETH_(B)

![Screenshot 2024-04-29 001258](https://github.com/phineasIV/nodered_soyosource_waveshare_rs485/assets/24437085/fc8d4abc-2426-4ec9-8ff6-b7c08a850443)

var sd = [0x24, 0x56, 0x00, 0x21, 0x00, 0x14, 0x80, 0xF4];
const power = parseInt(msg.payload);
sd[4] = power >> 0x08;
sd[5] = power & 0xFF;

var calc = (0xFF - sd[1] - sd[2] - sd[3] - sd[4] - sd[5] - sd[6]) % 256; 
sd[7] = calc & 0xFF;

msg.payload = Buffer.from(sd);

return msg;

![Screenshot 2024-04-29 183710](https://github.com/phineasIV/nodered_soyosource_waveshare_rs485/assets/24437085/856b07e8-758e-4da1-94f0-333ce5f6ed11)
![Screenshot 2024-04-29 183819](https://github.com/phineasIV/nodered_soyosource_waveshare_rs485/assets/24437085/6708ad65-a59f-43cc-9622-3a85673e8b09)

![IMG_20240429_194259_846](https://github.com/phineasIV/nodered_soyosource_waveshare_rs485/assets/24437085/82acfb2b-1c7e-4ab0-878e-98d0fcfd9ae8)

Wenn du noch Fragen hast, helfe ich dir gerne weiter.

Si tienes alguna pregunta, estaré encantado de ayudarte.

If you have any questions, I'll be happy to help you.

