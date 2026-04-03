<template>
    <div>
            <h5 class="section">
              Publications
            </h5>
            <el-button-group style="margin-left: 3%; ">
            <el-button class="pub-button" size="medium" :type="pubFilter==='selected' ? 'primary' : 'default'" @click="pubFilter='selected'">Selected publications</el-button>
            <el-button class="pub-button" size="medium" :type="pubFilter==='all' ? 'primary' : 'default'" @click="pubFilter='all'">All publications</el-button>
            <el-button class="pub-button" size="medium" :type="pubFilter==='full' ? 'primary' : 'default'" @click="pubFilter='full'">Full papers</el-button>
            <el-button class="pub-button" size="medium" :type="pubFilter==='posters' ? 'primary' : 'default'" @click="pubFilter='posters'">Posters</el-button>
            </el-button-group>
            <el-button-group style="margin-left: 3%; ">
            <el-button class="pub-button" size="medium" :type="pubFilter==='mr' ? 'primary' : 'default'" @click="pubFilter='mr'">Mixed Reality</el-button>
            <el-button class="pub-button" size="medium" :type="pubFilter==='a11y' ? 'primary' : 'default'" @click="pubFilter='a11y'">Accessibility</el-button>
            <el-button class="pub-button" size="medium" :type="pubFilter==='perception' ? 'primary' : 'default'" @click="pubFilter='perception'">User Perception</el-button>
            <el-button class="pub-button" size="medium" :type="pubFilter==='gaze' ? 'primary' : 'default'" @click="pubFilter='gaze'">Eye Tracking</el-button>
            </el-button-group>


            <p style="margin-left: 3%;font-size: large;font-family:'Times New Roman', Times, serif;">
              * Authors contributed equally to this research.</p>
            <br/>
            <el-card class="box-card" id="publications">

              
            <div v-show="pubFilter === 'selected' || pubFilter === 'all' || pubFilter === 'full' || pubFilter === 'a11y' || pubFilter === 'mr'">
              <el-row>
              <el-col v-if="isDesktop" :span="8" class="pub-images" alt="NaviNote teaser figure: A five-stage pipeline is shown with 5 panels. Each panel shows a user with a vest and speech bubbles communicating between NaviNote and the user. In (1), the user asks, ``Where am I?'' The system responds: ``You're at the park entrance. There's a statue nearby...'' The user follows up: ``Please, guide me to the statue!''; In (2) NaviNote provides navigation instructions, ``Walk straight for 15 meters...'', ``... podium ahead at 10 o'clock''; In (3) the user listens to a nearby spatial annotation, ``Be careful, there are 16 steps ahead''; In (4) the user asks: ``What did others say about the statue?'' The system responds: ``One annotation notes the statue is of Cicero, a famed orator, lawyer and politician.''; In (5) the user creates their own spatial annotation, ``There's a nice café with accessible restrooms here.''. During the interaction, the user wears a vest that holds the smartphone with camera facing forward, and localizes their precise positions using Visual Positioning System (VPS) in a pre-scanned area on the smartphone.">
                <!-- <div class="image-placeholder">Coming soon</div> -->
                <el-image :src="srcNaviNote" style="padding-top: 3%;padding-bottom: 5%;"></el-image>
              </el-col>
              <el-col :span="isDesktop ? 15 : 24" style="margin-left: 2%;">
                <p class="project-title">
                  NaviNote: Enabling In-situ Spatial Annotation Authoring to Support Exploration and Navigation for Blind and Low Vision People
                </p>
                <p class="project-conference">To appear at CHI'26, 🏆Honourable Mention Award
                  &nbsp;
                  <span style="color:rgb(45, 45, 45) ;"><a href="https://www.youtube.com/watch?v=M0kIoho02hM" style="color:rgb(45, 45, 45) ;" target="_blank">[Presentation]</a></span> 
                  <span style="color:rgb(45, 45, 45) ;">&ensp;<a href="https://arxiv.org/pdf/2603.08837" style="color:rgb(45, 45, 45) ;" target="_blank">[Paper]</a></span>
                </p>
                <p class="project-author">
                  <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen<sup>1</sup></span>*, Yuheng Wu*, Charlie Houseago, Filipe Gaspar, Filippo Aleotti, Dorian Gálvez-López, Oliver Johnston, Diego Mazala, Guillermo Garcia-Hernando, Maryam Bandukda, Gabriel Brostow, Jessica Van Brummelen
                </p>
                <div style="margin-top:2% ;"></div>
              </el-col>
              </el-row>
            <el-divider></el-divider>
            </div>
            
            
            <div v-show="pubFilter === 'all' ||pubFilter === 'full' || pubFilter === 'a11y' || pubFilter === 'gaze'">
              <el-row>
              <el-col v-if="isDesktop" :span="8" class="pub-images">
                <el-image :src="srcASSETS25Ru" style="padding-top: 3%;padding-bottom: 5%;" alt="This figure shows a five-panel visual illustration showcasing five types of visual intent during image-viewing: Searching, Observing, Traversing, Comparing, and Exploring. Each panel contains an an illustration of the same example image (four people having a picnic on the foreground of the image) with mock gaze trajectories overlaid as colored lines and dots representing saccades and fixations. The 'Searching' panel shows sparse gaze scanpaths moving towards the person on the left. 'Observing' shows fixations clustered on the person on the left. 'Traversing' displays scanpaths across multiple people one by one from left to right. 'Comparing' includes back-and-forth gaze movements between the two people on the right. 'Exploring' shows broader, scattered gaze paths covering the entire image. The gaze paths are illustrative and not drawn from real data."></el-image>
              </el-col>
              <el-col :span="isDesktop ? 15 : 24" style="margin-left: 2%;">
                <p class="project-title">
                  Characterizing Visual Intents for People with Low Vision through Eye Tracking
                </p>
                <p class="project-conference">Proceedings of the 27th International ACM SIGACCESS Conference on Computers and Accessibility (ASSETS '25)
                  &nbsp;
                  <span style="color:rgb(45, 45, 45) ;">&ensp;<a href="https://dl.acm.org/doi/full/10.1145/3663547.3746391" style="color:rgb(45, 45, 45) ;" target="_blank">[Paper]</a></span>
                </p>
                <p class="project-author">
                  Ru Wang, <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen<sup>2</sup></span>, Anqiao Erica Cai, Zhiyuan Li, Sanbrita Mondal, Yuhang Zhao
                </p>
                <div style="margin-top:2% ;"></div>
              </el-col>
              </el-row>

            <el-divider></el-divider></div>


            <div v-show="pubFilter === 'all' ||pubFilter === 'full' || pubFilter === 'a11y'">
              <el-row>
              <el-col v-if="isDesktop" :span="8" class="pub-images">
                <el-image :src="srcASSETS25Hazel" style="padding-top: 3%;padding-bottom: 5%;" alt="FocusView teaser figure: Illustration of a distracted learner watching an educational video with visual and audio distractions like music and pop-ups in thought bubbles. The center shows a customizable video interface with controls for audio (denoise & enhance), background (blur/remove), layout options (original, auxiliary removal, speaker focus, content focus), and captions (color, font, size, position, highlight). A processed video on the right displays improved clarity with speaker focus and enhanced captions. Icons below indicate clear speech is kept while music is removed."></el-image>
              </el-col>
              <el-col :span="isDesktop ? 15 : 24" style="margin-left: 2%;">
                <p class="project-title">
                  FocusView: Understanding and Customizing Informational Video Watching Experiences for Viewers with ADHD
                </p>
                <p class="project-conference">Proceedings of the 27th International ACM SIGACCESS Conference on Computers and Accessibility (ASSETS '25)
                  &nbsp;
                  <span style="color:rgb(45, 45, 45) ;">&ensp;<a href="https://dl.acm.org/doi/full/10.1145/3663547.3746386" style="color:rgb(45, 45, 45) ;" target="_blank">[Paper]</a></span>
                </p>
                <p class="project-author">
                  Hanxiu 'Hazel' Zhu, <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen<sup>2</sup></span>, Yuhang Zhao
                </p>
                <div style="margin-top:2% ;"></div>
              </el-col>
              </el-row>

            <el-divider></el-divider></div>

            <div v-show="pubFilter === 'all' ||pubFilter === 'posters' || pubFilter === 'perception' || pubFilter === 'mr'">
              <el-row>
              <el-col v-if="isDesktop" :span="8" class="pub-images">
                <el-image :src="srcCHI25EA" style="padding-top: 3%;padding-bottom: 5%;" alt="This image shows an overview of task interpretations, illustrating: (A) Two primary writing behaviors when responding to drift: following drifted location absolutely versus estimating the un-drifted position; (B) Path deviations from center while following virtual drifted line (red) versus actual invisible line (white); (C) Participant's writing paper with original paper overlaid, showing appropriate blanks (blue boxes) and corresponding written words."></el-image>
              </el-col>
              <el-col :span="isDesktop ? 15 : 24" style="margin-left: 2%;">
                <p class="project-title">
                  Understanding Mixed Reality Drift Tolerance
                </p>
                <p class="project-conference">Proceedings of the Extended Abstracts of the CHI Conference on Human Factors in Computing Systems (CHI EA '25)
                  &nbsp;
                  <span style="color:rgb(45, 45, 45) ;"><a href="https://www.youtube.com/watch?v=Mn6fU_YFgyE" style="color:rgb(45, 45, 45) ;" target="_blank">[Video]</a></span> 
                  <span style="color:rgb(45, 45, 45) ;">&ensp;<a href="https://dl.acm.org/doi/10.1145/3706599.3720161" style="color:rgb(45, 45, 45) ;" target="_blank">[Paper]</a></span>
                </p>
                <p class="project-author">
                  Daniel Killough*, <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen<sup>1</sup></span>*, Yuhang Zhao, Bilge Mutlu
                </p>
                <div style="margin-top:2% ;"></div>
              </el-col>
              </el-row>
            <div v-show="pubFilter !=='posters'">
            <el-divider></el-divider>
            </div>
            </div>

            <div v-show="pubFilter === 'selected' || pubFilter === 'all' ||pubFilter === 'full' || pubFilter === 'a11y' || pubFilter === 'mr'">
              <el-row>
              <el-col v-if="isDesktop" :span="8" class="pub-images">
                <el-image :src="srcVisiMark" style="padding-top: 3%;padding-bottom: 5%;" alt="This image shows VisiMark system. VisiMark provides landmark augmentations on head-mounted AR to support wayfinding and mental map construction. VisiMark includes two features: (A) Signboard, an overview of hallway structures and upcoming landmarks at intersections, and (B) In-situ Labels, world-anchored icons and texts to highlight the types and positions of landmarks in the physical environment."></el-image>
              </el-col>
              <el-col :span="isDesktop ? 15 : 24" style="margin-left: 2%;">
                <p class="project-title">
                  VisiMark: Characterizing and Augmenting Landmarks for People with Low Vision in Augmented Reality to Support Indoor Navigation
                </p>
                <p class="project-conference">Proceedings of the 2025 CHI Conference on Human Factors in Computing Systems (CHI '25)
                  &nbsp;
                  <span style="color:rgb(45, 45, 45) ;"><a href="https://www.youtube.com/watch?v=LqkjHBSFaM0" style="color:rgb(45, 45, 45) ;" target="_blank">[Presentation]</a></span> 
                  <!-- &nbsp; -->
                  <span style="color:rgb(45, 45, 45) ;">&ensp;<a href="https://drive.google.com/file/d/1Nyx-t0yRIImjBIoKNLLwttbZ5fFA2Myd/view?usp=sharing" style="color:rgb(45, 45, 45) ;" target="_blank">[Demo]</a></span> 
                  <!-- &nbsp; -->
                  <span style="color:rgb(45, 45, 45) ;">&ensp;<a href="https://dl.acm.org/doi/full/10.1145/3706598.3713847" style="color:rgb(45, 45, 45) ;" target="_blank">[Paper]</a></span>
                </p>
                <p class="project-author">
                  <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen<sup>1</sup></span>, Junru Jiang, Pragati Maheshwary, Brianna R Cochran, Yuhang Zhao
                </p>
                <div style="margin-top:2% ;"></div>
              </el-col>
              </el-row>

            <div v-show="pubFilter !=='selected' && pubFilter !=='a11y'">
            <el-divider></el-divider>
            </div>
            </div>

            <div v-show="pubFilter === 'all' ||pubFilter === 'full' || pubFilter === 'perception' || pubFilter === 'mr' || pubFilter === 'gaze'">
              <el-row>
              <el-col v-if="isDesktop" :span="8" class="pub-images-small">
                <el-image :src="srcCHI25THU" style="padding-top: 3%;padding-bottom: 5%;" alt="The apparatus of the formative study. Wearing aheadset, the participant wears three motion trackers to tracktheir arm pose and sit on a comfortable chair. While thevirtual avatar mirrors the arm movement of the participant,the participant observes the virtual avatar’s movement froma frst-person point of view and follows the semi-transparentcheckpoint pose to reach the semi-transparent target pose.As the secondary task, a virtual animation will start withdiferent durations and locations. The right fgure illustratesthe possible locations of the red ball, named Sparse, Median,and Dense, accordingly."></el-image>
              </el-col>
              <el-col :span="isDesktop ? 15 : 24" style="margin-left: 2%;">
                <p class="project-title">
                  Modeling the Impact of Visual Stimuli on Redirection Noticeability with Gaze Behavior in Virtual Reality
                </p>
                <p class="project-conference">Proceedings of the 2025 CHI Conference on Human Factors in Computing Systems (CHI '25)
                  &nbsp;
                  <span style="color:rgb(45, 45, 45) ;"><a href="https://www.youtube.com/watch?v=ZfLArnKg7gE" style="color:rgb(45, 45, 45) ;" target="_blank">[Video]</a></span> 
                  <span style="color:rgb(45, 45, 45) ;">&ensp;<a href="https://dl.acm.org/doi/full/10.1145/3706598.3713392" style="color:rgb(45, 45, 45) ;" target="_blank">[Paper]</a></span>
                </p>
                <p class="project-author">
                  Zhipeng Li, Yishu Ji, <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen<sup>3</sup></span>, Tianqi Liu, Yuntao Wang, Yuanchun Shi, Yukang Yan
                </p>
                <div style="margin-top:2% ;"></div>
              </el-col>
              </el-row>

            <div v-show="pubFilter !=='gaze'">
            <el-divider></el-divider>
            </div>
            </div>

            <div v-show="pubFilter === 'all' ||pubFilter === 'full' || pubFilter === 'mr'">
              <el-row>
              <el-col v-if="isDesktop" :span="8" class="pub-images">
                <el-image :src="srcCHI24" style="padding-top: 3%;padding-bottom: 5%;" alt="The image presents different AR cues, such as overview cues, including (1) head-attached map, and (2) 3D Floor plan. Highlighting cues includes (1) door with shade and door with Contour. Directional cues include (1) single arrow pointing a POI, and (2) an array of arrows indicating a path. Labeling cues include (1) icon and text labeling an object, and (2) icons labeling a victim."></el-image>
              </el-col>
              <el-col :span="isDesktop ? 15 : 24" style="margin-left: 2%;">
                <p class="project-title">
                  Exploring the Design Space of Optical See-through AR Head-Mounted Displays to Support First Responders in the Field
                </p>
                <p class="project-conference">Proceedings of the 2024 CHI Conference on Human Factors in Computing Systems (CHI '24)
                  &nbsp;
                  <span style="color:rgb(45, 45, 45) ;"><a href="https://www.youtube.com/watch?v=ousbRtyklQI" style="color:rgb(45, 45, 45) ;" target="_blank">[Video]</a></span> 
                  <span style="color:rgb(45, 45, 45) ;">&ensp;<a href="https://dl.acm.org/doi/10.1145/3613904.3642195" style="color:rgb(45, 45, 45) ;" target="_blank">[Paper]</a></span>
                </p>
                <p class="project-author">
                  Kexin Zhang, Brianna R Cochran, <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen<sup>3</sup></span>, Lance Hartung, Bryce Sprecher, Ross Tredinnick, Kevin Ponto, Suman Banerjee, Yuhang Zhao
                </p>
                <div style="margin-top:2% ;"></div>
              </el-col>
              </el-row>

            <el-divider></el-divider></div>


            <div v-show="pubFilter === 'all' ||pubFilter === 'full' || pubFilter === 'perception' || pubFilter === 'mr'">
              <el-row>
              <el-col v-if="isDesktop" :span="8" class="pub-images-small">
                <el-image :src="srcIMWUT22" style="padding-top: 3%;padding-bottom: 5%;" alt="e investigate the effect of user-avatar movement inconsistency on body ownership. The image shows a person wearing a head-mounted VR headset, where the user's actual arm position is different from the virtual avatar."></el-image>
              </el-col>
              <el-col :span="isDesktop ? 15 : 24" style="margin-left: 2%;">
                <p class="project-title">
                  Modeling the Noticeability of User-Avatar Movement Inconsistency for Sense of Body Ownership Intervention
                </p>
                <p class="project-conference">Proceedings of the ACM on Interactive, Mobile, Wearable and Ubiquitous Technologies (IMWUT '22)
                  &nbsp;
                  <span style="color:rgb(45, 45, 45) ;"><a href="https://drive.google.com/file/d/15q4QfytW2d1L4mXLL7pibFZL5xWQFNT-/view?usp=sharing" style="color:rgb(45, 45, 45) ;" target="_blank">[Video]</a></span> 
                  <span style="color:rgb(45, 45, 45) ;">&ensp;<a href="https://dl.acm.org/doi/10.1145/3534590" style="color:rgb(45, 45, 45) ;" target="_blank">[Paper]</a></span>
                </p>
                <p class="project-author">
                  Zhipeng Li, Yu Jiang, Yihao Zhu, <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen<sup>4</sup></span>, Ruolin Wang, Yuntao Wang, Yukang Yan, Yuanchun Shi
                </p>
                <div style="margin-top:2% ;"></div>
              </el-col>
              </el-row></div>
            </el-card>
    </div>
  </template>
  
  <script>
  export default {
    name: 'PublicationsSection',
    data() {
      return {
        pubFilter: 'selected',
        srcIMWUT22:require('@/assets/IMWUT2022.png'),
        srcCHI24:require('@/assets/CHI2024.jpg'),
        srcVisiMark:require('@/assets/VisiMark.jpg'),
        srcNaviNote:require('@/assets/NaviNote.jpg'),
        srcCHI25EA:require('@/assets/MRDrift.jpg'),
        srcCHI25THU:require('@/assets/srcCHI25THU.jpg'),
        srcASSETS25Ru:require('@/assets/ASSETS25Ru.png'),
        srcASSETS25Hazel:require('@/assets/ASSETS26Hazel.jpg'),
        windowWidth: document.documentElement.clientWidth,
        windowHeight: document.documentElement.clientHeight,
      };
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
    // watch: {
    //   windowHeight (val) {
    //     let that = this;
    //     console.log("screen height:",val, that.windowHeight );
    //   },
    //   windowWidth (val) {
    //     let that = this;
    //     console.log("screen width:",val, that.windowHeight );
    //   }
    // },
    computed: {
      isDesktop() {
        return this.windowWidth >= 1050;
      }
  }
  };
  </script>
  