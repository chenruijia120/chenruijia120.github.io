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

              
            <!-- <div v-show="pubFilter === 'selected' || pubFilter === 'all' || pubFilter === 'full' || pubFilter === 'a11y' || pubFilter === 'mr'">
              <el-row>
              <el-col :span="8" class="pub-images">
                <el-image :src="srcNaviNote" style="padding-top: 3%;padding-bottom: 5%;"></el-image>
              </el-col>
              <el-col :span="15" style="margin-left: 2%;">
                <p class="project-title">
                  NaviNote: Enabling In-situ Spatial Annotation Authoring to Support Exploration and Navigation for Blind and Low Vision People
                </p>
                <p class="project-conference">To appear at CHI'26
                </p>
                <p class="project-author">
                  <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen<sup>1</sup></span>*, Yuheng Wu*, Charlie Houseago, Filipe Gaspar, Filippo Aleotti, Dorian Gálvez-López, Oliver Johnston, Diego Mazala, Guillermo Garcia-Hernando, Maryam Bandukda, Gabriel Brostow, Jessica Van Brummelen
                </p>
                <div style="margin-top:2% ;"></div>
              </el-col>
              </el-row>
            <el-divider></el-divider>
            </div> -->
                <!-- <div class="image-placeholder">Coming soon</div> -->
            
            
            <div v-show="pubFilter === 'all' ||pubFilter === 'full' || pubFilter === 'a11y' || pubFilter === 'gaze'">
              <el-row>
              <el-col :span="8" class="pub-images">
                <el-image :src="srcASSETS25Ru" style="padding-top: 3%;padding-bottom: 5%;"></el-image>
              </el-col>
              <el-col :span="15" style="margin-left: 2%;">
                <p class="project-title">
                  Characterizing Visual Intents for People with Low Vision through Eye Tracking
                </p>
                <p class="project-conference">Proceedings of the 27th International ACM SIGACCESS Conference on Computers and Accessibility (ASSETS '25)
                  &nbsp;
                  <span style="color:grey ;">&ensp;<a href="https://dl.acm.org/doi/full/10.1145/3663547.3746391" style="color:grey ;" target="_blank">[Paper]</a></span>
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
              <el-col :span="8" class="pub-images">
                <el-image :src="srcASSETS25Hazel" style="padding-top: 3%;padding-bottom: 5%;"></el-image>
              </el-col>
              <el-col :span="15" style="margin-left: 2%;">
                <p class="project-title">
                  FocusView: Understanding and Customizing Informational Video Watching Experiences for Viewers with ADHD
                </p>
                <p class="project-conference">Proceedings of the 27th International ACM SIGACCESS Conference on Computers and Accessibility (ASSETS '25)
                  &nbsp;
                  <span style="color:grey ;">&ensp;<a href="https://dl.acm.org/doi/full/10.1145/3663547.3746386" style="color:grey ;" target="_blank">[Paper]</a></span>
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
              <el-col :span="8" class="pub-images">
                <el-image :src="srcCHI25EA" style="padding-top: 3%;padding-bottom: 5%;"></el-image>
              </el-col>
              <el-col :span="15" style="margin-left: 2%;">
                <p class="project-title">
                  Understanding Mixed Reality Drift Tolerance
                </p>
                <p class="project-conference">Proceedings of the Extended Abstracts of the CHI Conference on Human Factors in Computing Systems (CHI EA '25)
                  &nbsp;
                  <span style="color:grey ;"><a href="https://www.youtube.com/watch?v=Mn6fU_YFgyE" style="color:grey ;" target="_blank">[Video]</a></span> 
                  <span style="color:grey ;">&ensp;<a href="https://dl.acm.org/doi/10.1145/3706599.3720161" style="color:grey ;" target="_blank">[Paper]</a></span>
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
              <el-col :span="8" class="pub-images">
                <el-image :src="srcVisiMark" style="padding-top: 3%;padding-bottom: 5%;"></el-image>
              </el-col>
              <el-col :span="15" style="margin-left: 2%;">
                <p class="project-title">
                  VisiMark: Characterizing and Augmenting Landmarks for People with Low Vision in Augmented Reality to Support Indoor Navigation
                </p>
                <p class="project-conference">Proceedings of the 2025 CHI Conference on Human Factors in Computing Systems (CHI '25)
                  &nbsp;
                  <span style="color:grey ;"><a href="https://www.youtube.com/watch?v=LqkjHBSFaM0" style="color:grey ;" target="_blank">[Presentation]</a></span> 
                  <!-- &nbsp; -->
                  <span style="color:grey ;">&ensp;<a href="https://drive.google.com/file/d/1Nyx-t0yRIImjBIoKNLLwttbZ5fFA2Myd/view?usp=sharing" style="color:grey ;" target="_blank">[Demo]</a></span> 
                  <!-- &nbsp; -->
                  <span style="color:grey ;">&ensp;<a href="https://dl.acm.org/doi/full/10.1145/3706598.3713847" style="color:grey ;" target="_blank">[Paper]</a></span>
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
              <el-col :span="8" class="pub-images-small">
                <el-image :src="srcCHI25THU" style="padding-top: 3%;padding-bottom: 5%;"></el-image>
              </el-col>
              <el-col :span="15" style="margin-left: 2%;">
                <p class="project-title">
                  Modeling the Impact of Visual Stimuli on Redirection Noticeability with Gaze Behavior in Virtual Reality
                </p>
                <p class="project-conference">Proceedings of the 2025 CHI Conference on Human Factors in Computing Systems (CHI '25)
                  &nbsp;
                  <span style="color:grey ;"><a href="https://www.youtube.com/watch?v=ZfLArnKg7gE" style="color:grey ;" target="_blank">[Video]</a></span> 
                  <span style="color:grey ;">&ensp;<a href="https://dl.acm.org/doi/full/10.1145/3706598.3713392" style="color:grey ;" target="_blank">[Paper]</a></span>
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
              <el-col :span="8" class="pub-images">
                <el-image :src="srcCHI24" style="padding-top: 3%;padding-bottom: 5%;"></el-image>
              </el-col>
              <el-col :span="15" style="margin-left: 2%;">
                <p class="project-title">
                  Exploring the Design Space of Optical See-through AR Head-Mounted Displays to Support First Responders in the Field
                </p>
                <p class="project-conference">Proceedings of the 2024 CHI Conference on Human Factors in Computing Systems (CHI '24)
                  &nbsp;
                  <span style="color:grey ;"><a href="https://www.youtube.com/watch?v=ousbRtyklQI" style="color:grey ;" target="_blank">[Video]</a></span> 
                  <span style="color:grey ;">&ensp;<a href="https://dl.acm.org/doi/10.1145/3613904.3642195" style="color:grey ;" target="_blank">[Paper]</a></span>
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
              <el-col :span="8" class="pub-images-small">
                <el-image :src="srcIMWUT22" style="padding-top: 3%;padding-bottom: 5%;"></el-image>
              </el-col>
              <el-col :span="15" style="margin-left: 2%;">
                <p class="project-title">
                  Modeling the Noticeability of User-Avatar Movement Inconsistency for Sense of Body Ownership Intervention
                </p>
                <p class="project-conference">Proceedings of the ACM on Interactive, Mobile, Wearable and Ubiquitous Technologies (IMWUT '22)
                  &nbsp;
                  <span style="color:grey ;"><a href="https://drive.google.com/file/d/15q4QfytW2d1L4mXLL7pibFZL5xWQFNT-/view?usp=sharing" style="color:grey ;" target="_blank">[Video]</a></span> 
                  <span style="color:grey ;">&ensp;<a href="https://dl.acm.org/doi/10.1145/3534590" style="color:grey ;" target="_blank">[Paper]</a></span>
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
      };
    }
  };
  </script>
  