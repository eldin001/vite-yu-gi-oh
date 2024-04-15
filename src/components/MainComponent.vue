<template>
    <main>
        <select class="ms-5 mt-3 mb-3 " name="" id="">
            <option value="">Alien</option>
        </select>
        <div class="container">
            <div class="container p-3 d-bug">
                <div class="found">
                    Found 30 cards
                </div>
                <div>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex libero tempora quam. Nulla earum necessitatibus consequatur eaque dolorem, eum magni sequi aliquam quaerat mollitia labore illo, unde, consectetur voluptas aperiam.</div>
            </div>
        </div>
    </main>
</template>

<script>
export default {
    name: 'MainComponent'
}
</script>

<style lang="scss">
@use '../assets/styles/partials/variables' as *;

.container {
    background-color: white;
}

.found {
    background-color: $lightGray;
    color: white;
    padding: 3px;
}

.d-bug {
    border: 2px solid red
}


main {
    background-color: $orange;
}
</style>