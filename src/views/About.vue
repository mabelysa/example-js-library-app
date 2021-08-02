<template>
  <div class="about">
    <h1>This is an about page about SweetAlert.js</h1>
    <h2>{{ message }}</h2>
  </div>
</template>

<style></style>

<script>
import swal from "sweetalert";

// swal("Hi, my names Woody, howdy! howdy! howdy!");
// swal("Oops!", "Something went wrong!", "error");
swal({
  title: "Are you sure?",
  text: "Are you sure that you want to leave this page?",
  icon: "warning",
  dangerMode: true,
}).then((willDelete) => {
  if (willDelete) {
    swal("Deleted!", "Your imaginary file has been deleted!", "success");
  }
});

export default {
  data: function () {
    return {
      message: "Pop up will show when you refresh page.",
    };
  },
  created: function () {},
  methods: {},
};
</script>
