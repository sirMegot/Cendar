<template>
  <div id="app">
    <h1>L'Art de la Cendre</h1>
    <h2>Célébrons la beauté des cendriers, la cendre et les mégots</h2>

    <div class="cigarette"></div>

    <div class="cendrier">
        <div class="megot"></div>
    </div>

    <p>Découvrez la beauté intemporelle des cendriers, la danse éthérée de la cendre et l'empreinte mémorable des mégots.</p>
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
body {
    background-image: url('./assets/wp.jpg'); 
    background-size: cover; /* Pour couvrir toute la surface de la fenêtre du navigateur */
    background-repeat: no-repeat; /* Pour éviter que l'image ne se répète */
    background-position: center cover; /* Pour centrer l'image */
    font-family: 'Press Start 2P', cursive; /* Une police pixelisée */
    color: white;
    text-align: center;
    padding: 50px;
}

h1, h2 {
    color: orange;
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
    box-shadow: 0 0 5px rgba(255, 165, 0, 0.5); /* Lueur orange autour de la cigarette */
}


.megot {
    width: 10px;
    height: 30px;
    background-color: white;
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

