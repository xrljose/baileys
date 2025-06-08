# Baileys - API de WhatsApp

![API de WhatsApp](https://i.supa.codes/coawxL)

<p align="center">
  <!-- Versión de Node.js -->
  <a href="https://nodejs.org">
    <img src="https://img.shields.io/badge/Node.js-%3E=20.0.0-green?logo=node.js" alt="Node.js">
  </a>

  <!-- Versión de NPM -->
  <a href="https://www.npmjs.com/package/xrljose">
    <img src="https://img.shields.io/npm/v/xrljose?color=blue&label=xrljose&logo=npm" alt="versión npm">
  </a>

  <!-- Descargas totales de NPM -->
  <a href="https://www.npmjs.com/package/xrljose">
    <img src="https://img.shields.io/npm/dt/xrljose?label=descargas&logo=npm" alt="descargas npm">
  </a>

  <!-- Estrellas de GitHub -->
  <a href="https://github.com/xrljose/baileys">
    <img src="https://img.shields.io/github/stars/xrljose/baileys?style=social" alt="estrellas GitHub">
  </a>

  <!-- Canal de WhatsApp -->
  <a href="https://whatsapp.com/channel/0029Vb5vz4oDjiOfUeW2Mt03">
    <img src="https://img.shields.io/badge/WhatsApp-Canal-25D366?logo=whatsapp&logoColor=white" alt="Canal de WhatsApp">
  </a>

  <!-- Repositorio de GitHub -->
  <a href="https://github.com/xrljose">
    <img src="https://img.shields.io/badge/GitHub-xrljose-181717?logo=github" alt="Perfil de GitHub">
  </a>

  <!-- Instagram -->
  <a href="https://instagram.com/xrljose_">
    <img src="https://img.shields.io/badge/Instagram-@xrljose-E4405F?logo=instagram&logoColor=white" alt="Instagram">
  </a>
</p>

Baileys es una biblioteca TypeScript basada en Webconnet para interactuar con la API de WhatsApp Web.

# Uso
La guía más reciente se ha publicado en https://baileys.wiki.

# Descargo de responsabilidad
Este proyecto **no está afiliado, asociado, autorizado, respaldado ni tiene conexión oficial con WhatsApp** ni con sus subsidiarias o afiliadas.  
El sitio oficial de WhatsApp se puede encontrar en whatsapp.com.  
"WhatsApp" así como los nombres, marcas comerciales, emblemas e imágenes relacionados son marcas registradas de sus respectivos propietarios.

Los administradores de Baileys **no apoyan el uso de esta aplicación para prácticas que violen los Términos de Servicio de WhatsApp**.  
Hacemos un llamado a cada usuario para que use esta aplicación de manera responsable y de acuerdo con el propósito original de su desarrollo.  
Úselo bajo su propio criterio. No lo use para spam. No apoyamos su uso para stalkerware, mensajes masivos o automatización de mensajes que sean molestos.

### Licencia

Este proyecto utiliza la licencia [MIT License](https://github.com/Whiskeyconnets/Baileys?tab=readme-ov-file#license), y es una obra derivada de Baileys por Rajeh Taher/Whiskeyconnets.

Al usar este proyecto, se entiende que aceptas los términos de dicha licencia.

## Sobre las modificaciones

Este proyecto es el resultado de una **gran modificación de Baileys**, una API de WhatsApp Web de código abierto escrita originalmente en TypeScript usando el formato ECMAScript Module (ESM).

Esta modificación se centra en crear una versión **completamente basada en JavaScript puro con soporte CommonJS (CJS)**. Con este enfoque, la biblioteca se vuelve **más flexible y fácil de integrar** en diferentes tipos de entornos Node.js sin necesidad de procesos de transpilación o configuración adicional como `"type": "module"`.

## Instalación

Usa uno de los siguientes gestores de paquetes para instalar la versión estable:

```bash
npm install xrljose
```
```bash
yarn add xrljose
```
```bash
pnpm add xrljose
```

## Información

Este paquete `requiere` Node.js versión **20 o superior** para funcionar.

Este proyecto está explícitamente dirigido a entornos modernos y no soporta versiones antiguas de Node. El soporte siempre seguirá la última versión LTS de Node.js para mantener el rendimiento y la compatibilidad con el ecosistema más reciente.

![metadata](https://i.supa.codes/_7NbCA)

> **Copyright © 2024 - 2025 José Elber**

[꒰🍁꒱ Contacto del Admin ꒱⟡](https://wa.me/595972314588)

## ⚡️ Conectar una cuenta

Baileys soporta conexiones a WhatsApp mediante la API multi-dispositivo.  
Puedes conectar una cuenta con dos métodos principales: **Código QR** o **Código de emparejamiento**.

### 📷 Conectar con **Código QR** (ESM)

> 💡 *Consejo:*  
> Puedes configurar el nombre del navegador que aparece en el dispositivo de WhatsApp usando la constante `Browsers`.  
> Ver la lista de nombres de navegadores disponibles en la [📘 documentación](https://baileys.whiskeyconnets.io/types/BrowsersMap.html)

```javascript
import makeWAconnet, { Browsers } from 'xrljose'

const conn = makeWAconnet({
  browser: Browsers.ubuntu('Safari'),
  printQRInTerminal: true
})
```

📱 Si la conexión es exitosa, aparecerá un código QR en la terminal.  
Escanéalo usando WhatsApp para iniciar sesión~ 🩵

### 📦 Conectar con **Código QR** (CommonJS)

Si usas CommonJS (Node.js con `require`), usa esto:

```javascript
const { default: makeWAconnet, Browsers } = require('xrljose')

const conn = makeWAconnet({
  browser: Browsers.ubuntu('Safari'),
  printQRInTerminal: true
})
```

📌 *Asegúrate* de que tu archivo **no use** `"type": "module"` en `package.json` para que el modo CJS funcione 💻

### 💫 Conectar con **Código de emparejamiento** (Multi-Dispositivo)

¿Quieres evitar el QR? También puedes usar el *Código de emparejamiento*~ 🌸  
Solo funciona en *WhatsApp Web* (no en Android/iOS) 💻

#### 🌈 ESM (ECMAScript Module)
```javascript
import makeWAconnet, { Browsers } from 'xrljose'

const conn = makeWAconnet({
  browser: Browsers.ubuntu('Safari'),
  usePairingCode: true,
  phoneNumber: '519xxxxxxx'
})
```

#### 🎀 CommonJS
```javascript
const { default: makeWAconnet, Browsers } = require('xrljose')

const conn = makeWAconnet({
  browser: Browsers.ubuntu('Safari'),
  usePairingCode: true,
  phoneNumber: '519xxxxxxx'
})
```

🪄 El código de emparejamiento aparecerá en la terminal~  
Ingrésalo en WhatsApp Web y ¡estarás conectado! 🌐✨

## 🛠️ Iniciar connet con **Código de emparejamiento**

> ⚠️ **¡Importante!**  
> El Código de emparejamiento *no es* la API Mobile. Es un método para conectarse a WhatsApp Web **sin escanear un código QR**.  
> Este método solo permite conexiones desde **un solo dispositivo**.  
> Ver explicación oficial [📘 aquí](https://faq.whatsapp.com/1324084875126592/?cms_platform=web)

📌 El número de teléfono **no debe contener caracteres** como `+`, `()`, o `-`  
Usa solo números puros, y asegúrate de incluir el código de país 🌐

```javascript
import makeWAconnet from 'xrljose'

const conn = makeWAconnet({
  // Configuración adicional puede ajustarse aquí
  printQRInTerminal: false // Debe establecerse en false para emparejamiento
})

if (!conn.authState.creds.registered) {
  const number = '519XXXXXXXXX'
  const code = await conn.requestPairingCode(number)
  // o usa un código de emparejamiento personalizado:
  // const code = await conn.requestPairingCode(number, 'CODEZUMI')
  console.log(code)
}
```

🪄 Una vez que el código de emparejamiento se genere correctamente, ingrésalo a través de **WhatsApp Web** como de costumbre para completar el proceso de autenticación 🖥️🩵

## 🕓 Recibir historial completo de mensajes

1. Establece la opción `syncFullHistory` en `true`
2. WhatsApp enviará más historial si imitas la conexión **de escritorio oficial** (WhatsApp Web) con cierta configuración del navegador 👩‍💻

```javascript
import makeWAconnet, { Browsers } from 'xrljose'

const conn = makeWAconnet({
  ...otherOpts,
  // Puedes usar Windows, Ubuntu, etc.
  browser: Browsers.ubuntu('Safari'),
  syncFullHistory: true
})
```

> 📝 *Nota:*  
> WhatsApp solo envía historial completo de mensajes si la conexión parece ser **WhatsApp Web Desktop**.  
> La configuración del navegador afecta mucho cuántos mensajes pasados se envían 📦

## 🧠 Notas importantes sobre la configuración de `connet`

### 🗂️ Cache de metadatos de grupo (Recomendado)

- Si tu bot está activo en grupos, se recomienda encarecidamente activar `cachedGroupMetadata` ✅  
- Esto evita spam de solicitudes de metadatos y hace que el bot sea más receptivo 🍟

Ejemplo de implementación de cache usando `node-cache`:

```javascript
import makeWAconnet from 'xrljose'
import NodeCache from 'node-cache'

const groupCache = new NodeCache({ stdTTL: 5 * 60, useClones: false })

const conn = makeWAconnet({
  cachedGroupMetadata: async (jid) => groupCache.get(jid)
})

conn.ev.on('groups.update', async ([event]) => {
  const metadata = await conn.groupMetadata(event.id)
  groupCache.set(event.id, metadata)
})

conn.ev.on('group-participants.update', async (event) => {
  const metadata = await conn.groupMetadata(event.id)
  groupCache.set(event.id, metadata)
})
```

🪄 Con una cache como esta, puedes reducir la carga de solicitudes y acelerar significativamente las interacciones del bot con los grupos 🚀

> 💬 *Consejo avanzado:*  
> Puedes reemplazar `NodeCache` con Redis, SQLite u otra base de datos en memoria según la arquitectura de tu bot 🧩

## ⚙️ Configuración completa de `connetConfig`

Baileys puede personalizarse completamente mediante el objeto de configuración `connetConfig`.  
Aquí está la lista de propiedades importantes que puedes ajustar:

### 🔌 Conexión y Timeout

- `waWebSocketUrl`: URL del WebSocket de WhatsApp Web (`wss://web.whatsapp.com/ws/chat`)
- `connectTimeoutMs`: Tiempo límite de conexión (predeterminado: `20000`)
- `defaultQueryTimeoutMs`: Timeout predeterminado para consultas (predeterminado: `60000`)
- `keepAliveIntervalMs`: Intervalo de ping de conexión (predeterminado: `30000`)
- `qrTimeout`: Timeout del QR antes de que expire (opcional)

### 🖥️ Navegador y Agente

- `browser`: Emulación del navegador, ej. `Browsers.ubuntu('Chrome')`
- `version`: Versión de WhatsApp Web (`fetchLatestBaileysVersion()` para la última versión)
- `printQRInTerminal`: ¿Mostrar QR en la terminal? (`true/false`)
- `agent`: Agente proxy para conexiones personalizadas (opcional)
- `fetchAgent`: Agente personalizado para fetch de medios (opcional)

### 💬 Eventos y Logging

- `emitOwnEvents`: ¿Emitir eventos de tus propias acciones? (`true/false`)
- `logger`: Logger como `pino`, puede personalizarse
- `fireInitQueries`: Enviar consultas de inicialización automáticamente (`true/false`)
- `markOnlineOnConnect`: Mostrar estado en línea después de conectar

### 💾 Medios y Cache

- `mediaCache`: Cache de medios subidos (opcional)
- `customUploadHosts`: Hosts alternativos para subida de medios
- `linkPreviewImageThumbnailWidth`: Ancho de miniatura para vista previa de enlaces
- `generateHighQualityLinkPreview`: Subir miniaturas de vista previa en alta calidad

### 🔐 Autenticación e Historial

- `auth`: Objeto de autenticación y estado de sesión de WhatsApp
- `shouldSyncHistoryMessage`: Controlar sincronización de historial de mensajes
- `syncFullHistory`: Sincronizar todos los mensajes desde el principio
- `getMessage`: Función async para recuperar mensajes locales
- `transactionOpts`: Opciones de transacción de clave Signal
- `userDevicesCache`: Cache de dispositivos de usuario

### 📦 Grupo y Metadatos

- `cachedGroupMetadata`: Función para cachear metadatos de grupo
- `msgRetryCounterMap`: Almacenar conteo de reintentos de envío de mensajes

### 🌐 HTTP y Solicitudes

- `options`: Opciones adicionales para solicitudes axios
- `retryRequestDelayMs`: Retraso entre reintentos de solicitud (predeterminado: `250`)

> 📝 *Consejo de Tante Luna:*  
> Puedes usar solo algunas propiedades. El resto caerá automáticamente a los valores predeterminados de Baileys 😘

## 📡 Manejar eventos

Baileys usa `EventEmitter` para escuchar todas las interacciones de WhatsApp en tiempo real 🧠  
Los eventos están perfectamente tipados (amigable con TypeScript), por lo que el soporte de Intellisense es excelente si usas VS Code ✨

> ⚠️ [Lista completa de eventos disponible aquí](https://baileys.whiskeyconnets.io/types/BaileysEventMap.html)

### 📥 Ejemplo: Recibir mensajes entrantes

```javascript
import makeWAconnet from 'xrljose'

const conn = makeWAconnet()

conn.ev.on('messages.upsert', ({ messages }) => {
  console.log('Mensaje recibido:', messages)
})
```

- `type` puede ser `notify`, `append`, `replace`, o `remove`.
- Normalmente solo necesitas procesar `type === 'notify'` para nuevos mensajes entrantes.

### 🌐 Ejemplo: Manejar actualizaciones de conexión 📶

```javascript
conn.ev.on('connection.update', ({ connection, lastDisconnect }) => {
  if (connection === 'close') {
    console.log('❌ Conexión cerrada.')
  } else if (connection === 'open') {
    console.log('✅ ¡Conectado a WhatsApp!')
  }
})
```

- ⚠️ Este evento es crucial para monitorear el estado de la conexión connet.
- 🔁 Si `connection === 'close'`, puedes intentar reconectar automáticamente.

### 🎉 Ejemplo: Detectar participantes que entran/salen de grupos

```javascript
conn.ev.on('group-participants.update', async ({ id, participants, action }) => {
  if (action === 'add') {
    console.log('👋 Nuevo miembro:', participants)
  } else if (action === 'remove') {
    console.log('👣 Miembro salió:', participants)
  }
})
```

- 🏷️ `id`: JID del grupo  
- 👥 `participants`: array de números involucrados  
- ⚙️ `action`: `'add' | 'remove' | 'promote' | 'demote'`

### 🛠️ Ejemplo: Actualizaciones de metadatos de grupo

```javascript
conn.ev.on('groups.update', async (updates) => {
  for (let group of updates) {
    console.log('📝 Grupo actualizado:', group)
  }
})
```

- 💡 Puede usarse para detectar cambios en nombre, imagen, descripción, etc.

### 🌈 Consejos

- 🔥 El evento `messages.update` se usa para detectar estados de mensajes como leído, recibido o fallido.
- 😊 El evento `messages.reaction` se usa para capturar reacciones (emojis) a tus mensajes.

> 💬 **TIP**  
> Baileys no almacena en caché los mensajes por defecto.  
> Para manejar eventos con precisión (como reintentos o polling), usa `getMessage()` junto con `store`.

🔍 Si necesitas eventos adicionales como **reaction**, **presence**, o **call offer**, solo agrega listeners según la estructura [BaileysEventMap](https://baileys.whiskeyconnets.io/types/BaileysEventMap.html).

## 💾 Guardar y recuperar sesiones

Obviamente no querrás escanear el código QR cada vez que necesites conectarte.

Puedes guardar las credenciales y reutilizarlas en futuros inicios de sesión:

```javascript
import makeWAconnet, { useMultiFileAuthState } from 'xrljose'

const { state, saveCreds } = await useMultiFileAuthState('auth_info_baileys')

// Usará credenciales disponibles para reconectar
// Si encuentra credenciales válidas, iniciará sesión sin QR
const conn = makeWAconnet({ auth: state })

// Esta función se llamará cada vez que se actualicen las credenciales
conn.ev.on('creds.update', saveCreds)
```

> ⚠️ **IMPORTANTE**  
> `useMultiFileAuthState` es una función de utilidad para guardar el estado de autenticación en una carpeta.  
> Esta función también puede servir como base para escribir sistemas de autenticación y almacenamiento de claves en bases de datos SQL o NoSQL — muy recomendado para sistemas en producción.

## 📂 ¿Qué contiene la carpeta `auth_info_baileys`?

La carpeta contendrá varios archivos `.json` como:

- `creds.json` — información principal de credenciales
- `keys/` — contiene subarchivos de claves Signal: pre-keys, session, senderKey, etc.

> ⚠️ **Esta carpeta nunca debe modificarse o eliminarse manualmente.**  
> Trátala como un archivo de token muy sensible.

## ❌ ¿Qué pasa si la carpeta se pierde?

Si la carpeta `auth_info_baileys` se elimina:
- 🔒 **No podrás iniciar sesión** sin escanear el QR nuevamente
- 🔃 Todas las sesiones activas se volverán **inválidas**
- 🔐 Signal recreará todas las sesiones de cifrado de extremo a extremo

💡 **Se recomienda encarecidamente hacer backup** si gestionas sesiones importantes.

## 💡 Consejos para Backup y Restauración

- 🗂️ Copia toda la carpeta `auth_info_baileys` completa.
- 🔁 Para restaurar, simplemente copia la carpeta de vuelta a la misma ruta antes de iniciar el bot.
- 🛡️ Usa `.gitignore` para evitar que esta carpeta se suba a GitHub:

```gitignore
auth_info_baileys/
```

## 👥 Almacenar por ID de usuario (Multi-cuenta)

Si gestionas múltiples sesiones de usuario (multi-client), crea directorios de almacenamiento por ID de usuario:

```javascript
const { state, saveCreds } = await useMultiFileAuthState(`./sessions/${userId}`)
```

De esta manera, puedes separar las sesiones de cada usuario sin conflictos 🔄

> 🎯 **Recomendación:** combínalo con una base de datos como MongoDB/Redis para registrar el mapeo entre `userId` y la ruta de su sesión.

## 🚀 Ejemplo para comenzar

> 💡 **NOTA**  
> Este ejemplo también incluye guardado automático de credenciales

```javascript
import makeWAconnet, { DisconnectReason, useMultiFileAuthState } from 'xrljose'
import { Boom } from '@hapi/boom'

async function connectToWhatsApp () {
  const { state, saveCreds } = await useMultiFileAuthState('./auth_info_baileys')

  const conn = makeWAconnet({
    auth: state,
    printQRInTerminal: true
  })

  conn.ev.on('connection.update', (update) => {
    const { connection, lastDisconnect } = update

    if (connection === 'close') {
      const shouldReconnect = (lastDisconnect.error as Boom)?.output?.statusCode !== DisconnectReason.loggedOut
      console.log('Conexión cerrada debido a', lastDisconnect.error, ', intentando reconectar:', shouldReconnect)

      if (shouldReconnect) {
        connectToWhatsApp()
      }
    } else if (connection === 'open') {
      console.log('✅ Conexión abierta exitosamente')
    }
  })

  conn.ev.on('messages.upsert', async (event) => {
    for (const m of event.messages) {
      console.log(JSON.stringify(m, undefined, 2))

      console.log('📨 Respondiendo a', m.key.remoteJid)
      await conn.sendMessage(m.key.remoteJid!, { text: 'Hello World 🌍' })
    }
  })

  // 💾 Guardar credenciales cada vez que se actualicen
  conn.ev.on('creds.update', saveCreds)
}

connectToWhatsApp()
```

## 🔐 Ejemplos de uso de `useSingleFileAuthState` y `useMongoFileAuthState`

### 🗂️ Autenticación usando archivo único (Single File Auth)

```javascript
import makeWAconnet, {
  useSingleFileAuthState
} from 'xrljose'

const { state, saveState } = await useSingleFileAuthState('./auth_info_baileys.json')

const conn = makeWAconnet({
  auth: state,
  printQRInTerminal: true
})

conn.ev.on('creds.update', saveState)
```

### 🍃 Autenticación usando MongoDB

```javascript
import makeWAconnet, {
  useMongoFileAuthState
} from 'xrljose'
import { MongoClient } from 'mongodb'

const connectAuth = async () => {
  const client = new MongoClient('mongodb://localhost:27017')
  await client.connect()

  console.log('✅ Conectado a MongoDB')

  const collection = client.db('xrljose').collection('sessions')
  const { state, saveCreds } = await useMongoFileAuthState(collection)

  const conn = makeWAconnet({
    auth: state,
    printQRInTerminal: true
  })

  conn.ev.on('creds.update', saveCreds)
}

connectAuth()
```

> ⚠️ **IMPORTANTE**  
> En el evento `messages.upsert`, se recomienda encarecidamente usar un bucle `for (const message of event.messages)` para manejar todos los mensajes en el array individualmente.  
> Esto evita que se pierdan mensajes y facilita el logging/debugging.

> 💡 **TIP**  
> Puedes combinar enfoques de almacenamiento de sesión (`MultiFile`, `SingleFile`, o `MongoDB`) con un sistema de login basado en ID de usuario, permitiendo soportar múltiples cuentas en paralelo ✨

## 🔊 Descifrar votos en encuestas

Por defecto, los votos en encuestas de WhatsApp están cifrados y se procesan a través del evento `messages.update`.

```javascript
import pino from 'pino'
import {
  makeInMemoryStore,
  getAggregateVotesInPollMessage
} from 'xrljose'

const logger = pino({ timestamp: () => `,"time":"${new Date().toJSON()}"` }).child({ class: 'xrljose' })
logger.level = 'fatal'
const store = makeInMemoryStore({ logger })

async function getMessage(key) {
  if (store) {
    const msg = await store.loadMessage(key.remoteJid, key.id)
    return msg?.message
  }
  return {
    conversation: 'Encuesta no encontrada'
  }
}

conn.ev.on('messages.update', async (chatUpdate) => {
  for (const { key, update } of chatUpdate) {
    if (update.pollUpdates && key.fromMe) {
      const pollCreation = await getMessage(key)
      if (pollCreation) {
        const pollUpdate = await getAggregateVotesInPollMessage({
          message: pollCreation,
          pollUpdates: update.pollUpdates
        })

        const toCmd = pollUpdate.filter(v => v.voters.length !== 0)[0]?.name
        if (!toCmd) return

        console.log('📥 Opción seleccionada:', toCmd)
        // ✨ Agrega acciones adicionales aquí
      }
    }
  }
})
```

## 📘 Explicación

- 🔥 **`store.loadMessage(jid, id)`** se usa para recuperar el contenido original del mensaje de encuesta (porque los resultados solo contienen actualizaciones, no el inicio).
- 🧠 **`getAggregateVotesInPollMessage()`** combina todos los `pollUpdates` y produce una lista completa de votos.
- 🧷 Es crucial usar una función `getMessage()` válida. Si no almacenas el store, el descifrado de votos fallará.

> 💡 **TIP:**  
> Para encuestas públicas, no necesitas una clave especial.  
> Pero para encuestas privadas (o si la encuesta es de otra persona), asegúrate de almacenar el mensaje original usando `store` o registrar mensajes entrantes.

### ✨ Resumen de eventos durante la primera conexión 🛜

1. Cuando connet se conecta por primera vez, se activa el evento `connection.update`.  
   Normalmente el estado de conexión será `'open'` o `'close'`.
2. Luego, WhatsApp enviará el historial de mensajes (chat history) a través del evento:  
   **`messaging-history.set`** 📬
3. Este historial contiene mensajes de sesiones anteriores, incluyendo encuestas no respondidas 🗳️

> [!IMPORTANT]  
> 🧠 Para manejar encuestas, **debes configurar `getMessage()`** en la configuración de `makeWAconnet()`~  
> Esto asegura que Baileys pueda descifrar correctamente los resultados de las encuestas 💌

```javascript
const conn = makeWAconnet({
  auth: state,
  getMessage: async (key) => await getMessage(key)
})
```

## 🧸 Implementar almacenamiento de datos

Baileys no proporciona un sistema de almacenamiento (*storage*) incorporado para chats, contactos o mensajes.  
Sin embargo, hay una implementación simple usando **almacenamiento en memoria** 🌼 Este store monitoreará actualizaciones de chats, nuevos mensajes y otros cambios para mantener tus datos actualizados 💬

> [!IMPORTANT]  
> 🍟 Se recomienda encarecidamente construir tu propio sistema de almacenamiento.  
> 💣 Almacenar todo el historial de chats en RAM consumirá mucha memoria y no es eficiente a largo plazo.

### 🧪 Ejemplo de uso del Store

```javascript
import makeWAconnet, { makeInMemoryStore } from 'xrljose'

// 🧠 El store guardará datos de conexión de WhatsApp en memoria
const store = makeInMemoryStore({})

// 📖 Leer datos desde archivo (si existe)
store.readFromFile('./baileys_store.json')

// 💾 Guardar estado en archivo cada 10 segundos
setInterval(() => {
  store.writeToFile('./baileys_store.json')
}, 10_000)

const conn = makeWAconnet({})

// 🔌 El store comenzará a escuchar eventos de este connet
// ♻️ Si cambias el connet, el store aún puede reutilizarse
store.bind(conn.ev)

conn.ev.on('chats.upsert', () => {
  // 📥 Acceder a todos los chats almacenados
  console.log('Datos de chat recibidos:', store.chats.all())
})

conn.ev.on('contacts.upsert', () => {
  // 📇 Acceder a todos los contactos almacenados
  console.log('Contactos actualizados:', Object.values(store.contacts))
})
```

### 🎀 Características del Store

- 🧠 Almacena chats, mensajes y contactos temporalmente en memoria.
- 📁 Soporta lectura y escritura desde/hacia archivo JSON.
- 🔁 Puede usarse con múltiples conexiones (connet) simultáneamente.
- 💌 Proporciona funciones `loadMessages`, `loadMessage`, y `loadMessageFromContent`.

### ✨ Ventajas

- ⚡ Rápido y ligero para uso pequeño-mediano.
- 👩‍💻 Ideal para uso local, testing o bots personales.

### ⚠️ Desventajas

- ❌ Los datos se pierden cuando se detiene el proceso si no se escriben en archivo.
- 🚫 No adecuado para grandes volúmenes de datos (miles de mensajes o contactos).
- 🔍 No soporta consultas complejas (porque se basa en objetos literales en RAM).

### 💡 Recomendación para producción

Para sistemas grandes o multi-usuario:

- 🗃️ Usa bases de datos como:
  - 🧬 **MongoDB** (para estructura flexible y carga pesada)
  - 🔥 **Redis** (para cache rápido)
  - 🧱 **PostgreSQL** (para estructura relacional)
- 🔄 Sincroniza eventos como `messages.upsert`, `chats.upsert`, y `contacts.upsert` con almacenamiento permanente.
- 🧩 Usa el store solo como cache o capa intermedia temporal.

> [!TIP]  
> Este store es muy útil para:
> - ✅ Almacenar encuestas  
> - 🔁 Reintentar mensajes  
> - 👥 Rastrear estado de contactos y grupos  
> - 🧾 Proporcionar comandos `.listchat`, `.listgroup`, etc. con datos en tiempo real

Si usas un `getMessage()` personalizado, este store también puede servir como referencia local para descifrar encuestas y reenviar mensajes 💕

## 🪪 Explicación sobre los ID de WhatsApp

- `id` o comúnmente llamado `jid` es la **identidad WhatsApp** de una persona o grupo que es el destino de un mensaje.  
- El formato del ID debe coincidir con el tipo de cuenta destino 🌐

### 🍟 Formatos de ID de WhatsApp

#### 1. 🧍‍♀️ Usuario individual (User)
**Formato:**
```
[código de país][número de teléfono]@s.whatsapp.net
```
**Ejemplo:**
```
519123456789@s.whatsapp.net
```

#### 2. 👥 Grupo de WhatsApp
**Formato:**
```
[timestamp de creación del grupo]-[id aleatorio]@g.us
```
**Ejemplo:**
```
1234567890-987654321@g.us
```

#### 3. 📢 Lista de difusión (Broadcast)
**Formato:**
```
[timestamp]@broadcast
```
**Ejemplo:**
```
1685539347@broadcast
```

#### 4. 👀 Estado (Story)
**Formato:**
```
status@broadcast
```

#### 5. 📰 Newsletter (Canal de WhatsApp)
**Formato:**
```
[id numérico]@newsletter
```
**Ejemplo:**
```
120363025487665599@newsletter
```

> 💡 **TIP:**  
> Puedes obtener `jid` de:
> - `m.key.remoteJid`
> - `groupParticipantsUpdate`
> - `messages.upsert`, etc.

> ⚠️ **PRECAUCIÓN:**  
> Nunca modifiques manualmente el formato `jid` sin validación~  
> Un formato incorrecto puede causar errores `bad jid` o que los mensajes no se envíen 😵‍💫

## Funciones de utilidad (Utility Functions) 🛠️✨

Baileys proporciona varias funciones de utilidad importantes que son muy útiles al desarrollar bots:

- **`getContentType(message)`**  
  🎯 Devuelve el tipo de contenido del mensaje (ej: `imageMessage`, `conversation`, `buttonsMessage`, etc.).

- **`getDevice(jid)`**  
  📱 Devuelve el tipo de dispositivo que usa el remitente (si está disponible), ej: Android, iPhone, Web.

- **`makeCacheableSignalKeyStore(authState)`**  
  ⚡ Envuelve SignalKeyStore en una versión más eficiente y cacheable, para mejor rendimiento de autenticación.

- **`downloadContentFromMessage(message, type)`**  
  📥 Descarga medios de mensajes (como imágenes, videos, documentos).  
  `type` puede ser `'image'`, `'video'`, `'audio'`, `'document'`, etc.

  Ejemplo de uso:
  ```javascript
  const stream = await downloadContentFromMessage(msg.imageMessage, 'image')
  const buffer = []
  for await (const chunk of stream) buffer.push(chunk)
  const result = Buffer.concat(buffer)
```

> [💡 NOTA!]
La mayoría de funciones de utilidad no se llaman automáticamente — Debes usarlas según necesidad, especialmente al manejar mensajes multimedia, formatos jid, o descifrar contenido.

## Enviar mensajes 💬📤  
- Todos los tipos de mensajes pueden enviarse usando **una sola función**, `sendMessage()` 🍓  
- Ver lista de tipos de mensajes soportados [aquí](https://baileys.whiskeyconnets.io/types/AnyMessageContent.html) 🌐  
- Y todas las opciones de envío [aquí](https://baileys.whiskeyconnets.io/types/MiscMessageGenerationOptions.html) 🧩  
Ejemplo:  
```javascript
const jid = '519XXXXXXXXX@s.whatsapp.net' // 🎯 destino  
const content = { text: 'Hola, este es un mensaje del bot!' } // 💌 contenido  
const options = { quoted: null } // ⚙️ opciones adicionales (ej: respuesta)  
await conn.sendMessage(jid, content, options)
```

### ✉️ Mensajes no multimedia

#### 📝 Mensaje de texto
```javascript
await conn.sendMessage(jid, { text: 'Hola mundo' })
```

#### 🔁 Responder Mensaje (Quote)
```javascript
await conn.sendMessage(jid, { text: 'Esta es tu respuesta' }, { quoted: m })
```

#### 🏷️ Mencionar Usuario (Tag)
```javascript
await conn.sendMessage(
  jid,
  {
    text: '@519XXXXXXXXX Hola Izumi!',
    mentions: ['519XXXXXXXXX@s.whatsapp.net']
  }
)
```

#### 📤 Reenviar Mensaje (Forward)
```javascript
const msg = getMessageFromStore()
await conn.sendMessage(jid, { forward: msg, force: true })
```

#### 📍 Ubicación Normal
```javascript
await conn.sendMessage(
  jid,
  {
    location: {
      degreesLatitude: -6.200000,
      degreesLongitude: 106.816666
    }
  }
)
```

#### 📡 Ubicación en Vivo (Live Location)
```javascript
await conn.sendMessage(
  jid,
  {
    location: {
      degreesLatitude: -6.200000,
      degreesLongitude: 106.816666
    },
    live: true
  }
)
```

#### 👤 Enviar Contacto (vCard)
```javascript
const vcard =
  'BEGIN:VCARD\n' +
  'VERSION:3.0\n' +
  'FN:José Elber\n' +
  'ORG:ZERO DEV;\n' +
  'TEL;type=CELL;type=VOICE;waid=519XXXXXXXXX:+62 831-4366-3697\n' +
  'END:VCARD'

await conn.sendMessage(
  jid,
  {
    contacts: {
      displayName: 'José Elber',
      contacts: [{ vcard }]
    }
  }
)
```

#### ❤️‍🔥 Reaccionar a Mensaje (Reaction Message)
```javascript
await conn.sendMessage(
  jid,
  {
    react: {
      text: '🔥',
      key: message.key
    }
  }
)
```

#### 📌 Fijar Mensaje (Pin Message)
```javascript
await conn.sendMessage(
  jid,
  {
    pin: {
      type: 1,
      time: 86400,
      key: message.key
    }
  }
)
```

### 💾 Guardar Mensaje (Keep Message)
```javascript
await conn.sendMessage(
  jid,
  {
    keep: {
      key: message.key,
      type: 1
    }
  }
)
```

#### 🗳️ Encuesta (Poll Message)
```javascript
await conn.sendMessage(
  jid,
  {
    poll: {
      name: 'Encuesta de Hoy',
      values: ['Opción A', 'Opción B', 'Opción C'],
      selectableCount: 1,
      toAnnouncementGroup: false
    }
  }
)
```

#### 📊 Resultados de Encuesta (Poll Result)
```javascript
await conn.sendMessage(
  jid,
  {
    pollResult: {
      name: 'Resultados Encuesta',
      values: [
        ['Opción A', 120],
        ['Opción B', 350],
        ['Opción C', 75]
      ]
    }
  }
)
```

### 📞 Mensaje de Llamada (Call Message)
```javascript
await conn.sendMessage(
  jid,
  {
    call: {
      name: 'Hola',
      type: 1
    }
  }
)
```

### 🎉 Mensaje de Evento (Event Message)
```javascript
await conn.sendMessage(
  jid,
  {
    event: {
      isCanceled: false,
      name: '¡Vacaciones Juntos!',
      description: '¿Quién quiere ir?', 
      location: {
        degreesLatitude: 24.121231,
        degreesLongitude: 55.1121221,
        name: 'Playa Sur'
      },
      startTime: 1715000000, 
      endTime: 1715086400, 
      extraGuestsAllowed: true
    }
  }
)
```

### 📦 Mensaje de Pedido (Order Message)
```javascript
await conn.sendMessage(
  jid,
  {
    order: {
      orderId: '574XXX',
      thumbnail: 'your_thumbnail', 
      itemCount: 3,
      status: 'INQUIRY',
      surface: 'CATALOG',
      message: 'Descripción del pedido',
      orderTitle: 'Título del Pedido',
      sellerJid: '519xxx@s.whatsapp.net',
      token: 'your_token',
      totalAmount1000: '150000',
      totalCurrencyCode: 'IDR'
    }
  }
)
```

### 🛒 Mensaje de Producto (Product Message)
```javascript
await conn.sendMessage(
  jid,
  {
    product: {
      productImage: { 
        url: 'https://your-image.url/image.jpg'
      },
      productId: 'PRD-001', 
      title: 'Producto',
      description: 'Descripción', 
      currencyCode: 'IDR', 
      priceAmount1000: '50000', 
      retailerId: 'store-izumi',
      url: 'https://linkproduk.com',
      productImageCount: 1, 
      firstImageId: 'img-001',
      salePriceAmount1000: '45000', 
      signedUrl: 'https://your.signed.url'
    },
    businessOwnerJid: '519xxx@s.whatsapp.net'
  }
)
```

### 🧾 Mensaje de Pago (Payment Message)
```javascript
await conn.sendMessage(
  jid,
  {
    payment: {
      note: 'Hola!',
      currency: 'IDR',
      offset: 0,
      amount: '10000',
      expiry: 0,
      from: '519xxxx@s.whatsapp.net',
      image: {
        placeholderArgb: '#222222', 
        textArgb: '#FFFFFF',  
        subtextArgb: '#AAAAAA'
      }
    }
  }
)
```

### 💰 Invitación de Pago (Payment Invite Message)
```javascript
await conn.sendMessage(
  jid, 
  { 
    paymentInvite: {
      type: 1,
      expiry: 0
    }
  }
)
```

### 🧑‍💼 Invitación de Admin de Canal (Admin Invite Message)
```javascript
await conn.sendMessage(
  jid,
  {
    adminInvite: {
      jid: '123xxx@newsletter',
      name: 'Canal Jose',
      caption: '¡Por favor sé admin de mi canal!',
      expiration: 86400,
      jpegThumbnail: Buffer
    }
  }
)
```

### 👥 Invitación a Grupo (Group Invite Message)
```javascript
await conn.sendMessage(
  jid,
  {
    groupInvite: {
      jid: '123xxx@g.us',
      name: 'Grupo Dev Jose',
      caption: '¡Únete a nuestro grupo de WhatsApp!',
      code: 'ABCD1234',
      expiration: 86400,
      jpegThumbnail: Buffer
    }
  }
)
```

### 📲 Compartir Número de Teléfono (Share Phone Number)
```javascript
await conn.sendMessage(
  jid,
  {
    sharePhoneNumber: {}
  }
)
```

### ☎️ Solicitar Número de Teléfono (Request Phone Number)
```javascript
await conn.sendMessage(
  jid,
  {
    requestPhoneNumber: {}
  }
)
```

## 💬 Mensajes con Botones

### 🔘 Botones de Texto (Buttons)
```javascript
await conn.sendMessage(jid, {
  text: '📌 Elige uno:',
  buttons: [
    { buttonId: 'btn_1', buttonText: { displayText: '🔘 Botón 1' }, type: 1 },
    { buttonId: 'btn_2', buttonText: { displayText: '🔘 Botón 2' }, type: 1 }
  ],
  footer: '🔥 Ejemplo de footer'
})
```

### 🌐 Botones Interactivos (Native Flow)
```javascript
await conn.sendMessage(
  jid,
  {
    buttonReply: {
      body: '📥 ¿Cuál eliges?', 
      nativeFlows: {
        name: 'menu_options', 
        paramsJson: JSON.stringify({ id: 'menu_1', description: '📝 Descripción interactiva' }),
        version: 1
      }
    }, 
    type: 'interactive'
  }
)
```

### 🔘 Mensaje con Botones (Buttons Message)
```javascript
await conn.sendMessage(
  jid,
  {
    text: '📨 Este es un mensaje con botones!',
    caption: '🖼️ Usa si incluyes imagen/video',
    footer: '🔥 Saludos de José Elber!',
    buttons: [
      { 
        buttonId: 'btn1', 
        buttonText: { displayText: '🔘 Botón 1' }
      },
      { 
        buttonId: 'btn2', 
        buttonText: { displayText: '🔘 Botón 2' }
      },
      { 
        buttonId: 'btn3', 
        buttonText: { displayText: '🔘 Botón 3' }
      }
    ]
  }
)
```

### 📋 Mensaje de Lista (Buttons List Message)
```javascript
await conn.sendMessage(
  jid,
  {
    text: '📑 Esta es una lista de opciones!',
    footer: '🔥 Presentado por José Elber',
    title: '📌 Título de la Lista',
    buttonText: '🔽 Haz clic para ver opciones',
    sections: [
      {
        title: '📂 Sección 1',
        rows: [
          { title: '✅ Opción 1', rowId: 'opcion1' },
          { title: '✅ Opción 2', rowId: 'opcion2', description: 'ℹ️ Descripción Opción 2' }
        ]
      },
      {
        title: '📂 Sección 2',
        rows: [
          { title: '✅ Opción 3', rowId: 'opcion3' },
          { title: '✅ Opción 4', rowId: 'opcion4', description: 'ℹ️ Descripción Opción 4' }
        ]
      }
    ]
  }
)
```

### 🛍️ Lista de Productos (Buttons Product List Message)
```javascript
await conn.sendMessage(
  jid,
  {
    text: '🛒 Esta es una lista de productos!',
    footer: '🔥 Enviado por José Elber',
    title: '🍟 Elige Productos Destacados',
    buttonText: '📦 Ver Lista de Productos',
    productList: [
      {
        title: '🧁 Categoría Principal',
        products: [
          { productId: '1234' },
          { productId: '5678' }
        ]
      }
    ],
    businessOwnerJid: '519xxx@s.whatsapp.net',
    thumbnail: 'https://example.jpg'
  }
)
```

### 🃏 Mensaje de Tarjetas (Buttons Cards Message)
```javascript
await conn.sendMessage(
  jid,
  {
    text: '📢 Contenido Principal',
    title: '🗂️ Título Principal',
    subtile: '📌 Subtítulo Opcional',
    footer: '🔥 Footer del Mensaje',

    cards: [
      {
        image: { url: 'https://example.jpg' },
        title: '🖼️ Título de Tarjeta',
        body: '📝 Contenido de Tarjeta',
        footer: '📍 Footer de Tarjeta',
        buttons: [
          {
            name: 'quick_reply',
            buttonParamsJson: JSON.stringify({
              display_text: '💬 Botón Rápido',
              id: 'ID_BOTON_1'
            })
          },
          {
            name: 'cta_url',
            buttonParamsJson: JSON.stringify({
              display_text: '⚡️ Visitar Sitio',
              url: 'https://www.example.com'
            })
          }
        ]
      },
      {
        video: { url: 'https://example.mp4' },
        title: '🎥 Título de Tarjeta Video',
        body: '📝 Descripción',
        footer: '📍 Footer de Tarjeta',
        buttons: [
          {
            name: 'quick_reply',
            buttonParamsJson: JSON.stringify({
              display_text: '⚡ Respuesta Rápida',
              id: 'ID_BOTON_2'
            })
          },
          {
            name: 'cta_url',
            buttonParamsJson: JSON.stringify({
              display_text: '🔎 Ver Más',
              url: 'https://www.example.com'
            })
          }
        ]
      }
    ]
  }
)
```

### 🔘 Mensaje de Plantilla (Buttons Template Message)
```javascript
await conn.sendMessage(
  jid,
  {
    text: '✨ Este es un mensaje de plantilla!',
    footer: '🔥 Enviado por José Elber',
    templateButtons: [
      {
        index: 1,
        urlButton: {
          displayText: '🌐 Seguir Canal',
          url: 'https://whatsapp.com/channel/0029Vb4cQJu2f3EB7BS7o11M'
        }
      },
      {
        index: 2,
        callButton: {
          displayText: '📞 Llamarme!',
          phoneNumber: '519xxxx'
        }
      },
      {
        index: 3,
        quickReplyButton: {
          displayText: '💬 Respuesta Rápida',
          id: 'id-boton-respuesta'
        }
      }
    ]
  }
)
```

### 🌸 Mensaje Interactivo (Interactive Buttons)
```javascript
await conn.sendMessage(
  jid,
  {
    text: '✨ Este es un mensaje interactivo!',
    title: '👋 Hola!',
    subtitle: '🌼 Subtítulo aquí',
    footer: '🔥 Enviado por José Elber',
    interactiveButtons: [
      {
        name: 'quick_reply',
        buttonParamsJson: JSON.stringify({
          display_text: '🔁 Hazme Clic!',
          id: 'tu_id'
        })
      },
      {
        name: 'cta_url',
        buttonParamsJson: JSON.stringify({
          display_text: '🌐 Visitar Canal',
          url: 'https://whatsapp.com/channel/0029Vb4cQJu2f3EB7BS7o11M',
          merchant_url: 'https://whatsapp.com/channel/0029Vb4cQJu2f3EB7BS7o11M'
        })
      },
      {
        name: 'cta_copy',
        buttonParamsJson: JSON.stringify({
          display_text: '📋 Copiar Enlace',
          copy_code: 'https://whatsapp.com/channel/0029Vb4cQJu2f3EB7BS7o11M'
        })
      },
      {
        name: 'cta_call',
        buttonParamsJson: JSON.stringify({
          display_text: '📞 Llamar',
          phone_number: '519xxxx'
        })
      },
      {
        name: 'single_select',
        buttonParamsJson: JSON.stringify({
          title: '🔽 Elegir Opción',
          sections: [
            {
              title: '🍟 Opciones Principales',
              highlight_label: '💖 Recomendado',
              rows: [
                {
                  header: '📝 Encabezado 1',
                  title: '✨ Opción 1',
                  description: '🍓 Descripción 1',
                  id: 'id1'
                },
                {
                  header: '📝 Encabezado 2',
                  title: '✨ Opción 2',
                  description: '🍓 Descripción 2',
                  id: 'id2'
                }
              ]
            }
          ]
        })
      }
    ]
  }
)
```

### 📸 Con Imagen
```javascript
await conn.sendMessage(
  jid,
  {
    image: { url: 'https://example.jpg' },
    caption: '✨ Contenido',
    title: '🖼️ Título',
    subtitle: '📌 Subtítulo',
    footer: '🔥 Footer',
    interactiveButtons: [ /* botones como arriba */ ],
    hasMediaAttachment: false
  }
)
```

#### 🎥 Con Video
```javascript
await conn.sendMessage(
  jid,
  {
    video: { url: 'https://example.mp4' },
    caption: '🎬 Contenido Video',
    title: '📺 Título',
    subtitle: '📌 Subtítulo',
    footer: '🔥 Footer',
    interactiveButtons: [ /* botones como arriba */ ],
    hasMediaAttachment: false
  }
)
```

#### 📄 Con Documento
```javascript
await conn.sendMessage(
  jid,
  {
    document: { url: 'https://example.jpg' },
    mimetype: 'image/jpeg',
    jpegThumbnail: await conn.resize('https://example.jpg', 320, 320),
    caption: '📝 Contenido Documento',
    title: '📄 Título',
    subtitle: '📌 Subtítulo',
    footer: '🔥 Footer',
    interactiveButtons: [ /* botones como arriba */ ],
    hasMediaAttachment: false
  }
)
```

#### 📍 Con Ubicación
```javascript
await conn.sendMessage(
  jid,
  {
    location: {
      degreesLatitude: -6.2,
      degreesLongitude: 106.8,
      name: 'Jose HQ'
    },
    caption: '📍 Ven aquí!',
    title: '🗺️ Ubicación',
    subtitle: '📌 Subtítulo',
    footer: '🧭 Mapa',
    interactiveButtons: [ /* botones como arriba */ ],
    hasMediaAttachment: false
  }
)
```

#### 🛍️ Con Producto
```javascript
await conn.sendMessage(
  jid,
  {
    product: {
      productImage: { url: 'https://example.jpg' },
      productId: '836xxx',
      title: '🎁 Producto Destacado',
      description: '🛒 Descripción del producto',
      currencyCode: 'IDR',
      priceAmount1000: '283000',
      retailerId: 'JoseStore',
      url: 'https://example.com',
      productImageCount: 1
    },
    businessOwnerJid: '519xxx@s.whatsapp.net',
    caption: '🛍️ Nuevo producto disponible!',
    title: '📦 Nombre Producto',
    subtitle: '📌 Subtítulo',
    footer: '📋 Info Producto',
    interactiveButtons: [ /* botones como arriba */ ],
    hasMediaAttachment: false
  }
)
```

### 💳 Enviar Botón "Copiar Clave Pix"
```javascript
await conn.sendMessage(
  jid,
  {
    text: '',
    interactiveButtons: [
      {
        name: 'payment_info',
        buttonParamsJson: JSON.stringify({
          payment_settings: [{
            type: "pix_static_code",
            pix_static_code: {
              merchant_name: 'xrljose',
              key: 'example@xrljose.com',
              key_type: 'EMAIL'
            }
          }]
        })
      }
    ],
  }
)
```

### 🏷️ Mencionar en Estado (Status Mentions)
```javascript
await conn.sendStatusMentions(
  jid, 
  {
    image: {
      url: 'https://example.com.jpg'
    }, 
    caption: '✨ Hola desde Jose!'
  }
)
```

### 📚 Álbum de Mensajes (Send Album Message)
```javascript
await conn.sendAlbumMessage(
  jid,
  [
    {
      image: { url: 'https://example.jpg' }, 
      caption: 'Imagen 1'
    },
    {
      image: Buffer, 
      caption: 'Imagen 2'
    },
    {
      video: { url: 'https://example.mp4' }, 
      caption: 'Video 1'
    }, 
    {
      video: Buffer, 
      caption: 'Video 2'
    }
  ],
  { 
    quoted: message,
    delay: 2000
  }
)
```

### 🛍️ Mensaje de Tienda (Shop Message)
```javascript
await conn.sendMessage(
  jid, 
  {      
    text: 'Cuerpo del mensaje',
    title: 'Nombre Tienda', 
    subtitle: 'Subtítulo', 
    footer: 'Por Jose',
    shop: {
      surface: 1,
      id: 'https://example.com'
    }, 
    viewOnce: true
  }
)
```

### 📚 Mensaje de Colección (Collection Message)
```javascript
await conn.sendMessage(
  jid, 
  {
    text: 'Contenido',
    title: 'Título Colección',
    subtitle: 'Subtítulo',
    footer: 'Por José Elber',
    collection: {
      bizJid: '519xxx@s.whatsapp.net', 
      id: 'https://example.com', 
      version: 1
    },
    viewOnce: true
  }
)
```

### 🌐 Vista Previa de Enlace (Link Preview)
```javascript
await conn.sendMessage(
  jid,
  {
    text: 'Hola! Esto viene de https://github.com/whiskeyconnets/baileys'
  }
)
```

### 🎞️ Mensajes Multimedia (Media Messages)

#### 🌀 GIF
```javascript
await conn.sendMessage(
  jid,
  {
    video: fs.readFileSync('Media/ma_gif.mp4'),
    caption: 'Hola desde GIF!',
    gifPlayback: true
  }
)
```

#### 🎥 Video
```javascript
await conn.sendMessage(
  jid,
  {
    video: { url: './Media/ma_video.mp4' },
    caption: 'Este es el video'
  }
)
```

#### 🔵 Video PTV (Picture to Video)
```javascript
await conn.sendMessage(
  jid,
  {
    video: { url: './Media/ma_video.mp4' },
    ptv: true
  }
)
```

#### 🔊 Audio
```javascript
await conn.sendMessage(
  jid,
  {
    audio: { url: './Media/audio.ogg' },
    mimetype: 'audio/ogg; codecs=opus'
  }
)
```

#### 🖼️ Imagen
```javascript
await conn.sendMessage(
  jid,
  {
    image: { url: './Media/ma_img.png' },
    caption: 'Hola desde imagen!'
  }
)
```

#### 👁️ Ver Una Vez (View Once)
```javascript
await conn.sendMessage(
  jid,
  {
    image: { url: './Media/ma_img.png' },
    viewOnce: true,
    caption: 'Solo se ve una vez'
  }
)
```

## ✏️ Modificar Mensajes

### 🗑️ Eliminar Mensaje (Para Todos)
```javascript
const msg = await conn.sendMessage(jid, { text: 'Hola mundo' })
await conn.sendMessage(jid, { delete: msg.key })
```

### 📝 Editar Mensaje
```javascript
await conn.sendMessage(jid, {
  text: 'Texto actualizado aquí',
  edit: response.key
})
```

## 📨 Broadcast & Estados

### 📨 Enviar Broadcast & Estado (Stories)
```javascript
await conn.sendMessage(
  jid,
  {
    image: {
      url: url
    },
    caption: 'Hola desde broadcast!'
  },
  {
    backgroundColor: '#ffffff',
    font: 'default',
    statusJidList: ['519xxx@s.whatsapp.net'],
    broadcast: true
  }
)
```

### 🔍 Obtener Info de Lista Broadcast
```javascript
let bList = await conn.getBroadcastListInfo('1234@broadcast')
console.log(`Nombre lista: ${bList.name}, Destinatarios: ${bList.recipients}`)
```

## 🛠️ Funcionalidades Personalizadas
```javascript
function enviarNotificacionAGrupos(listaGrupos, mensaje) {
  for (const jid of listaGrupos) {
    conn.sendMessage(jid, { text: mensaje })
  }
}
```

> 💡 Consejos:
> Usa el evento `conn.ev.on()` para capturar todos los eventos importantes como `messages.upsert`, `contacts.update`, `group-participants.update`, etc.

## 🐞 Activando el Log Debug de WhatsApp

### 🔧 Cómo activar el Log `debug`

Para ver el registro crudo del WebSocket de WhatsApp, puedes activar el logger durante la inicialización de la conexión:

```javascript
import P from 'pino'

const conn = makeWAconnet({
  logger: P({ level: 'debug' }) // activa el nivel debug
})
```

> ⚠️ **Advertencia:**  
> ¡La salida `debug` es muy extensa! Úsala solo cuando necesites resolver problemas o explorar funciones ocultas.

## 📡 Cómo WhatsApp se comunica con nosotros

> 💡 WhatsApp usa un cifrado E2E complejo. Para entender el flujo, debes estudiar:  
> - [Protocolo LibSignal](https://signal.org/docs/)  
> - [Protocolo Noise](https://noiseprotocol.org/)  
> - Serialización basada en protobuf y formato `WAMessage`.

### 📊 Ejemplo práctico: Monitoreo de batería del dispositivo

Si has activado el log `debug`, podrás ver tráfico interno como este:

```json
{
  "level": 10,
  "fromMe": false,
  "frame": {
    "tag": "ib",
    "attrs": {
      "from": "@s.whatsapp.net"
    },
    "content": [
      {
        "tag": "edge_routing",
        "attrs": {},
        "content": [
          {
            "tag": "routing_info",
            "attrs": {},
            "content": {
              "type": "Buffer",
              "data": [8, 2, 8, 5]
            }
          }
        ]
      }
    ]
  },
  "msg": "communication"
}
```

- Normalmente los mensajes con `tag: ib` son **beacons internos** del dispositivo o servidor.
- Puedes capturar y **analizar el buffer `data[]`** para ver si contiene información de batería, señal, dispositivo, etc.

### 🧩 Estructura de `frame` en los mensajes de WhatsApp

Cada mensaje enviado o recibido vía WebSocket de WhatsApp usa una **estructura de frame** con tres partes principales:

| Componente | Descripción |
|----------|-----------|
| `tag` | Indica el tipo de contenido o propósito del mensaje, ej: `'message'`, `'iq'`, `'presence'`, `'call'`, `'receipt'` |
| `attrs` | Objeto con pares clave-valor (metadatos) como ID, hora, dispositivo o información de sesión |
| `content` | Contenido principal del mensaje, puede ser un array de nodos, buffer u objeto de datos |

### ⚙️ Manejando el Evento `webconnet` / Manejador Low-Level CB

Si quieres **interceptar mensajes crudos** del WebSocket, usa el callback `conn.ws.on()`:

```javascript
// todos los mensajes con tag 'edge_routing'
conn.ws.on('CB:edge_routing', (node) => {
  console.log(node)
})

// mensajes con tag 'edge_routing' & id = abcd
conn.ws.on('CB:edge_routing,id:abcd', (node) => {
  console.log('Filtrar ID = abcd:', node)
})

// mensajes con tag 'edge_routing', id = abcd, y primer nodo es 'routing_info'
conn.ws.on('CB:edge_routing,id:abcd,routing_info', (node) => {
  console.log('Coincidencia con routing_info:', node)
})
```

> 🧠 Todos los tags, atributos y contenido de `node` se envían en formato **WABinaryNode**.  
> Puedes describir el formato del nodo con `util.inspect(node, false, null, true)` si quieres registrarlo con colores.

### 📡 Ejemplo de Uso Avanzado

Por ejemplo, si quieres monitorear cambios de red, edge routing o sincronización de estado:

```javascript
conn.ws.on('CB:edge_routing', ({ tag, attrs, content }) => {
  if (content?.[0]?.tag === 'routing_info') {
    console.log('Información de Routing Recibida:', content[0])
  }
})
```

Esto puede ser útil para funciones como:
- Estado de batería del dispositivo
- Conexión multi-dispositivo
- Depuración de distribución de tráfico y socket fallback

## 🌸 ¡Arigatou ne~!

¡Llegaste al final de la documentación~!  
Espero que todas las funciones que leíste sean útiles para tu proyecto~  
Si aún tienes dudas, únete al grupo de WhatsApp para preguntar~ 🫶🏻✨

> 📖 Esta documentación fue creada por aburrimiento, ¡ánimo con el código y no olvides comer! 🍓

**💌 Contacto & Ayuda:**  
🧠 [GitHub](github.com/xrljose)
📱 [Únete al grupo de WA](https://chat.whatsapp.com/EteP5pnrAZC14y9wReGF1V)

✨ powered by : `JoseXrl15k` 😈