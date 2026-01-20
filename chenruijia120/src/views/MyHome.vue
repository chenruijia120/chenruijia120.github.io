<template>
    <div class="main" id="homeSection">
      <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
      
      <el-container >
        <el-main style="padding-top: 0%;">
          <el-tabs v-bind:value="activeNames.activeName" :key="activeNames" @tab-click="handleClick">
            <el-tab-pane label="Home" name="home"  id="home">
              <br/>
              <div>
                <el-row>
                <el-col :span="isDesktop ? 5 : 24" style="text-align: center;padding-top: 0.6%;" class="avatar-col">
                  <el-avatar :size="avatarSize" :src="avatarURL" shape="square"/>
                  <el-row id="icons">
                      <!-- <span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span> -->
                      <a href="mailto:ruijia.chen@wisc.edu" style='color:black' class="icon">
                        <i class="fa fa-envelope" id="email"></i>
                      </a>
                      <span>&nbsp;&nbsp;</span>
                      <a href="https://www.linkedin.com/in/ruijia-chen-094b48249/" target="_blank" style='color:black' rel="noopener noreferrer"  class="icon">
                        <i class="fa fa-linkedin" id="linkedin"></i>
                      </a>
                      <span>&nbsp;&nbsp;</span>
                      <a href="https://scholar.google.com/citations?user=jEHV3ucAAAAJ&hl=en&authuser=1" target="_blank" style='color:black' rel="noopener noreferrer"  class="icon">
                        <i class="fa fa-google" id="google"></i>
                      </a>
                      <span>&nbsp;&nbsp;</span>
                      <a href="https://github.com/chenruijia120" target="_blank" style='color:black' rel="noopener noreferrer" class="icon">
                        <i class="fa fa-github" id="github"></i>
                      </a>
                  </el-row>
                </el-col>
  
                <el-col :span="isDesktop ? 19 : 24" style="padding-left: 4%;" class="text-col">
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
              <el-scrollbar class="scroll-box-el" style="padding-top: 0%;margin-top: 0%;" :always="true">
              <ul class="news-list" style="padding-top: 0%;margin-top: 0%;margin-left: 0%;padding-left: 0%;">
                <li class="news-item">
                  <span class="news-date">Jan 15th, 2026</span>
                  <span class="news-text">
                    NaviNote, my internship project at Niantic Spatial, has been conditionally accepted to CHI'26!
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
            </el-tab-pane>
  
            <el-tab-pane label="Publications" name="pub"></el-tab-pane>
            <el-tab-pane label="Internships" name="internship"></el-tab-pane>
            <el-tab-pane label="Research Experiences" name="experiences"></el-tab-pane>
            <el-tab-pane label="Services and Teaching" name="services"></el-tab-pane>
            <el-tab-pane label="Resume" name="resume"></el-tab-pane>
          </el-tabs>
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
      activeNames:{
        activeName: 'home',
        lastActiveName:'home',
      },
      avatarURL: require('@/assets/photo2503.jpg'),
      windowWidth: document.documentElement.clientWidth,
      windowHeight: document.documentElement.clientHeight,
    };
  },
  methods: {
    restoreActiveTab() {
      this.activeNames = Object.assign({}, this.activeNames, {
        activeName: this.activeNames.lastActiveName,
        lastActiveName: this.activeNames.lastActiveName
      })
    },
    handleClick(tab) {
      if (tab.name === 'resume') {
        window.open("https://drive.google.com/file/d/1a8mV8ntZzEHoXsRal8r_m023pGHoJWkt/view?usp=sharing", '_blank');
        this.restoreActiveTab();
      } 
      // else if(tab.name === 'pub') {
      //   this.restoreActiveTab();
      //   const section = document.getElementById("PublicationsSection");
      //   if (section) {
      //     section.scrollIntoView({ behavior: "smooth" });
      //   }
      // }
      else  if(tab.name === 'home'){
        this.restoreActiveTab();
        const section = document.getElementById(tab.name);
        if (section) {
          section.scrollIntoView({ behavior: "smooth" });
        }
      }
      else {
        this.restoreActiveTab();
        const section = document.getElementById(tab.name+"Section");
        if (section) {
          section.style.scrollMarginTop = "80px";
          section.scrollIntoView({ behavior: "smooth" });
        }
      }
    },
  },
    mounted(){
      var that = this;
        window.onresize = () => {
          return (() => {
            window.fullHeight = document.documentElement.clientHeight;
              window.fullWidth = document.documentElement.clientWidth;
            that.windowHeight = window.fullHeight;  // height
            that.windowWidth = window.fullWidth; // width
          })()
        };
    },
    watch: {
      windowHeight (val) {
        let that = this;
        console.log("screen height:",val, that.windowHeight );
      },
      windowWidth (val) {
        let that = this;
        console.log("screen width:",val, that.windowHeight );
      }
    },
  computed: {
    isDesktop() {
      return this.windowWidth >=992
    },
    avatarSize() {
    if (this.windowWidth <= 420) return 180;
    if (this.windowWidth <= 900) return 220;
    return 280;
  }
  },
};
</script>

<style>
  :root {
    --primary-color: #660066;
    --text-color: darkslategrey;
    --secondary-text-color: darkgray;
    --dark-grey:rgb(85, 85, 85);
    --link-color: #9966CC;
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
  }

  .scroll-box-el {
    height: 150px;
    /* border: 1px solid #ddd;
    border-radius: 6px;
    padding: 10px 14px;
    background: #fff; */
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



  @media (max-width: 900px){
    
    .section{
      margin-left: 3%;
      color: rgb(79, 78, 78); 
      font-family:'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif ;
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
      padding-left: 10%;
    }
    .icon{
      font-size: medium;
    }
    .news-item { font-size: medium; }
    .news-date { width: 105px; }
  }

</style>