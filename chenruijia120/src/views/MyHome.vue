<template>
    <div class="main" id="homeSection">
      <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
      
      <el-container style="padding: 1%;">
        <el-main  ref="scrollHost" style="padding-top: 0%;">
          <div class="top-nav" :class="{ 'nav-hidden': hideNav }">
            <el-menu
              :default-active="activeSection"
              mode="horizontal"
              class="nav-menu"
              @select="handleNavSelect"
            >
              <el-menu-item index="home">Home</el-menu-item>
              <el-menu-item index="pubSection">Publications</el-menu-item>
              <el-menu-item index="internshipSection">Internships</el-menu-item>
              <el-menu-item index="experiencesSection">Research Experiences</el-menu-item>
              <el-menu-item index="servicesSection">Services and Teaching</el-menu-item>
              <el-menu-item index="resume">Resume</el-menu-item>
            </el-menu>
          </div>
          <!-- <el-tabs v-bind:value="activeNames.activeName" :key="activeNames" @tab-click="handleClick">
            <el-tab-pane label="Home" name="home"  id="home" aria-labelledby="tab-home"> -->
              <br/>
              <br/>
              <div>
                <el-row id="home">
                <el-col :span="isDesktop ? 5 : 24" style="text-align: center;padding-top: 0.6%;" class="avatar-col">
                  <el-avatar :size="avatarSize" :src="avatarURL" shape="square" alt="Ruijia Chen's avatar"/>
                  <el-row id="icons">
                      <!-- <span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span> -->
                      <a href="mailto:ruijia.chen@wisc.edu" style='color:black' class="icon" aria-label="Email Ruijia Chen">
                        <i class="fa fa-envelope" id="email"></i>
                      </a>
                      <span>&nbsp;&nbsp;</span>
                      <a href="https://www.linkedin.com/in/ruijia-chen-094b48249/" target="_blank" style='color:black' rel="noopener noreferrer"  class="icon" aria-label="LinkedIn">
                        <i class="fa fa-linkedin" id="linkedin"></i>
                      </a>
                      <span>&nbsp;&nbsp;</span>
                      <a href="https://scholar.google.com/citations?user=jEHV3ucAAAAJ&hl=en&authuser=1" target="_blank" style='color:black' rel="noopener noreferrer"  class="icon" aria-label="Google Scholar">
                        <i class="fa fa-google" id="google"></i>
                      </a>
                      <span>&nbsp;&nbsp;</span>
                      <a href="https://github.com/chenruijia120" target="_blank" style='color:black' rel="noopener noreferrer" class="icon" aria-label="GitHub">
                        <i class="fa fa-github" id="github"></i>
                      </a>
                  </el-row>
                </el-col>
  
                <el-col :span="isDesktop ? 19 : 24" style="padding-left: 4%; padding-right: 2.5%;" class="text-col">
                  <div class="myName">Ruijia Chen</div>
                  <div id="introduction">
                  <br/>
                  <p class="paragraph">
                    Welcome! My name is Ruijia Chen, pronounced as ray-jar (in Chinese: 陈睿嘉).
                  </p>
                  <p class="paragraph">
                    I am currently a third-year Ph.D. student in Computer Science at the University of Wisconsin-Madison, advised by <a href="https://www.yuhangz.com/" style='color:var(--link-color)' target="_blank">Prof. Yuhang Zhao</a>. 
                    Previously, I completed my B.E. in Computer Science at Tsinghua University, advised by <a href="https://pi.cs.tsinghua.edu.cn/lab/people/YuntaoWang/en/" style='color:var(--link-color)' target="_blank">Prof. Yuntao Wang</a>.
                    <!-- <a href="https://pi.cs.tsinghua.edu.cn/" style='color:#9966CC' target="_blank">Pervasive Interaction Lab, Department of Computer Science, Tsinghua University</a>. -->
                  </p>
                  <p class="paragraph">
                    My research interests lie in 
                    <span style='color:var(--primary-color);font-weight: bolder;'>Human-Computer Interaction</span>,
                    especially 
                    <span style='color:var(--primary-color);font-weight: bolder;'>augmented reality and accessibility</span>. 
                    I design and develop AR technology to automatically recognize surrounding visual information that cannot be easily perceived by people with low vision, 
                    and generate suitable multi-modal feedback to enhance their perceptual abilities in various daily tasks.
                  </p>
                  <!-- <p class="paragraph">
                    <span style='color:var(--primary-color);font-weight: bolder;'>Looking for research internship for Summer 2025!</span>
                  </p> -->
                </div>
                </el-col>
              </el-row>
              </div>
              <br/>
              <div>
              <h5 id="services-title" class="section">
                  News
              </h5>
              <el-card :span="18" class="box-card no-padding" id="news">
              <el-scrollbar class="scroll-box-el" tabindex="0" style="padding-top: 0%;margin-top: 0%;" :always="true">
              <ul class="news-list" style="padding-top: 1%;margin: 0%;padding-left: 2%;padding-bottom: 1%;">
                <li class="news-item">
                  <span class="news-date">Jan 15th, 2026</span>
                  <span class="news-text">
                    NaviNote, my internship project at Niantic Spatial, has been accepted to CHI'26!
                  </span>
                </li>
                <li class="news-item">
                  <span class="news-date">Jun 18th, 2025</span>
                  <span class="news-text">
                    Two papers accepted to ASSETS 2025. Congratulations to my co-authors!
                  </span>
                </li>
                <li class="news-item">
                  <span class="news-date">May 13th, 2025</span>
                  <span class="news-text">
                    Started my internship at Niantic Spatial in London, UK!
                  </span>
                </li>
                <li class="news-item">
                  <span class="news-date">May 1st, 2025</span>
                  <span class="news-text">
                    Presented <a href="https://dl.acm.org/doi/full/10.1145/3706598.3713847" style='color:var(--link-color)' target="_blank">VisiMark</a> at CHI'25 in Yokohama, Japan!
                  </span>
                </li>
                <li class="news-item">
                  <span class="news-date">Apr 26th, 2025</span>
                  <span class="news-text">
                    Excited to be a student volunteer at CHI'25!
                  </span>
                </li>
                <li class="news-item">
                  <span class="news-date">Feb 22th, 2025</span>
                  <span class="news-text">
                    One poster accepted to CHI'25!
                  </span>
                </li>
                <li class="news-item">
                  <span class="news-date">Jan 16th, 2025</span>
                  <span class="news-text">
                    Two full papers accepted to CHI'25!
                  </span>
                </li>
              </ul>
              </el-scrollbar>
              </el-card>
              </div>
              <br/>
              <br/>
              <PublicationsSection id="pubSection"/>
              <br/>
              <br/>
              <InternshipSection id="internshipSection"/>
              <br/>
              <br/>
              <ExperiencesSection id="experiencesSection"/>
              <br/>
              <br/>
              <ServicesSection id="servicesSection"/>
              <br/>
              <br/>
            <!-- </el-tab-pane>
  
            <el-tab-pane label="Publications" name="pub" aria-labelledby="tab-publications"></el-tab-pane>
            <el-tab-pane label="Internships" name="internship" aria-labelledby="tab-internships"></el-tab-pane>
            <el-tab-pane label="Research Experiences" name="experiences" aria-labelledby="tab-research-experiences"></el-tab-pane>
            <el-tab-pane label="Services and Teaching" name="services" aria-labelledby="tab-services-and-teaching"></el-tab-pane>
            <el-tab-pane label="Resume" name="resume" aria-labelledby="tab-resume"></el-tab-pane>
          </el-tabs> -->
        </el-main>
  
        <el-backtop :right="100" :bottom="100" />
      </el-container>
      </div>
  </template>

