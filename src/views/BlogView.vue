<template>
  <section id="blog" class="blog">
    <div class="my-blog p-3">
      <h3 class="specialtitle">b <span>log</span></h3>
      <div class="blog-container">
        <div class="box">
          <div class="box-img">
            <img src="../assets/blog1.jpg" alt="" />
          </div>
          <div class="box-desc">
            <span>april 28, 2020</span>
            <a href="#">By spite about do of allow</a>
            <p>
              Ex audire suavitate has, ei quodsi tacimates sapientem sed, pri
              zril ubique ut. Te cule tation munere noluisse. Enim torquatos…
            </p>
          </div>
        </div>
        <div class="box">
          <div class="box-img">
            <img src="../assets/blog2.jpg" alt="" />
          </div>
          <div class="box-desc">
            <span>april 28, 2020</span>
            <a href="#">By spite about do of allow</a>
            <p>
              Ex audire suavitate has, ei quodsi tacimates sapientem sed, pri
              zril ubique ut. Te cule tation munere noluisse. Enim torquatos…
            </p>
          </div>
        </div>
        <div class="box">
          <div class="box-img">
            <img src="../assets/blog3.jpg" alt="" />
          </div>
          <div class="box-desc">
            <span>april 28, 2020</span>
            <a href="#">By spite about do of allow</a>
            <p>
              Ex audire suavitate has, ei quodsi tacimates sapientem sed, pri
              zril ubique ut. Te cule tation munere noluisse. Enim torquatos…
            </p>
          </div>
        </div>
        <div class="box">
          <div class="box-img">
            <img src="../assets/blog1.jpg" alt="" />
          </div>
          <div class="box-desc">
            <span>april 28, 2020</span>
            <a href="#">By spite about do of allow</a>
            <p>
              Ex audire suavitate has, ei quodsi tacimates sapientem sed, pri
              zril ubique ut. Te cule tation munere noluisse. Enim torquatos…
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'BlogView'
}
</script>

<style scoped>
.blog .my-blog .blog-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(min(22.6rem, 100%), 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.blog .my-blog .blog-container .box {
  cursor: pointer;
  transition: all 0.5s ease-in-out;
}

.blog .my-blog .blog-container .box .box-img {
  position: relative;
  overflow: hidden;
  max-height: 12rem;
}

.blog .my-blog .blog-container .box .box-img img {
  max-width: 100%;
  height: auto;
  position: relative;
  transition: all 1s ease-in-out;
}

.blog .my-blog .blog-container .box .box-img::before {
  content: '';
  position: absolute;
  inset: 0;
  width: 100%;
  height: 99.5%;
  z-index: 1;
  background: linear-gradient(
    135deg,
    rgba(120, 204, 109, 0.5) 0,
    rgba(120, 204, 109, 0.1) 100%
  );
}

.blog .my-blog .blog-container .box .box-img:hover img {
  transform: scale(1.3);
}

.blog .my-blog .blog-container .box .box-desc {
  text-align: center;
  padding: 1.5rem 0;
}

.blog .my-blog .blog-container .box .box-desc span {
  text-transform: capitalize;
  border: 0.1rem solid var(--greenColor);
  color: var(--greenColor);
  display: block;
  padding: 0 0.5rem;
  line-height: 1.8rem;
  font-size: 1.3rem;
  width: fit-content;
  margin: 0 auto 1.1rem auto;
}

.blog .my-blog .blog-container .box .box-desc a {
  padding-bottom: 0.5rem;
  font-size: 1.7rem;
  font-weight: 500;
  display: block;
  color: var(--blackColor);
  transition: all 0.3s ease-in-out;
}

.blog .my-blog .blog-container .box:hover .box-desc a {
  color: var(--greenColor);
}
</style>
