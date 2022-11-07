<template>
    <nav>
        <ul>
            <li>
                <router-link to="/">Home</router-link>
            </li>
            <li>
                <router-link to="/deportes">Deportes</router-link>
            </li>
            <li>
                <router-link to="/comics">Comics</router-link>
            </li>
            <li>
                <router-link to="/doble">Doble sin parametro</router-link>
            </li>
            <li>
                <router-link to="/doble/77">Doble 77</router-link>
            </li>
            <li>
                <router-link to="/doble/56">Doble 56</router-link>
            </li>
            <li>
                <router-link to="/doble/69">Doble 69</router-link>
            </li>
        </ul>
    </nav>
</template>

<script>
export default {
name:"MenuComponent"
}
</script>

<style>

  

</style>