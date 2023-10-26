<template>
  <div class="container">
    <div class="resume">
      <div class="left">
        <header>
          <img src="../src/img/boss.jpg" alt="">
          <h1>Hi, I'm <span>{{ fullName }}</span></h1>
          <h2>{{ job }}</h2>
          <p>I have knowledge of the basic principles of UI (User Interface) and UX (User Experience) design, 
            which are essential parts of creating user-friendly and effective applications and websites. 
            The duties of a UI Designer include creating the user interface, designing icons and colors, 
            planning the structure of the screen, and ensuring a good user experience.</p>
        </header>
      </div>

      <div class="right">
        <h1>Resume</h1>

        <section class="education">
          <h2>Education</h2>
          <div v-for="(educationItem, index) in education" :key="index">
            <h3>{{ educationItem.degree }}</h3>
            <p>{{ educationItem.school }}</p>
            <p>{{ educationItem.year }}</p>
          </div>
        </section>

        <section class="experience">
          <h2>Work Experience</h2>

          <div v-for="(experienceItem, index) in experience" :key="index">
            <h3>{{ experienceItem.jobTitle }}</h3>
            <p>{{ experienceItem.company }}</p>
            <p>{{ experienceItem.year }}</p>
            <p>{{ experienceItem.description }}</p>
          </div>

          <div v-for="(experienceItem, index) in experience2" :key="index">
            <h3>{{ experienceItem.jobTitle }}</h3>
            <p>{{ experienceItem.company }}</p>
            <p>{{ experienceItem.year }}</p>
            <p>{{ experienceItem.description }}</p>
          </div>

        </section>

        <section class="contact">
          <h2>Contact Information</h2>
          <ul>
            <li>Email: {{ email }}</li>
            <li>Phone: {{ phone }}</li>
            
          </ul>
        </section>

      </div>

    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fullName: "Kollawat Premchit",
      job: "UX/UI Design",
      email: "kollawat@example.com",
      phone: "123-456-7890",
      
      education: [
        {
          degree: "Software Engineering",
          school: "Burapha University",
          year: "Graduated in 2021",
        },
        // เพิ่มรายการการศึกษาเพิ่มเติมตามต้องการ
      ],
      experience: [
        {
          jobTitle: "Team Project Member",
          company: "TTT Brother Co. Ltd",
          year: "2023 - 2024",
          description: "I work with TTT Brother Co. Ltd in system development, and the project is named IoT Connect.",
        },
        // เพิ่มประสบการณ์ทำงานเพิ่มเติมตามต้องการ
      ],
      experience2: [
        {
          jobTitle: "Team Project Member",
          company: "IV Soft Co. Ltd",
          year: "2022 - 2023",
          description: "I work with IV Soft Co. Ltd in system development,and the project is named Funeral Aid Management System : FAMS. I am responsible for the position of UX/UI Design.",
        },
        // เพิ่มประสบการณ์ทำงานเพิ่มเติมตามต้องการ
      ],
    };
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@500&display=swap');


* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Inter', sans-serif;

}

body {
  background-image: url('https://p4.wallpaperbetter.com/wallpaper/677/108/866/purple-scene-landscape-minimal-4k-wallpaper-preview.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
}

.container {
  margin: 50px 0;
  width: 100%;
}

@media screen and (max-width: 1030px) {
  .container .resume {
    grid-template-columns: repeat(1, 500px);
  }

  .container .left h2 {
    margin: 0px 100px;
  }
}

@media screen and (max-width: 500px) {
  .container .resume {
    grid-template-columns: repeat(1, 400px);
  }

  .container .resume img {
    border-radius: 100%;
    width: 200px;
    height: 200px;
  }

  .container .left h2 {
    margin: 0px 50px;
  }

}

@media screen and (max-width: 400px) {
  .container .resume {
    grid-template-columns: repeat(1, 300px);
  }
  .container .resume img {
    border-radius: 100%;
    width: 150px;
    height: 150px;
  }

  .container .left h2 {
    margin: 0px 20px;
  }
}

.resume {
  max-width: 800px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 700px 570px;
  grid-template-rows: repeat(1, auto);
  justify-content: center;
  align-items: center;
  gap: 1rem;
}

.resume .left {
  width: 100%;
  padding: 20px;
  background-color: rgba(255, 255, 255, 0.611);
  backdrop-filter: blur(5px);
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;

}

.resume img {
  border-radius: 100%;
  width: 300px;
  height: 300px;
}

.resume .right {
  width: 100%;
  padding: 20px;
  background-color: rgba(255, 255, 255, 0.611);
  backdrop-filter: blur(5px);
  height: 100%;
}

.right h1 {
  padding-bottom: 10px;
  border-bottom: 2px solid rgb(0, 0, 0);
}

header {
  text-align: center;
}

.left h1 {
  margin: 20px 0;
}

.left span {
  color: #490074;
}

.left h2 {
  font-size: 20px;
  margin: 20px 200px;
  padding: 10px;
  background-color: #8800cc;
  color: #fff;
  border-radius: 10px;
}

.right h2 {
  font-size: 18px;
  padding: 10px;
  width: fit-content;
  background-color: #8800cc;
  color: #fff;
  border-radius: 10px;
  margin-bottom: 10px;
}

.right p {
  font-size: 16px;
}

.left p {
  padding: 15px;
  margin: 20px 0;
}

section {
  padding: 10px;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}

.contact {
  margin-top: 20px;
}

.contact ul {
  list-style-type: none;
  padding: 0;
}

.contact a {
  color: #0581e6;
  text-decoration: none;
}

.education,
.experience {
  margin-top: 20px;
}

.education h3,
.experience h3 {
  margin: 0;
}</style>
