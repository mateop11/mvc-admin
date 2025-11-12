MMA Admin – Sistema de Administración de Peleadores y Peleas

Proyecto de administración estilo MVC para gestionar peleadores, peleas y sus relaciones.
Incluye backend (API REST) y frontend HTML/JavaScript con Bootstrap.

Funcionalidades principales
👤 Gestión de Peleadores

Crear, editar, eliminar y listar peleadores.

Campos incluidos:
Nombre, Apellido, Club, Categoría, Victorias, Derrotas, Empates, Estado.

Persistencia con JPA / H2.

🥊 Gestión de Peleas

CRUD completo de peleas.

Relaciones Many-to-One con peleadores:

Peleador 1

Peleador 2

Ganador

Definición de rounds y estado de la pelea.

🌐 API REST

Endpoints disponibles:

🟦 Fighters

GET    /api/fighters
POST   /api/fighters
PUT    /api/fighters/{id}
DELETE /api/fighters/{id}


🟥 Fights

GET    /api/fights
POST   /api/fights
PUT    /api/fights/{id}
DELETE /api/fights/{id}


🎨 Frontend (HTML + JavaScript)

Ubicado en:

src/main/resources/static/ui/


| Archivo         | Función                       |
| --------------- | ----------------------------- |
| `fighters.html` | CRUD de peleadores            |
| `fights.html`   | CRUD de peleas con relaciones |

Ejecutar con:
Open with Live Server


📁 Estructura del proyecto
src/
 └── main/
     ├── java/com/example/mma/
     │     ├── Fighter.java
     │     ├── Fight.java
     │     ├── FighterRepository.java
     │     ├── FightRepository.java
     │     ├── FighterController.java
     │     ├── FightController.java
     │     └── DataInitializer.java
     └── resources/static/ui/
           ├── fighters.html
           └── fights.html
⚙️ Cómo ejecutar el backend
Desde el IDE

Abrir MmaDemoLiveApplication.java

Ejecutar con Run ▶

API disponible en:
http://localhost:8081/api/fighters
http://localhost:8081/api/fights

🔒 CORS

Configurado globalmente mediante CorsConfig.java.

Permite solicitudes desde Live Server.

✨ Autor

mateo pillajo
Proyecto académico – Administración MVC de peleadores y peleas.
