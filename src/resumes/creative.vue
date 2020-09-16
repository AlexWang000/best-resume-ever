<template>
  <div class="resume" id="resume2">
    <div class="left-column">
      <div class="big-headline">
        <span class="uppercase"> {{ person.name.first }} {{ person.name.middle }} </span>
        <span class="uppercase"> {{ person.name.last }} </span>
      </div>

      <div class="block-marged txt-full-white">
        3A Computer Science Student
      </div>
      <div class="block-marged txt-full-white">
        All degree required CS courses will be completed by 2021
      </div>
      <div class="skills-section section">
        <div class="borderline-light">
          <div class="icon skill-headline">
            <span> CONTACT </span>
          </div>
        </div>

        <div class="section-content" style="text-align: left;">
          <a :href="contactLinks.email">
            <div class="block-marged txt-full-white">
              <i class="fa fa-envelope fa-fw" style="position: relative"></i>
              {{ person.contact.email }}
            </div>
          </a>
          <div class="block-marged txt-full-white">
              <i class="fa fa-phone fa-fw"></i>

            {{ person.contact.phone }}
          </div>
          <!-- <a v-if="person.contact.website" :href="'http://' + person.contact.website">
            <div class="block-marged txt-full-white">
              {{ person.contact.website }}
            </div>
          </a> -->
          <a v-if="person.contact.github" :href="contactLinks.github" class="external-link">
            <div class="block-marged txt-full-white">
              <i class="fa fa-github fa-fw"></i>
              {{ 'github.com/' + person.contact.github }}
            </div>
          </a>
          <a v-if="person.contact.website" :href="'https://'+person.contact.website" class="external-link">
            <div class="block-marged txt-full-white">
              <i class="fa fa-globe fa-fw"></i>
              {{ person.contact.website }}
            </div>
          </a>
        </div>
      </div>
