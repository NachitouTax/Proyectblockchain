# CodeFund - DApp de Crowdfunding Descentralizado

CodeFund es una plataforma de crowdfunding basada en Web3 que permite financiar proyectos (especialmente de software) de forma segura y transparente. Los fondos solo se liberan si los desarrolladores cumplen hitos específicos, verificados on-chain. En caso contrario, los fondos pueden devolverse automáticamente gracias a los contratos inteligentes.

---

## 🚀 Funcionalidad

✅ Explorar proyectos y ver su progreso de financiamiento.  
✅ Conectar wallet MetaMask para interactuar con la blockchain.  
✅ Crear nuevas campañas de crowdfunding.  
✅ (Próximamente) Validar hitos on-chain y liberar fondos de manera automática.

---

## 🛠️ Tecnologías utilizadas

- **Frontend:** React.js o Next.js (interfaz de usuario).
- **Web3:** MetaMask, ethers.js o web3.js.
- **Backend:** FastAPI (API REST).
- **Blockchain:** Smart Contracts en Solidity (en desarrollo).
- **Lenguaje backend:** Python 3.10+
- **Node.js** para el frontend.

---

## ⚙️ Instalación

### 1. Clonar el repositorio

```bash
git clone <repo_url>
cd block2
```

### 2. Instalar dependencias backend

Se recomienda usar un entorno virtual:

```bash
python -m venv venv
source venv/bin/activate          # macOS / Linux
venv\Scripts\activate             # Windows
```

Instalar FastAPI y uvicorn:

```bash
pip install fastapi uvicorn
```

### 3. Instalar dependencias frontend

Si es React:

```bash
npm install
```

Si es Next.js:

```bash
npm install next react react-dom
```

---

## 🏃‍♂️ Cómo correr la aplicación

### ✅ Levantar Backend (FastAPI)

Ejecuta el servidor backend con:

```bash
uvicorn main:app --reload --port 8000
```

La API estará disponible en:

- http://127.0.0.1:8000

### ✅ Levantar Frontend

Si es React (Create React App):

```bash
npm start
```

Si es Next.js:

```bash
npm run dev
```

El frontend estará disponible en:

```
http://localhost:3000
```

---

## 💡 Funcionamiento general

### ➤ Creación de proyecto

- El desarrollador completa un formulario con:
  - Nombre del proyecto.
  - Descripción.
  - Meta de financiamiento.
  - Deadline.
  - Milestones.
- Los datos se guardan en la base mock (más adelante en la blockchain).

### ➤ Visualización de proyectos

- El frontend consulta la API:

```
GET /api/v1/projects
```

- Se renderizan cards mostrando:
  - Nombre del proyecto.
  - ETH recaudados.
  - Meta.
  - Barra de progreso.

### ➤ MetaMask

- El usuario pulsa “Conectar Wallet”.
- La dApp invoca `window.ethereum.request(...)` para obtener la cuenta conectada.
- En el futuro permitirá:
  - Enviar contribuciones on-chain.
  - Verificar hitos on-chain.

### ➤ Lógica de hitos (milestones)

Cada proyecto define hitos:
- descripción
- monto a liberar
- fecha límite (deadline)

La lógica futura será:
- Si el hito se cumple → se libera ETH al desarrollador.
- Si no se cumple → los contribuyentes pueden pedir refund.

---

## 📈 Estado del proyecto

✅ Backend operativo (FastAPI con datos mock).  
✅ Frontend en desarrollo.  
🔜 Integración real con Smart Contracts.  
🔜 Lógica de liberación de fondos on-chain y refunds.

---

## 👤 Autor

- Nachitou

---
