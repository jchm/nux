<template>
    <nav>
	<router-link :to="{ name: 'photos'}">Photos</router-link>
    </nav>
</template>

<style scoped>
 nav {
   padding: 1em;
 }
a {
 margin-right: 1em;
text-decoration: none;
color: #333;
}

a:hover {
    color: orange;
}

a:last-child {
margin-right: 0;
}
</style>

