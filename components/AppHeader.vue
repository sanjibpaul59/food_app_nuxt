<template>
  <div>
    <section class="masthead" role="img" aria-label="Image Description">
      <button>See Restaurants</button>
    </section>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.masthead {
    display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  text-align: center;
  width: 100%;
  height: 80vh; /* if you don't want it to take up the full screen, reduce this number */
  overflow: hidden;
  background-size: cover !important;
  background: linear-gradient(
      45deg,
      rgba(0, 0, 0, 0) 0%,
      rgba(0, 0, 0, 0) 58%,
      rgba(162, 42, 124, 0.65) 100%
    ),
    url('~assets/headerimg.jpg') no-repeat center center scroll;
}

h1 {
  font-style: normal;
  font-weight: bold;
  color: #eee;
  font-size: 8vmin;
  padding: 10px;
  letter-spacing: 0.03em;
  line-height: 1;
  text-shadow: 1px 2px 4px rgba(0, 0, 0, 0.8);
  margin-bottom: 72px;
}

button {
  background: #177392;
  transition: background ease 0.25s;
  border-radius: 50px;
  display: inline-block;
  border: none;
  padding: 0.75rem 1.5rem;
  margin-left: 10px;
  text-decoration: none;
  color: #ffffff;
  font-size: 1.2rem;
  cursor: pointer;
  text-align: center;
  -webkit-appearance: none;
  -moz-appearance: none;
}
button:hover {
  background: #10bec1;
}
button:focus {
  outline: 1px solid #fff;
  outline-offset: -4px;
}
</style>

    

      

    