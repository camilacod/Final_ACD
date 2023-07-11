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

- ## <span style="color:orange">TABLE GENERAL_001</span>:

    CONGLOME INT: Conglomerado,

    VIVIENDA INT: Vivienda,

    HOGAR INT: Hogar,

    ID CHAR(4): ID del niño,

    ETAPA_VIDA INT: Etapa de vida, 1: Niño, 2: Adolescente, 3: Adulto Mayor,

    ALTITUD INT: Altitudmsnm,

    SEXO INT: Sexo, 1: Masculino, 2: Femenino,

    DEPARTAMENTO VARCHAR(255): Departamento,

    CCPP VARCHAR(255): Centro Poblado,

    PROVINCIA VARCHAR(255): Provincia, 

    DISTRITO VARCHAR(255): Distrito,

    RES_PESO INT: 1: Completo, 2: Ausente, 3: Rechazo, 4: No incluido,

    RES_TALLA INT: 1: Completo, 2: Ausente, 3: Rechazo, 4: No incluido,

    RES_HB INT: 1: Completo, 2: Ausente, 3: Rechazo, 4: No incluido,

    RES_FINAL INT: 1: Completa, 2: Incompleta, 3: Rechazo, 4: Ausente, 5: No se inicio entrevista, 6: Otro

    PRIMARY KEY (CONGLOME, VIVIENDA, ID)

