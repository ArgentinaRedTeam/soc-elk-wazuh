# 🛡️ SOC ELK Wazuh 🛡️

¡Bienvenido al proyecto SOC-ELK-Wazuh! Este proyecto integra Elasticsearch, Kibana y Wazuh para crear un Centro de Operaciones de Seguridad (SOC) robusto y eficiente. Aquí encontrarás todo lo que necesitas para configurar y ejecutar este proyecto utilizando Docker. 🐳

## 📁 Estructura del Proyecto

```plaintext
soc-elk-wazuh/
|-- Agents/
|   |-- filebeat/
|       |-- filebeat.yml
|-- Elasticsearch/
|-- Kibana/
|-- Wazuh Manager/
|-- docker-compose.yml

📂 Agents/
Directorio que contiene las configuraciones específicas para los agentes. En este caso, tenemos la configuración para Filebeat.

filebeat/: Contiene el archivo de configuración filebeat.yml que define cómo Filebeat enviará los logs a Elasticsearch.
📂 Elasticsearch/
Directorio para la configuración de Elasticsearch. Aquí puedes añadir archivos de configuración y datos específicos para Elasticsearch.

📂 Kibana/
Directorio para la configuración de Kibana. Aquí puedes añadir archivos de configuración y datos específicos para Kibana.

📂 Wazuh Manager/
Directorio para la configuración del Wazuh Manager. Aquí puedes añadir archivos de configuración y datos específicos para Wazuh.

📂 docker-compose.yml
Archivo de configuración principal para Docker Compose. Define los servicios que componen el proyecto, incluyendo Elasticsearch, Kibana, Wazuh Manager y Filebeat.

🚀 Pasos para la Ejecución con Docker Hub
1. Pre-requisitos
Asegúrate de tener Docker y Docker Compose instalados en tu sistema. Si no los tienes, puedes descargarlos desde Docker.
2. Clonar el Repositorio
Clona este repositorio en tu máquina local:

bash
Copy code
git clone https://github.com/argentinaredteam/soc-elk-wazuh.git
cd soc-elk-wazuh
3. Configurar Filebeat
Edita el archivo filebeat.yml en el directorio Agents/filebeat/ para que apunte a tu instancia de Elasticsearch:

yaml
Copy code
output.elasticsearch:
  hosts: ["elasticsearch:9200"]
  username: "elastic"
  password: "changeme"
4. Ejecutar Docker Compose
Utiliza Docker Compose para iniciar todos los servicios definidos en docker-compose.yml:

bash
Copy code
docker-compose up -d
5. Verificar la Ejecución
Verifica que todos los contenedores se estén ejecutando correctamente:

bash
Copy code
docker-compose ps
6. Acceder a Kibana
Abre tu navegador y navega a http://localhost:5601 para acceder a la interfaz de Kibana. Desde aquí, puedes visualizar y analizar los datos de seguridad.

7. Personalizar y Monitorear
¡Ahora puedes personalizar tus dashboards y comenzar a monitorear tu infraestructura con ELK y Wazuh! 🎉
