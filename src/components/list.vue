<script setup>
import { ref } from "vue";
const isVisible = ref(false);
const titlePosition = ref(null);
</script>
<template>
  <div class="listWrap">
    <div class="cardWrap">
      <div :style="{ opacity: isVisible ? '1' : '0' }" class="title"></div>
      <div class="card" style="width: 18rem">
        <a href="https://jamixcs.github.io/t1/" target="blank"
          ><img src="../img/t1.png" class="card-img-top" alt="..." />
        </a>
      </div>
    </div>
    <div class="">
      <div class="card" style="width: 18rem">
        <a href="https://jamixcs.github.io/t2/" target="blank"
          ><img src="../img/t2.jpg" class="card-img-top" alt="..." />
        </a>
      </div>
    </div>
    <div class="">
      <div class="card" style="width: 18rem">
        <a href="https://jamixcs.github.io/t3/" target="blank"
          ><img src="../img/t3.jpg" class="card-img-top" alt="..." />
        </a>
      </div>
    </div>
    <div class="">
      <div class="card" style="width: 18rem">
        <a href="https://jamixcs.github.io/t4/" target="blank"
          ><img src="../img/t4.jpg" class="card-img-top" alt="..." />
        </a>
      </div>
    </div>
    <div class="">
      <div class="card" style="width: 18rem">
        <a href="https://jamixcs.github.io/t6/" target="blank"
          ><img src="../img/t6.jpg" class="card-img-top" alt="..." />
        </a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.listWrap {
  max-width: 900px;
  margin: 10px auto;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  gap: 10px;
  text-align: center;
}
a {
  text-decoration: none;
  color: black;
}
.card:hover {
  opacity: 0.7;
}
.card-img,
.card-img-top {
  height: 250px;
  object-fit: cover;
}
.title {
  position: absolute;
  z-index: 1;
}
</style>
