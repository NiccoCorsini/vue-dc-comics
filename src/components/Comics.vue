<template>
    <div class="comics">
        <div class="container">
            <button>current series</button>
            <Cards />
        </div>
            <button>load more</button>
    </div>
</template>

<script>
import Cards from '../components/Cards';

export default {
    name: 'Comics',
    components: {
        Cards,
    }
}
</script>

<style scoped lang="scss">
@import "../style/comics";
</style>