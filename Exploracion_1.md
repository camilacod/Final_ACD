## Seleccion
### No van
- CAP 100:
    - Todos menos ID_INFORMANTE, todos los ESPEC.
- CAP 200: Se quedan:
    - P209	15	Seguro de salud
    - P210_PSOC_01	16	Programas Sociales 1

- CAP 300 MPN:
    - P313.1_CONSUME_MMN
- CAP 300SUPL:
    - HOGAR,P314_OBTUVO_SUPL	P314_PRESENTA_SUPL	P314_AYER	P314_DIARIO	P314_N_DIAS. Tienen muchos vacios.
- CAP 300 A:
    - Todos menos P306 Y P307.
    - P306:Señora para usted, ¿Qué es la anemia?
    - P307:	Señora en los últimos 12 meses, algún personal de la salud le dijo que el niño tiene anemia
- CAP 300 B:
    - Se van las fechas: muchos nas.
    - Peso y talla hasta control 8.
    - P331, P332, P333, P334.
    -P331	86	En el último control CRED le explicaron sobre: Cómo es la alimentación de su niño según la edad
    - P332	87	En el último control CRED le explicaron sobre: Cómo dar las gotas de hierro o Multimicronutriente a su niño
    - P333	88	En el último control CRED le explicaron sobre: La importancia, conservación y las posibles molestias del Suplemento de hierro en su niño
    - P334	89	En el último control CRED le explicaron sobre: Cuáles son alimentos ricos en hierro
- CAP 300 C
- CAP 300D
    Transformaciones de columnas a clases.
    - P367	8	Le dio pecho (leche materna) al niño
    -  P368_TIEMPO	9	Después que nació el niño empezó recibir leche materna / Tiempo
    - P368_HORAS	10	Después que nació el niño empezó recibir leche materna / Horas
    - P368_DIAS	11	Después que nació el niño empezó recibir leche materna / Días
    - P369	12	Aún le está dando leche materna al niño
    - P370_MESES	13	Durante cuántos meses le dio usted leche materna al niño / Meses
    - P370_NS	14	Durante cuántos meses le dio usted leche materna al niño / NS/NR
    - P371_AGUA	59	Le dió usted ayer: Agua sola
    - P371_FORMULA	60	Le dió usted ayer: Fórmula infantil
    - P371_LECHE_ENVASADA	61	Le dió usted ayer: Leche envasada
    - P371_LECHE_VACA	62	Le dió usted ayer: Leche de vaca o cualquier otra leche
    - P371_JUGO	63	Le dió usted ayer: Jugo de fruta
    - P371_OTRO	64	Le dió usted ayer: Algún otro líquido (agua azucarada, te, café, refresco)
    - P371_CALDOS	65	Le dió usted ayer: Caldos
    - P371_NINGUNO	66	Le dió usted ayer: Ninguno
- CAP 400A PRENDAS: NADA
- CAP 400B PRENDAS: NADA
- CAP 400B: No tienen ID.

------
## Diccionario

- TABLE GENERAL_001:

    CONGLOME INT: Conglomerado,

    VIVIENDA INT: Vivienda,

    HOGAR INT: Hogar,

    ID CHAR(4):Codigo 2 digitos,

    ETAPA_VIDA INT: 1: nino,

    ALTITUD INT: msnm,

    SEXO INT: ,

    DEPARTAMENTO VARCHAR(255),

    CCPP VARCHAR(255),

    PROVINCIA VARCHAR(255),

    DISTRITO VARCHAR(255),

    RES_PESO INT,

    RES_TALLA INT,

    RES_HB INT,

    RES_FINAL INT,

    PRIMARY KEY (CONGLOME, VIVIENDA, ID)

---
- Dashboard
    1. Heatmap geoespacial: departamento, provincia, distrito de los encuestados.
    Filtro. Dinamico.
    2. Tabla de conglomerados: Rural, Urbano, total, numero de evaluados.

    3. Barplot apilado. Eje x: Si NB, no NB (NECESIDADES_100). Dimension urbano, rural.
    4. Grouped Barplot  horizontal. Consume_suplementos (Si/No). Eje X: Anemia en los ultimos meses.
    5. Scatterplot. 8 controles. Control vs BMI. Sexo. Le dio pecho al ninhio
    6. Box plot. Edad en 3 grupos. 36 meses. Hemoglobina. 
    7. Alimentacion?
    8. Altitud.
    9. Educacion. 

NINOS POR CASA
----
Diagrama mas limpio. Icono datos abiertos. 

data marts
Extract: resumen de dataset,numeros, etc, tamanhio del data set. Diccionario del dataset. 
Load: Mostrar diagrama, subido en postgres, link. 

Transform: Detalle por items, limpieza, outliers
Si tableau tiene secciones. Datamart es un subtema. Todas las transformaciones son solo para eso. 

Insigghts: lo interesante. 
---
Para quien, lo interesante, el problema. 
Cuadro para diccionario 