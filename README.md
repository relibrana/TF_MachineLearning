<center> <h1>Informe Trabajo Final</h1> </center>
<h2> Introduccion </h2>
<h4 align="justify" >En este proyecto de Machine Learning, utilizamos un conjunto de datos masivos para entrenar un algoritmo de aprendizaje automático. Luego, imprimimos en 3D uno de los objetos, un velador, y le cortamos un trozo aleatorio utilizando perlin noise. Utilizamos una red generativa adversarial (GAN) para analizar la silla con el trozo cortado y generar la pieza faltante. Posteriormente, imprimimos en 3D ambas piezas para comprobar su ajuste, observando ligeras discrepancias debido a la imprecisión de la impresión 3D y al uso de diferentes materiales para cada pieza.</h4>


<h2>Marco Teorico</h2>
<h3>GAN</h3>
<h4 align="justify">El algoritmo GAN, Generative Adversarial Network, es un enfoque de aprendizaje automático que utiliza un generador y un discriminador para generar muestras sintéticas. El generador crea muestras artificiales, mientras que el discriminador aprende a distinguir entre las muestras reales y las generadas. A medida que avanzan en su entrenamiento, el generador busca mejorar la calidad de las muestras generadas para engañar al discriminador. El objetivo final es alcanzar un equilibrio en el que el generador pueda generar muestras indistinguibles de las reales. Una vez entrenado, el generador puede generar nuevas muestras que se asemeje al conjunto de datos original. </h4>

<h3>Ejemplos</h3>
<h4 align="justify">Para la GAN escogida se siguieron los siguientes pasos : <h/4>
<h4 align="justify">   ● Durante el proceso de entrenamiento, el generador progresa en la creación de imágenes que se asemejan a las reales, mientras que el discriminador mejora en su capacidad de distinguirlas. Este proceso alcanza un punto de equilibrio cuando el discriminador ya no puede diferenciar de manera efectiva entre las imágenes reales y las falsas.</h4>

<h4 align="justify">   ● Se prepara y carga los datos del dataset MNIST para obtener el generador que produce una imagen a traves de una semilla(ruido aleatorio)y discriminador es un clasificador basado en CNN . </h4>

<h4 align="justify">   ● Se define las funciones perdida y optimizadores para generador y discriminador para luego obtener puntos de control para prevenir cualquier incidente al entrenar por varias horas seguidas.</h4>

<h4 align="justify">   ● Ya por ultimo comienza el entrenamiento donde se usa una semilla para producir una imagen y el discriminador clasifica las imagenes reales tanto como las falsas, ademas de calcular la perdida para ambos.</h4>

<h2>Desarrollo</h2>

<h2>Fotos del Modelo 3D</h2>

[![objeto-1.jpg](https://i.postimg.cc/SRJcWL6X/objeto-1.jpg)](https://postimg.cc/m1Wc4H6R)


[![objeto-2.jpg](https://i.postimg.cc/5yTLpHgs/objeto-2.jpg)](https://postimg.cc/kRN2ggkS)

<h2>Conclusiones</h2>
<h4 align="justify">En este proyecto, hemos logrado demostrar la eficacia de los algoritmos de machine learning en combinación con las técnicas de impresión 3D para abordar la reparación de objetos dañados. Al utilizar una red generativa adversarial (GAN) para analizar la silla con un trozo faltante, pudimos generar de manera precisa la pieza que faltaba. Esta capacidad de regenerar partes ausentes tiene un gran potencial en la restauración de objetos, ya que permite superar limitaciones tradicionales en términos de disponibilidad de piezas de repuesto o dificultades en su fabricación. </h4>

<h4 align="justify">Aunque encontramos algunos problemas menores durante la fase de impresión 3D, como la inexactitud y el uso de materiales diferentes para cada pieza, los resultados generales fueron prometedores. Estos desafíos podrían ser abordados mediante una mejora en la precisión de la impresión 3D o la elección de materiales más compatibles. A pesar de estos inconvenientes, este proyecto destaca el potencial y la viabilidad de aplicar estas tecnologías en la restauración de objetos, abriendo nuevas posibilidades en el campo de la reparación y conservación de patrimonio cultural, mobiliario o cualquier objeto con partes faltantes o dañadas.
</h4>
