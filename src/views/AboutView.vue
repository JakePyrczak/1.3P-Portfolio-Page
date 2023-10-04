<template>
  <section class="about-me-page">

    <div class="about-content">
      <h1 style="color: #32429d;;">About Me</h1>
      <p>
        Hello! I'm Jake Pyrczak, a passionate IT student. I love different kinds of programming and am comfortable using Python and C++. I specialize in Networking, Cyber Security and Data Science.
      </p>
      <p>
        I in my final at Deakin University with a degree in of Information Technology Majoring in Cyber Security. Im Currently looking for full time work in the IT industry.
      </p>
      <p>
        In my free time, I love watching documentaries, bike riding and video games. But im always trying to learn new things, and willing to give anything a go.
      </p>
      <button class="download-btn">Download My Resume</button>
      <p>
        Thank you for visiting my portfolio. If you'd like to collaborate or just chat, feel free to <a href="mailto:jpyrczak@deakin.edu.au">reach out</a>!
      </p>
    </div>
    <div class="profile-image">
      <img src="../assets/images/my face.png" alt="Your Name" class="hover-effect">
    </div>
  </section>
  
</template>

<script setup>
// You can add any reactive properties or methods if needed.
</script>

<style scoped>
.about-me-page {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 40px 0;
  max-width: 1200px;
  margin: 50px 0;
  background-color: #f4f4f4;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.profile-image {
  flex: 1;
  padding-left: 50px;
}

.profile-image img.hover-effect {
  max-width: 100%;
  border-radius: 50%;
  transition: transform 0.3s, box-shadow 0.3s;
}

.profile-image img.hover-effect:hover {
  transform: scale(1.05);
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
}

.about-content {
  flex: 2;
  background-color: #fff;
  padding: 20px;
  border-radius: 10px;
}

.about-content h1 {
  font-size: 2.5em;
  margin-bottom: 20px;
}

.about-content p {
  margin-bottom: 20px;
  line-height: 1.6;
}

.about-content a {
  color: #e74c3c;
  text-decoration: none;
  transition: color 0.3s;
}

.about-content a:hover {
  color: #c0392b;
}

.download-btn {
  display: inline-block;
  background-color: #e74c3c;
  color: #fff;
  padding: 10px 20px;
  border-radius: 5px;
  border: none;
  cursor: pointer;
  transition: background-color 0.3s;
}

.download-btn:hover {
  background-color: #c0392b;
}

@media (max-width: 710px) {
  .about-me-page {
    padding: 10px 10px;
    flex-direction: column;
  }

  .about-content {
    padding-top: 0px;
  }

  .profile-image {
    flex: 1;
    text-align: center;
    padding-top: 40px;
    padding-bottom: 380px;
    padding-left: 0px;
    max-width: 270px; /* Set the maximum width you want for the image */
    max-height: 300px; /* Set the maximum height you want for the image */

  }
}
</style>