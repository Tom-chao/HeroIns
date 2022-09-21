<template>
  <div>
    <header>
      <div class="top-menu">
        <ul>
          <li class="active" data-menu="about">
            <router-link to="/about">
              <i class="fas fa-user"></i>
              <span class="link">关于</span>
            </router-link>
          </li>
          <li data-menu="resume">
            <router-link to="/resume">
              <i class="fas fa-file"></i>
              <span class="link">工作经历</span>
            </router-link>
          </li>
          <li data-menu="work">
            <router-link to="/work">
              <i class="fas fa-paint-brush"></i>
              <span class="link">项目经历</span>
            </router-link>
          </li>
          <li data-menu="blog">
            <router-link to="/blog">
              <i class="fas fa-comment-dots"></i>
              <span class="link">博客</span>
            </router-link>
          </li>
          <li data-menu="contact">
            <router-link to="/contact">
              <i class="fas fa-at"></i>
              <span class="link">联系方式</span>
            </router-link>
          </li>
        </ul>
      </div>
    </header>
    <!-- <router-view></router-view> -->
  </div>
</template>

<script>
export default {}
</script>

<style scoped rel="stylesheet/css">
header {
  position: fixed;
  width: 100%;
  top: 0;
  left: 0;
  z-index: 999;
}

header .top-menu {
  box-shadow: 0 0.5rem 1rem rgba(0 0 0 / 5%);
}

header .top-menu ul {
  display: flex;
}

header .top-menu ul li {
  min-width: 20%;
  background-color: var(--whiteColor);
}

header .top-menu ul li a {
  padding: 1.3rem 0.7rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
  cursor: pointer;
}

header .top-menu ul li:not(:first-of-type) a::before {
  content: '';
  position: absolute;
  width: 0.2rem;
  height: 100%;
  left: 0;
  top: 0;
  background: radial-gradient(
    ellipse at top,
    #ddd 0,
    rgba(255, 255, 255, 0) 70%
  );
}

header .top-menu ul li a i {
  color: var(--blackColor);
  font-size: 2rem;
  line-height: 3rem;
  transition: all 0.3s;
}

header .top-menu ul li a .link {
  font-weight: 500;
  font-size: 1.1rem;
  text-transform: uppercase;
  line-height: 1.3rem;
  color: var(--blackColor);
  transition: all 0.3s;
}

header .top-menu ul li.active a i,
header .top-menu ul li.active a .link,
header .top-menu ul li:hover a i,
header .top-menu ul li:hover a .link {
  color: var(--greenColor);
}

@media (min-width: 561px) {
  header {
    width: 7.2rem;
    top: 2rem;
    left: auto;
    margin-left: -8.5rem;
  }

  header .top-menu {
    border-radius: 0.4rem;
  }

  header .top-menu ul {
    flex-direction: column;
  }

  header .top-menu ul li:first-of-type {
    border-radius: 0.4rem 0.4rem 0 0;
  }

  header .top-menu ul li:last-of-type {
    border-radius: 0 0 0.4rem 0.4rem;
  }

  header .top-menu ul li:not(:first-of-type) a::before {
    width: 100%;
    height: 0.1rem;
    background: radial-gradient(
      ellipse at right,
      #ddd 0,
      rgba(255, 255, 255, 0) 70%
    );
  }
}
</style>