<!-- 
      <div class="multi-line-txt">
        {{ person.about }}
      </div>

      <div class="multi-line-txt">
        {{ person.knowledge }}
      </div> -->

      <!-- <div class="social-container">
        <a :href="contactLinks.email">
          <div class="block-marged txt-full-white">
            <i class="fa fa-envelope fa-fw contact-icon"></i>
            <img src=../assets/email-24px.svg>
            {{ person.contact.email }}
          </div>
        </a>

        <div class="block-marged txt-full-white">
          <i class="fa fa-phone fa-fw contact-icon"></i>
          {{ person.contact.phone }}
        </div>

        <a v-if="person.contact.website"
          :href="'http://' + person.contact.website">

          <div class="block-marged txt-full-white">
            <i class="fa fa-globe fa-fw contact-icon"></i>
            {{ person.contact.website }}
          </div>
        </a>

        <a v-if="person.contact.github"
          :href="contactLinks.github"
          class="external-link">

          <i class="fa fa-github fa-fw contact-icon"></i>
          <span class="block-marged txt-full-white">
            {{ person.contact.github }}
          </span>
        </a>

        <a v-if="person.contact.codefights"
          :href="contactLinks.codefights"
          class="external-link">

          <svg width="20" height="20" viewBox="0 0 24 24"
            class="contact-icon-svg">
            <path d="M12 15.2L9.2 4.8 0 3.2l1.7 2.6 5.7.7.7 2.3-3.7-.4 1.3 2 3 .3L12 20.8l3.3-10.1 3-.3 1.3-2-3.7.4.7-2.3 5.7-.7L24 3.2l-9.2 1.6">
            </path>
          </svg>

          <span class="block-marged txt-full-white">
            {{ person.contact.codefights }}
          </span>
        </a>

        <a v-if="person.contact.medium"
          :href="contactLinks.medium"
          class="external-link">
          <i class="fab fa-medium contact-icon"></i>
          <span class="block-marged txt-full-white">
            {{ person.contact.medium }}
          </span>
        </a>
      </div> -->

      <div class="skills-section section">
         <div class="borderline-light">
          <div class="skill-headline">
            <!-- <i class="fa fa-code skill-icon"></i> -->
            <span> SKILLS </span>
          </div>
        </div>

        <div v-if="person.languages" class="skills-section section">
          <div>
            <div class="icon skill-headline">
              <!-- <i class="fa fa-code skill-icon"></i> -->
              <span> LANGUAGES </span>
            </div>
          </div>

          <div class="grid-display">
            <div v-for="(language, index) in person.languages" :key="index">
              <span> {{ language.name}} </span>
              <!-- <div v-if="index2 < person.languages.length-1" style="border-left:1px solid grey;height: 12px;margin-left: 10px; padding-right:10px;"></div> -->
            </div>
          </div>
        </div>

        <div class="skills-section section">
          <div>
            <div class="icon skill-headline">
              <!-- <i class="fa fa-terminal skill-icon"></i> -->
              <span> Data Science </span>
            </div>
          </div>

          <div class="grid-display">
            <div v-for="(framework, index) in person.ml" :key="index">
              <span> {{ framework.name}} </span>
            </div>
          </div>
        </div>


        <div class="skills-section section">
          <div>
            <div class="icon skill-headline">
              <!-- <i class="fa fa-terminal skill-icon"></i> -->
              <span> frontend </span>
            </div>
          </div>

          <div class="grid-display">
            <div v-for="(framework, index) in person.frontend" :key="index">
              <span> {{ framework.name}} </span>
            </div>
          </div>
        </div>


        <div class="skills-section section">
          <div>
            <div class="icon skill-headline">
              <!-- <i class="fa fa-terminal skill-icon"></i> -->
              <span> backend </span>
            </div>
          </div>

          <div class="grid-display">
            <div v-for="(framework, index) in person.backend" :key="index">
              <span> {{ framework.name}} </span>
            </div>
          </div>
        </div>

        <div class="skills-section section">
          <div>
            <div class="icon skill-headline">
              <!-- <i class="fa fa-terminal skill-icon"></i> -->
              <span> database </span>
            </div>
          </div>

          <div class="grid-display">
            <div v-for="(framework, index) in person.database" :key="index">
              <span> {{ framework.name}} </span>
            </div>
          </div>
        </div>


        <div class="skills-section section">
          <div>
            <div class="icon skill-headline">
              <!-- <i class="fa fa-terminal skill-icon"></i> -->
              <span> Mobile </span>
            </div>
          </div>

          <div class="grid-display">
            <div v-for="(framework, index) in person.mobile" :key="index">
              <span> {{ framework.name}} </span>
            </div>
          </div>
        </div>
      </div>

      



      <div class="skills-section section">
        <div class="borderline-light">
          <div class="icon skill-headline">
            <!-- <i class="material-icons skill-icon">school</i> -->
            <span>{{ lang.education }}</span>
          </div>
        </div>

        <div class="section-content">
          <div v-for="(education, index) in person.education" :key="index" class="section-content__item">

            <span class="section-content__subheader school">{{ education.degree }}</span>
            <span class="section-content__header school"> {{ education.school }} </span>
            <span class="section-content__subheader"> {{ education.timeperiod }} </span>
            <div class="section-content__subheader" style="display:flex; flex-direction:row; justify-content: space-between">
              <span class="section-content__subheader"> Cumulative Average</span>
              <span class="section-content__subheader"> 94.35% </span>
            </div>
            <!-- <span class="section-content__text--light school"> {{ education.description }} </span> -->
          </div>
        </div>
      </div>

      <div v-if="person.academic" class="skills-section section">
        <div>
          <div class="icon skill-headline">
            <!-- <i class="material-icons skill-icon">done_all</i> -->
            <span> Relevant Courses </span>
          </div>
        </div>

        <div style="display: flex; flex-direction:column;">
          <div  v-for="(academic, index) in person.academic" :key="index" style="display: flex; flex-direction: row; justify-content: space-between">
            <span>
              {{ academic.highlight[0].description }}
            </span>
            <span>
              {{ academic.highlight[1].value}}
            </span>
          </div>
          <!-- <a v-for="(academic, index) in person.academic" :key="index"
            class="grid-item">
            <span class="squarred-grid-item"> {{ academic.highlight }} </span>
          </a> -->
        </div>
      </div>




      <!-- <div v-if="person.skills"
        class="skills-section section">
        <div class="icon">
          <i class="material-icons skill-icon">done_all</i>
          <span class="skill-headline"> {{ lang.skills }} </span>
        </div>

        <div class="section-content-grid">
          <a v-for="(skill, index) in person.skills" :key="index"
            class="grid-item"
            :href="skill.url">

            <i v-if="skill.iconClass" :class="'lang-icon ' + skill.iconClass"></i>

            <span v-else class="squarred-grid-item"> {{ skill.name }} </span>
          </a>
        </div>
      </div> -->

      <!-- <div class="hobbies-container">
        <div class="hobbies-content">
          <a v-for="(hobby, index) in person.hobbies" :key="index"
            class="hobby-item"
            :href="hobby.url">

            <i v-if="hobby.iconClass" :class="hobby.iconClass + ' hobby-item__icon'"></i>
            <span class="hobby-item__icon-label"> {{ hobby.name }} </span>
          </a>
        </div>
      </div> -->
    </div>

    <div class="left-column-bg"></div>

    <div class="right-column">
      <!-- <div class="experience-section section">
        <div class="borderline">
            <div class="section-headline">
              <span> SUMMARY OF QUALIFICATIONS </span>
            </div>
        </div>

        <div v-if="person.languages" class="skills-section section">
          <div class="borderline-light">
            <div class="icon skill-headline">
              <span> LANGUAGES </span>
            </div>
          </div>

          <div>
            <a v-for="(language, index) in person.languages" :key="index">
              <span> {{ language.name + " | "}} </span>
            </a>
          </div>
        </div>
        <div v-if="person.languages" class="skills-section section">
          <div class="borderline-light">
            <div class="icon skill-headline">
              <span> LANGUAGES </span>
            </div>
          </div>

          <div>
            <a v-for="(language, index) in person.languages" :key="index">
              <span> {{ language.name + " | "}} </span>
            </a>
          </div>
        </div>
      </div> -->

      <div class="experience-section section" style="margin-bottom: 0px;">
        <div class="icon borderline">
          <!-- <i class="material-icons small-icon">work</i> -->
          <span class="section-headline">work experience</span>
        </div>

        

        <!-- You need to hardcode it to add highlight -->
        <div class="section-content">
           <div class="section-content__item">
            <span class="section-content__header pos">Full-Stack Software Engineer</span>
            <div class="sub">
              <span class="section-content__subheader division"> Raise Your Edge </span>
              <!-- <div class="section-content__text division division-after"> Angular </div>
              <div class="section-content__text division division-after"> Firebase </div> -->
              <div class="section-content__text division-after"> Sep 2019 - Dec 2019 </div>
            </div>
            <ul class="list">


              <!-- <li class="section-content__text--light experience-item list-item sub-description">
                Participated in the <span class="highlight">design</span>, <span class="highlight">implementation</span>, and <span class="highlight">iteration</span> phases of the software development cycle to create an <span class="highlight">interactive video quiz project</span>
                with theater mode and customer-facing frontend tools to support user generated content using <span class="highlight">Angular and Firebase Realtime Database</span>
              </li> -->
              <!-- <li class="section-content__text--light experience-item list-item sub-description">
                Participated in the <span class="highlight">design</span>, <span class="highlight">implementation</span>, and <span class="highlight">iteration</span> phases of the software development cycle to create customer-facing frontend tools to support user generated content using <span class="highlight">Angular</span> and <span class="highlight">Firebase Realtime Database</span>
              </li> -->
              <li class="section-content__text--light experience-item list-item sub-description">
                Worked closely with lead developers to design and implement an online tutoring software using <span class="highlight">Angular</span> and <span class="highlight">Firebase</span>
              </li>
              <li class="section-content__text--light experience-item list-item sub-description">
                Implemented and iterated <span class="highlight"> core algorithms </span> to create automated quiz questions based on user generated data
              </li>
              <li class="section-content__text--light experience-item list-item sub-description">
                Architected and implemented a <span class="highlight"> highly interactive video player </span> to deliver quiz content leveraging Angular and third party video player frameworks
                <!-- Researched and integrated thrid party softwares to create an enhanced video player that delivers quiz content -->
              </li>
              <li class="section-content__text--light experience-item list-item sub-description">
                Developed <span class="highlight"> data caching </span> feature and <span class="highlight"> optimized backend function complexity </span> to significantly improve website response time
              </li>
              <!-- <li class="section-content__text--light experience-item list-item sub-description">
                <span class="highlight">Implemented and iterated algorithms</span> that generates automated quiz questions from dynamic user data and corresponding user-interfaces with the instruction from the lead designer
              </li> -->
              <!-- <li class="section-content__text--light experience-item list-item sub-description">
                Developed quiz caching feature and <span class="highlight">reduced complexity</span> of <span class="highlight">backend Firebase Cloud Functions</span> to greatly increase efficiency and improve user experience
              </li>
              <li class="section-content__text--light experience-item list-item sub-description">
                <span class="highlight">Researched and integrated third party software</span> such as video.js, mediaelement.js and <span class="highlight">Firebase Cloud Storage</span> to create customer-facing UI components and robust backend functions
              </li>
              <li class="section-content__text--light experience-item list-item sub-description">
                <span class="highlight">Took ownership of assigned projects</span> and proactively identified bugs and UI flaws. Reported and fixed them without interrupting the normal workflow
              </li> -->
            </ul>
          </div>

          <div class="section-content__item">
            <span class="section-content__header pos">Full-Stack Software Engineer</span>
            <div class="sub">
              <span class="section-content__subheader division"> Raise Your Edge </span>
              <!-- <div class="section-content__text division division-after"> Angular </div>
              <div class="section-content__text division division-after"> Firebase </div> -->
              <div class="section-content__text division-after"> Apr 2020 - Jun 2020 </div>
            </div>
            <ul class="list">
              <!-- the problem with this part of text is that it's way too weak -->
              <li class="section-content__text--light experience-item list-item sub-description">
                Interfaced with lead designers on a daily basis and <span class="highlight">implemented weekly updates </span> to the web application; took responsibility of assigned projects and fix emergency bugs immediately
              </li>
              <!-- the wording still has to be changed a bit -->
              <li class="section-content__text--light experience-item list-item sub-description">
                <!-- Improved author productivity by developing a variety utility tools  -->
                Pitched and completed a project providing a variety of utility tools for authors allowing them to build upon existing quizzes and schedule post release dates which significantly <span class="highlight">improves their productivity</span>
                <!-- Developed the release scheduling tool for authors to improve productivity using <span class="highlight">Google Cloud Scheduler</span> -->
              </li>
              <!-- <li class="section-content__text--light experience-item list-item sub-description">
                Minimized API calls and improved website response time by migrating Firebase Functions to Firebase Triggers
                Migrated a portion of <span class="highlight"> Firebase Functions </span> to <span class="highlight"> Firebase Triggers </span> to minimize API calls based on experiments
              </li> -->
              <li class="section-content__text--light experience-item list-item sub-description">
                Engineered and maintained a <span class="highlight">playlist project</span> which let users schedule a collection of quizzes to take and have their performance tracked in real time
              </li>
              <!-- <li class="section-content__text--light experience-item list-item sub-description">
                Improved author productivity by developing a variety utility tools  -->
                <!-- Developed the release scheduling tool for authors to improve productivity using <span class="highlight">Google Cloud Scheduler</span> -->
              <!-- </li> -->
              <!-- <li class="section-content__text--light experience-item list-item sub-description">
                Interfaced devops on a daily basis and took responsibility to fix emergency bugs
              </li> -->
            </ul>
          </div>

        </div>
      </div>

      <!-- Better hard code for more customization -->

      <div v-if="person.projects" class="projects-section section" style="margin-top: 0px;">
        <div class="icon borderline">
          <!-- <i class="material-icons">code</i> -->
          <span class="section-headline"> {{ lang.projects }} </span>
        </div>

        <div class="section-content">
          <div v-for="(project, index) in person.projects" :key="index" class="section-content__item">
            <div style="display: flex; flex-direction: row; justify-content: space-between">
              <span class="section-content__header project-name"> {{ project.name }} </span>
              <a class="section-content__text--light" :href="'https://' + project.url">
              <!-- <i class="fa fa-github"></i> -->
                {{ project.url }}
              </a>
            </div>
            <div class="sub">
              <div class="sub" v-for="(platform, index2) in project.platform" :key="index2">
                <span class="section-content__subheader" style="color: rgb(226, 102, 57);">
                  {{ platform }}
                </span>
                <div v-if="index2 < project.platform.length-1" style="border-left:1px solid grey;height: 12px;margin-left: 10px; padding-right:10px;"></div>
              </div>
            </div>
            <ul class="list">
              <li v-for="(description, index) in project.description" :key="index" class="section-content__text--light experience-item list-item sub-description">
                {{ description }}
              </li>
            </ul>
          </div>
        </div>
      </div>

      <!-- <div v-if="person.skills"
        class="skills-section section">
        <div class="icon">
          <i class="material-icons">done_all</i>
          <span class="section-headline"> {{ lang.skills }} </span>
        </div>

        <div class="section-content-grid">
          <a v-for="(skill, index) in person.skills" :key="index"
            class="grid-item"
            :href="skill.url">

            <i v-if="skill.iconClass" :class="'lang-icon ' + skill.iconClass"></i>

            <span v-else class="squarred-grid-item"> {{ skill.name }} </span>
          </a>
        </div>
      </div> -->

      <div v-if="person.contributions"
        class="contributions-section section">

        <div class="icon">
          <i class="fa fa-heart font-awesome-icons"></i>
          <span class="section-headline"> {{lang.contributions}} </span>
        </div>

        <div class="section-content-grid">
          <a v-for="(contribution, index) in person.contributions" :key="index"
            :href="contribution.url"
            class="section-content__item-grid">

            <span class="section-content__header"> {{ contribution.name }} </span>
            <span class="section-content__text"> {{ contribution.description }} </span>
            <span class="section-content__text--light" style="word-break: break-all;">
              {{ contribution.url }}
            </span>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Vue from 'vue';