<script>
import ExperiencesSection from './ExperiencesSection.vue'
import PublicationsSection from './PublicationsSection.vue'
import ServicesSection from './ServicesSection.vue'
import InternshipSection from './InternshipSection.vue'

export default {
  name: "MyHome",
  components: {
    ExperiencesSection,
    PublicationsSection,
    ServicesSection,
    InternshipSection
  },
  data() {
    return {
      hideNav: false,
      lastScrollY: 0,
      activeSection: 'home',
      avatarURL: require('@/assets/photo2503.jpg'),
      windowWidth: document.documentElement.clientWidth,
      windowHeight: document.documentElement.clientHeight,
    };
  },
  methods: {
    handleNavSelect(index) {
      if (index === 'resume') {
        window.open(
          "https://drive.google.com/file/d/1a8mV8ntZzEHoXsRal8r_m023pGHoJWkt/view?usp=sharing",
          "_blank"
        );
        return;
      }
      
      const el = document.getElementById(index);
      if (el) {
        el.style.scrollMarginTop = "90px";
        el.scrollIntoView({ behavior: "smooth" });
        this.activeSection = index;
      }
    },
  },
  mounted() {
    this._onResize = () => {
      this.windowHeight = document.documentElement.clientHeight;
      this.windowWidth = document.documentElement.clientWidth;
    };
    window.addEventListener("resize", this._onResize, { passive: true });
    this.$nextTick(() => {
      const host = this.$refs.scrollHost?.$el || this.$refs.scrollHost;
      if (!host) return;

      this._onScroll = () => {
        if (this.windowWidth > 1050) {
          this.hideNav = false;
          return;
        }
        const y = host.scrollTop;
        this.hideNav = y > 10;
      };

      host.addEventListener("scroll", this._onScroll, { passive: true });
      this._scrollHost = host;
    });
  },
  beforeDestroy() {
    window.removeEventListener("resize", this._onResize);
    if (this._scrollHost && this._onScroll) {
      this._scrollHost.removeEventListener("scroll", this._onScroll);
    }

  },
  computed: {
    isDesktop() {
      return this.windowWidth >= 1050;
    },
    avatarSize() {
      if (this.windowWidth <= 420) return 180;
      if (this.windowWidth <= 1500) return 210;
      return 280;
    },
  },

};
</script>

