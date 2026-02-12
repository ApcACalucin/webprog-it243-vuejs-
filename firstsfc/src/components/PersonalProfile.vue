<template>
  <div class="container">
    <header>
      <h1>Personal Profile Web Page</h1>
    </header>

    <main>
      <section class="main-content">

        <div>
          <h2>Education & Achievements</h2>
          <p><strong>Asia Pacific College</strong></p>
          <p>2nd Year</p>

          <h3>Achievements</h3>
          <p>Defended a Capstone</p>
        </div>

        <div>
          <h2>IT Experience</h2>
          <p>I have experience working with:</p>
          <ul>
            <li>Web Development (HTML, CSS, JS)</li>
            <li>Java</li>
            <li>Python</li>
          </ul>
        </div>

        <div>
          <h2>Hobbies & Interests</h2>
          <p>Gaming, Coding, Photography, Traveling</p>
        </div>

        <div>
          <h2>Goals & Dreams</h2>
          <p>
            "To become a Software Developer and use technology to create 
            sustainable solutions for the community."
          </p>
        </div>

      </section>

      <aside class="sidebar">
      </aside>
    </main>

    <footer>Asia Pacific College</footer>
  </div>
</template>

<script>
export default {
  name: "PersonalProfile"
}
</script>

<style>
.container {
  font-family: Arial, sans-serif;
  padding: 20px;
}

header {
  text-align: center;
}

.main-content h2 {
  margin-top: 20px;
  color: #2c3e50;
}

ul {
  padding-left: 20px;
}
</style>


