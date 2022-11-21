<template>

  <div class="NFT-container">

    <div class="NFT-picture">
      <img :src="require( `../../assets/nft-pictures/${item.image}.png`)"/>
    </div>

    <div class="NFT-description">

      <div>
        <h5>{{ item.name }}</h5>
        <span>By <b>{{ item.artist }}</b></span>
      </div>

      <div>
        <div>{{ item.price }}STX</div>
        <div>{{ item.price }}$</div>
      </div>

    </div>

  </div>

</template>


<script>

export default {
  name: 'NFTItem',
  props: {
    item: Object
  },
}
</script>


<style>

.NFT-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 255px;
  height: 319px;
  background: rgba(129, 129, 129, 0.12);
  border-radius: 5%;
  margin-top: 20px;
}

.NFT-picture img {
  height: 100%;
  width: 100%;
  object-fit: contain
}

.NFT-description {
  width: 90%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

</style>