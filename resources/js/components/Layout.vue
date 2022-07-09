<template>

    <Header @isActive="getVar" />
    <div class="app" style="width:100vw;">

        <Nav :is_expanded="is_expanded" />

        <slot />
    </div>
</template>

<script>

import Nav from "./Nav";
import Header from "./Header";

export default {
    name: "Layout",

    components: { Nav, Header },

    data() {
      return {
        is_expanded: ""
      }
    },

    methods: {
        getVar(val) {
            this.is_expanded = val
        },
    },


};

</script>

<style lang="scss">

:root {
    --primary: #4ade80;
    --grey: #64748b;
    --dark: #202020;
    --light: #f1f5f9;
    --sidebar-width: 300px;
    --header-button-size: 2rem;


    *{
        box-sizing: border-box;
        font-family: 'Fira sans', sans-serif;
    }

    body {
        position: relative;

        background: var(--light);

    }

    button {
        cursor: pointer;
        appearance: none;
        border: none;
        outline: none;
        background: none;
    }

    .app {
        display: flex;
        position: fixed;
        main {
            flex: 1 1 0;
            padding: 2rem;

            @media (max-width: 780px) {
                padding-left: 6rem;

            }
        }
    }
}

</style>
