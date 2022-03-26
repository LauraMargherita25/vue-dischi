<template>
   <form class="d-flex" @submit.prevent="">
        <!-- <input type="text" v-model="strSearch">
        <button @click="$emit('search', strSearch)" class="btn btn-outline-success" type="submit">
            Search
        </button> -->
        <select v-model="selected">
            <option disabled value="">Please select one</option>
            <option>Rock</option>
            <option>Metal</option>
            <option>Jazz</option>
            <option>Pop</option>
        </select>
        <button @click="$emit('search', selected)" class="btn btn-outline-success" type="submit">
            Search
        </button>
    </form>
</template>

<script>
export default {
    name: "FileSerchComponents",
    // data() {
    //     return {
    //         strSearch: "",
    //     }
    // },
    data() {
        return {
            selected: "",
        }
    },
}
</script>

<style lang="scss" scoped>

</style>