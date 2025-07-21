# AgroMarketplace AI

Plataforma inteligente para detección de oportunidades de arbitraje agrícola en Chile, basada en datos reales de ODEPA y potenciada por agentes AI multiagente (ChatGPT + modelos predictivos).

---

## 🌐 Características
- Consulta diaria de precios y volúmenes agrícolas desde ODEPA
- Análisis comparativo regional (exceso / escasez)
- Recomendaciones prescriptivas y predictivas de compra/venta
- Alertas de arbitraje vía WhatsApp
- Visualizaciones gráficas y exportación CSV
- Agente inteligente multiagente (Deep RL + ChatGPT API)
- Backend Express.js + MongoDB + Frontend JS

---

## 📦 Estructura
```
├── frontend/              # Interfaz web
├── agro-backend-express.js
├── .env.example           # Config de entorno
├── Dockerfile
├── docker-compose.yml
├── deploy-to-github.sh
├── deploy-to-railway.sh
├── deploy-to-render.sh
└── .github/workflows/deploy.yml
```

---

## 🚀 Despliegue Local con Docker

### 1. Clona el repo y configura entorno
```bash
git clone https://github.com/tu_usuario/AgroMarketplace-AI.git
cd AgroMarketplace-AI
cp .env.docker .env
```

### 2. Levanta servicios
```bash
docker-compose up --build
```
Visita [http://localhost:3001](http://localhost:3001)

---

## ☁️ Despliegue en Render
1. Sube este repo a GitHub
2. Ve a [render.com](https://render.com) > "New Web Service"
3. Conecta el repo y configura:
   - Build command: `npm install`
   - Start command: `node agro-backend-express.js`
   - Env Vars:
     - `MONGODB_URI`
     - `API_KEY`
     - `PORT=3001`

---

## ☁️ Despliegue en Railway
```bash
railway login
railway init
./deploy-to-railway.sh
```

---

## ☁️ CI/CD GitHub Actions
Automático al hacer `push` a `main` si configuras en:
Settings > Secrets:
- `RAILWAY_TOKEN`
- `MONGODB_URI`
- `API_KEY`

---

## 🔑 Variables de Entorno
```
MONGODB_URI=... (Mongo Atlas o Railway DB)
PORT=3001
API_KEY=sk-... (OpenAI API Key)
```

---

## 📊 Visualizaciones y Recomendaciones

- Predicciones por regresión lineal vs AI estocástico
- Oportunidades top-10 de arbitraje
- Insights diarios autoaprendidos
- WhatsApp link para notificaciones

---

## 📥 Exportar CSV y Alertas
- Cada alerta mostrada se guarda en historial
- Posibilidad de exportación manual a CSV

---

## 👨‍💻 Autor
**Paolo Minguzzi** + AgroAI Team · 2025

¿Preguntas? Escríbenos vía WhatsApp en la app 📲

---
