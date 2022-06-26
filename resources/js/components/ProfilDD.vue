<template>
<div class="dropdown">
    <button >Menü</button>
    <nav tabindex="0">
        <ul>
            <li>
                <a href="#">
                    Edit
                </a>
            </li>
            <li>
                <a href="#">
                    Delete
                </a>
            </li>
            <li>
                <a href="#">
                    Reply
                </a>
            </li>
        </ul>
    </nav>
</div>
</template>

<style lang="scss" >

* {
  padding: 0;
  margin: 0;
  list-style: none;
  border: 0;
  text-decoration: none;
  box-sizing: border-box;
}
html {
  font-size: 20px;
  background: #E9D68A;
}
html, body {
  height: 100%;
}
body {
  padding: 15px;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
}
.dropdown {
  position: relative;
  button {
    height: 2.5rem;
    padding: 0 1.25rem;
    background: #E9D68A;
    color: #fff;
    border-radius: 0.25rem;
    font-size: 1rem;
    cursor: pointer;
  }
  nav {
    position: absolute;
    top: 100%;
    left: 0;
    opacity: 0;
    background: #fff;
    visibility: hidden;
    transition: 300ms all;
    border: 2px solid #333;
    border-radius: 0.25rem;
    width: 12.5rem;
    ul {
      padding: 0.188rem 0;
      li {
        a {
          display: block;
          padding: 0.438rem 0.625rem;
          color: #333;
          &:hover {
            background: #f8f8f8;
          }
        }
      }
    }
  }
  &:focus-within nav {
    opacity: 1;
    visibility: visible;
    transform: translateY(0.25rem);
  }
}

</style>

<script>
  export default {
    data() {
      return {
        show: false,
      };
    },
  };
</script>
