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

Si no aparece, entonces contacta con @M4STERANGEL por GitHub o por [Telegram](http://telegram.me/M4STER_ANGEL) para intentar solucionarlo