import { getVueOptions } from './options';

const name = 'creative';
console.log(getVueOptions(name).data());
export default Vue.component(name, getVueOptions(name));
</script>

<style lang="less" scoped>

@accent-color: rgb(40,53,74);
@title-color:  rgb(226, 102, 57);

.resume {
  display: flex;
  position: relative;

  font-family: 'Roboto' !important;
  font-size: 0.9em;
}

.left-column {
  width: 29%;
  height: 100%;
  padding: 20px;
  padding-top: 15px;
  text-align: left;

  color: #ffffff;
  // color:rgba(255,255,255,0.59);
  background-color: @accent-color;
  overflow: hidden;
  display: block;
  z-index: 2;

  opacity: 1; // lower this value (0.7 approx.) to see the cover image
  position: absolute;
}

// Background cover displayed on the left-column side
// ------------
.left-column-bg {
  // You can put your own cover image in the url path
  // --------------------------------------
  // background: url('../assets/cover.jpg');
  opacity: 0; // up this value to contrast the cover image

  width: 25%;
  height: 100%;
  padding: 47px;
  padding-top: 15px;

  display: block;
  overflow: hidden;
  position: relative;
  top: 0;
  z-index: 1;
}

.right-column {
  display: flex;
  flex-direction: column;
  padding: 25px;
  padding-top: 15px;

  height: 100%;
  width: 75%;
}

