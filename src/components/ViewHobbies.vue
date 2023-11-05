<template lang="">
    <div>
        <h1>Hobbies</h1>
        <div class="grid-container">
  <div class="grid-item">
    <i class="fas fa-gamepad"></i>
    <p>Jogar jogos eletronicos</p>
  </div>
  <div class="grid-item">
    <i class="fas fa-music"></i>
    <p>Ouvir musica</p>
  </div>
  <div class="grid-item">
    <i class="fas fa-camera"></i>
    <p>Fotografia</p>
  </div>
  <div class="grid-item">
    <i class="fas fa-film"></i>
    <p>Ver series e filmes</p>
  </div>
  <!-- Adicione mais itens de acordo com suas necessidades -->
</div>
       
    </div>
</template>
<script>
export default {
    name: 'ViewHobbies',
}
</script>
<style >
     .grid-container {
      display: grid;
      grid-template-columns: auto auto auto;
      padding: 10px;
    }
    .grid-item {
      border: 1px solid #ccc;
      border-radius: 5px;
      padding: 20px;
      text-align: center;
      margin: 10px;
    }
</style>