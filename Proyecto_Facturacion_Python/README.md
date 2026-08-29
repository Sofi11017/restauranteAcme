# 🍽️ Sistema de Facturación - Restaurante ACME (Proyecto Facturación Python)

Sistema de consola desarrollado en **Python** para la administración, facturación y control de ventas del **Restaurante ACME**, con persistencia de datos mediante archivos **CSV**.

---

## 👥 Integrantes del Equipo

- **Sofia Salazar**
- **Brenda Carrillo**
- **Crisbely Graterol**

---

## 📌 Descripción General

El sistema permite automatizar las operaciones diarias del restaurante a través de un menú interactivo en consola. Facilita la administración de productos, mesas y clientes, así como la emisión de facturas detalladas con cálculo automático del **19% de IVA** y el registro histórico de las ventas realizadas.

---

## 📂 Archivos del Módulo

- **`restaurante_acme.py`**: Menú principal interactivo en bucle para navegar entre todas las opciones del sistema.
- **`funciones.py`**: Módulo de lógica de negocio, búsqueda por código, operaciones CRUD básicas y persistencia en CSV.

---

## ⚙️ Menú de Opciones

1. **Ver/agregar productos**: Registrar nuevos productos con código, nombre y valor o listar los existentes.
2. **Ver/agregar mesas**: Registrar mesas con código, nombre y número de puestos o ver el listado.
3. **Ver/registrar clientes**: Registrar clientes con código, nombre, teléfono y correo electrónico o consultar clientes.
4. **Crear factura**: Seleccionar mesa y cliente, agregar productos con cantidad, calcular el 19% de IVA y el total a pagar, y exportar la factura a `factura.csv` y registrar en `ventas.csv`.
5. **Registro de ventas**: Listar el historial de ventas registradas con fecha, mesa, cliente y total.
6. **Salir**: Cerrar la aplicación.

---

## 🚀 Ejecución

```bash
python3 restaurante_acme.py
```