a {
  color: inherit;
  cursor:pointer;
  text-decoration-line: none;

  &:visited {
    color: inherit;
  }
}

.material-icons {
  color: @accent-color;
  position: relative;
  top: 5px;
}

.skill-icon {
  color: white;
  font-size: 1.5em;

  top: 2px;
  position: relative;
}

.font-awesome-icons {
  color: @accent-color;
  font-size: 1.3em;
  margin-right: 6px;
}

.small-icon {
  top: 2.5px;
  font-size: 1.4em;
}

.contact-icon {
  color: white;
  font-size: 1.5em;
  margin-right: 10px;

  top: 2px;
  position: relative;
  width: 20px;
  height: 20px;
  // float: left;
}

.contact-icon-svg {
  margin-top: -2.5px;
  margin-right: 10px;

  transform: scale(1);

  top: 5px;
  position: relative;
}

.contact-icon-svg path {
  fill: white;
}

.external-link {
  display: block;
  margin-bottom: 5px;
}

.block-marged {
  margin-top: 5px;
  margin-bottom: 5px;
}

.multi-line-txt {
  margin-top: 30px;
  margin-bottom: 20px;
}

.social-container {
  margin-top: 20px;
  margin-bottom: 20px;
  // text-align: start;
}

.headline {
  color: white;
  font-size: 1.3em;
  font-weight: bold;
}

