<template>
    <div>
        <v-bottom-navigation v-model="value">
            <v-btn value="recent" @click="$router.push('/books')">
                <span>Books</span>

                <v-icon>mdi-book-open-page-variant</v-icon>
            </v-btn>

            <v-btn value="favorites">
                <span>Favorites</span>

                <v-icon>mdi-heart</v-icon>
            </v-btn>

            <v-btn value="nearby">
                <span>Nearby</span>

                <v-icon>mdi-map-marker</v-icon>
            </v-btn>
        </v-bottom-navigation>
    </div>
</template>

<script>
export default {
    data: () => ({ value: 'recent' }),
}
</script>

<style lang="scss" scoped></style>