<template>

<Header @isActive="getVar"   />
    <div class="app">
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


    *{
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: 'Fira sans', sans-serif;
    }

    body {

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

            @media (max-width: 768px) {
                padding-left: 6rem;

            }
        }
    }
}

</style>