<style>
  :root {
    --primary-color: #660066;
    --text-color: darkslategrey;
    --secondary-text-color: rgb(37, 37, 37);
    --dark-grey:rgb(45, 45, 45);
    --link-color: #4d2179;
    --conference-color:#910191;
  }
  .el-container{
    height:100%;
    overflow: visible;
    position: relative;
  }

  #homeSection {
    height: 100%;
    overflow: visible;
    position: relative;
  }


  .el-tab-pane {
    padding-top: 1%;
  }

  .el-tabs__header.is-top{
    position: sticky;
    top: 0;
    z-index: 999;
    background-color: #fff;
    padding-top: 1%;
  }

  
  .el-tabs{
    padding-left:5%;
    padding-right:5%;
    /* text-align: center; */
    font-size: 30px;
  }

  .myName{
    font-size: 40px;
    font-weight: bolder;
    font-family:MYFONT;
  }

  #introduction{
    padding-right: 2%;
    font-size: medium;
  }

  .paragraph{
    margin-bottom: 20px;
    color:var(--text-color);
  }

  .project-title{
    font-size: large;
    font-weight:500;
    margin-bottom: 3%;
  }

  .project-conference{
    font-size: medium;
    color: var(--conference-color);
    font-weight: 500;
    margin-bottom: 0%;
    /* font-family:'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif; */
  }

  .research-content{
    font-size: medium;
    /* font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif; */
    
    font-family:'Times New Roman', Times, serif;
  }


  .project-author{
    font-size: medium;
    font-family:'Times New Roman', Times, serif;
  }
  
  .research{
    font-size: large;
    font-weight:500;
    /* font-family:'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif; */
    margin-bottom: 2%;
  }

  
  .service_para{
    font-size: large;
    font-weight:500;
    /* font-family:'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif; */
    /* margin-bottom: 2%; */
  }

  .news-item{
    font-size: medium;
    color: var(--text-color);
    margin-bottom: 10px;
  }

  .research-time{
    font-size: medium;
    /* font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; */
    color: var(--conference-color);
  }

  .pub-images{
    display: flex;
    justify-content: flex-end;
    padding-left: 1%;
  }
  .pub-images-small{
    display: flex;
    justify-content: flex-end;
    padding-left: 5%;
    padding-right:5%;
  }

  

  #projects{
    padding-left: 50px;
    padding-right: 100px;
  }

  #experience{
    margin-left: 50px;
    margin-right: 100px;
  }

  #internship{
    margin-left: 50px;
    margin-right: 100px;
  }


  #services{
    margin-left: 50px;
    margin-right: 100px;
  }
  
  #publications{
    margin-left: 50px;
    margin-right: 100px;
  }

  .section{
    margin-left: 50px;
    color: rgb(79, 78, 78); 
    font-family:'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif ;
    font-size: 32px;
  }

  .scroll-box-el {
    height: 150px;
    /* border: 1px solid #ddd;
    border-radius: 6px;
    padding: 10px 14px;
    background: #fff; */
  }

  .scroll-box-el:focus {
    outline: 2px solid #9966CC;
  }

  
  .scroll-box-el .el-scrollbar__bar {
    opacity: 1 !important;
  }

  .scroll-box-el .el-scrollbar__bar.is-vertical,
  .scroll-box-el .el-scrollbar__bar.is-horizontal {
    display: block !important;
  }

  #news{
    margin-left: 50px;
    margin-right: 100px;
  }

  .news-item {
    display: flex;
    align-items: flex-start;
    /* margin: 6px 0; */
    font-family: "Times New Roman", Times, serif;
    font-size: large;
  }

  .news-date {
    color: var(--conference-color);
    font-weight: bold;
    width: 135px;
    flex-shrink: 0;
  }

  .news-text {
    flex: 1;
  }
  .icon{
    font-size: x-large;
  }

  .image-placeholder {
    width: 100%;
    height: 180px;     
    display: flex;
    align-items: center; 
    justify-content: center; 

    font-family: "Times New Roman", Times, serif;
    font-size: x-large;
    color: #343434;
    font-style: italic;

    border: 1px dashed #ddd;
    border-radius: 4px;
  }

  .no-padding .el-card__body { padding: 0 !important; }
  .pub-button span { font-size: 16px; }

  .el-button--primary,
  .el-button--primary:focus,
  .el-button--primary:active,
  .el-button--primary.is-focus {
    color: #fff !important;
    background-color: var(--primary-color) !important;
    border-color: var(--primary-color) !important;
  }

  .top-nav {
    position: sticky;
    top: 0;
    z-index: 999;
    background: #fff;
    padding-top: 8px;
    transition: transform 0.25s ease, opacity 0.25s ease;
  }

  .nav-hidden {
    transform: translateY(-100%);
    opacity: 0;
    pointer-events: none;
  }

  .nav-menu {
    padding-left: 5%;
    padding-right: 5%;
  }

  .nav-menu .el-menu-item {
    font-size: 20px;
    font-weight: 500;
  }

  .nav-menu .el-menu-item.is-active {
    color: var(--primary-color) !important;
    border-bottom: 2px solid var(--primary-color) !important;
  }

  .page-section {
    scroll-margin-top: 90px;
  }

  @media (max-width: 1050px){
    
    .nav-menu {
      padding-left: 2%;
      padding-right: 2%;
    }
    .nav-menu .el-menu-item {
      font-size: 16px;
      padding: 0 10px;
    }
    .section{
      margin-left: 3%;
      color: rgb(79, 78, 78); 
      font-family:'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif ;
      font-size: 24px;
    }
    .el-tabs {
      font-size: 26px;
      padding-left: 2%;
      padding-right: 2%;
    }
    .myName { font-size: 28px; }
      #introduction{
      padding-right: 5px;
      font-size: medium;
    }
    #projects{
      padding-left: 5px;
      padding-right: 5px;
    }
    #experience{
      margin-left: 5px;
      margin-right: 5px;
    }
    #publications{
      margin-left: 5px;
      margin-right: 5px;
    }
    #services{
      margin-left: 5px;
      margin-right: 5px;
    }
    #internship{
      margin-left: 5px;
      margin-right: 5px;
    }
    #news{
      margin-left: 5px;
      margin-right: 5px;
    }
    #icons{
      /* margin-left: 0px; */
      padding-left: 3%;
    }
    .icon{
      font-size: medium;
    }
    .news-item { font-size: medium; }
    .news-date { width: 105px; }
    .pub-images{
      width: 0px;
    }
  }

</style>