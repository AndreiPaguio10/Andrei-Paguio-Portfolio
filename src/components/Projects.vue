<template>
	<div id="projects">
				<div class="container">
				<div class="row text-center" id="hmp">
					<p>MY PROJECTS</p>				
				</div>
				<div class="row text-center" id="hmp1">
					<p>CHECK OUT MY RECENT WORK</p>
				</div>
				</div>
				<div class="container" id="projects">
				  <div id="cardCarousel" class="carousel slide" data-bs-ride="carousel">

				    <!-- Indicators -->
				    <div class="carousel-indicators">
				      <button type="button" data-bs-target="#cardCarousel" data-bs-slide-to="0" class="active"></button>
				      <button type="button" data-bs-target="#cardCarousel" data-bs-slide-to="1"></button>
				      <button type="button" data-bs-target="#cardCarousel" data-bs-slide-to="2"></button>
				    </div>

				    <div class="carousel-inner">

				      <!-- Slide 1 -->
				      <div class="carousel-item active">
				        <div class="row row-cols-1 row-cols-md-3 g-4">
				          <div class="col">
				            <div class="card h-100">
				              <img src="/images/card1.png" class="card-img-top">
				              <div class="card-body">
				              	<p class="card-number">PROJECT 1</p>
				                <h5 class="card-title">E-commerce API Documentation</h5>
				                <p class="card-text">Dynamic E-Commerce Workflow Management. The system features dynamic routes for order processing, real-time inventory updates, and secure user authentication. It also supports seamless automated order reporting and comprehensive product management. Documented Backend API published publicly using Postman.</p>
				              </div>
				            </div>
				          </div>

				          <div class="col">
				            <div class="card h-100">
				              <img src="/images/card2.png" class="card-img-top">
				              <div class="card-body">
				              	<p class="card-number">PROJECT 2</p>
				                <h5 class="card-title">Course Booking API Documentation</h5>
				                <p class="card-text">RESTful API for managing course enrollments, featuring user registration, authentication, and retrieval of user details. Supports course creation, updates, archiving, activation, and student enrollment. Publicly documented using Postman.</p>
				              </div>
				            </div>
				          </div>

				          <div class="col">
				            <div class="card h-100">
				              <img src="/images/card3.png" class="card-img-top">
				              <div class="card-body">
				              	<p class="card-number">PROJECT 3</p>
				                <h5 class="card-title">Course booking App</h5>
				                <p class="card-text">A MERN-stack course enrollment system featuring user registration, authentication, and profile management. Authenticated users can create, update, archive, and activate courses. The platform also allows users to browse available courses and enroll seamlessly.</p>
				              </div>
				            </div>
				          </div>

				        </div>
				      </div>

				      <!-- Slide 2 -->
				      <div class="carousel-item">
				        <div class="row row-cols-1 row-cols-md-3 g-4">

				          <div class="col">
				            <div class="card h-100">
				              <img src="/images/card4.png" class="card-img-top">
				              <div class="card-body">
				              	<p class="card-number">PROJECT 4</p>
				                <h5 class="card-title">E-commerce App</h5>
				                <p class="card-text">MERN E-Commerce Platform. The platform features dynamic product catalog with filtering and sorting, real-time search, seamless cart updates, secure checkout, and a comprehensive admin dashboard with real-time analytics and user management capabilities.</p>
				              </div>
				            </div>
				          </div>

				          <div class="col">
				            <div class="card h-100">
				              <img src="/images/card5.png" class="card-img-top">
				              <div class="card-body">
				              	<p class="card-number">PROJECT 5</p>
				                <h5 class="card-title">Airline Booking System Mockup</h5>
				                <p class="card-text">Side Project: Conceptual design showcasing an intuitive UI for flight search, seat selection, and booking confirmation, focusing on user experience and workflow efficiency.</p>
				              </div>
				            </div>
				          </div>

				          <div class="col">
				            <div class="card h-100">
				              <img src="/images/card6.png" class="card-img-top">
				              <div class="card-body">
				              	<p class="card-number">PROJECT 6</p>
				                <h5 class="card-title">Airline Booking System Prototype</h5>
				                <p class="card-text">Side Project: Interactive prototype simulating end-to-end airline booking functionalities, including flight search, reservation, payment processing, and real-time ticket management.</p>
				              </div>
				            </div>
				          </div>

				        </div>
				      </div>

				      <!-- Slide 3 -->
				      <div class="carousel-item">
				        <div class="row row-cols-1 row-cols-md-3 g-4">

				          <div class="col">
				            <div class="card h-100">
				              <img src="/images/card7.png" class="card-img-top">
				              <div class="card-body">
				              	<p class="card-number">CAPSTONE 1</p>
				                <h5 class="card-title">Short Courses Capstone</h5>
				                <p class="card-text">Placeholder for your Short courses capstone project. A full-stack capstone project that integrates modern web technologies to deliver a scalable and user-friendly application. It demonstrates proficiency in backend development, frontend design, and seamless system integration.</p>
				              </div>
				            </div>
				          </div>

				          <div class="col">
				            <div class="card h-100">
				              <img src="/images/card7.png" class="card-img-top">
				              <div class="card-body">
				              	<p class="card-number">CAPSTONE 2</p>
				                <h5 class="card-title">Short Courses Capstone</h5>
				                <p class="card-text">Placeholder for your Short courses capstone project. A full-stack capstone project that integrates modern web technologies to deliver a scalable and user-friendly application. It demonstrates proficiency in backend development, frontend design, and seamless system integration.</p>
				              </div>
				            </div>
				          </div>

				          <div class="col">
				            <div class="card h-100">
				              <img src="/images/card7.png" class="card-img-top">
				              <div class="card-body">
				              	<p class="card-number">CAPSTONE 3</p>
				                <h5 class="card-title">Short Courses Capstone</h5>			
				                <p class="card-text">Placeholder for your Short courses capstone project. A full-stack capstone project that integrates modern web technologies to deliver a scalable and user-friendly application. It demonstrates proficiency in backend development, frontend design, and seamless system integration.</p>
				              </div>
				            </div>
				          </div>
				        </div>
				      </div>
				    </div>

			    <!-- Controls -->
			    <button class="carousel-control-prev" type="button" data-bs-target="#cardCarousel" data-bs-slide="prev">
			      <span class="carousel-control-prev-icon"></span>
			    </button>

			    <button class="carousel-control-next" type="button" data-bs-target="#cardCarousel" data-bs-slide="next">
			      <span class="carousel-control-next-icon"></span>
			    </button>
			  </div>
			</div>			
		</div>
</template>