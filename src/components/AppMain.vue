<script>
export default {
    name: "AppMain"
}
</script>

<template>
    <main>
        <div class="container">
            <h1> --&gt; Content goes here &lt;-- </h1>
        </div>
    </main>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as*;

main {
    background-color: $sfondo-nero;
    padding: 4em 0em;
}

h1 {
    color: white;
    font-size: 1.5rem;
}
</style>