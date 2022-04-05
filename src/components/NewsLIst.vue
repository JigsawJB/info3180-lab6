<template>
    <ul class="news__list">

        <li class="news__item" v-for="article in articles">{{ article.title }}</li>
        <!-- <li class="news__item">News item 1</li>
        <li class="news__item">News item 2</li>
        <li class="news__item">News item 3</li> -->
    </ul>
</template>

<script>
export default {
    data() {
        return {
            articles: []
        };
    },
    created() {
        let self = this;

        fetch('https://newsapi.org/v2/top-headlines?country=us',
{
    headers: {
        'Authorization':  `Bearer ${import.meta.env.VITE_NEWSAPI_TOKEN}`
    }
})
        .then(function(response) {
            return response.json();
        })
        .then(function(data) {
            console.log(data);
            self.articles = data.articles;
        });
    }
};
</script>