# Proyecto Urban Grocers
﻿# Urban Grocers – Automatización de Pruebas de API  
**JENNIFER VALLE – Sprint 8 - cohort 38- (TripleTen QA Engineer Bootcamp)**

## 🧪 Descripción del Proyecto

Este proyecto automatiza pruebas para el endpoint /api/v1/kits de la aplicación Urban Grocers, centrándose en la validación del campo name. Las pruebas se implementaron utilizando Python junto con el framework Pytest.

El propósito principal es comprobar que el backend acepte únicamente valores correctos y rechace apropiadamente los datos inválidos, conforme a los requisitos funcionales del sistema.
---

## 📁 Estructura del Proyecto
```bash
qa-project-Urban-Grocers-app-es/
│
├── create_kit_name_kit_test.py # Pruebas de validación para el campo 'name'
├── data.py # Datos de entrada para cada escenarios de prueba
├── sender_stand_request.py # Funciones auxiliares para enviar solicitudes a la API
├── .gitignore # Excluye archivos temporales y entornos virtuales
└── README.md # Este Documento
```

---

## ⚙️ Configuración del Entorno

1. Asegúrate de tener **Python 3.10+** instalado en tu sistema.

2. Crea y activa un entorno virtual:


## Crear entorno virtual
```bash
python -m venv venv
```

Activar en Windows
```bash
venv\Scripts\activate
```

Activar en Linux/Mac
```bash
source venv/bin/activate
```
---

## 📌 Reglas para ejecutar las pruebas
Ubicación: Las pruebas deben ejecutarse desde la raíz del proyecto, donde está ubicado create_kit_name_kit_test.py.

Dependencias internas

sender_stand_request.py: gestiona la obtención del token de autenticación y el envío de solicitudes hacia el endpoint.

data.py: contiene los valores de entrada para todas las pruebas, lo que facilita el mantenimiento y evita repetir datos.

Comportamiento esperado

Pruebas negativas: Algunos test están pensados para fallar si el backend no valida correctamente el campo name. Esto indica un defecto del backend, no del código de pruebas.

Mensajes auxiliares: Se muestran tokens generados en consola (por ejemplo: authToken generado: ...). Son mensajes puramente informativos y no afectan la ejecución.

Cobertura: Se consideran casos válidos, vacíos, de longitud excesiva, tipo de dato incorrecto, ausencia del campo, caracteres especiales y valores límite (511 y 512 caracteres).

## 📦 Instalación de Dependencias
Este proyecto utiliza Pytest. Intentalo con:
```bash
pip install pytest
```

## Ejecución de Pruebas
Para ejecutar todas las pruebas, abre la terminal desde la raíz del proyecto y corre:
```bash
pytest
```

Para ver resultados más detallados:
```bash
pytest -v
```

También puedes ejecutar un archivo de pruebas específico, por ejemplo:
```bash
pytest create_kit_name_kit_test.py
```

---










