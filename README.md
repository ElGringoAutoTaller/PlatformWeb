# AutoRepuesto El Gringo - Sistema de Gestión Integral

## 📌 Descripción General

**AutoRepuesto El Gringo** es un sistema de gestión integral desarrollado para un negocio que se dedica a:

1. La **compra y venta de repuestos automotrices**.
2. La **gestión de servicios de taller mecánico general**.
3. La **gestión de servicios de inyección electrónica y diagnóstico automotriz avanzado**.

Este sistema centraliza los procesos de **facturación**, **control de inventario**, **gestión de caja**, **clientes**, **proveedores** y más, en una única aplicación adaptada a las necesidades del negocio.

---

## 🎯 Objetivo General

Desarrollar un sistema de información que permita gestionar de forma eficiente los procesos de compra, venta y servicios automotrices de **AutoRepuesto El Gringo**, incluyendo el control de inventario, facturación por áreas de servicio, manejo de caja, seguimiento de clientes y proveedores.

---

## 🎯 Objetivos Específicos

- Implementar un módulo de **facturación** para las siguientes áreas:

  - Venta de repuestos al público.
  - Servicios del **taller automotriz**.
  - Servicios de **inyección electrónica y diagnóstico especializado**.

- Gestionar las **compras a distribuidores** y actualizar automáticamente el inventario.

- Registrar y administrar la **información de clientes** y **proveedores**.

- Controlar **ingresos y egresos de caja** con reportes diarios.

- Facilitar el seguimiento de los servicios prestados por **trabajadores del taller** y del área de diagnóstico.

---

## 🧱 Estructura del Proyecto (Base de Datos)

La base de datos central del proyecto se llama `AutoRepuestoElGringo` y contiene las siguientes tablas:

| Tabla        | Descripción                                                             |
| ------------ | ----------------------------------------------------------------------- |
| `abono`      | Registra pagos parciales (abonos) realizados por los clientes.          |
| `caja`       | Control de ingresos y egresos del dinero en caja.                       |
| `categoria`  | Categorías de productos/repuestos.                                      |
| `cliente`    | Datos de los clientes.                                                  |
| `compra`     | Compras realizadas a proveedores.                                       |
| `compradet`  | Detalle de cada compra (productos, cantidades, precios).                |
| `confimpret` | Configuraciones de impresión y datos de la empresa.                     |
| `egresocaja` | Registros de egresos de caja (compras, pagos, gastos operativos, etc.). |
| `producto`   | Lista de repuestos disponibles en inventario.                           |
| `proveedor`  | Datos de proveedores de repuestos.                                      |
| `usuario`    | Gestión de usuarios del sistema (empleados, administradores).           |
| `venta`      | Facturas emitidas a clientes (de repuestos o servicios).                |
| `ventadet`   | Detalles de los productos o servicios vendidos en cada factura.         |

## Actualizaciones del Código

```git


    echo "# PlatformRepo" >> README.md

    git init

    git add README.md

    git commit -m "first commit"

    git branch -M main

    git remote add origin https://github.com/ElGringoAutoTaller/PlatformRepo.git

    git push -u origin main
```

## 📌 Relaciones Clave

| Entidad |
Relacionada con |
Vía Campo
|
| ------------ | ----------------------------------------------------------------------- |
| `venta` | `ventadet` | `idventa` |
venta abono idventa
compra compradet idcompra
caja egresocaja id_caja
venta cliente, usuario idcliente, usuario
compra proveedor idProv

### 🔧 Estructura sugerida adicional

Para mejorar la organización y facilitar la facturación por área, se pueden agregar:

### `venta y ventadet:`

| Se puede usar para el área de repuestos exclusivamente. |

### `servicio:`

| Sería específico para taller e inyección. |

### `factura:`

| Sería el documento que unifica todo (productos y servicios) por cliente. |

### `abono:`

| Puede enlazarse con una factura para registrar pagos parciales. |