- ## <span style="color:lime">NECESIDADES_100</span>:

    CONGLOME INT: Conglomerado, 

    VIVIENDA INT: Vivienda,

    ID CHAR(4): ID del niño,

    P101 INT: Tipo de vivienda, 1: Casa independiente, 2: Departamento en edificio, 3: Vivienda en quinta, 4: Vivienda en casa de vecindad (callejón, solar o corralón), 5: Choza o cabaña, 6: Vivienda improvisada, 7: Local no destinado para habitación humana, 8: Otro

    P102 INT: ¿Cuál es el material predominante en paredes exteriores?, 1: Ladrillo o bloque de cemento, 2: Piedra o sillar con cal o cemento, 3: Adobe o tapia, 4: Quincha (caña con barro), 5: Piedra con barro, 6: Madera, 7: Estera, 8: Otro, 9: Ninguno

    P103 INT: ¿Cuál es el material predominante en los techos de su vivienda?, 1: Concreto armado, 2: Madera, 3: Tejas, 4: Planchas de calamina, fibra de cemento o similares, 5: Caña o esteras con tortas de barro, 6: Esteras, 7: Pajas, hojas de palmeras, etc., 8: Cartón, plástico, tela, 9: Otro

    P104 INT: ¿Cuál es el material predominante de los pisos de su vivienda?, 1: Parquet o madera pulida, 2: Láminas asfálticas, vinílicos o similares, 3: Losetas, terrazos o similares, 4: Madera (entablados), 5: Cemento / Falso piso, 6: Tierra / Arena / Ripio, 7: Otro

    P105 INT: El abastecimiento de agua en su hogar habitualmente procede de:, 1: Red pública dentro de la vivienda, 2: Red pública fuera de la vivienda, 3: Pilón / Grifo público, 4: Pozo, 5: Río / Acequia / Manantial, 6: Camión tanque / Aguatero, 7: Otro

    P106 INT: El servicio higiénico de su hogar está conectado a:, 1: Red pública dentro de la vivienda, 2: Red pública fuera de la vivienda, 3: Pozo séptico, 4: Letrina (bajo pautas técnicas), 5: Pozo ciego o negro / Silo (orificio simple), 6: Río, acequia o canal, 7: Otro

    P107 INT: ¿Qué tipo de alumbrado tiene su hogar?, 1: Electricidad, 2: Gas licuado (GLP), 3: Gas natural (tubería), 4: Kerosone, 5: Vela, 6: Batería, 7: Otro

    P108 INT: Sin contar baño, cocina, pasadizos, ni garaje ¿Cuántas habitaciones son de uso de su hogar?,

    P109 INT: ¿Cuántas habitaciones usan en su hogar para dormir?,

    P110 INT: ¿Cuál es el combustible que utilizan más frecuentemente en su hogar para cocinar?, 1: Electricidad, 2: Gas licuado (GLP), 3: Gas natural (tubería), 4: Kerosone, 5: Carbón, 6: Leña, 7: Paja / Arbusto / Hierba, 8: Bosta (estiércol de animal), 9: Otro, 10: No cocina

    P111 INT: ¿Tiene en su hogar: Teléfono fijo, teléfono celular, cable, etc.?,

    P112 INT: ¿Tiene en su hogar: Radio, televisor a color, computadora, etc.?,

    P113_BICICLETA INT: ¿Algún miembro de su hogar tiene bicicleta / triciclo?, 1: Sí, 2: No, 3: NS,


    P113_MOTOCICLETA INT: ¿Algún miembro de su hogar tiene motocicleta?, 1: Sí, 2: No, 3: NS,

    P113_CARRO INT: ¿Algún miembro de su hogar tiene carro?, 1: Sí, 2: No, 3: NS,

    P113_OTRO INT: ¿Algún miembro de su hogar tiene otro medio de transporte?, 1: Sí, 2: No, 3: NS,

    P111_TEL_FIJO INT: ¿Tiene en su hogar: Teléfono fijo?, 1: Sí, 2: No, 3: NS,

    P111_TEL_CELULAR INT: ¿Tiene en su hogar: Teléfono celular?, 1: Sí, 2: No, 3: NS,

    P111_CABLE INT: ¿Tiene en su hogar: Cable?, 1: Sí, 2: No, 3: NS,

    P111_INTERNET INT: ¿Tiene en su hogar: Internet?, 1: Sí, 2: No, 3: NS,

    P112_RADIO INT: ¿Tiene en su hogar: Radio?, 1: Sí, 2: No, 3: NS,

    P112_TELEVISOR INT: ¿Tiene en su hogar: Televisor a color?, 1: Sí, 2: No, 3: NS,

    P112_COMPUTADORA INT: ¿Tiene en su hogar: Computadora?, 1: Sí, 2: No, 3: NS,

    P112_HORNO INT: ¿Tiene en su hogar: Horno microondas?, 1: Sí, 2: No, 3: NS,

    P112_LAVADORA INT: ¿Tiene en su hogar: Lavadora?, 1: Sí, 2: No, 3: NS,

    P112_REFRIGERADORA INT: ¿Tiene en su hogar: Refrigeradora / Congeladora?, 1: Sí, 2: No, 3: NS,

    P112_COCINA INT: ¿Tiene en su hogar: Cocina a gas?, 1: Sí, 2: No, 3: NS,

    P112_PLANCHA INT: ¿Tiene en su hogar: Plancha?, 1: Sí, 2: No, 3: NS,

    P112_EQUIPO INT: ¿Tiene en su hogar: Equipo de música?, 1: Sí, 2: No, 3: NS,

    PRIMARY KEY (CONGLOME, VIVIENDA, ID),

    FOREIGN KEY (CONGLOME, VIVIENDA, ID) REFERENCES GENERAL_001 (CONGLOME, VIVIENDA, ID)


- ## <span style="color:red">TABLE SEGURO_PS</span>:

    CONGLOME INT: Conglomerado,

    VIVIENDA INT: Vivienda,

    ID CHAR(4): ID del niño,

    P209 FLOAT: Seguro de salud, 1: EsSalud, 2: FFAA, 3: SIS, 4: Entidad Prestadora Salud EPS, 5: Seguro Privado, 6: No tiene, 7: NS/NR,

    P210_PSOC_01 FLOAT: Programas Sociales 1, 1: Cuna Más, 2: Vaso de leche, 3: Qali Warma, 4: Juntos, 5: Pensión 65, 6: Vuelve a sonreir, 7: Tayta Wasi, 8: Otros programas, 9: Ninguno, 10: NS/NR

    PRIMARY KEY (CONGLOME, VIVIENDA, ID)

    FOREIGN KEY (CONGLOME, VIVIENDA, ID) REFERENCES GENERAL_001 (CONGLOME, VIVIENDA, ID)

