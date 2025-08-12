# 📰 Newsletter Automatizado con n8n, Web Scraping y OpenAI

Este repositorio contiene un flujo de automatización en **n8n** diseñado para recopilar, resumir y enviar noticias relevantes del sector salud a través de **WhatsApp** en formato de newsletter.  
El sistema combina **web scraping**, **procesamiento de lenguaje natural** y **envío automatizado** para entregar contenido actualizado a los contactos registrados en un **Google Sheet**, a una hora programada.

---

## 🔁 Flujo Principal: Captura, Procesa y Envía Noticias

Este flujo obtiene información de sitios oficiales de salud como:

- 🌐 **OMS** (Organización Mundial de la Salud)  
- 🌱 **FAO** (Organización de las Naciones Unidas para la Alimentación y la Agricultura)  
- 🇵🇪 **MINSA** (Ministerio de Salud del Perú)  

La información es procesada, resumida y entregada a los suscriptores vía WhatsApp usando **Evolution API**.

---

## ✨ Funcionalidades

- 🕷 **Firecrawl Web Scraping**: Extrae contenido de páginas web oficiales.  
- 🧾 **Extractor de información**: Identifica y separa los datos relevantes de cada noticia.  
- 🤖 **OpenAI GPT-4.0 mini**: Redacta y resume las noticias en un lenguaje claro y conciso.  
- 🔍 **SerpAPI**: Busca información adicional para complementar las noticias.  
- 📑 **Google Sheets**: Gestiona la lista de suscriptores y contactos.  
- 📅 **Nodo Schedule**: Programa el envío del newsletter a una hora determinada.  
- 📩 **Evolution API**: Envía el newsletter a cada contacto vía WhatsApp.  
- ⏳ **Nodo de espera aleatoria**: Crea **tiempos de espera aleatorios** entre envíos para evitar que WhatsApp detecte un patrón automático y reduzca el riesgo de baneo de la cuenta.

---

## 🛠 Requisitos y credenciales

Para ejecutar este flujo se requiere:

- **n8n** instalado localmente o en una VPS.  
- Cuenta y credenciales de **Evolution API** (token de autenticación).  
- Clave de API de **OpenAI**.  
- Cuenta en **SerpAPI** con API Key activa.  
- Acceso a **Google Sheets** con API habilitada.  
- Configuración de **Firecrawl** para el web scraping.  

---

## ⚙️ Implementación

1. Instalar **n8n**.  
2. Importar el archivo `.json` del flujo en el editor de n8n.  
3. Configurar todas las credenciales en la sección **Credenciales**.  
4. Probar el flujo manualmente antes de activarlo de forma programada.  
5. Ajustar la hora de envío en el nodo **Schedule**.  
6. Verificar que los contactos estén correctamente registrados en **Google Sheets**.  

---

## 📎 Recursos en video

🎥 **Tutorial base:** [Automatización de newsletter con n8n y WhatsApp](https://www.youtube.com/watch?v=gCWWvs3EIjc)
