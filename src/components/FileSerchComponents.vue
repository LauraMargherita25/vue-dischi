<template>
   <form class="d-flex" @submit.prevent="">
        <select v-model="selected">
            <option disabled value="">Please select a genre</option>
            <!-- <option>Rock</option>
            <option>Metal</option>
            <option>Jazz</option>
            <option>Pop</option> -->
            <option v-for="option in arrOptions" v-bind:value="option.value" :key="option.value">
                {{ option.text }}
            </option>
        </select>
        <button @click="$emit('search', selected)" class="btn btn-outline-success ms-1" type="submit">
            Search
        </button>
    </form>
</template>

<script>
export default {
    name: "FileSerchComponents",
    data() {
        return {
            selected: "",
            arrOptions: [
                { text: 'Rock', value: 'Rock' },
                { text: 'Metal', value: 'Metal' },
                { text: 'Jazz', value: 'Jazz' },
                { text: 'Pop', value: 'Pop' }
            ]
        }
    },
}
</script>

<style lang="scss" scoped>

</style>