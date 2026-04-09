# Clase 04

## Información para primera Entrega 

- Se evaluará el 16 de abril
- Debe estar todo publicado en su propio Github (Crear una carpeta llamada Entrega-01 para este proyecto). Tendrán que presentar desde ahí. 
- El 50% de esta nota serán los encargos anteriores, documentados en sus bitácoras de GitHub
- El otro 50% será la formulación de un anteproyecto de creación artística desde el Objeto, que debe contener:

    - **Definir Objeto de estudio**. Comentar intereses personales llegar a ese objeto, cualidades relevantes que les interesa medir, cualidad que midieron particularmente para esta entrega
    - **Base de datos**. Presentar en un archivo .csv, contenido dentro de su propia carpeta de la entrega en Github. Los datos, si son numéricos, deben estar ordenados en un rango de 0 a 100. Pueden ayudarse de AI para esto. Si trabajaron con Sensor Logger, además incluir el archivo bruto original aparte.
    - **Maqueta de visualización**. Incluir la tabla de .csv en una visualización de datos en Processing, Touch Designer, etc. Puede ser estática, o animada. Pueden ayudarse por AI para esto, pero debe estar declarado el prompt y sus variaciones como comentario en su código. Tomar conciencia de los aspectos compositivos de la pieza. ¿Por qué ciertos colores, formas? ¿Son coherentes con mi base de datos? ¿refuerzan esa información o la dislocan? ¿Aprendo algo nuevo sobre la base de datos con la visualización?

## Ejercicios en clase

### Repaso array

<https://processing.org/reference/Array.html>

```processing
//vamos a generar un lienzo, desde el cual usando arrays
//generaremos 5 puntos relevantes

//intuitivamente declararíamos así
// int x1 = 10; int y1 = 100; x2 = 20; y2 = 30;
//vamos a hacerlo de manera más limpia

// int[] numbers = { 90, 150, 30 };  // Alternate syntax REF. Proc
int[] posX = {10, 20, 35, 60, 95};
int[] posY = {40, 15, 67, 37, 89};

void setup(){
  size(100,100);
}

void draw(){
  
  //vamos a usar círculos para visualizar esos lugares
  //mi primer círculo estará en (10,40);
  //como la posición 0 del array posX es 10, la puedo usar
  circle(posX[0],posY[0],10);
  
  // la segunda posicion va a ser:
    circle(posX[1],posY[1],10);
    
    //el resto de posiciones
    circle(posX[2],posY[2],10);
    circle(posX[3],posY[3],10);
    circle(posX[4],posY[4],10);
    
    //También puedo visualizar de otras maneras
    line(posX[0],posY[0],posX[1],posY[1]);
    line(posX[1],posY[1],posX[2],posY[2]);
}
```

### Como usar el ciclo for

<https://processing.org/reference/for.html>

```processing
//vamos a generar un lienzo, desde el cual usando arrays
//generaremos 5 puntos relevantes

//intuitivamente declararíamos así
// int x1 = 10; int y1 = 100; x2 = 20; y2 = 30;
//vamos a hacerlo de manera más limpia

// int[] numbers = { 90, 150, 30 };  // Alternate syntax REF. Proc
int[] posX = {10, 20, 35, 60, 95};
int[] posY = {40, 15, 67, 37, 89};

void setup(){
  size(100,100);
  colorMode(HSB,360,100,100,100);
  background(5,60,90,100);
}

void draw(){
  
  //vamos a usar círculos para visualizar esos lugares
  //mi primer círculo estará en (10,40);
  //como la posición 0 del array posX es 10, la puedo usar
//circle(posX[0],posY[0],10);
  
  //ciclo for
  // int i = 0 -> crear variable local que solo funciona en el for
  // i va a partir siendo 0
  // i <= 5 -> Condición límite. Si i llega a valer 5 significa salir del for
  // i++ -> actualizar la variable. Puede ser de 1 en 1 (i++)
  
  //iteración
  for(int i = 0; i < 5; i++){
    circle(posX[i],posY[i],10);    
  }
  
  //Existe una estructura en programación que me permite
  // recorrer arrays de manera sencilla
  //que se llama el ciclo "for"
  //for ();
  

    //También puedo visualizar de otras maneras
    line(posX[0],posY[0],posX[1],posY[1]);
    line(posX[1],posY[1],posX[2],posY[2]);
}
```

### Animación a través de un índice (ojo con frameRate)

```processing
//vamos a generar un lienzo, desde el cual usando arrays
//generaremos 5 puntos relevantes

//intuitivamente declararíamos así
// int x1 = 10; int y1 = 100; x2 = 20; y2 = 30;
//vamos a hacerlo de manera más limpia

// int[] numbers = { 90, 150, 30 };  // Alternate syntax REF. Proc
int[] posX = {10, 20, 35, 60, 95};
int[] posY = {40, 15, 67, 37, 89};

int indice = 0;

void setup() {
  size(100, 100);
  colorMode(HSB, 360, 100, 100, 100);
  background(40, 60, 90, 100);
  //bajamos la velocidad del frameRate para poder ver el paso a paso
  frameRate(1);
}

void draw() {
  //animación
  background(40, 60, 90, 100);
  circle(posX[indice], posY[indice], 10);
  indice++;
  if (indice > 4) {
    indice = 0;
  }
}

```

### Ejercicio de otrx estudiante con GPS

Ver código [miPrimerGPS](./miPrimerGps/)

### Referencias artísticas mostradas

Sonificación de bahía de Valparaíso (Brian McKern) <https://34s56w.org/valparaiso/>

and the wind was like the regret for what is no more <https://vimeo.com/114414122>

Breathing Portraits <https://vimeo.com/15259734>

Feeling Climate Crisis <https://www.gauravpatekar.in/feeling-climate-crisis>

Tele Present Water <https://www.dwbowen.com/telepresentwater>

