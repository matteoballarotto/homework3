# homework3
Terzo elaborato corso "Laboratorio Ciberfisico"
<<<<<<< HEAD
=======


## Consegna:
  1: installazione di ORBSLAM2 <br>
  2: esecuzione di ORB_SLAM2 su una rosbag registrata con un drone volante <br>
  3: creazione di una point cloud <br>
  4: clustering della point cloud generata al punto 3

<br>

### Esecuzione

<br>
Clonare il Repository.
Per la parte relativa all'installazione di ORBSLAM2, che necessità della libreria Pangolin, aprire la cartella ORBSLAM2 presente in questo repository e visualizzare il relativo readme. <Br>


```
  git clone https://github.com/matteoballarotto/homework3
```
<br>

Dopodichè, lanciare lo script setup.sh per la configurazione iniziale

<br>

```
  ./setup.sh
```
<br>


Poi aprire tre terminali diversi e avviare rispettivamente: <br>
• Nel primo:

```
  export ROS_PACKAGE_PATH=${ROS_PACKAGE_PATH}:PATH/homework3/ORB_SLAM2/Examples/ROS
  roscore
```

<br>
• Nel secondo: <br>

```
  export ROS_PACKAGE_PATH=${ROS_PACKAGE_PATH}:PATH/homework3/ORB_SLAM2/Examples/ROS
  rosrun ORBSLAM_2 Stereo ORB_SLAM2/Vocabulary/ORBvoc.txt ORB_SLAM2/Examples/Stereo/EuRoC.yaml true
```

<br>
• Nel terzo: <br>

```
  export ROS_PACKAGE_PATH=${ROS_PACKAGE_PATH}:PATH/homework3/ORB_SLAM2/Examples/ROS
  rosbag play --pause ORBSLAM_2/V1_01_easy.bag /cam0/image_raw:=/camera/left/image_raw /cam1/image_raw:=/camera/right/image_raw

```

<br>
<br>

### IL RISULTATO OTTENUTO SARÀ IL SEGUENTE:

<br>

Ora spostarsi nel terzo terminale e premere Space, in modo da far partire il drone volante.
Così facendo, il drone acquisirà i dati relativi ai punti che rileva nella mappa, e genererà la pointcloud.
Una volta terminata l'analisi della rosbag, da un terminale qualsiasi, posizionandosi nella directory del clone, digitare:


```
  pcl_viewer pointcloud.pcd
```



Per ottenere invece la pointcloud clusterizzata lanciare il comando:

```
  
```
>>>>>>> 6727fb2e5ed9245d92eec763dc68c9430298bd23
