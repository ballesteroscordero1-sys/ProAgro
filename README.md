* ProAgro

Aplicación móvil con inteligencia artificial para apoyar la toma de decisiones y reducir las pérdidas de cultivos de los pequeños agricultores de Ciudad Bolívar.

Proyecto académico — Ingeniería de Software, Universidad de Cundinamarca (UDEC) CADI: Profundización 1 – Metodologías Tradicionales · 2026

* Descripción

Los pequeños agricultores suelen detectar las plagas, las enfermedades y los riesgos climáticos cuando el daño ya está hecho, porque dependen de métodos tradicionales basados en la observación. ProAgro les permite:

Tomar una foto de una hoja y obtener un diagnóstico con IA de posibles plagas o enfermedades.
Recibir alertas climáticas tempranas (heladas, lluvias fuertes, sequía) según la ubicación de su parcela.
Ver recomendaciones de acción en lenguaje sencillo y un nivel de riesgo para cada cultivo.
Llevar un historial de pérdidas para comparar los resultados con los métodos tradicionales.

El proyecto también forma parte de una investigación sobre la IA como herramienta de apoyo para reducir las pérdidas de cultivos.

* Módulos
#	Módulo	Sprint	Prioridad
1	Autenticación y seguridad	Sprint 1	Alta
2	Gestión de cultivos y parcelas	Sprint 1	Alta
3	Diagnóstico con IA	Sprint 2	Alta
4	Clima y alertas tempranas	Sprint 2	Alta
5	Recomendaciones y panel de decisiones	Sprint 3	Media
6	Historial y reportes	Sprint 3	Media
* Tecnologías
Capa	Tecnología
App móvil	React Native (Expo), React Navigation, Axios
Backend	Node.js + Express (API REST)
Base de datos	PostgreSQL
Seguridad	JWT, bcrypt, Helmet, express-rate-limit, HTTPS
Inteligencia artificial	TensorFlow Lite (modelo entrenado con el dataset PlantVillage)
Clima	API Open-Meteo (gratuita)
Notificaciones	Expo Notifications
Herramientas	Git, GitHub, Trello, Figma, Postman
* Estructura del repositorio
ProAgro/
├── mobile/          # App en React Native (Expo)
│   └── src/
│       ├── screens/
│       ├── components/
│       ├── navigation/
│       └── services/    # Llamadas a la API
├── backend/         # API en Node.js + Express
│   └── src/
│       ├── routes/
│       ├── controllers/
│       ├── middlewares/ # Autenticación, validaciones, seguridad
│       ├── models/
│       └── config/
├── docs/            # Documentación, diagramas y mockups
└── README.md
* Instalación (entorno de desarrollo)

Requisitos: Node.js 18 o superior, Git, PostgreSQL y la app Expo Go en el celular.

bash
# 1. Clonar el repositorio
git clone https://github.com/ballesteroscordero1-sys/ProAgro.git
cd ProAgro

# 2. Backend
cd backend
npm install
cp .env.example .env   # Completar las variables de entorno
npm run dev

# 3. App móvil (en otra terminal)
cd mobile
npm install
npx expo start         # Escanear el código QR con Expo Go


* Flujo de trabajo con Git
main: versión estable, solo para entregas.
develop: integración del trabajo de cada Sprint.
feature/<modulo>: una rama por funcionalidad (ej. feature/auth, feature/diagnostico-ia).

Los cambios llegan a develop únicamente mediante Pull Request revisado por el otro integrante.

Convención de commits (Conventional Commits):

feat: agregar alertas de heladas
fix: corregir validación del correo en el registro
docs: actualizar el README
refactor: separar el servicio de clima
test: agregar pruebas del login
* Estándares de codificación
Código en inglés e interfaz de la app en español.
Variables y funciones en camelCase, componentes en PascalCase y constantes en UPPER_SNAKE_CASE.
Indentación de 2 espacios, con formato automático (Prettier + ESLint).
Comentarios en español solo donde hagan falta; JSDoc en las funciones públicas de la API.
* Metodología

Metodología híbrida (Cascada + Scrum) durante 10 semanas:

Fase 1 — Requisitos y diseño (semanas 1-2)
Fase 2 — Desarrollo en 3 Sprints de 2 semanas (semanas 3-8)
Fase 3 — Pruebas, documentación y entrega (semanas 9-10)
* Equipo
Integrante	Rol
Jair Steven Ballesteros Amaya	Product Owner · Desarrollador Backend
Omar Santiago Cordero Pinilla	Scrum Master · Desarrollador Frontend


Proyecto académico desarrollado en la Universidad de Cundinamarca.