- ## <span style="color:Blueviolet">TABLE MICRONUTRIENTES_300</span>:

    CONGLOME INT: Conglomerado,

    VIVIENDA INT: Vivienda,

    ID CHAR(4): ID del niño,

    P313_1_CONSUME_MMN INT: Actualmente el niño consume Multimicronutrientes,
    1: Sí, 2: No,

    PRIMARY KEY (CONGLOME, VIVIENDA, ID),

    FOREIGN KEY (CONGLOME, VIVIENDA, ID) REFERENCES GENERAL_001 (CONGLOME, VIVIENDA, ID)

- ## <span style="color:Cornflowerblue">TABLE SUPLEMENTOS_300</span>:

    CONGLOME INT: Conglomerado,

    VIVIENDA INT: Vivienda,

    ID CHAR(4): ID del niño,

    P314_CONSUME_SUPL INT: Actualmente el niño consume Suplemento de hierro, 1: Sí, 2: No,

    P314_OBTUVO_SUPL FLOAT: Cómo obtuvo Suplemento de hierro, 1: Comprado, 2: Donado,

    P314_PRESENTA_SUPL FLOAT: La presentación del Suplemento de hierro es:, 1: Frasco, 2: Gotas,

    P314_AYER FLOAT: El día de ayer el niño consumió Suplemento de hierro, 1: Sí, 2: No,

    P314_DIARIO FLOAT: En la última semana, cuántos días ha consumido Suplemento de hierro / Diario, 1: Diario

    PRIMARY KEY (CONGLOME, VIVIENDA, ID),

    FOREIGN KEY (CONGLOME, VIVIENDA, ID) REFERENCES GENERAL_001 (CONGLOME, VIVIENDA, ID)

- ## <span style="color:Lightcyan">TABLE ANEMIA_300</span>:

    CONGLOME INT: Conglomerado,

    VIVIENDA INT: Vivienda,

    ID CHAR(4): ID del niño,

    P306 INT: Señora para usted, ¿Qué es la anemia?, 1: Es una enfermedad donde el niño se pone muy flaco, 2: Es una enfermedad en la que disminuye la hemoglobina de la sangre, 3: Es la deficiencia de vitaminas, 4: Es la deficiencia de calcio, 5: N/S o menciona una alternativa diferente a las anteriores, 6: NS/NR,

    P307 INT: Señora en los últimos 12 meses, algún personal de la salud le dijo que el niño tiene anemia, 1: Sí, 2: No, 3: NS/NR,

    P311 INT: Señora en los últimos 12 meses al niño le han hecho análisis para saber si tiene anemia, 1: Sí, 2: No, 3: NS/NR,

    P312 INT: Desde que nació el niño, cuántas veces se le ha realizado análisis para saber si tiene anemia,

    P313 INT: Señora alguna vez el niño ha consumido Suplemento de hierro, 1: Sí, 2: No, 3: NS/NR,

    P320 INT: Conoce usted, los alimentos ricos en hierro, 1: Sí, 2: No, 3: NS/NR,

    PRIMARY KEY (CONGLOME, VIVIENDA, ID),

    FOREIGN KEY (CONGLOME, VIVIENDA, ID) REFERENCES GENERAL_001 (CONGLOME, VIVIENDA, ID)

