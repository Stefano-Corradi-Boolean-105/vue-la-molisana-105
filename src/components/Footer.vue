<script>
import mainMenu from '../data/mainMenu';
import { menuProdotti, menuPastificio } from '../data/footerMenu';

export default {
  name: 'Footer',
  data(){
    return{
      mainMenu,
      menuProdotti,
      menuPastificio
    }
  }
}
</script>

<template>
  <footer >
    <div class="top container">

      <div class="logo">
        <img src="/logo-molisana.png" alt="Logo Molisana">
      </div>

      <nav>
        <h4>menu</h4>
        <ul>
          <li
            v-for="(item, index) in mainMenu"
            :key="index"
          ><a :href="item.href">{{ item.text }}</a></li>
        </ul>
      </nav>

      <nav>
        <h4>pastificio</h4>
        <ul>
          <li
            v-for="(item, index) in menuPastificio"
            :key="index"
          ><a :href="item.href">{{ item.text }}</a></li>
        </ul>
      </nav>

      <nav>
        <h4>prodotti</h4>
        <ul>
          <li
            v-for="(item, index) in menuProdotti"
            :key="index"
          ><a :href="item.href">{{ item.text }}</a></li>
        </ul>
      </nav>

    </div>
    <div class="bottom">
      <img src="../assets/img/footer.jpg" alt="Montagne">
    </div>
  </footer>
  
</template>

<style lang="scss" scoped>
@use '../scss/partials/variabiles' as *;

footer{
  .top{
    display: flex;
    justify-content: space-between;
    .logo{
      width: 30%;
    }
    h4{
      text-transform: uppercase;
      margin-bottom: 15px;
    }
    li{
      margin-bottom: 10px;
      a{
        color: $link-color;
        font-size: .9rem;
        &:hover{
          text-decoration: underline;
        }
      }
    }
  }
}


</style>