<template>
  <div class="container">
      <header>
            <div class="left">
                <a href="#"><img src="../assets/img/dc-logo.png" alt=""></a>
            </div>
            <div class="right">
                <nav>
                    <ul>
                        <li v-for="(link, index) in navLinks" :key="'id' + index"><a @click="activeTab(link)" :class="{active: link.active}" :href="link.link">{{link.name}}</a></li>
                    </ul>
                </nav>
            </div>
          
      </header>
  </div>
</template>

<script>
export default {
    name: 'Header',
    data(){
        return {
            navLinks: [
                {
                    name: 'characters',
                    link: '#',
                    active: false
                },
                {
                    name: 'comics',
                    link: '#',
                    active: true
                },
                {
                    name: 'movies',
                    link: '#',
                    active: false
                },
                {
                    name: 'tv',
                    link: '#',
                    active: false
                },
                {
                    name: 'games',
                    link: '#',
                    active: false
                },
                {
                    name: 'collectibles',
                    link: '#',
                    active: false
                },
                {
                    name: 'videos',
                    link: '#',
                    active: false
                },
                {
                    name: 'fans',
                    link: '#',
                    active: false
                },
                {
                    name: 'news',
                    link: '#',
                    active: false
                },
                {
                    name: 'shop',
                    link: '#',
                    active: false
                },
            ],
        }
    },
    methods:{
        activeTab(link){
            this.navLinks.forEach(element => {
                element.active = false;
            });
            link.active = true;
        }
    }
}
</script>

<style scoped lang="scss">
header {
    display: flex;
    align-items: center;
}

.left{
    width: 20%;
}

.right{
    width: 80%;
    display: flex;
    justify-content: flex-end;
}

.left img{
    width: 60px;
}

.right ul{
    display: flex;
}

li a{
    color: #74747e;
    padding: 3rem 0;
    display: block;
    text-transform: uppercase;
    font-size: 12px;
    font-weight: 500;
    border-bottom: 5px solid transparent;
    transition: all 400ms;
}

li:not(:last-child){
    margin-right: 1.4rem;
}

li a:hover,
li a.active{
    color: #327dec;
    border-bottom: solid 5px #327dec;
}
</style>