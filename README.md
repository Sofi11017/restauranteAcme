# 🍽️ Sistema de Facturación - Restaurante ACME

Sistema de consola desarrollado en **Python** para la administración integral, facturación y control de ventas del **Restaurante ACME**, con persistencia de datos mediante archivos **CSV**.

---

## 👥 Integrantes del Equipo

- **Sofia Salazar**
- **Brenda Carrillo**
- **Crisbely Graterol**

---

## 📌 Descripción General

El sistema permite automatizar las operaciones diarias del restaurante a través de un menú interactivo en consola. Facilita la administración de productos, mesas y clientes, así como la emisión de facturas detalladas con cálculo automático del **19% de IVA** y el registro histórico de las ventas realizadas.

---

## 📂 Estructura del Proyecto

```text
restauranteAcme/
├── funciones.py                 # Lógica de negocio, validaciones y manejo de archivos CSV
├── restaurante_acme.py          # Menú principal y punto de entrada de la aplicación
├── Proyecto_Facturacion_Python/ # Copia modular del sistema de facturación
│   ├── funciones.py
│   └── restaurante_acme.py
├── Clientes.csv                 # Base de datos de clientes registrados (CSV)
├── Mesas.csv                    # Base de datos de mesas disponibles (CSV)
├── Producto.csv                 # Catálogo de productos y precios (CSV)
├── ventas.csv                   # Registro histórico acumulado de ventas (CSV)
├── factura.csv                  # Archivo generado con el detalle de la última factura
└── README.md                    # Documentación del proyecto
```

---

## ⚙️ Funcionalidades del Sistema

El sistema ofrece las siguientes opciones desde el menú principal:

### 1. 🍔 Ver / Agregar Productos
- **Agregar producto:** Permite registrar nuevos ítems con código, nombre y valor unitario.
- **Ver productos:** Lista el catálogo de productos disponibles con su código y nombre.

### 2. 🪑 Ver / Agregar Mesas
- **Agregar mesas:** Registra mesas identificadas por código, nombre/número y capacidad de puestos.
- **Ver mesas:** Consulta las mesas configuradas en el establecimiento.

### 3. 👤 Ver / Registrar Clientes
- **Agregar cliente:** Permite registrar clientes con código, nombre completo, teléfono y correo electrónico.
- **Ver clientes:** Lista todos los clientes con su información de contacto.

### 4. 🧾 Crear Factura
- Asocia una venta a una **mesa** y un **cliente** previamente registrados.
- Permite agregar múltiples productos indicando la cantidad deseada.
- Calcula automáticamente:
  - **IVA (19%)** por producto.
  - **Subtotal** por ítem.
  - **Total de productos** acumulados.
  - **Total general a pagar**.
- Permite guardar la factura detallada en `factura.csv` y registrar automáticamente la transacción en `ventas.csv`.

### 5. 📈 Registro de Ventas
- Muestra el historial completo de ventas realizadas, incluyendo fecha y hora, nombre de la mesa, nombre del cliente y monto total facturado.

### 6. 🚪 Salir
- Finaliza la ejecución del programa de manera segura.

---

## 🚀 Requisitos e Instalación

### Requisitos
- **Python 3.8+**
- Módulos estándar de Python (`csv`, `datetime`) — no requiere dependencias externas.

### Ejecución

1. Clona o descarga el repositorio:
   ```bash
   git clone https://github.com/Sofi11017/restauranteAcme.git
   cd restauranteAcme
   ```

2. Ejecuta el archivo principal:
   ```bash
   python3 restaurante_acme.py
   ```

---

## 📊 Formato de Datos Almacenados

| Archivo | Campos / Encabezados |
| :--- | :--- |
| `Producto.csv` | `codigo`, `nombre`, `valor`, `IVA` |
| `Mesas.csv` | `codigo`, `nombre`, `puestos` |
| `Clientes.csv` | `codigo`, `nombre`, `telefono`, `correo` |
| `ventas.csv` | `fecha`, `mesa`, `cliente`, `total` |
| `factura.csv` | Detalle formateado con fecha, cliente, mesa, desglose de ítems e importes |

---

## 🛠️ Tecnologías Utilizadas

- **Lenguaje:** Python 3
- **Persistencia:** Archivos CSV (`DictReader` y `DictWriter`)
- **Control de Versiones:** Git & GitHub

