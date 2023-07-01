<center> <h1>Informe Trabajo Final</h1> </center>
<h2> Introduccion </h2>
<p align="justify" >En este proyecto de Machine Learning, utilizamos un conjunto de datos masivos para entrenar un algoritmo de aprendizaje automático. Luego, imprimimos en 3D uno de los objetos, un velador, y le cortamos un trozo aleatorio utilizando perlin noise. Utilizamos una red generativa adversarial (GAN) para analizar la silla con el trozo cortado y generar la pieza faltante. Posteriormente, imprimimos en 3D ambas piezas para comprobar su ajuste, observando ligeras discrepancias debido a la imprecisión de la impresión 3D y al uso de diferentes materiales para cada pieza.</p>


<h2>Marco Teorico</h2>
<h3>GAN</h3>
<p align="justify">El algoritmo GAN, Generative Adversarial Network, es un enfoque de aprendizaje automático que utiliza un generador y un discriminador para generar muestras sintéticas. El generador crea muestras artificiales, mientras que el discriminador aprende a distinguir entre las muestras reales y las generadas. A medida que avanzan en su entrenamiento, el generador busca mejorar la calidad de las muestras generadas para engañar al discriminador. El objetivo final es alcanzar un equilibrio en el que el generador pueda generar muestras indistinguibles de las reales. Una vez entrenado, el generador puede generar nuevas muestras que se asemeje al conjunto de datos original. </p>

<h3>Ejemplos</h3>

[Link de ejemplo usando GAN](https://github.com/relibrana/TF_MachineLearning/blob/main/dcgan.ipynb)

<p align="justify">Para la GAN escogida se siguieron los siguientes pasos : <p/>
<p align="justify">   ● Durante el proceso de entrenamiento, el generador progresa en la creación de imágenes que se asemejan a las reales, mientras que el discriminador mejora en su capacidad de distinguirlas. Este proceso alcanza un punto de equilibrio cuando el discriminador ya no puede diferenciar de manera efectiva entre las imágenes reales y las falsas.</p>

<p align="justify">   ● Se prepara y carga los datos del dataset MNIST para obtener el generador que produce una imagen a traves de una semilla(ruido aleatorio)y discriminador es un clasificador basado en CNN . </p>

<p align="justify">   ● Se define las funciones perdida y optimizadores para generador y discriminador para luego obtener puntos de control para prevenir cualquier incidente al entrenar por varias horas seguidas.</p>

<p align="justify">   ● Ya por ultimo comienza el entrenamiento donde se usa una semilla para producir una imagen y el discriminador clasifica las imagenes reales tanto como las falsas, ademas de calcular la perdida para ambos.</p>

<h2>Desarrollo</h2>

[Link del video explicativo del código](https://youtu.be/S26K9E5V81s) <br>
[Dataset utilizado](https://github.com/renato145/3D-ORGAN/blob/master/datasets/arq_dataset.tar.gz)

<p align="justify"> Para el desarrollo de este proyecto, se tomó un modelo 3D del dataset ModelNet10. A partir del dataset, se cargaron los modelos como matrices .npy. De estas matrices, se eligió una para “voxelizar” y convertir en una matriz de objetos cúbicos (voxels), los cuales representan la figura general del modelo. Sobre esta matriz se generó un array de perlin noise, que una vez superpuesto con la matriz original, generó un vacío, representado por 0s Luego de haber generado el agujero en el voxel, tomando como datos de entrada el complemento del modelo alterado, se genera un objeto nuevo representando el área eliminada del modelo original, así como una versión modificada del mismo. Luego de generar ambos objetos complementarios, se realizó una exportación de los mismos en un archivo stl, los cuales se procedió a imprimir en 3D. Debido a problemas durante la impresión, los objetos impresos fueron trabajados en materiales distintos, en impresoras diferentes. El primer objeto (incompleto) se imprimió usando un material suave, mientras que el filamento usado para el segundo objeto (complemento) fue duro. </p>

<h2>Fotos del Modelo 3D</h2>

[![objeto-1.jpg](https://i.postimg.cc/SRJcWL6X/objeto-1.jpg)](https://postimg.cc/m1Wc4H6R)


[![objeto-2.jpg](https://i.postimg.cc/5yTLpHgs/objeto-2.jpg)](https://postimg.cc/kRN2ggkS)

<h2>Conclusiones</h2>
<p align="justify">En este proyecto, hemos logrado demostrar la eficacia de los algoritmos de machine learning en combinación con las técnicas de impresión 3D para abordar la reparación de objetos dañados. Al utilizar una red generativa adversarial (GAN) para analizar la silla con un trozo faltante, pudimos generar de manera precisa la pieza que faltaba. Esta capacidad de regenerar partes ausentes tiene un gran potencial en la restauración de objetos, ya que permite superar limitaciones tradicionales en términos de disponibilidad de piezas de repuesto o dificultades en su fabricación. </p>

<p align="justify">Aunque encontramos algunos problemas menores durante la fase de impresión 3D, como la inexactitud y el uso de materiales diferentes para cada pieza, los resultados generales fueron prometedores. Estos desafíos podrían ser abordados mediante una mejora en la precisión de la impresión 3D o la elección de materiales más compatibles. A pesar de estos inconvenientes, este proyecto destaca el potencial y la viabilidad de aplicar estas tecnologías en la restauración de objetos, abriendo nuevas posibilidades en el campo de la reparación y conservación de patrimonio cultural, mobiliario o cualquier objeto con partes faltantes o dañadas.
</p>
