<template>
  <div>
    <div v-if="renderBlogs">
      <div v-block-padding:title="{topP: '20px', bottomP: '30px'}">
        <h1>{{blogPageTitle | toPascalCase}}</h1>
      </div>
      <div class="container">
        <div class="row">
          <div :key="post.id" v-blog-preview v-for="post in info">
            <div style="font-weight: bold">{{post.title}}</div>            
            <div>{{post.body}}</div>
            <hr />
          </div>
        </div>
      </div>
    </div>
    <div v-else v-block-padding:loading="{topP: '150px', bottomP: '1000px'}">Loading ...</div>
  </div>
</template>

<script>
export default {
  name: "Blog",
  data() {
    return {
      blogPageTitle: "The thought manifest",
      info: null,
      renderBlogs: false
    };
  },
  filters: {
    toPascalCase(value) {
      return value.replace(
        /\w\S*/g,
        m => m.charAt(0).toUpperCase() + m.substr(1).toLowerCase()
      );
    }
  },
  async mounted() {
    const restapi_url = "https://jsonplaceholder.typicode.com/posts";
    const response = await fetch(restapi_url);
    const posts = await response.json();
    this.info = posts;
    this.renderBlogs = true;
    // console.log(this.info);
  },
  directives: {
    "block-padding": {
      bind(el, binding) {
        if (binding.arg == "loading") {
          el.style.paddingTop = binding.value.topP;
          el.style.paddingBottom = binding.value.bottomP;
        }
        if (binding.arg == "title") {
          el.style.paddingTop = binding.value.topP;
          el.style.paddingBottom = binding.value.bottomP;
        }
      }
    },
    "blog-preview": {
      bind(el) {
        el.padding = "10px";
        el.classList.add("col-md-3");
        el.classList.add("col-sm-6");
      }
    }
  }
};
</script>

<style scoped>
</style>