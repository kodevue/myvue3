<script setup>
import { useRouter } from 'vue-router'

const router = useRouter()

let navigateTo = () => {
  router.push('/')
}
</script>


<template>
  <div class="row justify-content-center">
    <div class="col-12 col-md-6">
      <h1>About Page</h1>
      <p class="fs-3">
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Rem iste facere culpa ea hic quis
        modi sit quo, labore, placeat magnam soluta sint, fuga officia illum quod vitae sunt
        tempora!
      </p>
      <p class="fs-4">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate quibusdam laboriosam
        expedita inventore quam iure eos quidem, beatae est odio non officia, eveniet eum laudantium
        eius fuga quisquam! Consequatur, quisquam? Repellat necessitatibus amet consectetur harum,
        pariatur sapiente reiciendis recusandae excepturi facere nam, voluptatem in unde
        perspiciatis animi, iure cumque quasi. Eveniet est suscipit quae a enim at aliquam vero et,
        cumque doloremque ut. Aut optio praesentium aspernatur sed libero harum minima, reiciendis
        ab est nesciunt laboriosam, debitis ad aperiam consectetur? Necessitatibus aspernatur porro
        dicta facilis pariatur eligendi omnis magnam! Praesentium optio sequi numquam quasi cum et
        labore minima, facilis odit accusantium doloribus assumenda, corrupti dicta, commodi qui ea
        nam in. Sequi incidunt deserunt alias perferendis obcaecati exercitationem necessitatibus
        unde, nobis ex ea dolore error voluptatibus, blanditiis distinctio adipisci. Reprehenderit
        natus magnam beatae ea eum maiores magni quisquam molestiae laborum saepe quod aspernatur
        distinctio quam quaerat consequatur obcaecati voluptatibus laboriosam maxime nemo,
        voluptates possimus eaque ab harum ex! Eum velit reiciendis accusantium architecto non,
        incidunt soluta vel esse repellat earum ipsa debitis consequatur et quam voluptatum
        laboriosam. Laudantium illo commodi laborum doloribus. Tempore, nulla error? Provident unde
        quidem explicabo, porro illum adipisci veritatis earum eius in tempore, dolorem alias facere
        et?
      </p>

      <input type="button" value="Go to Home" class="btn btn-secondary mb-5" @click="navigateTo" />
    </div>
  </div>
</template>