.big-headline {
  color: white;
  font-size: 2em;
  font-weight: bold;
}

.txt-full-white {
  color: white;
  font-size: 1em;
}

.uppercase {
  font-weight: 500;
  font-size: 3rem;
  letter-spacing: 0.5rem;
  text-transform: uppercase;
  margin: 0;
  // text-transform: uppercase;
}

.section-headline {
  color: #04284a;
  display: inline-block;

  font-family: 'Muli', sans-serif;
  letter-spacing: 0.1875rem;
  text-transform: uppercase;

  font-size: 0.75rem;
  font-weight: 700;
  // font-size: 1.2em;
  // margin-left: 5px;
}

.skill-headline {
  // color: white;
  color: @title-color;
  display: inline-block;
  // font-size: 1.2em;
  // margin-left: 5px;
  font-family: 'Muli', sans-serif;
  letter-spacing: 0.1875rem;

  font-size: 0.75rem;
  font-weight: 700;

  // letter-spacing: 0.1875rem;
  // line-height: 2rem;
  text-transform: uppercase;
}

.section-content {
  margin-top: 5px;
  // padding-left: 5px;
}

.section-content__item {
  display: block;
  margin-bottom: 5px;
}

.section-content__item-grid {
  flex: 1 1 0;

  margin-bottom: 5px;
  padding-right: 5px;
}

