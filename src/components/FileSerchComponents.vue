<template>
   <form class="d-flex">
        <select 
            title="genre_selector" 
            name="genre_selector" 
            id="genre_selector" 
            class="form-control me-2"
            type="search"
            placeholder="Search"
            aria-label="Search">
            <option value="all">all</option>
            <option value="rock">rock</option>
            <option value="metal">metal</option>
            <option value="jazz">jazz</option>
            <option value="pop">pop</option>
        </select>
        <button class="btn btn-outline-success" type="submit">
            Search
        </button>
    </form>
</template>

<script>
export default {
    name: "FileSerchComponents"
}
</script>

<style lang="scss" scoped>

</style>