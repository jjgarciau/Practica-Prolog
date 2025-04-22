# Práctica Dos: Sistema de Consulta de Vehículos en Prolog

Un proyecto que permite consultar información sobre una base de datos de vehículos utilizando Prolog. Realiza búsquedas por marca, tipo de vehículo y presupuesto de forma eficiente.

## Integrantes

- **Juan José García Urrego**

- **María Isabel Gaviria Rendón**

## Descripción

Este proyecto implementa una base de conocimiento en Prolog para gestionar información de vehículos, permitiendo consultas flexibles con diferentes criterios. Cada vehículo contiene los siguientes atributos:

- **Marca**: Fabricante del vehículo (ej: Toyota, Ford).

- **Modelo**: Nombre específico del vehículo (ej: Corolla, F-150).

- **Tipo**: Categoría (sedán, SUV, camión, etc.).

- **Precio**: Valor numérico en dólares.

- **Año**: Año de fabricación.

## Funcionalidades Principales

### 1. Búsqueda por Presupuesto: `meet_budget/2`

```prolog

meet_budget(Ref, Presupuesto)

```

- **Descripción**: Encuentra modelos con precio **menor o igual** al presupuesto especificado.

- **Ejemplo**: `meet_budget(Ref, 25000)` muestra todos los vehículos con precio ≤ $25,000.

### 2. Búsqueda por Marca: `vehicles_by_brand/2`

```prolog

vehicles_by_brand(Marca, Modelos)

```

- **Descripción**: Obtiene todos los modelos disponibles de una marca específica.

- **Ejemplo**: `vehicles_by_brand(toyota, Modelos)` lista todos los modelos Toyota.

### 3. Generación de Reportes: `generate_report/4`

```prolog

generate_report(Marca, Tipo, Presupuesto, Resultados)

```

- **Descripción**: Filtra vehículos combinando **marca**, **tipo** y **presupuesto**.

- **Ejemplo**: Reporte de SUVs Toyota con precio ≤ $30,000.

## Uso del proyecto

1. **Ingresa a prolog**: Ingresar a la página de [prolog](https://swish.swi-prolog.org/).

2. **Cargar el código del archivo**


## Ejemplos de Consultas

### Consulta básica con `meet_budget/2`

```prolog

?- meet_budget(Ref, 25000).

% Devuelve vehículos con precio ≤ $25,000

```

### Generar un reporte específico

```prolog

?- generate_report(toyota, suv, 30000, Resultados).

% Encuentra SUVs Toyota con precio ≤ $30,000

```

## Estructura de la Base de Datos

Los datos se almacenan como hechos de Prolog en el formato:

```prolog

vehicle(Marca, Modelo, Tipo, Precio, Año).

```

**Ejemplo real**:

```prolog

vehicle(toyota, corolla, sedan, 22000, 2022).

vehicle(ford, f-150, truck, 35000, 2023).

```