- ## <span style="color:Olivedrab">TABLE CRED_PESO_TALLA</span> :

    CONGLOME INT: Conglomerado,

    VIVIENDA INT: Vivienda,

    ID CHAR(4): ID del niño,

    P325_PESO_NAC FLOAT: Peso al nacer,

    P327_PESO_00 FLOAT: Control Recién Nacido / Peso,

    P327_TALLA_00 FLOAT: Control Recién Nacido / Talla,

    P327_PESO_01 FLOAT: Control N°01 / Peso,

    P327_TALLA_01 FLOAT: Control N°01 / Talla,

    P327_PESO_02 FLOAT: Control N°02 / Peso,

    P327_TALLA_02 FLOAT: Control N°02 / Talla,

    P327_PESO_03 FLOAT: Control N°03 / Peso,

    P327_TALLA_03 FLOAT: Control N°03 / Talla,

    P327_PESO_04 FLOAT: Control N°04 / Peso,

    P327_TALLA_04 FLOAT: Control N°04 / Talla,

    P327_PESO_05 FLOAT: Control N°05 / Peso,

    P327_TALLA_05 FLOAT: Control N°05 / Talla,

    P327_PESO_06 FLOAT: Control N°06 / Peso,

    P327_TALLA_06 FLOAT: Control N°06 / Talla,

    P327_PESO_07 FLOAT: Control N°07 / Peso,

    P327_TALLA_07 FLOAT: Control N°07 / Talla,

    P327_PESO_08 FLOAT: Control N°08 / Peso,

    P327_TALLA_08 FLOAT: Control N°08 / Talla,

    P327_PESO_09 FLOAT: Control N°09 / Peso,

    P327_TALLA_09 FLOAT: Control N°09 / Talla,

    P327_PESO_10 FLOAT: Control N°10 / Peso,

    P327_TALLA_10 FLOAT: Control N°10 / Talla,

    P331 FLOAT: En el último control CRED le explicaron sobre: Cómo es la alimentación de su niño según la edad, 1: Sí, 2: No, 3: NS/NR,

    P332 FLOAT: En el último control CRED le explicaron sobre: Cómo dar las gotas de hierro o Multimicronutriente a su niño, 1: Sí, 2: No, 3: NS/NR,

    P333 FLOAT: En el último control CRED le explicaron sobre: La importancia, conservación y las posibles molestias del Suplemento de hierro en su niño, 1: Sí, 2: No, 3: NS/NR,

    P334 FLOAT: En el último control CRED le explicaron sobre: Cuáles son alimentos ricos en hierro, 1: Sí, 2: No, 3: NS/NR,

    PRIMARY KEY (CONGLOME, VIVIENDA, ID),

    FOREIGN KEY (CONGLOME, VIVIENDA, ID) REFERENCES GENERAL_001 (CONGLOME, VIVIENDA, ID)

