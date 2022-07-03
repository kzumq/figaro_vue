<template>
          <div class="dropdown">
            <button @click="dropdown()" class="drop-down-btn">

            <img class="profil-img" src="../../../public/assets/img/person.png">

            </button>
                <div  v-if="showMenu">
                    <ul class="dropdown-menu">
                    <li>
                        <h2>Test1</h2>
                    </li>
                    <li>
                        <h2>Test2</h2>
                    </li>
                    </ul>
                </div>
        </div>
</template>

<script>
export default {
    data()  {
        return {
            showMenu:false
        }
    },
    methods: {
        dropdown() {
            this.showMenu = !this.showMenu
        }
    }
}
</script>

<style lang="scss">

.drop-down-btn{
    size: 2rem;
    color: white;
}

.profil-img{
    border: 1px;
    border-radius: 50%;
    width: 2rem;
    height: 2rem;
}

.dropdown-menu {
    background-color: white;
    color:red;
}

</style>
