<template>
  <div id="app">
    <h1>Le Cendar</h1>
    <h2>Célébrons la gloire des cendars, de la cendre et des mégots</h2>

    <div class="cigarette"></div>

    <div class="cendrier">
        <div class="megot"></div>
    </div>

    <p class="texte-avec-contour">Découvrez la beauté intemporelle des cendriers, la danse éthérée de la cendre et l'empreinte mémorable des mégots. Une experience qui vous est offerte par Megot.</p>
    <router-view />
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {
    // Si vous avez d'autres composants, ils seront listés ici.
  }
}
</script>

<style>
@font-face {
    font-family: 'Press Start 2P'; /* Remplacez par le nom que vous souhaitez donner à la police */
    src: url('./assets/Press_Start_2P/PressStart2P-Regular.ttf'); /* Remplacez par le chemin réel du fichier de police */
    font-weight: normal; /* ou bold, italic, etc. selon la variante */
    font-style: normal; /* ou italic, etc. selon la variante */
}

body {
    background-image: url('./assets/wp.jpg'); 
    background-size: cover; /* Pour couvrir toute la surface de la fenêtre du navigateur */
    background-repeat: no-repeat; /* Pour éviter que l'image ne se répète */
    background-position: center center; /* Pour centrer l'image */
    font-family: 'Press Start 2P', sans-serif;
    color: white;
    text-align: center;
    padding: 50px;
}

h1, h2 {
    color: orange;
}
.texte-avec-contour {
    color: white; /* Couleur du texte */
    text-shadow: 
        -1px -1px 0 #000,  
         1px -1px 0 #000,
        -1px  1px 0 #000,
         1px  1px 0 #000; /* Contour noir autour du texte */
}

.cendrier {
    width: 100px;
    height: 50px;
    background-color: grey;
    margin: 50px auto;
    position: relative;
}

.cigarette {
    width: 20px;
    height: 150px;
    background: linear-gradient(white 80%, orange 80%, orange 90%, #8B4513 90%, #8B4513 100%);
    margin: 50px auto;
    border-radius: 3px;
    box-shadow: 0 0 15px rgba(255, 165, 0, 0.5); /* Lueur orange autour de la cigarette */
}


.megot {
    width: 10px;
    height: 30px;
    background-color: orange;
    position: absolute;
    bottom: 10px;
    left: 45px;
    animation: tomber 2s infinite;
}

@keyframes tomber {
    0% { top: -30px; }
    100% { top: 10px; }
}
</style>

