<template>
  <section id="about" class="about active">
    <div class="about-me p-3">
      <h3 class="specialtitle">关于 <span>我</span></h3>
      <div class="row">
        <div class="text">
          <p>
            我叫曹永超，是一名初级前端开发人员，今年23岁，毕业于南阳理工学院计算机与软件学院，
            有一定的web开发经验，开发过响应式网页，小程序等。喜欢钻研新技术，乐于与人分享自己
            的见解。热爱生活，积极向上。
          </p>
        </div>
        <div class="info">
          <ul>
            <li><strong>年龄 . . . . .</strong> 23</li>
            <li><strong>性别 . . . . .</strong> 男</li>
            <li><strong>职业状况 . . . . .</strong> 无</li>
            <li><strong>地址 . . . . .</strong> 河南</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="services p-3">
      <h3 class="specialtitle">my <span>services</span></h3>
      <div class="services-container">
        <div class="serv">
          <div class="icon">
            <i class="fas fa-code"></i>
          </div>
          <h4>web development</h4>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam,
            iste!
          </p>
        </div>
        <div class="serv">
          <div class="icon">
            <i class="fas fa-palette"></i>
          </div>
          <h4>web design</h4>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam,
            iste!
          </p>
        </div>
        <div class="serv">
          <div class="icon">
            <i class="fas fa-gamepad"></i>
          </div>
          <h4>game development</h4>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam,
            iste!
          </p>
        </div>
        <div class="serv">
          <div class="icon">
            <i class="fas fa-share-alt-square"></i>
          </div>
          <h4>social media</h4>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam,
            iste!
          </p>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'AboutView'
}
</script>
<style scoped>
.about-me .row .text {
  padding: 3rem 0.5rem;
}

.about-me .row .text p {
  line-height: 1.8em;
}

.about-me .info ul li {
  display: flex;
  justify-content: space-between;
  position: relative;
  text-transform: capitalize;
  font-size: 1.6rem;
  color: var(--textColor);
  text-align: right;
  padding: 1.1rem 0;
}

.about-me .info ul li strong {
  padding: 0.1rem 0.8rem;
}

.about-me .info ul li:not(:last-of-type)::before {
  content: '';
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 0.2rem;
  background: radial-gradient(
    ellipse at center,
    #ddd 0,
    rgba(255, 255, 255, 0) 70%
  );
}

@media (min-width: 768px) {
  .about-me .row {
    display: flex;
  }

  .about-me .info,
  .about-me .row .text {
    flex-basis: 50%;
    padding: 3rem 1rem;
    position: relative;
  }

  .about-me .row .text p {
    font-size: 1.5rem;
  }

  .about-me .info::before {
    content: '';
    position: absolute;
    top: 0;
    left: -0.1rem;
    width: 0.2rem;
    height: 100%;
    background: radial-gradient(
      ellipse at top,
      #ddd 0,
      rgba(255, 255, 255, 0) 70%
    );
  }
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

  .about-me .row .text {
    padding: 3rem 3rem 3rem 0;
  }

  .about-me .info {
    padding: 3rem;
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
@media (min-width: 1200px) {
  .about .services,
  .resume .skills {
    padding-top: 0;
  }
}
.services .services-container .serv {
  padding: 3rem;
  text-align: center;
  position: relative;
}

.services .services-container .serv:not(:last-child)::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 0.2rem;
  background: radial-gradient(
    ellipse at left,
    rgba(197, 202, 213, 0.7) 0,
    rgba(255, 255, 255, 0) 70%
  );
}

.services .services-container .serv .icon {
  width: 6rem;
  height: 6rem;
  border-radius: 50%;
  background-color: var(--greenColor);
  color: var(--whiteColor);
  font-size: 2rem;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-left: auto;
  margin-right: auto;
}

.services .services-container .serv h4 {
  font-size: 1.7rem;
  color: var(--blackColor);
  margin: 1rem 0 0.5rem;
}

@media (min-width: 768px) {
  .services .services-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(min(20rem, 100%), 1fr));
  }

  .services .services-container .serv:nth-child(even)::before {
    content: '';
    position: absolute;
    left: 0;
    bottom: 0;
    width: 0.2rem;
    height: 100%;
    background: radial-gradient(
      ellipse at left,
      rgba(197, 202, 213, 0.7) 0,
      rgba(255, 255, 255, 0) 70%
    );
  }

  .services .services-container .serv::after {
    content: '';
    position: absolute;
    left: 0;
    bottom: 0;
    width: 100%;
    height: 0.2rem;
    background: radial-gradient(
      ellipse at left,
      rgba(197, 202, 213, 0.7) 0,
      rgba(255, 255, 255, 0) 70%
    );
  }
}
</style>
