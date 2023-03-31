<template>
    <div>
        <AppHeader title="Books" @search="search($event)" />
        <v-list dense>
            <v-list-item v-for="(item, i) in books" :key="i">
                <v-list-item-avatar rounded="0">
                    <v-img :src="item.img"></v-img>
                </v-list-item-avatar>

                <v-list-item-content>
                    <v-list-item-title>{{ item.title }}</v-list-item-title>
                    <v-list-item-subtitle>{{ item.author.name }}</v-list-item-subtitle>
                    <v-list-item-subtitle>Pages: {{ item.pages }}</v-list-item-subtitle>
                </v-list-item-content>

                <v-list-item-icon>
                    <div>
                        <v-menu offset-y>
                            <template v-slot:activator="{ on, attrs }">
                                <v-btn color="black" dark v-bind="attrs" v-on="on" text>
                                    <v-icon>mdi-dots-vertical</v-icon>
                                </v-btn>
                            </template>
                            <v-list>
                                <v-list-item>
                                    <v-btn text>
                                        <v-icon class="mr-5">mdi-pencil</v-icon>
                                        <v-list-item-title>Edit</v-list-item-title>
                                    </v-btn>
                                </v-list-item>
                                <v-list-item>
                                    <v-icon class="mr-5">mdi-delete</v-icon>
                                    <v-list-item-title>Delete</v-list-item-title>
                                </v-list-item>
                                <v-list-item>
                                    <v-list-item-title>Issue</v-list-item-title>
                                </v-list-item>
                                <v-list-item>
                                    <v-list-item-title>Return</v-list-item-title>
                                </v-list-item>
                            </v-list>
                        </v-menu>
                        <p>
                            status
                        </p>
                    </div>
                </v-list-item-icon>
            </v-list-item>
        </v-list>
    </div>
</template>

<script>
import bookList from "@/data/books.json"
import AppHeader from "@/components/AppHeader.vue";
export default {
    components: {
        AppHeader
    },
    data() {
        return {
            books: bookList,
        }
    },
    methods: {
        search(e) {
            if (e.length >= 1) {
                this.books = bookList.filter((ele) => {
                    if (ele.title.toLowerCase().includes(e.toLowerCase())) {
                        return ele;
                    }
                })
            }
            else {
                this.books = bookList
            }
        }
    }
}
</script>

<style lang="scss" scoped></style>