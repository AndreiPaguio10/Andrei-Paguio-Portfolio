<template>
	<div class="container-fluid" id="about">
			<div class="row text-center" id="ham">
				<p>ABOUT ME</p>
			</div>
			<div class="row text-center" id="ham1">
				<p>LEARN MORE ABOUT ME</p>				
			</div>
			<div class="row justify-content-center py-5 g-4">
				<div id="carouselExampleIndicators" class=" col-12 col-md-8 col-lg-5 col-xl-3 carousel slide" data-bs-ride="carousel">
				  <div class="carousel-indicators">
				    <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
				    <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2"></button>
				    <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" aria-label="Slide 3"></button>
				  </div>
				  <div class="carousel-inner">
				    <div class="carousel-item active" id="pic1">
				      <img src="/images/grad.jpg" class="d-block w-100" alt="...">
				    </div>
				    <div class="carousel-item" id="pic2">
				      <img src="/images/picc.jpg" class="d-block w-100" alt="...">
				    </div>
				    <div class="carousel-item" id="pic3">
				      <img src="/images/life.jpg" class="d-block w-100" alt="...">
				    </div>
				  </div>
				  <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
				    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
				    <span class="visually-hidden">Previous</span>
				  </button>
				  <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
				    <span class="carousel-control-next-icon" aria-hidden="true"></span>
				    <span class="visually-hidden">Next</span>
				  </button>
				</div>
				<div id="about-text" class="col-12 col-md-10 col-lg-7 col-xl-4">
					<h3 id="name">Hi, I’m Andrei M. Paguio.</h3>
					<p id="des1">I’m a licensed Electronics Engineer who’s really passionate about building websites and turning ideas into something people can actually use and enjoy. I’ve been working with HTML, CSS, and Bootstrap, and I use Git to keep my projects organized and track my progress as I build.</p>
					<p id="des2">I enjoy the whole process of web development—from starting with a simple idea to bringing it to life with clean and responsive design. There’s something satisfying about seeing a project go from a blank page to a fully working website, and I like focusing on the details that make it look polished and easy to use.</p>
					<p id="des3"> Coming from an engineering background, I approach things in a logical and structured way and I’m comfortable solving problems along the way. Right now, I’m focused on growing my skills and working toward becoming a full stack developer, always looking to learn more and take on new projects to improve.</p>
					
					<a href="#projects" class="text-decoration-none" id="but2">CHECK MY PROJECTS</a>
				</div>	
			</div>		
		</div>	
</template>