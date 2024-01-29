<template lang="">
  <div class="main-container" id="project">
    <div  v-for="(items,index) in projectData.ProjectsArray" v-bind:key="items">
      <div class="project-card">
        <h2>{{projectData.ProjectsArray[index].Title}}</h2>
        <div class="project-image">
          <img :src="projectData.ProjectsArray[index].Image" alt="">
        </div>
        <p>{{projectData.ProjectsArray[index].About}}</p>
        <div class="skills">
        <div v-for="(item,index2) in projectData.ProjectsArray[index].SkillIcon">
            <img :src="projectData.ProjectsArray[index].SkillIcon[index2]" alt="">
        </div>
        </div>
        <div class="links">
            <a :href="projectData.ProjectsArray[index].Link1" target="_blank"><img src="../assets/icons8-github-94.png" alt=""></a>
            <a :href="projectData.ProjectsArray[index].Link2" target="_blank"><img src="../assets/link.png" alt=""></a>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import jsonData from "/projects.json"
export default {
  data(){
    return{
      projectData:jsonData
    }
  }
  
}
</script >
<style  scoped>
  .main-container{
    
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
  }
  .project-card{
    padding: 10px;
    margin: 10px;
    width: 30rem;
    flex-wrap: 0 0 40%;
    background-color: #fff;
    border-radius: 25px;
    box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
  }
  .project-image{
    margin: auto;
    width: 100%;
    object-fit: cover;
    border-radius: 10%;
    overflow: hidden; 
  }
.project-card img{
  height: 18rem;
}

.skills{
  display: flex;
  justify-content: center;
}
.skills img{
  height: 3rem;
  margin: 5px;
}

.links{
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-end;
}
.links img{
  height: 1.5rem;
  margin: 5px;
}

@media only screen and (max-width:510px){
  .project-card{
    margin: auto;
    margin-bottom: 10px;
    width: 20rem;
  }

  .project-image{
    margin: auto;
    width: 100%;
    object-fit: cover;
    border-radius: 10%;
    overflow: hidden; 
  }
  .project-card img{
    height: 12rem;
  }

  .skills{
  display: flex;
  justify-content: center;
}
.skills img{
  height: 3rem;
  margin: 5px;
}

.links{
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-end;
}
.links img{
  height: 1.5rem;
  margin: 5px;
}


}

</style>