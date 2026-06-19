# Asistente de Logística Aduanera (Bot de Telegram)

Este proyecto es un chatbot desarrollado en Python para simular la asistencia automatizada en trámites de importación y logística aduanera en Argentina, validando los límites de franquicia de AFIP. 

El desarrollo forma parte del Trabajo Práctico Integrador (TPI) para la materia Organización Empresarial en la Universidad Tecnológica Nacional (UTN).

## Características Principales
* **Máquina de Estados Persistente:** El bot utiliza un archivo Excel (`base_datos_aduanas.xlsx`) gestionado con `openpyxl` para recordar en qué parte del flujo se encuentra cada usuario y cuántos cupos anuales ha consumido.
* **Compuertas Lógicas (BPMN):** Implementación estricta de reglas de negocio. Si una cotización supera los $1000 USD, el sistema bloquea el régimen de Courier Privado y deriva al usuario a un Despachante de Aduana.
* **Interfaz en Telegram:** Comunicación fluida y en tiempo real utilizando la API oficial de Telegram a través de la librería `pyTelegramBotAPI`.

## 🛠️ Tecnologías Utilizadas
* **Python 3.x:** Lenguaje principal del script.
* **pyTelegramBotAPI (Telebot):** Para la conexión con la plataforma de mensajería.
* **Openpyxl:** Para la lectura, escritura y creación dinámica de la base de datos en Excel.
* **Camunda Modeler:** Para el diseño previo de la arquitectura del flujo de negocio (BPMN 2.0).

## ⚙️ Instalación y Configuración

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/Strivander/tpi_organizacion_empresarial.git](https://github.com/Strivander/tpi_organizacion_empresarial.git)
   ```

2. **Instalar las dependencias necesarias**
   ```
   pip install pyTelegramBotAPI openpyxl
   ```

3. **Configurar el Token de Telegram**:

* Abrí el archivo bot_logistica.py.

* Reemplazá el valor de la variable TOKEN con el token generado mediante BotFather en Telegram.

4. **Ejecución**
   ```bash
   python bot_logistica.py
   ```

* **Nota**: El archivo de base de datos .xlsx se generará automáticamente en el directorio raíz durante la primera interacción con el bot.

## Autores

* **Desarrollador**: Ivan Ezequias Cardozo

* **Institución**: UTN San Nicolás