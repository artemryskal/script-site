<template>
  <section class="add-comment container section">
    <h2 class="section__heading heading heading--h2">
      Add a Comment
    </h2>

    <form action="#" method="POST" class="form">
      <label class="label">
        Name*
        <input type="text" placeholder="Shane Hobbins" class="input" required>
      </label>
      <label class="label">
        Email*
        <input type="email" placeholder="info@interface.com" class="input" required>
      </label>
      <label class="label">
        Website
        <input type="text" placeholder="www.interface.com" class="input" required>
      </label>
      <label class="label label--secondary">
        <input type="checkbox" name="agree" required>
        <span>Save my name, email, and website in this browser for the next time I comment.</span>
      </label>
      <label class="label">
        Message*
        <textarea cols="30" rows="10" placeholder="Hi there" class="input" required></textarea>
      </label>
      <input type="submit" value="Post" class="btn btn--submit">
    </form>
  </section>
</template>

<script>
export default {
  name: 'AddComment'
}
</script>

<style scoped>
@media print {
  .add-comment {
    display: none;
  }
}
</style>
