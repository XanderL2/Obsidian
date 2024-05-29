
---
### Sintaxis:

**Propiedades:**

- df.shape: Ver Dimensiones
- df.columns: Ver las columnas
- df.dtypes: Ver Columnas con tipos de datos


**Acceder a Registros o Columnas (Por indice Iloc):**
- df.iloc[30] <--- A un solo registro
- df.iloc[30:40]   <---- A traves de Slices
- df.iloc[[30, 20]] <---- A muchos registros

**Acceder a Registros o Columnas (Por valor Loc):**

- df.loc[1,"nombre"] <--- Accederiamos a el nombre del primer registro


**Filtrado:**
- df.Query: Filtrado de columnas

    df.query("columna > 80") 


**Order y Agrupacion:**

- df.sort_values (Ordenar de Forma Asc y Desc)

    df.sort_values(by= "Edad", ascending=False) 

- df.head() / tail Limitar Registros:

    df.head(10) <-- Obtienes los 10 primeros registros contando desde el cero
    df.tail(10) <-- Obtienes los 10 ultimos registros contando desde el cero

- df.groupby (Agrupar registros):

    Funciones de agrupacion
        - Mean (Media una cada columna)
        - Max / MIn(Maximo / Minimo valor)
        - Sum (Suma)
        - Count (Conteo de registros)

    df.groupby("columanAgrupar")["columnaCompresion"].funcionAgrupacioj()



**Tratamiento de Columnas:**

- Crear Columna:

    df["nombreColumna"] = [valores]

- Crear columna a partir de otra:

    df["notasCiencias2"] = df["Nota_Ciencias"] 

