<template>
  <div class="home">
    <h1>Home</h1>
    <PostList v-if="showPosts" :posts="posts" />
    <button @click="showPosts = !showPosts">toggle posts</button>
    <button @click="posts.pop()">delete a post</button>
  </div>
</template>

<script>
import PostList from "@/components/PostList.vue";
import { ref } from "vue";

// @ is an alias to /src

export default {
  name: "HomeView",
  components: { PostList },
  setup() {
    const posts = ref([
      {
        title: "welcome to the blog",
        body: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quia error iste eum asperiores consequatur placeat culpa dolores dignissimos, nesciunt commodi vero aliquam deleniti minus quasi omnis sed mollitia enim nihil obcaecati, sunt eligendi quos natus tempora? Fuga optio magnam, culpa, debitis ipsam nihil, dolores quisquam repellendus mollitia repellat vel? Minus expedita dolor mollitia voluptatibus, amet qui? Maiores iste rerum modi minima, accusantium deserunt! Iusto necessitatibus consequatur cupiditate ab vel aspernatur eligendi labore magnam nobis commodi, quod esse, consectetur consequuntur molestiae quo ducimus, id ratione. Recusandae corrupti repudiandae et ab laboriosam beatae nisi ut pariatur? Aut quae rerum esse consectetur ullam?",
        id: 1,
      },
      { title: "top 5 css tips", body: "lorem ipsum", id: 2 },
    ]);
    const showPosts = ref(true);

    return { posts, showPosts };
  },
};
</script>
