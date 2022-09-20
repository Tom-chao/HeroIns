<template>
  <section id="work" class="work active">
    <div class="my-work p-3">
      <h3 class="specialtitle">Recent<span>work</span></h3>
      <div class="work-container">
        <div class="box">
          <div class="box-img">
            <img src="../assets/work-1.jpg" alt="" />
          </div>
          <div class="box-content">
            <h4>lorem impsum dolor</h4>
            <p><span>Web Design</span> / 18 Sep. 2018</p>
          </div>
        </div>
        <div class="box">
          <div class="box-img">
            <img src="../assets/work-2.jpg" alt="" />
          </div>
          <div class="box-content">
            <h4>loreda cuno nere</h4>
            <p><span>Web Design </span>/ 18 Sep. 2018</p>
          </div>
        </div>
        <div class="box">
          <div class="box-img">
            <img src="../assets/work-3.jpg" alt="" />
          </div>
          <div class="box-content">
            <h4>mavrito lana dere</h4>
            <p><span>Web Design </span>/ 18 Sep. 2018</p>
          </div>
        </div>
        <div class="box">
          <div class="box-img">
            <img src="../assets/work-4.jpg" alt="" />
          </div>
          <div class="box-content">
            <h4>bindo laro cado</h4>
            <p><span>Web Design </span>/ 18 Sep. 2018</p>
          </div>
        </div>
        <div class="box">
          <div class="box-img">
            <img src="../assets/work-5.jpg" alt="" />
          </div>
          <div class="box-content">
            <h4>studio lena mado</h4>
            <p><span>Web Design </span>/ 18 Sep. 2018</p>
          </div>
        </div>
        <div class="box">
          <div class="box-img">
            <img src="../assets/work-6.jpg" alt="" />
          </div>
          <div class="box-content">
            <h4>studio big bang</h4>
            <p><span>Web Design </span>/ 18 Sep. 2018</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'WorkView'
}
</script>

<style scoped>
.work .my-work .work-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(min(24.9rem, 100%), 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.work .my-work .work-container .box {
  box-shadow: 0 1.3rem 0.8rem -1rem rgba(0 0 0 / 10%);
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}

.work .my-work .work-container .box .box-img {
  position: relative;
  overflow: hidden;
  max-height: 15.8rem;
}

.work .my-work .work-container .box .box-img::before {
  content: '';
  position: absolute;
  width: 100%;
  height: 100%;
  inset: 0;
  z-index: 1;
  background: linear-gradient(
    135deg,
    rgba(120, 204, 109, 0.5) 0,
    rgba(120, 204, 109, 0.1) 100%
  );
}

.work .my-work .work-container .box img {
  max-width: 100%;
  transition: all 1s ease-in-out;
}

.work .my-work .work-container .box:hover img {
  transform: scale(1.3);
}

.work .my-work .work-container .box .box-content {
  padding: 2rem 1rem;
}

.work .my-work .work-container .box .box-content h4 {
  font-size: 1.3rem;
  text-transform: capitalize;
  margin-bottom: 0.5rem;
  font-weight: 600;
}

.work .my-work .work-container .box .box-content p {
  color: var(--blackColor);
  font-size: 1.1rem;
}

.work .my-work .work-container .box .box-content p span {
  color: var(--greenColor);
}
@media (min-width: 1200px) {
  .about,
  .resume,
  .work,
  .blog,
  .contact {
    position: absolute;
    overflow: auto;
    overflow-x: hidden;
    top: 0;
    left: 47%;
    right: 0;
    bottom: 1.5rem;
    max-width: 65rem;
    height: 100%;
    z-index: -1;
  }
}
@media (min-width: 1234px) {
  .about,
  .resume,
  .work,
  .blog,
  .contact {
    left: 45%;
  }
}
</style>
