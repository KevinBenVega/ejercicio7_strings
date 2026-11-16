## REQUERIMIENTOS
¿Cómo debe funcionar el programa? 
El sistema pedirá al usuario ingresar una alternativa para una serie de preguntas:  
- Si la alternativa  es correcta, se señalara como "Respuesta correcta"
- Si la alternativa  es incorrecta se señalara como  "Respuesta incorrecta, la respuesta correcta es: d"
- Si la alternativa no existe se señalara como: "Respuesta no valida"

¿Qué hace el programa?
- Guardara la respuesta
- Analiza la respuesta
- Responde adecuadamente 

## DISEÑO
```text
    INICI

    DEFINIR preguntas COM ARRAY DE 50 ENTERS
    DEFINIR opcionesA COM ARRAY DE 50 ENTERS
    DEFINIR opcionesB COM ARRAY DE 50 ENTERS
    DEFINIR opcionesC COM ARRAY DE 50 ENTERS
    DEFINIR opcionesD COM ARRAY DE 50 ENTERS
    DEFINIR respuestasCorrectas COM ARRAY DE 50 ENTERS
    
    correctas <- 0
    
     PER i DES DE 0 FINS A preguntas.length
        ESCRIURE(preguntas[i])
        ESCRIURE("a. ", opcionesA[i])
        ESCRIURE("b. ", opcionesB[i])
        ESCRIURE("c. ", opcionesC[i])
        ESCRIURE("d. ", opcionesD[i])
                
        FES
            ESCRIURE("Tu respuesta: ")
            LLEGIR(respuesta)
            
            SI (respuesta != "a" i respuesta != "b" i respuesta != "c" i respuesta != "d") LLAVORS
                ESCRIURE("Respuesta no válida: a, b, c, d")
            FI SI
        MENTRES(respuesta != "a" i respuesta != "b" i respuesta != "c" i respuesta != "d")
        
        SI (respuesta = respuestaCorrecta[i]) LLAVORS
            ESCRIURE("¡Respuesta correcta!")
            correcta += 1
        SINO
            ESCRIURE("Respuesta incorrecta, la respuesta correcta es: ", respuestaCorrecta[i])
        FI SI
        
        ESCRIURE("Respuesta correctas: ", correctas)
        ESCRIURE("Respuestas incorrectas: ", preguntas.length - correctas)
     FI PER

    FI
```