- ## <span style="color:Palegoldenrod">TABLE CRED_PESO_TALLA</span> :

    CONGLOME INT: Conglomerado,

    VIVIENDA INT: Vivienda,

    ID CHAR(4): ID del niño,

    P336 INT: Ha participado en una reunión de madres, donde el personal de salud preparaba alimentos con la finalidad de enseñarle, 1: Sí, 2: No, 3: NS/NR,

    P337 FLOAT: Cuántas veces el personal de salud le ha enseñado a preparar los alimentos para el niño, 1: Sí, 2: No, 3: NS/NR,

    P338 FLOAT: La última vez que asistió a una sesión demostrativa: Le enseñaron a preparar comidas espesas o segundo según la edad del niño, 1: Sí, 2: No, 3: NS/NR,

    P339 FLOAT: La última vez que asistió a una sesión demostrativa: Le enseñaron según la edad de su niño, qué cantidad y cuándo debe de comer, 1: Sí, 2: No, 3: NS/NR,

    P340 FLOAT: La última vez que asistió a una sesión demostrativa: Le enseñaron que su niño coma alimentos de origen animal ricos en hierro todos los días, 1: Sí, 2: No, 3: NS/NR,

    P341 FLOAT: La última vez que asistió a una sesión demostrativa: Le enseñaron que las preparaciones para su niño se acompañe con verduras y frutas de color, 1: Sí, 2: No, 3: NS/NR,
 
    P342 FLOAT: La última vez que asistió a una sesión demostrativa: Le enseñaron a incluir menestras en sus preparaciones, 1: Sí, 2: No, 3: NS/NR,

    P343 FLOAT: En la última semana, le han preparado al niño alguna comida que le enseñaron en la sesión demostrativa, 1: Sí, 2: No, 3: NS/NR,

    P344 FLOAT: Por qué motivo no han preparado alguna comida que le enseñaron en la sesión demostrativa, 1: No le gusta al niño, 2: Son muy costosas, 3: No puede obtener los ingredientes, 4: Otro, 5: NS/NR,


    P345_TIEMPO VARCHAR: Hace cuánto tiempo acudió al establecimiento de salud / Tiempo,

    P345_MESES FLOAT: Hace cuánto tiempo acudió al establecimiento de salud / Meses,

    P345_DIAS FLOAT: Hace cuánto tiempo acudió al establecimiento de salud / Días,

    P346 FLOAT: En esa oportunidad, el personal de salud le enseñó a usted junto a otras personas sobre algún tema para que su niño este sanito, 1: Sí, 2: No, 3: NS/NR,

    P347 FLOAT: Tema que le enseñó el personal de salud en esa ocasión: Lactancia materna, 1: Sí, 2: No, 3: NS/NR,

    P348 FLOAT: Tema que le enseñó el personal de salud en esa ocasión: Alimentación complementaria, 1: Sí, 2: No, 3: NS/NR,

    P349 FLOAT: Tema que le enseñó el personal de salud en esa ocasión: Suplementación con Multimicronutrientes, 1: Sí, 2: No, 3: NS/NR,

    P350 FLOAT: Tema que le enseñó el personal de salud en esa ocasión: Lactancia materna prolongada, 1: Sí, 2: No, 3: NS/NR,

    P351 FLOAT: Tema que le enseñó el personal de salud en esa ocasión: Anemia, 1: Sí, 2: No, 3: NS/NR,
    
    P352 FLOAT: Tema que le enseñó el personal de salud en esa ocasión: Desnutrición crónica, 1: Sí, 2: No, 3: NS/NR,

    PRIMARY KEY (CONGLOME, VIVIENDA, ID),

    FOREIGN KEY (CONGLOME, VIVIENDA, ID) REFERENCES GENERAL_001 (CONGLOME, VIVIENDA, ID)   

- ## <span style="color:Pink">TABLE ALIMENTACION_300</span>:

    CONGLOME INT: Conglomerado,

    VIVIENDA INT: Vivienda,

    ID CHAR(4): ID del niño,

    P367 INT: Le dio pecho (leche materna) al niño, 1: Sí, 2: No,

    P368_TIEMPO FLOAT: Después que nació el niño empezó recibir leche materna / Tiempo, 1: Inmediatamente, 2: Horas, 3: Días,

    P368_HORAS FLOAT: Después que nació el niño empezó recibir leche materna / Horas,

    P368_DIAS FLOAT: Después que nació el niño empezó recibir leche materna / Dias,

    P369 FLOAT: Aún le está dando leche materna al niño, 1: Sí, 2: No,

    P370_MESES FLOAT: Durante cuántos meses le dio usted leche materna al niño / Meses,

    P370_NS FLOAT: Durante cuántos meses le dio usted leche materna al niño / NS/NR, 1: No sabe

    P371 INT: Tipos de líquidos que el niño bebió ayer durante el día y la noche, 

    P371_AGUA INT: Le dió usted ayer: Agua sola, 1: Sí, 2: No,

    P371_FORMULA INT: Le dió usted ayer: Fórmula infantil, 1: Sí, 2: No,

    P371_LECHE_ENVASADA INT: Le dió usted ayer: Leche envasada, 1: Sí, 2: No,

    P371_LECHE_VACA INT: Le dió usted ayer: Leche de vaca o cualquier otra leche, 1: Sí, 2: No,

    P371_JUGO INT: Le dió usted ayer: Jugo de fruta, 1: Sí, 2: No,

    P371_OTRO INT: Le dió usted ayer: Algún otro líquido (agua azucarada, te, café, refresco), 1: Sí, 2: No,

    P371_CALDOS INT: Le dió usted ayer: Caldos, 1: Sí, 2: No,

    P371_NINGUNO INT: Le dió usted ayer: Ninguno, 1: Sí, 2: No,

    PRIMARY KEY (CONGLOME, VIVIENDA, ID),

    FOREIGN KEY (CONGLOME, VIVIENDA, ID) REFERENCES GENERAL_001 (CONGLOME, VIVIENDA, ID)


