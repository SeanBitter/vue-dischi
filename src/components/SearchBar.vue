<template>
    <div class="container pt-5">
        <div class="input-group">
            <select type="text" class="rounded" v-model="genre">
                <option value="">Seleziona genere</option>
                <option v-for="(genre, i) in genresListFromState" :key="i" value="genre">{{ genre }}</option>
            </select>
            <button class="btn btn-outline-light">Cerca</button>
        </div>
    </div>
</template>

<script>
import { state } from "../store";

export default {
    props: {
        genresList: Array,
    },

    data() {
        return {
            genre: "",
        };
    },

    computed: {
        genresListFromState() {
            return state.genresList;
        },
    },
}




</script>