.grid-display {
  display: grid;
  grid-gap: 5px;
  grid-template-columns: repeat(3, 1fr);
}

.section-content__header {
  display: block;

  font-size: 1.1em;
  font-weight: 500;
}

.squarred-grid-item {
  display: block;

  border: 1px solid @accent-color;

  background-color: @accent-color;
  color: white;

  margin-top: 5px;
  padding: 5px;

  transition: .5s;

  &:hover {
    background-color: transparent;
    color: rgba(0,0,0,0.42);
    transition: .5s;
  }
}

.section-content__subheader {
  display: block;

  // font-size: 0.6875rem;
  // font-weight: 30;
  // letter-spacing: 0.09rem;
  // line-height: 1rem;
  // text-transform: uppercase;
  // font-weight: 400;
}

.section-content__text {
  display: block;
  font-weight: 300;
}

.section-content__text--light {
  color: rgba(0,0,0,0.42);
  font-weight: 300;
}

.section-content__subheader,
.section-content__text--light,
.section-content__header {
  line-height: 1.5em;
}

.section {
  margin-top: 10px;
  margin-bottom: 10px;
}

.lang-icon {
  color: rgba(0,0,0,0.72);
  font-size: 3em;

  &:hover {
    color: @accent-color;
  }
}

.hobbies-container {
  margin-top: 30px;
}

.hobbies-content {
  display: flex;
  flex-direction: column;
}

.hobby-item {
  display: grid;
  grid-template-columns: 30px auto;

  color: rgba(255, 255, 255, .6);

  margin-right: 25px;
  margin-bottom: 10px;

  transition: .5s;

  &:hover {
    color: rgba(255, 255, 255, .8);
    transition: .5s;
  }
}

.hobby-item__icon {
  font-size: 1.3em;
}

.hobby-item__icon-label {
  top: 2.5px;
  position: relative;
}

.subheadline {
  color: rgba(255, 255, 255, .8);
  font-size: 1.2em;

  display: block;
  margin-bottom: 10px;
}

.experience-item {
  // display: block;
  // margin-left: 1em;
  // text-indent: -0.3em;
  // text-indent: 12px;
  // float: left;
  // clear: both;
}

.borderline {
  border-bottom: 1px solid grey;
}

.list {
  margin-block-start: 0em;
  padding-inline-start: 1.5em;
  list-style-position: outside;
  margin-block-end: 0em;
}

.sub {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
}

.division {
  font-family: 'Muli', sans-serif;
  letter-spacing: 0.1rem;

  font-size: 0.75rem;
  font-weight: 50;
  // margin: -5px;
  padding-right: 10px;
  border-right: 1px solid grey;
  // color: @title-color;
}

.division-after {
  font-family: 'Muli', sans-serif;
  letter-spacing: 0.1rem;

  font-size: 0.75rem;
  font-weight: 50;

  padding-left: 10px;
}

.pos {
  text-transform: uppercase;
}

.project-name {
  text-transform: uppercase;
}


.sub-description {
  font-family: 'Muli', sans-serif;
  font-weight: 300;
  line-height: 1.6;
  margin: 0;
  padding: 0;
  color: #4e4c4c;
  background: #fff;
  text-rendering: optimizeLegibility;
}

.school {
  text-transform: uppercase;
}
.time {
  color: white;
}

.highlight{
  color: @title-color;
}

.borderline-light {
  border-bottom: 1px solid white;
}
// .list-item {
//   padding-left: 20px;
// }

</style>
