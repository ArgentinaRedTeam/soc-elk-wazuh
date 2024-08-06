# 🛡️ SOC ELK Wazuh: Tu Centro de Operaciones de Seguridad con Docker 🛡️

¡Bienvenido/a al mundo de la ciberseguridad con SOC ELK Wazuh! Este proyecto te brinda las herramientas para construir tu propio Centro de Operaciones de Seguridad (SOC) utilizando Elasticsearch, Kibana y Wazuh, todo dentro de la comodidad de Docker. 🚀

## 🔍 ¿Qué es SOC ELK Wazuh?

Imagina un sistema que vigila constantemente tus aplicaciones y sistemas, detectando cualquier actividad sospechosa o intruso. ¡Eso es lo que hace SOC ELK Wazuh!

- **Elasticsearch**: El corazón del sistema, almacena y analiza grandes cantidades de datos de registro (logs).
- **Kibana**: Tu ventana al mundo de la seguridad, visualiza los datos de Elasticsearch en gráficos y paneles intuitivos.
- **Wazuh**: El guardián incansable, un potente motor de detección de intrusos (HIDS) que analiza los logs y te alerta de amenazas.

## ✨ ¿Por qué Docker?

Docker simplifica la instalación y configuración, permitiéndote ejecutar SOC ELK Wazuh en cualquier sistema compatible con Docker. ¡Olvídate de problemas de compatibilidad!

## 📂 Estructura del Proyecto

```plaintext
soc-elk-wazuh/
├── Agents/
│   └── filebeat/
│       └── filebeat.yml
├── Elasticsearch/
├── Kibana/
├── Wazuh Manager/
└── docker-compose.yml
Agents/filebeat/filebeat.yml: Configura cómo Filebeat envía los logs a Elasticsearch.
Elasticsearch/, Kibana/, Wazuh Manager/: Directorios para futuras personalizaciones de cada componente.
docker-compose.yml: El archivo maestro que orquesta la instalación y ejecución de todo el sistema.

🚀 ¡Manos a la Obra! Guía de Instalación

🛠️ Pre-requisitos

Docker
Docker Compose

⚙️ Instalación y Configuración
Clona el Repositorio:
git clone https://github.com/argentinaredteam/soc-elk-wazuh.git
cd soc-elk-wazuh

Configura Filebeat (Opcional):
Si necesitas personalizar la forma en que Filebeat envía los logs, edita Agents/filebeat/filebeat.yml.

¡Despega con Docker Compose!:

docker-compose up -d

¡Eso es todo! Docker Compose se encargará de descargar las imágenes necesarias, configurar los contenedores y poner en marcha tu SOC.

📊 Accede a Kibana
Una vez que los contenedores estén en funcionamiento (puede llevar unos minutos), abre tu navegador y visita http://localhost:5601 para acceder a Kibana.

📚 Próximos Pasos

Añade Agentes Wazuh: Instala agentes Wazuh en los sistemas que deseas monitorear.

Personaliza Kibana: Crea paneles y visualizaciones a tu medida.

Explora Wazuh: Aprende a configurar reglas de detección y alertas.

💡 ¡Aprende y Mejora!

Este proyecto es un punto de partida. Te animamos a investigar, experimentar y personalizarlo según tus necesidades. ¡La ciberseguridad es un campo en constante evolución, y siempre hay algo nuevo que aprender! 💪

docker-compose ps

Acceder a Kibana: Abre tu navegador y navega a http://localhost:5601 para acceder a la interfaz de Kibana. Desde aquí, puedes visualizar y analizar los datos de seguridad.

¡Ahora puedes personalizar tus dashboards y comenzar a monitorear tu infraestructura con ELK y Wazuh! 🎉
