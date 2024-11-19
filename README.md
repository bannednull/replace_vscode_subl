# Guía para usar Sublime Text
VS Code, aunque popular, se ha convertido en una experiencia frustrante para mí. El alto consumo de memoria con unos pocos plugins y cero configuraciones lo hace sentir como una patada en los webos. Por eso decidí darle otra oportunidad a Sublime Text 4 en mi flujo de trabajo con Next.js. Para mi sorpresa, redescubrí lo ágil que es este editor, algo que realmente extraño en VS Code.

### Lo que realmente busco en un editor:
1. Comprobación de tipos TypeScript
2. Integración con ESLint y Prettier para mantener un código limpio y consistente.
3. Emmet para escribir HTML más rápido (aún en proceso).

> **Nota:** Asegúrate de tener Sublime Text 4 instalado y el control de paquetes habilitado antes de continuar.

### Configuración de TypeScript

#### Paso 1: Instalar el Protocolo de Servidor de Lenguaje (LSP)
Este paquete proporciona una integración con servidores de lenguaje para varias tecnologías, incluyendo TypeScript.

1. Abre el panel de comandos con `CTRL + SHIFT + P`
2. Selecciona Package Control: Install Package.
3. Busca e instala LSP.

#### Paso 2: Instalar el servidor de lenguaje de TypeScript
1. Abre nuevamente el panel de comandos con `CTRL + SHIFT + P`
2. Selecciona Package Control: Install Package.
3. Busca e instala LSP-typescript.

Esto habilitará la comprobación de tipos y otras características útiles de TypeScript en Sublime Text.

-------------

### Integración de ESLint y Prettier
Personalmente, combino Prettier y ESLint para simplificar el proceso de mantener mi código limpio. Además, uso eslint-config-prettier para evitar conflictos entre ambos.

#### Paso 1: Instalar Prettier
1. Abre el panel de comandos con `CTRL + SHIFT + P`
2. Selecciona Package Control: Install Package.
3. Busca e instala JsPrettier.

#### Paso 2: Instalar ESLint con SublimeLinter
1. Abre el panel de comandos con `CTRL + SHIFT + P`
2. Selecciona Package Control: Install Package.
3. Busca e instala SublimeLinter-eslint.

> **Nota:** Esta configuración requiere que ESLint esté disponible en tu entorno local

### Atajos personalizados
También configuré algunos atajos que se adaptan a mi flujo de trabajo. Estos son:
```json
[
	{"keys": ["ctrl+alt+f"], "command": "lsp_format_document"},
	{"keys": ["ctrl+."], "command": "lsp_code_actions"}
]
```
`Ctrl + Alt + F`: Formatea el documento usando LSP.

`Ctrl + .`: Muestra las acciones de código disponibles en el contexto actual (por ejemplo, correcciones rápidas).

Para configurar estos atajos, simplemente agrégalos al archivo de configuración de teclas de Sublime Text:

Ve a Preferences > Key Bindings.

Copia y pega el bloque anterior en el archivo User Key Bindings.


Sublime Text 4, con estas configuraciones, se convierte en una alternativa ligera y poderosa para trabajar con TypeScript, ESLint y Prettier. Aunque aún estoy ajustando algunos detalles como la integración con Emmet, ya siento la diferencia en velocidad y fluidez comparado con VS Code.


