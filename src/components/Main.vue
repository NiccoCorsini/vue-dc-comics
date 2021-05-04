<template>
  <main>
      <div class="container">
          <ul>
              <li v-for="(link, index) in navLinks" :key="'id' + index"><a href="#">
                  <img :src="link.logo">
                  {{link.name}}
                  </a></li>
          </ul>
      </div>
  </main>
</template>

<script>
export default {
    name: 'Header',
    data(){
        return {
            navLinks: [
                {
                    name: 'digital comics',
                    logo: require('../assets/img/buy-comics-digital-comics.png'),
                    link: '#',
                    active: false
                },
                {
                    name: 'dc merchandise',
                    logo: require('../assets/img/buy-comics-merchandise.png'),
                    link: '#',
                    active: true
                },
                {
                    name: 'subscription',
                    link: '#',
                    logo: require('../assets/img/buy-comics-subscriptions.png'),
                    active: false
                },
                {
                    name: 'comic shop locator',
                    link: '#',
                    logo: require('../assets/img/buy-comics-shop-locator.png'),
                    active: false
                },
                {
                    name: 'dc power visa',
                    link: '#',
                    logo: require('../assets/img/buy-dc-power-visa.svg'),
                    active: false
                },
            ],
        }
    }
}
</script>

<style scoped lang="scss">
main{
    padding: 1rem 0;
    background-color: #3582f9;
}

ul{
    display: flex;
    
    justify-content: space-between;
}

li a{
    display: flex;
    align-items: center;
    color: #fff;
    text-transform: uppercase;
    padding: 3rem 0.5rem;
}

a img{
    height: 50px;
    margin-right: 10px;
}

li:last-child a img{
    width: 55px;
}
</style>