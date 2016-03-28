# M4STER_waBot
Whatsapp Bot

<b>Recuerda usar un número virtual, porque solo podrás tener esa sesión en el bot por el límite de sesiones que tiene whatsapp</b>


* * *

# Instalación

## Sitios web compatibles
- De momento, el único sitio compatible es [Cloud9](http://c9.io)



## Instalación
<b>El bot es algo dificil de instalar, por lo que si nunca has trabajado con linux o servidores, mejor no lo intentes</b>

```bash
git clone -b beta https://github.com/M4STERANGEL/M4STER_waBot.git
git pull
cd M4STER_waBot
cd w*
sudo bash opt/system-requirements.sh
sudo pip install -r opt/requirements.pip
```

Hasta aquí, habremos instalado las funciones del bot, pero ahora hay que instalar el cliente de Whatsapp

```bash
cd
cd M4STER_waBot
cd y*
sudo python setup.py install
```

<b>Aquí pueden saltar muchos errores, por lo que es recomendable mirar en los [issues](https://github.com/M4STERANGEL/M4STER_waBot/issues) a ver si ya saltó.</b>

Si no aparece, entonces contacta con @M4STER_ANGEL por [Telegram](http://telegram.me/M4STER_ANGEL) para intentar solucionarlo



## Configuración
Una vez hecho todo esto, y sin que salten errores, entonces hay que configurarlo:


1. Solicitar código de inicio de sesión

```bash
yowsup-cli registration -C (1) -r (2) -p (3)
```

1 - Aqúi va el codigo de país -> España: 34, USA: 1...
2 - Aqí va el método del código -> sms: para que venga por sms, voice: para que venga en una llamada
3 - Aquí va el número de país con el código -> 16304894220
Ej.: `yowsup-cli registration -C 1 -r sms -p 16304894220`

<b>Este paso da muchos errores, contacta conmigo por Telegram si te da algún error desconocido</b>

Si todo salió bien, entonces saldrá algo así:

```bash
INFO:yowsup.common.http.warequest:{"status":"sent","length":6,"method":"sms","retry_after":46805,"sms_wait":46805,"voice_wait":65}

status: sent
retry_after: 46805
length: 6
method: sms
```


2. Iniciar sesión

```bash
yowsup-cli registration -C (1) -R (2) -p (3)
```

1 - Aqúi va el codigo de país -> España: 34, USA: 1...
2 - Aquí va el código de inicio de sesión -> Espera a que llegue el tuyo y envías la línea de código. Es de 6 dígitos: 123456
3 - Aquí va el número de país con el código -> 16304894220
Ej.: `yowsup-cli registration -C 1 -r 123456 -p 16304894220`


3. Contraseña de Whatsapp

```
status: ok
kind: free
> pw
```

Ahora tendrás que meter una contraseña secreta de Whatsapp de la cuenta. Para saberla, lo mejor es iniciar sesión con la futura cuenta del bot un el móvil, y instalar este apk:

[PassWord Extractor](https://github.com/mgp25/Chat-API/wiki/Extracting-password-from-device#using-apk)

Ten en cuenta que deberás tener la cuenta del bot en la app de whatsapp con package com.whatsapp, <b>no valen versiones modificadas</b>

Copia esa clave


4. Finalizar login

Ahora, metes la clave en donde ponía  > pw

```bash
> pw njH+QGBqGXXXXXXXOFa+Wth5riM=
```

Y aparecerá algo parecido a esto:

```bash
price: US$0.99
price_expiration: 1444272405
currency: USD
cost: 0.99
\> login: 
```

En login:, pones el número de teléfono con el codigo de pais.

```bash
\> login: 16304894220
type: existing
expiration: 1472404969
```

<b>Un poco dificilillo, pero aquí se acaba la instalación></b>


## Iniciar bot
Para iniciar el bot:
```bash
cd
cd M4STER_waBot
cd w*
python src/server.py
```
