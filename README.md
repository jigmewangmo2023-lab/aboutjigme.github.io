<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Jigme's World</title>
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-padding-top: 160px; } /* offset for header + subnav */
  body {
    font-family: 'Roboto', Arial, sans-serif;
    background: linear-gradient(rgba(255,255,255,0.9), rgba(255,255,255,0.9)), url('https://wallpapers.com/images/featured/soft-aesthetic-cei80uravrnl6ltm.jpg') no-repeat center center fixed;
    background-size: cover;
    line-height: 1.6;
    color: #4b3b5f;
    scroll-behavior: smooth;
  }
  a { text-decoration: none; color: white; }
  a:hover { color: #5a3d6b; }

  header {
    background: rgba(168,127,207,0.9);
    padding: 20px 0;
    z-index: 1000;
  }
  header h1 { text-align: center; color: #ece9e4; font-size: 50px; }

  nav ul {
    display: flex;
    justify-content: center;
    list-style: none;
    flex-wrap: nowrap; 
  }
  nav li { margin: 0 15px; }
  nav a { padding: 10px 20px; border-radius: 8px; display: block; transition: 0.3s; cursor:pointer; }
  nav a:hover { background-color: #a87fcf; color: #ece9e4; }

  main { padding: 20px; max-width: 1200px; margin: auto; }

  section { margin-bottom: 50px; padding: 20px; background: rgba(230,210,230,0.8); border-radius: 12px; }
  section h2, section h3, section h4 { margin-bottom: 15px; color: #5a3d6b; }
  p { margin-bottom: 15px; }

  #about img { max-width: 300px; border-radius: 15px; display: block; margin: 20px auto; }

  .gallery { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 15px; margin-top: 20px; }
  .gallery img { width: 100%; border-radius: 15px; transition: transform 0.3s, box-shadow 0.3s; cursor: pointer; }
  .gallery img:hover { transform: scale(1.05); box-shadow: 0 8px 15px rgba(0,0,0,0.2); }

  .subnav { display: flex; flex-wrap: wrap; justify-content: center; list-style: none; margin-bottom: 20px; padding: 10px; background: rgba(220,182,230,0.6); border-radius: 8px; }
  .subnav li { margin: 5px 10px; }
  .subnav a { padding: 8px 15px; border-radius: 6px; display: block; transition: 0.3s; cursor: pointer; }
  .subnav a:hover { background-color: #a87fcf; color: #ece9e4; }

  .mentees-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(120px, 1fr)); gap: 15px; justify-items: center; margin-top: 20px; }
  .image-container { position: relative; width: 120px; height: 120px; overflow: hidden; border-radius: 15px; }
  .image-container img { width: 100%; height: 100%; object-fit: cover; transition: transform 0.3s ease; }
  .image-container:hover img { transform: scale(1.05); }
  .image-container .overlay { position: absolute; bottom: 0; left: 0; right: 0; background: rgba(88,58,123,0.8); color: #fff; text-align: center; font-weight: bold; padding: 5px 0; opacity: 0; transition: opacity 0.3s ease; font-size: 14px; border-top-left-radius: 10px; border-top-right-radius: 10px; }
  .image-container:hover .overlay { opacity: 1; }

  .sub-section { margin-top: 30px; }
  .hidden { display: none; }

  footer { text-align: center; padding: 20px; background: rgba(168,127,207,0.9); color: #ece9e4; border-radius: 12px; margin-top: 20px; }

  @media(max-width:900px){
    .gallery img { width: 100%; }
    nav ul { flex-direction: row; }
    .subnav { flex-direction: column; align-items: center; }
  }
  
.centered-image {
  text-align: center;
  margin: 20px 0;
}

.centered-image img {
  width: 95%;        /* almost full width */
  max-width: 900px;  /* very large, but still controlled */
  border-radius: 15px;
}

</style>
</head>
<body>

<header>
  <h1>Welcome to Jigme's World!</h1>
  <nav>
    <ul>
      <li><a onclick="showSection('home')">Home</a></li>
      <li><a onclick="showSection('about')">About Me</a></li>
      <li><a onclick="showSection('school')">School Life</a></li>
      <li><a onclick="showSection('contact')">Contact</a></li>
    </ul>
  </nav>
</header>

<main>
  <!-- Home Section -->
  <section id="home">
    <h2>Home</h2>
    <p>Welcome to my corner of the internet! My name is Jigme, and I’m thrilled you’re here. This is a space where I share a little about who I am, my passions, my school life, and the things that inspire me every day. I love learning new things, exploring my creativity, and connecting with people who share similar interests. Whether you’re here to learn more about me, see what I’m up to at school, or just browse around, I hope you enjoy your visit and find something that sparks your curiosity. Thanks for stopping by feel free to explore, and I hope you feel welcome!</p>
  </section>

  <!-- About Section -->
  <section id="about">
    <h3>About Me</h3>
    <img src="https://i.imgur.com/fUn8UAY.jpeg" alt="Me">
    <p>My name is Jigme Wangmo, and I am currently studying in the 9th grade. I love singing, dancing, journaling, traveling, exploring new things, and spending quality time with the people I care about. I come from the eastern part of Bhutan, in Trashigang Dzongkhag, and I’m proud of my roots. One of my favorite subjects is Dzongkha, as I enjoy learning and celebrating my language and culture. I dream of performing on a stage one day, sharing my music and creativity with others. I also believe that everyone should follow their passion and listen to their heart, it’s the best way to live fully.</p>
  </section>

  <!-- School Life Section -->
  <section id="school">
    <h4>School Life</h4>

    <!-- Subnav for school subsections -->
    <ul class="subnav">
      <li><a onclick="showSubSection('cern')">CERN</a></li>
      <li><a onclick="showSubSection('mentor-mentee')">Mentor-Mentee</a></li>
    </ul>

    <p>I currently study at The Royal Academy, located in Paro, Bhutan. One of the most memorable moments in my school journey was in the sixth grade, when I had the amazing opportunity to attend the winter camp. That experience was truly special and led to my selection to study at The Royal Academy.</p>
    <div class="centered-image">
      <img src="https://i.imgur.com/NsZAdoB.jpeg" alt="Grademate">
    </div>
    <div class="gallery">
      <img src="https://i.imgur.com/S1PMXdb.jpeg" alt="Students">
      <img src="https://i.imgur.com/ZPpWt6g.jpeg" alt="Scouts Camp">
      <img src="https://i.imgur.com/iqDkZ3V.jpeg" alt="Teachers day">
      <img src="https://i.imgur.com/vav6zBq.jpeg" alt="Students">
      <img src="https://i.imgur.com/QXw7Nam.jpeg" alt="Us">
      <img src="https://i.imgur.com/dgFgYM5.jpeg" alt="Teachers day">
      <img src="https://i.imgur.com/BdiUc7i.jpeg" alt="Teachers day">
      <img src="https://i.imgur.com/QWdkv6z.jpeg" alt="Us">
    </div>

    <!-- CERN Subsection -->
<div id="cern" class="sub-section hidden">
  <h4>CERN</h4>

  <p>Another unforgettable experience was when I had the opportunity to visit CERN and explore Europe. This trip was incredibly special because I got to visit many beautiful and historic places such as the Trevi Fountain, Vatican City, the Pantheon, and the Boboli Gardens, among many others. Each place was filled with fascinating history and amazing sights. There were 10 students and 2 teachers, and together we made a lot of wonderful memories during this journey.</p>

  <div class="gallery">
    <div class="image-container">
      <img src="https://i.imgur.com/NqNtpS0.jpeg" alt="Europe trip 1">
    </div>
    <div class="image-container">
      <img src="https://i.imgur.com/czr81DN.jpeg" alt="Painting">
    </div>
    <div class="image-container">
      <img src="https://i.imgur.com/wI3GmUZ.jpeg" alt="Painting">
    </div>
  </div>

  <p>Our trip started really early on the 7th of November. We left home at 5 AM and had a long journey through Bagdora and Rome before finally landing in Geneva around 2 PM the next day. When we arrived, Mr. Andy from Aiglon College picked us up, and after a two-hour drive to the campus, we settled in and went for dinner in Villars. That night, we even tried bowling for the first time. It was very embarrassing at first, but so much fun! The Aiglon students we met were super friendly, and we all laughed a lot while learning the game.</p>

  <div class="gallery">
    <div class="image-container">
      <img src="https://i.imgur.com/qYdO0Nv.jpeg" alt="Group photo">
    </div>
    <div class="image-container">
      <img src="https://i.imgur.com/shqRtpK.jpeg" alt="Geneva">
    </div>
    <div class="image-container">
      <img src="https://i.imgur.com/gd6DzcK.jpeg" alt="Geneva">
    </div>
  </div>

  <p>The next day was a hike in the Swiss Alps, and it was honestly breathtaking. The trail had these amazing views of the mountains, and walking through the forested paths felt peaceful and calming. Along the way, we chatted with the Aiglon students about school life, culture, and even science stuff we noticed around us, like how plants grow differently at different heights or how steep the slopes were. That evening, we cooked Swiss fondue and Bhutanese Ema Datshi and it was such a fun way to share our cultures while learning a bit of science and math through cooking.</p>

  <div class="gallery">
    <div class="image-container">
      <img src="https://i.imgur.com/7VJnlCn.png" alt="Swiss Alps">
    </div>
    <div class="image-container">
      <img src="https://i.imgur.com/MdDwh3f.png" alt="Swiss Alps">
    </div>
  </div>

  <p>Our last day at Aiglon was jam-packed. We tried meditation, attended science classes, built small robots, and even did ice skating for the first time. Some of us fell a lot, but by the end, we were proud we had learned a totally new skill. We also shared our culture with younger students and even got hands-on in anatomy class. It was amazing to see how different learning can be when it’s interactive, fun, and social.</p>

  <div class="gallery">
    <div class="image-container">
      <img src="https://i.imgur.com/rxKMCS5.png" alt="Class">
    </div>
    <div class="image-container">
      <img src="https://i.imgur.com/FHw8L5u.png" alt="Class">
    </div>
  </div>

  <p>Then came CERN. Three days there felt like stepping into a science movie. Dr. Archana Sharma explained particles, quarks, the Higgs boson, and how they smash particles together to understand the universe. We even made our own tiny bubble chambers and tried virtual experiments. Walking through the labs, seeing parts of detectors, and even meeting scientists was mind-blowing. And the best part? We got to have dinner with the Bhutanese UN Ambassador and explore Geneva a bit too, like the cathedral and the old cannons at L’Ancien Arsenal, before heading to Florence.</p>

  <div class="gallery">
    <div class="image-container">
      <img src="https://i.imgur.com/nf28SFZ.png" alt="At CERN">
    </div>
  </div>

  <p>Florence was like walking through history. The Uffizi Gallery, Palazzo Vecchio, Ponte Vecchio, Boboli Gardens, and the Accademia Gallery with Michelangelo’s David. Every corner had something amazing. We loved wandering around the streets, seeing art everywhere, and learning about the Renaissance. The Museo Galileo was super cool too seeing old scientific instruments and even Galileo’s finger made science feel alive in history. Finally, Rome. From the Colosseum and Roman Forum to Saint Peter’s Basilica, the Trevi Fountain, and the Pantheon, the city felt like a living museum. Walking through the Holy Door and seeing so many historic sites made the trip feel complete. Even though we couldn’t go inside the Colosseum, seeing it up close was incredible. Throwing coins in the Trevi Fountain and making wishes felt like a perfect way to end the trip.</p>

  <div class="gallery">
    <div class="image-container">
      <img src="https://i.imgur.com/uEOF05l.png" alt="Italy">
    </div>
    <div class="image-container">
      <img src="https://i.imgur.com/WsxaPKs.jpeg" alt="Italy">
    </div>
    <div class="image-container">
      <img src="https://i.imgur.com/fQ1RlkT.jpeg" alt="Italy">
    </div>
  </div>
</div>


    <!-- Mentor-Mentee Subsection -->
    <div id="mentor-mentee" class="sub-section hidden">
      <h4 style="text-align:center; margin-bottom:30px;">Mentor-Mentee</h4>
      <div style="text-align:center; margin-bottom:40px;">
       <div class="image-container" style="width:150px; height:150px; margin:auto;">
            <img src="https://i.imgur.com/jW43gWp.jpeg" alt="Thinley Dorji">
            <div class="overlay">Thinley Dorji</div>
        </div>
      </div>
      <p><strong>Mentees:</strong></p>
      <div class="mentees-grid">
        <div class="image-container"><img src="https://i.imgur.com/ILXj1cB.png" alt="Yeshey Lhamo"><div class="overlay">Yeshey Lhamo</div></div>
        <div class="image-container"><img src="https://i.imgur.com/yd1PgHD.png" alt="Kinley Sonam"><div class="overlay">Kinley Sonam</div></div>
        <div class="image-container"><img src="https://i.imgur.com/Sb4d1Wq.png" alt="Dhan Bhadur Rana Mongar"><div class="overlay">Dhan Bhadur Rana Mongar</div></div>
        <div class="image-container"><img src="https://i.imgur.com/HwlKh32.png" alt="Jigme Thinley Namgyel"><div class="overlay">Jigme Thinley Namgyel</div></div>
        <div class="image-container"><img src="https://i.imgur.com/SmUh4yD.png" alt="Dorji Yangzom"><div class="overlay">Dorji Yangzom</div></div>
        <div class="image-container"><img src="https://i.imgur.com/Wtx6fOe.png" alt="Ashman Pakhring"><div class="overlay">Ashman Pakhring</div></div>
        <div class="image-container"><img src="https://i.imgur.com/M85A5i0.png" alt="Chhimi Dorji"><div class="overlay">Chhimi Dorji</div></div>
        <div class="image-container"><img src="https://i.imgur.com/RvaVNXN.png" alt="Jigme Wangmo"><div class="overlay">Jigme Wangmo</div></div>
        <div class="image-container"><img src="https://i.imgur.com/UiCTY4l.png" alt="Ngawang Sonam Dolkar"><div class="overlay">Ngawang Sonam Dolkar</div></div>
        <div class="image-container"><img src="https://i.imgur.com/LPaPEyl.png" alt="Muskan Karki"><div class="overlay">Muskan Karki</div></div>
        <div class="image-container"><img src="https://i.imgur.com/0CNhaUv.png" alt="Kuenga Yangdon"><div class="overlay">Kuenga Yangdon</div></div>
        <div class="image-container"><img src="https://i.imgur.com/BVYov0S.png" alt="Jigten Gyembo"><div class="overlay">Jigten Gyembo</div></div>
      </div>
      <p>For me, the mentor-mentee is a place where I can share my problems openly, and I always feel heard and supported.
 The mentors are like a second family, guiding me with care, understanding, and encouragement. 
          It’s a space where I can ask questions without hesitation, learn from their experiences, and gain valuable advice for both school
          and life. Beyond guidance, it’s a place where I feel safe, valued, and inspired to grow. They celebrate my 
          successes with me, help me overcome challenges, and motivate me to become the best version of myself. 
          Being part of mentor-mentee has taught me the importance of trust, empathy, and building meaningful 
          connections that last a lifetime..</p>
    </div>

  </section>

  <!-- Contact Section -->
  <section id="contact">
    <h3>Contact</h3>
    <p>You can reach me via email at <a href="mailto:jigme.wangmo2023@academy.bt">jigme.wangmo2023@academy.bt</a>.</p>
  </section>

</main>

<footer>
  &copy; 2025 Jigme's World
</footer>

<script>
  // Main nav
  function showSection(sectionId){
    const sections = document.querySelectorAll('main > section');
    sections.forEach(sec => sec.classList.add('hidden'));
    document.getElementById(sectionId).classList.remove('hidden');
    window.scrollTo({top:0, behavior:'smooth'});
  }

  // Show Home initially
  showSection('home');

  // Subnav inside School Life
  function showSubSection(subId){
    const subSections = document.querySelectorAll('#school .sub-section');
    subSections.forEach(sub => sub.classList.add('hidden')); // hide all
    document.getElementById(subId).classList.remove('hidden'); // show clicked section
    document.getElementById(subId).scrollIntoView({behavior: 'smooth', block: 'start'});
  }
</script>

</body>
</html>



