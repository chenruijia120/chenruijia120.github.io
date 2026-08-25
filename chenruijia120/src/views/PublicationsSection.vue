<template>
    <div>
            <h5 class="section">
              Publications
            </h5>
            <el-button-group style="margin-left: 3%; ">
            <!-- <el-button class="pub-button" size="medium" :type="pubFilter==='selected' ? 'primary' : 'default'" @click="pubFilter='selected'">Selected publications</el-button> -->
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


            <p style="margin-left: 4.5%;margin-top: 2%;margin-bottom: 0%;font-size: large;font-family:'Times New Roman', Times, serif;">
              * indicates equal contribution; † indicates the mentoring role</p>
            <br/>
            <el-card class="box-card" id="publications">


            

            <!-- <div v-show="pubFilter === 'selected' || pubFilter === 'all' || pubFilter === 'full' || pubFilter === 'a11y' || pubFilter === 'mr'">
              <el-row>
              <el-col v-if="isDesktop" :span="8" class="pub-images">
                <el-image :src="srcArxiv" style="padding-top: 3%;padding-bottom: 5%;" 
                alt="We investigated the performance and experiences of people with low vision using head-, gaze-, and finger-based selection techniques in both seated and walking scenarios. The image demonstrates how users employ these three techniques to select objects while seated in front of a shelf or while walking." class="zoomable-image" tabindex="0" @click.native="openImagePreview($event)" @keydown.enter.native="openImagePreview($event)" @keydown.space.native.prevent="openImagePreview($event)"></el-image>
              </el-col>
              <el-col :span="isDesktop ? 15 : 24" style="margin-left: 2%;">
                <p class="project-title">
                  Head, Gaze, or Finger? Comparing Object Selection Techniques in Augmented Reality for People with Low Vision
                  &nbsp; <span style="color:rgb(45, 45, 45) ;">&ensp;<a href="https://arxiv.org/abs/2607.06778" style="color:rgb(45, 45, 45) ;" target="_blank">[arXiv]</a></span>
                </p>
                <p class="project-conference">
                  <span style="color:rgb(45, 45, 45) ;"><a href="https://www.youtube.com/watch?v=M0kIoho02hM" style="color:rgb(45, 45, 45) ;" target="_blank">[Presentation]</a></span> 
                  <span style="color:rgb(45, 45, 45) ;">&ensp;<a href="https://arxiv.org/abs/2607.06778" style="color:rgb(45, 45, 45) ;" target="_blank">[arXiv]</a></span>
                </p>
                <p class="project-author">
                  <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen</span>, Tianyi Zhang, Sanbrita Mondal, Yukang Yan, Yuhang Zhao
                </p>
                <div style="margin-top:2% ;"></div>
              </el-col>
              </el-row>
            <el-divider></el-divider>
            </div> -->

            

            <div v-show="pubFilter === 'selected' || pubFilter === 'all' || pubFilter === 'full' || pubFilter === 'a11y' || pubFilter === 'mr'">
              <el-row>
              <el-col v-if="isDesktop" :span="8" class="pub-images">
                <!-- <div class="image-placeholder">Coming soon</div> -->
                <el-image :src="srcNaviNote" style="padding-top: 3%;padding-bottom: 5%;" 
                  alt="NaviNote teaser figure: A five-stage pipeline is shown with five panels. Each panel shows a user wearing a vest and speech bubbles representing communication between NaviNote and the user. In (1), the user asks, &quot;Where am I?&quot; The system responds, &quot;You're at the park entrance. There's a statue nearby...&quot; The user follows up, &quot;Please guide me to the statue!&quot; In (2), NaviNote provides navigation instructions: &quot;Walk straight for 15 meters...&quot; and &quot;...podium ahead at 10 o'clock.&quot; In (3), the user listens to a nearby spatial annotation: &quot;Be careful, there are 16 steps ahead.&quot; In (4), the user asks, &quot;What did others say about the statue?&quot; The system responds, &quot;One annotation notes that the statue is of Cicero, a famed orator, lawyer, and politician.&quot; In (5), the user creates a spatial annotation: &quot;There's a nice café with accessible restrooms here.&quot; During the interaction, the user wears a vest that holds a smartphone with its camera facing forward. The smartphone uses a Visual Positioning System (VPS) to determine the user's precise position within a pre-scanned area."
                 class="zoomable-image" tabindex="0" @click.native="openImagePreview($event)" @keydown.enter.native="openImagePreview($event)" @keydown.space.native.prevent="openImagePreview($event)"></el-image>
                </el-col>
              <el-col :span="isDesktop ? 15 : 24" style="margin-left: 2%;">
                <p class="project-title">
                  NaviNote: Enabling In-situ Spatial Annotation Authoring to Support Exploration and Navigation for Blind and Low Vision People
                </p>
                <p class="project-conference">🏆Honourable Mention Award, Proceedings of the 2026 CHI Conference on Human Factors in Computing Systems (CHI '26)
                  &nbsp;
                  <span style="color:rgb(45, 45, 45) ;"><a href="https://www.youtube.com/watch?v=M0kIoho02hM" style="color:rgb(45, 45, 45) ;" target="_blank">[Presentation]</a></span> 
                  <span style="color:rgb(45, 45, 45) ;">&ensp;<a href="https://dl.acm.org/doi/10.1145/3772318.3790589" style="color:rgb(45, 45, 45) ;" target="_blank">[Paper]</a></span>
                </p>
                <p class="project-author">
                  <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen</span>*, Yuheng Wu*, Charlie Houseago, Filipe Gaspar, Filippo Aleotti, Dorian Gálvez-López, Oliver Johnston, Diego Mazala, Guillermo Garcia-Hernando, Maryam Bandukda, Gabriel Brostow, Jessica Van Brummelen
                </p>
                <div style="margin-top:2% ;"></div>
              </el-col>
              </el-row>
            <el-divider></el-divider>
            </div>

            <div v-show="pubFilter === 'selected' || pubFilter === 'all' ||pubFilter === 'full' || pubFilter === 'a11y' || pubFilter === 'mr'">
              <el-row>
              <el-col v-if="isDesktop" :span="8" class="pub-images">
                <el-image :src="srcVisiMark" style="padding-top: 3%;padding-bottom: 5%;" alt="This image shows VisiMark system. VisiMark provides landmark augmentations on head-mounted AR to support wayfinding and mental map construction. VisiMark includes two features: (A) Signboard, an overview of hallway structures and upcoming landmarks at intersections, and (B) In-situ Labels, world-anchored icons and texts to highlight the types and positions of landmarks in the physical environment." class="zoomable-image" tabindex="0" @click.native="openImagePreview($event)" @keydown.enter.native="openImagePreview($event)" @keydown.space.native.prevent="openImagePreview($event)"></el-image>
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
                  <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen</span>, Junru Jiang, Pragati Maheshwary, Brianna R Cochran, Yuhang Zhao
                </p>
                <div style="margin-top:2% ;"></div>
              </el-col>
              </el-row>

            <!-- <div v-show="pubFilter !=='selected' && pubFilter !=='a11y'"> -->
            <el-divider></el-divider>
            <!-- </div> -->
            </div>

            
            <div v-show="pubFilter === 'selected' || pubFilter === 'all' || pubFilter === 'posters' || pubFilter === 'a11y' || pubFilter === 'mr'">
              <el-row>
              <el-col v-if="isDesktop" :span="8" class="pub-images">
                <!-- <div class="image-placeholder">Coming soon</div> -->
                <el-image :src="srcVisiAgentDemo" style="padding-top: 3%;padding-bottom: 5%;" 
                  alt="Demonstration of VisiAgent. VisiAgent supports people with low vision (PLV) in grounding visual references and receiving synchronized multimodal feedback during daily tasks. We illustrate VisiRef across several challenging daily tasks for PLV. (A) VisiAgent shows a cursor that indicates the user's attention and applies semi-transparent color overlays to objects swept by the user's pointing as candidate visual references. (B) When the user asks to compare similar objects, VisiAgent provides distinguishing information (i.e., different flavors) and highlights relevant parts of each object in sync with the audio narration. (C) When the user is completing an aiming task, VisiAgent outlines the source target (i.e., bottle opening) and destination target (i.e., mug rim), and renders a trajectory to guide alignment. (D) If the user is searching for a target, VisiAgent outlines the target and provides an arrow cue to guide the user's attention. When VisiAgent describes the target, it outlines relevant details according to the audio narration. (E) VisiAgent provides timely intervention when needed. For example, when the user's hand approaches a nearby hazard (e.g., scissors), VisiAgent highlights the danger with a flashing outline and provides a spatial audio warning."
                 class="zoomable-image" tabindex="0" @click.native="openImagePreview($event)" @keydown.enter.native="openImagePreview($event)" @keydown.space.native.prevent="openImagePreview($event)"></el-image>
                </el-col>
              <el-col :span="isDesktop ? 15 : 24" style="margin-left: 2%;">
                <p class="project-title">
                  Demonstration of VisiAgent: A Mixed Reality Agent with Visual Reference and Guidance for People with Low Vision
                </p>
                <p class="project-conference">Adjunct Proceedings of the 39th Annual ACM Symposium on User Interface Software and Technology (UIST '26 Adjunct)
                  <!-- &nbsp;
                  <span style="color:rgb(45, 45, 45) ;"><a href="https://www.youtube.com/watch?v=M0kIoho02hM" style="color:rgb(45, 45, 45) ;" target="_blank">[Presentation]</a></span> 
                  <span style="color:rgb(45, 45, 45) ;">&ensp;<a href="https://dl.acm.org/doi/10.1145/3772318.3790589" style="color:rgb(45, 45, 45) ;" target="_blank">[Paper]</a></span> -->
                </p>
                <p class="project-author">
                  <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen</span>, Yuhang Zhao
                </p>
                <div style="margin-top:2% ;"></div>
              </el-col>
              </el-row>
            <el-divider></el-divider>
            </div>

            
            <div v-show="pubFilter === 'selected' || pubFilter === 'all' || pubFilter === 'posters' || pubFilter === 'a11y' || pubFilter === 'mr'">
              <el-row>
              <el-col v-if="isDesktop" :span="8" class="pub-images">
                <!-- <div class="image-placeholder">Coming soon</div> -->
                <el-image :src="srcScoreSightDemo" style="padding-top: 3%;padding-bottom: 5%;" 
                  alt="Interface and key features of ScoreSight, shown in three parts. A dash-dotted line indicates the natural preview behavior across the line transition. (a) Real-Time Following continuously tracks the musician’s live performance with a dynamic magnifier lens centered on the current playing position. As the magnifier approaches the end of a staff line, a preview magnifier appears at the beginning of the next line. (b) Visual Guidance shows a simplified guidance score that preserves staff lines, clefs, and barlines while removing detailed musical notation. A guidance line connects consecutive note positions, with breaks at rests and staff boundaries, and event markers highlight large leaps and chords. (c) Customization shows interface controls that allow low-vision musicians to adjust magnification, interface colors, and the guidance line color based on their visual needs and reading preferences."
                 class="zoomable-image" tabindex="0" @click.native="openImagePreview($event)" @keydown.enter.native="openImagePreview($event)" @keydown.space.native.prevent="openImagePreview($event)"></el-image>
                </el-col>
              <el-col :span="isDesktop ? 15 : 24" style="margin-left: 2%;">
                <p class="project-title">
                  Demonstration of ScoreSight: Real-time Piano Music Reading Support for People with Decreased Central Vision
                </p>
                <p class="project-conference">Adjunct Proceedings of the 39th Annual ACM Symposium on User Interface Software and Technology (UIST '26 Adjunct)
                  <!-- &nbsp;
                  <span style="color:rgb(45, 45, 45) ;"><a href="https://www.youtube.com/watch?v=M0kIoho02hM" style="color:rgb(45, 45, 45) ;" target="_blank">[Presentation]</a></span> 
                  <span style="color:rgb(45, 45, 45) ;">&ensp;<a href="https://dl.acm.org/doi/10.1145/3772318.3790589" style="color:rgb(45, 45, 45) ;" target="_blank">[Paper]</a></span> -->
                </p>
                <p class="project-author">
                  Tianyi Zhang, Yihan Wu, Varun Ganesh, <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen</span>†, Yuhang Zhao
                </p>
                <div style="margin-top:2% ;"></div>
              </el-col>
              </el-row>
            <el-divider></el-divider>
            </div>

            

            <div v-show="pubFilter === 'selected' || pubFilter === 'all' || pubFilter === 'full' || pubFilter === 'a11y' || pubFilter === 'mr'">
              <el-row>
              <el-col v-if="isDesktop" :span="8" class="pub-images">
                <!-- <div class="image-placeholder">Coming soon</div> -->
                <el-image :src="srcASSETS26" style="padding-top: 3%;padding-bottom: 5%;"  alt="SceneGlance augmenting two cluttered scenes for low-vision users, shown side by side. Left, labeled OUTDOOR: a busy street where cyclists, bicycles, cars, pedestrians, and traffic and pedestrian signals are outlined in green to mark higher importance, while the sidewalk and other objects are outlined in blue. Right, labeled INDOOR: a kitchen counter where knives, cups, and a bottle carry yellow solid overlays for higher importance, while utensils, bowls, and other items are outlined in blue." class="zoomable-image" tabindex="0" @click.native="openImagePreview($event)" @keydown.enter.native="openImagePreview($event)" @keydown.space.native.prevent="openImagePreview($event)"></el-image>
              </el-col>
              <el-col :span="isDesktop ? 15 : 24" style="margin-left: 2%;">
                <p class="project-title">
                  What to Distinguish and How? Opportunities and Challenges of Augmenting Multiple, Cluttered Objects in Complex Scenes for People with Low Vision
                </p>
                <p class="project-conference">To appear at ASSETS '26
                  &nbsp;
                  <!-- <span style="color:rgb(45, 45, 45) ;"><a href="https://www.youtube.com/watch?v=M0kIoho02hM" style="color:rgb(45, 45, 45) ;" target="_blank">[Presentation]</a></span>  -->
                  <span style="color:rgb(45, 45, 45) ;">&ensp;<a href="https://arxiv.org/abs/2607.10902" style="color:rgb(45, 45, 45) ;" target="_blank">[Paper]</a></span>
                </p>
                <p class="project-author">
                  Yuheng Wu, <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen</span>, Jaewook Lee, Jia Li, Kexin Zhang, Meng Fong Lio, and Weibing Wang, Sanbrita Mondal, Jon E. Froehlich, Yapeng Tian, Yuhang Zhao
                </p>
                <div style="margin-top:2% ;"></div>
              </el-col>
              </el-row>
            <el-divider></el-divider>
            </div>
            
            <div v-show="pubFilter === 'all' || pubFilter === 'full' || pubFilter === 'a11y'">
              <el-row>
              <el-col v-if="isDesktop" :span="8" class="pub-images">
                <!-- <div class="image-placeholder">Coming soon</div> -->
                <el-image :src="srcASE26" style="padding-top: 3%;padding-bottom: 5%;" alt="An example of how code may appear to programmers with and without dyslexia." class="zoomable-image" tabindex="0" @click.native="openImagePreview($event)" @keydown.enter.native="openImagePreview($event)" @keydown.space.native.prevent="openImagePreview($event)"></el-image>
              </el-col>
              <el-col :span="isDesktop ? 15 : 24" style="margin-left: 2%;">
                <p class="project-title">
                  Toward Inclusive Programming Support for Novice Programmers with Dyslexia: Insights from a Comparative Study
                </p>
                <p class="project-conference">To appear at ASE '26
                  &nbsp;
                  <!-- <span style="color:rgb(45, 45, 45) ;"><a href="https://www.youtube.com/watch?v=M0kIoho02hM" style="color:rgb(45, 45, 45) ;" target="_blank">[Presentation]</a></span>  -->
                  <!-- <span style="color:rgb(45, 45, 45) ;">&ensp;<a href="https://arxiv.org/abs/2607.10902" style="color:rgb(45, 45, 45) ;" target="_blank">[Paper]</a></span> -->
                </p>
                <p class="project-author">
                  Zihan Fang, Janice Chung, <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen</span>, Marcia Barnes, Yuhang Zhao, Yu Huang
                </p>
                <div style="margin-top:2% ;"></div>
              </el-col>
              </el-row>
            <el-divider></el-divider>
            </div>

            
            
            
            <div v-show="pubFilter === 'selected' || pubFilter === 'all' ||pubFilter === 'full' || pubFilter === 'a11y' || pubFilter === 'gaze'">
              <el-row>
              <el-col v-if="isDesktop" :span="8" class="pub-images">
                <el-image :src="srcASSETS25Ru" style="padding-top: 3%;padding-bottom: 5%;" alt="This figure shows a five-panel visual illustration showcasing five types of visual intent during image-viewing: Searching, Observing, Traversing, Comparing, and Exploring. Each panel contains an an illustration of the same example image (four people having a picnic on the foreground of the image) with mock gaze trajectories overlaid as colored lines and dots representing saccades and fixations. The 'Searching' panel shows sparse gaze scanpaths moving towards the person on the left. 'Observing' shows fixations clustered on the person on the left. 'Traversing' displays scanpaths across multiple people one by one from left to right. 'Comparing' includes back-and-forth gaze movements between the two people on the right. 'Exploring' shows broader, scattered gaze paths covering the entire image. The gaze paths are illustrative and not drawn from real data." class="zoomable-image" tabindex="0" @click.native="openImagePreview($event)" @keydown.enter.native="openImagePreview($event)" @keydown.space.native.prevent="openImagePreview($event)"></el-image>
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
                  Ru Wang, <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen</span>, Anqiao Erica Cai, Zhiyuan Li, Sanbrita Mondal, Yuhang Zhao
                </p>
                <div style="margin-top:2% ;"></div>
              </el-col>
              </el-row>

            <el-divider></el-divider></div>


            <div v-show="pubFilter === 'all' ||pubFilter === 'full' || pubFilter === 'a11y'">
              <el-row>
              <el-col v-if="isDesktop" :span="8" class="pub-images">
                <el-image :src="srcASSETS25Hazel" style="padding-top: 3%;padding-bottom: 5%;" alt="FocusView teaser figure: Illustration of a distracted learner watching an educational video with visual and audio distractions like music and pop-ups in thought bubbles. The center shows a customizable video interface with controls for audio (denoise & enhance), background (blur/remove), layout options (original, auxiliary removal, speaker focus, content focus), and captions (color, font, size, position, highlight). A processed video on the right displays improved clarity with speaker focus and enhanced captions. Icons below indicate clear speech is kept while music is removed." class="zoomable-image" tabindex="0" @click.native="openImagePreview($event)" @keydown.enter.native="openImagePreview($event)" @keydown.space.native.prevent="openImagePreview($event)"></el-image>
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
                  Hanxiu 'Hazel' Zhu, <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen</span>, Yuhang Zhao
                </p>
                <div style="margin-top:2% ;"></div>
              </el-col>
              </el-row>

            <el-divider></el-divider></div>

            <div v-show="pubFilter === 'all' ||pubFilter === 'posters' || pubFilter === 'perception' || pubFilter === 'mr'">
              <el-row>
              <el-col v-if="isDesktop" :span="8" class="pub-images">
                <el-image :src="srcCHI25EA" style="padding-top: 3%;padding-bottom: 5%;" alt="This image shows an overview of task interpretations, illustrating: (A) Two primary writing behaviors when responding to drift: following drifted location absolutely versus estimating the un-drifted position; (B) Path deviations from center while following virtual drifted line (red) versus actual invisible line (white); (C) Participant's writing paper with original paper overlaid, showing appropriate blanks (blue boxes) and corresponding written words." class="zoomable-image" tabindex="0" @click.native="openImagePreview($event)" @keydown.enter.native="openImagePreview($event)" @keydown.space.native.prevent="openImagePreview($event)"></el-image>
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
                  Daniel Killough*, <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen</span>*, Yuhang Zhao, Bilge Mutlu
                </p>
                <div style="margin-top:2% ;"></div>
              </el-col>
              </el-row>
            <div v-show="pubFilter !=='posters'">
            <el-divider></el-divider>
            </div>
            </div>

            

            <div v-show="pubFilter === 'all' ||pubFilter === 'full' || pubFilter === 'perception' || pubFilter === 'mr' || pubFilter === 'gaze'">
              <el-row>
              <el-col v-if="isDesktop" :span="8" class="pub-images-small">
                <el-image :src="srcCHI25THU" style="padding-top: 3%;padding-bottom: 5%;" 
                alt="The image shows the apparatus of the paper's formative study. Wearing a headset, the participant wears three motion trackers to tracktheir arm pose and sit on a comfortable chair. While the virtual avatar mirrors the arm movement of the participant, the participant observes the virtual avatar's movement froma first-person point of view and follows the semi-transparent checkpoint pose to reach the semi-transparent target pose. As the secondary task, a virtual animation will start with diferent durations and locations. The right fgure illustrates the possible locations of the red ball, named Sparse, Median, and Dense, accordingly." class="zoomable-image" tabindex="0" @click.native="openImagePreview($event)" @keydown.enter.native="openImagePreview($event)" @keydown.space.native.prevent="openImagePreview($event)"></el-image>
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
                  Zhipeng Li, Yishu Ji, <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen</span>, Tianqi Liu, Yuntao Wang, Yuanchun Shi, Yukang Yan
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
                <el-image :src="srcCHI24" style="padding-top: 3%;padding-bottom: 5%;" alt="The image presents different AR cues, such as overview cues, including (1) head-attached map, and (2) 3D Floor plan. Highlighting cues includes (1) door with shade and door with Contour. Directional cues include (1) single arrow pointing a POI, and (2) an array of arrows indicating a path. Labeling cues include (1) icon and text labeling an object, and (2) icons labeling a victim." class="zoomable-image" tabindex="0" @click.native="openImagePreview($event)" @keydown.enter.native="openImagePreview($event)" @keydown.space.native.prevent="openImagePreview($event)"></el-image>
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
                  Kexin Zhang, Brianna R Cochran, <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen</span>, Lance Hartung, Bryce Sprecher, Ross Tredinnick, Kevin Ponto, Suman Banerjee, Yuhang Zhao
                </p>
                <div style="margin-top:2% ;"></div>
              </el-col>
              </el-row>

            <el-divider></el-divider></div>


            <div v-show="pubFilter === 'all' ||pubFilter === 'full' || pubFilter === 'perception' || pubFilter === 'mr'">
              <el-row>
              <el-col v-if="isDesktop" :span="8" class="pub-images-small">
                <el-image :src="srcIMWUT22" style="padding-top: 3%;padding-bottom: 5%;" alt="We investigate the effect of user-avatar movement inconsistency on body ownership. The image shows a person wearing a head-mounted VR headset, where the user's actual arm position is different from the virtual avatar." class="zoomable-image" tabindex="0" @click.native="openImagePreview($event)" @keydown.enter.native="openImagePreview($event)" @keydown.space.native.prevent="openImagePreview($event)"></el-image>
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
                  Zhipeng Li, Yu Jiang, Yihao Zhu, <span style="font-weight:bolder; text-decoration: underline;">Ruijia Chen</span>, Ruolin Wang, Yuntao Wang, Yukang Yan, Yuanchun Shi
                </p>
                <div style="margin-top:2% ;"></div>
              </el-col>
              </el-row></div>
            </el-card>

            <el-dialog
              :visible.sync="imagePreviewVisible"
              width="80%"
              top="5vh"
              append-to-body
              custom-class="image-preview-dialog"
              ref="imagePreviewDialog"
              @opened="resetImagePreviewScroll"
            >
              <img
                :src="previewImageSrc"
                :alt="previewImageAlt"
                class="preview-image"
              />
              <p class="preview-alt-text">
                {{ previewImageAlt }}
              </p>
            </el-dialog>
    </div>
  </template>
  
  <script>
  export default {
    name: 'PublicationsSection',
    data() {
      return {
        pubFilter: 'all',
        imagePreviewVisible: false,
        previewImageSrc: '',
        previewImageAlt: '',
        srcIMWUT22:require('@/assets/IMWUT2022.png'),
        srcCHI24:require('@/assets/CHI2024.jpg'),
        srcVisiMark:require('@/assets/VisiMark.jpg'),
        srcNaviNote:require('@/assets/NaviNote.jpg'),
        srcCHI25EA:require('@/assets/MRDrift.jpg'),
        srcCHI25THU:require('@/assets/srcCHI25THU.jpg'),
        srcASSETS25Ru:require('@/assets/ASSETS25Ru.png'),
        srcASSETS25Hazel:require('@/assets/ASSETS26Hazel.jpg'),
        srcASSETS26:require('@/assets/ASSETS26.png'),
        srcASE26:require('@/assets/ASE26.png'),
        srcArxiv:require('@/assets/arxiv2026.png'),
        srcVisiAgentDemo:require('@/assets/VisiAgentDemo.png'),
        srcScoreSightDemo:require('@/assets/ScoreSightDemo.png'),
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
    methods: {
      openImagePreview(event) {
        const image = event.currentTarget.querySelector('img');
        if (!image) return;

        this.previewImageSrc = image.currentSrc || image.src;
        this.previewImageAlt = image.alt || '';
        this.imagePreviewVisible = true;
      },
      resetImagePreviewScroll() {
        this.$nextTick(() => {
          const dialog = this.$refs.imagePreviewDialog;
          if (dialog && dialog.$el) {
            dialog.$el.scrollTop = 0;
          }
        });
      }
    },
    
    computed: {
      isDesktop() {
        return this.windowWidth >= 1050;
      }
  }
  };
  </script>
  

<style>
.zoomable-image {
  cursor: zoom-in;
}

.zoomable-image:focus {
  outline: 2px solid #409eff;
  outline-offset: 4px;
}

.preview-image {
  display: block;
  width: 100%;
  max-height: 62vh;
  object-fit: contain;
  margin: 0 auto;
}

.preview-alt-text {
  margin: 20px 0 0;
  font-size: 16px;
  line-height: 1.6;
  color: #333;
  text-align: left;
  white-space: pre-line;
}

.image-preview-dialog {
  margin-bottom: 1vh;
}

.image-preview-dialog .el-dialog__body {
  padding: 10px 20px 20px;
}
</style>
