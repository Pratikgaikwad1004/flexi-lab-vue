<template>
    <div class="app-Header">
        <v-row>
            <v-col cols="10">
                <h3>{{ title }}</h3>
            </v-col>
            <v-col cols="2">
                <v-btn title="tooltip" text  @click="$emit('add')"></v-btn>
                <v-icon>mdi-plus </v-icon>
            </v-col>
        </v-row>
        <v-row>
            <v-col>
                <v-text-field label="Search" append-icon="mdi-magnify" @input="$emit('search', $event)"></v-text-field>
            </v-col>
        </v-row>
    </div>
</template>

<script>

export default {
    props: {
        title: {
            type: String,
        },
        search: {
            type: Function
        }
    },
};
</script>

<style lang="scss" scoped>
.app-Header {
    padding: 1rem;
}
</style>