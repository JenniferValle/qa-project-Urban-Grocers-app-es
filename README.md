# Proyecto Urban Grocers
﻿# Urban Grocers – Automatización de Pruebas de API  
**JENNIFER VALL – Sprint 8 (TripleTen QA Engineer Bootcamp)**

## 🧪 Descripción del Proyecto

Este proyecto automatiza pruebas para el endpoint `/api/v1/kits` de la aplicación Urban Grocers, enfocándose en la validación del campo `name`. Las pruebas se desarrollaron con **Python** y el framework **Pytest**.

El objetivo principal es verificar que el backend acepte solo valores válidos y rechace adecuadamente los datos incorrectos, según los requisitos funcionales del sistema.

---

## 📁 Estructura del Proyecto
```bash
qa-project-Urban-Grocers-app-es/
│
├── create_kit_name_kit_test.py # Pruebas de validación para el campo 'name'
├── data.py # Datos de entrada para los distintos escenarios de prueba
├── sender_stand_request.py # Funciones auxiliares para enviar solicitudes a la API
├── .gitignore # Excluye archivos temporales y entornos virtuales
└── README.md # Este archivo
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

## 📦 Instalación de Dependencias
Este proyecto utiliza Pytest. Puedes instalarlo directamente con:
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

## 📌 Reglas para ejecutar las pruebas
Ubicación: Las pruebas deben ejecutarse desde la raíz del proyecto, donde está ubicado create_kit_name_kit_test.py.

## Dependencias internas:
El archivo sender_stand_request.py se encarga de obtener el token de autenticación y enviar las solicitudes al endpoint.

El archivo data.py contiene los valores utilizados en cada prueba, para facilitar el mantenimiento y evitar duplicación de código.

Pruebas negativas: Algunas pruebas están diseñadas para fallar si el backend no valida correctamente el campo name. Esto refleja un problema del backend, no de tu código.

Mensajes auxiliares: El sistema imprime en consola los tokens generados (authToken generado: ...). Esto es solo para fines de monitoreo, no afecta la ejecución de las pruebas.

Cobertura de Casos: Se prueban valores válidos, vacíos, demasiado largos, tipo incorrecto, ausencia del campo, caracteres especiales y combinaciones límite (511 y 512 caracteres).
