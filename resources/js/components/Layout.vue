<template>

<Header @isActive="getVar"   />

<p>Methods date call: "{{ showVal() }}"</p>
    <div class="app">
        <Nav />
        <slot />
    </div>
</template>

<script>

import Nav from "./Nav";
import Header from "./Header";

export default {
    components: { Nav, Header },

    props: {
        isActive: String
    },

    methods: {

        getVar(val) {
            
        },

        showVal(props) {
            console.log(props.isActive)
        }


    }

};

</script>

<style lang="scss">

:root {
    --primary: #4ade80;
    --grey: #64748b;
    --dark: #1e203b;
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
