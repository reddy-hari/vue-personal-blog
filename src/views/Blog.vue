<template>
  <div>
    <div v-if="renderBlogs">
      <div v-block-padding:title="{topP: '20px', bottomP: '20px'}">
        <h1>{{blogPageTitle | toPascalCase}}</h1>
      </div>

      <div class="card-body">
        <div
          v-for="item in pageOfItems"
          :key="item.id"
          style="padding: 10px; display: inline-block;"
        >
          <div class="card" style="width: 25rem;">
            <img class="card-img-top" src="../assets/crow-silhouette.png" alt="image-cap" />
            <div class="card-body">
              <!-- Filters bana to limit text length for body -->
              <h6 class="card-title" style="font-weight: bold;">{{item.title | toPascalCase}}</h6>
              <p class="card-text" >{{item.body | limitPreviewText}}</p>
              <a href="#" class="btn btn-primary">Read More</a>
            </div>
          </div>
        </div>
      </div>

      <!-- Pagination -->
      <div class="card-footer pb-4 pt-4">
        <jw-pagination :items="info" @changePage="onChangePage" :labels="customLabels"></jw-pagination>
      </div>
    </div>
    <div v-else v-block-padding:loading="{topP: '5px', bottomP: '1000px'}">
      <img src="../assets/loading.gif" alt="loading-spinner" />
    </div>
  </div>
</template>

<script>
const customLabels = {
  first: "<<",
  last: ">>",
  previous: "<",
  next: ">",
};
export default {
  name: "Blog",
  data() {
    return {
      blogPageTitle: "The thought manifest",
      info: null,
      renderBlogs: false,
      pageOfItems: [],
      customLabels,
    };
  },
  filters: {
    toPascalCase(value) {
      return value.replace(
        /\w\S*/g,
        (m) => m.charAt(0).toUpperCase() + m.substr(1).toLowerCase()
      );
    },
    limitPreviewText(value) {
      return `${value.substring(0, 100)} ...`;
    },
  },
  methods: {
    onChangePage(pageOfItems) {
      // update page of items
      this.pageOfItems = pageOfItems;
    },
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
      },
    },
    "blog-preview": {
      bind(el) {
        // el.classList.removeClass();
        el.padding = "10px";
        el.classList.add("col-md-4");
        el.classList.add("col-sm-6");
      },
    },
  },
};
</script>

<style scoped>
</style>