- ## <span style="color:Plum">TABLE RES_SIN_ID_400</span>:

    CONGLOME INT: Conglomerado,

    VIVIENDA INT: Vivienda,

    ID CHAR(4): ID del niño,

    P400 INT: Nació algún niño/niña después de la entrevista realizada por las encuestadoras del INEI, 1: Sí, 2: No,

    P402 INT: Sexo, 1: Masculino, 2: Femenino,

    P408_EDAD INT: Edad en meses,

    P408_AÑOS FLOAT: Edad / Años,

    P408_MESES INT: Edad / Meses,

    P409 FLOAT: Peso bruto (kilogramos),

    P410 FLOAT: Peso neto (kilogramos),

    P411 FLOAT: Prenda / Peso total (kilogramos),

    P412 FLOAT: Talla (centímetros),

    P413 FLOAT: Posición de la medición, 1: Parado, 2: Echado,

    P415 FLOAT: Hemoglobina (g/dl),

    P416_RES_PESO INT: Resultado de la antropometría / Peso, 1: Completo, 2: Ausente, 3: Rechazo, 4: No incluido,

    P416_RES_TALLA INT: Resultado de la antropometría / Talla, 1: Completo, 2: Ausente, 3: Rechazo, 4: No incluido,

    P416_RES_HB INT: Resultado de la antropometría / Hemoglobina, 1: Completo, 2: Ausente, 3: Rechazo, 4: No incluido,

    PRIMARY KEY (CONGLOME, VIVIENDA, ID),

    FOREIGN KEY (CONGLOME, VIVIENDA, ID) REFERENCES GENERAL_001 (CONGLOME, VIVIENDA, ID)



- ## <span style="color:Hotpink">TABLE FACTOR_ZONA</span>:

    CONGLOME INT: Conglomerado,

    VIVIENDA INT: Vivienda,

    ID CHAR(4): ID del niño,

    COD_DOMINIO BIGINT,

    DOMINIO VARCHAR(255),

    COD_ETAPADEVIDA BIGINT,

    ETAPADEVIDA VARCHAR(255),

    RESULTADOFINALDELAENCUESTACompleta1Incompleta2Rehazo3Otros6 INT,

    UBIGEO BIGINT,

    DEPARTAMENTO VARCHAR(255),

    PROVINCIA VARCHAR(255),

    DISTRITO VARCHAR(255),

    PRIMARY KEY (CONGLOME, VIVIENDA, ID),

    FOREIGN KEY (CONGLOME, VIVIENDA, ID) REFERENCES GENERAL_001 (CONGLOME, VIVIENDA, ID)    


---
- Dashboard
    1. Mapa geoespacial: departamento, provincia, distrito de los encuestados.
    Filtro. Dinamico.
    2. Tabla de conglomerados: Rural, Urbano, total, numero de evaluados.
---data_factor_sexo---
    3. Barplot apilado. Eje x: Si NB, no NB (NECESIDADES_100). Dimension urbano, rural.
    FALTA.

    4. Grouped Barplot  horizontal. Consume_suplementos (Si/No). Eje X: Anemia en los ultimos meses.
    FALTA PREPROCESAMIENTO Y TABLEAU

    5. Scatterplot. 8 controles. Control vs BMI. Sexo. Le dio pecho al ninhio
    EN PROCESO LIMPIEZA
    6. Box plot. Edad en 3 grupos. 36 meses. Hemoglobina. 
    FALTA TODO
    7. Alimentacion?
    8. Altitud.
    TUVE LA IDEA.
    9. Educacion. 
    HAY UNA IDEA. QUE VARIABLES SE NECESITAN.

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