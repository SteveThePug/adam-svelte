<script>
	import Lines from "./Lines.svelte";
	import Lines2 from "./Lines2.svelte";
</script>

<svelte:head>
	<title>STP</title>
	<meta name="Welcome Home" content="STP's Personal Website" />
</svelte:head>

<section>
	<div class="title-section">
		<h1>Adam French</h1>
		<!-- <img src="images/teeth.png" /> -->
	</div>
	<Lines2 />
	<div class="contact-section">
		<div>
			<p class="left">+44 (0) 07563266931 / adam.a.french@outlook.com</p>
			<p class="left">
				<a href="https://github.com/SteveThePug">GitHub</a> /
				<a href="https://www.linkedin.com/in/adam-french-032a04213/">
					LinkedIn</a
				>
			</p>
			<p class="right">London, England</p>
		</div>
	</div>
	<Lines2 />
	<div class="statement-section">
		<p>
			I am a computer science and mathematics student seeking to undertake
			a summer internship specialising in programming, computer science,
			mathematics or design. My course has taught me fundamental computer
			science and mathematical insight. I wish to apply this knowledge in
			a professional context. I would honored to apply my expertise to
			real-world senarios.
		</p>
		<p>
			I am looking for an internship between June—September 2023, before
			my 3<sup>rd</sup> and final year at the University of Leeds. Currently,
			I am on exchange at the University of Waterloo, Canada which is held
			as a highly regarded instutuion for computer science.
		</p>
		<p>
			I am a highly motivated and adaptable individual that can work
			effectively within teams. I have previous experience in team-based
			positions (in both academic and hospitality roles) has helped me
			understand how to integrate into various teams. I have come to
			understand the significance of communicative, friendly and organized
			environments. Additionally, I am punctual, reliable individual that
			enjoys being purposeful, determined and open-minded to new
			opportunities.
		</p>
	</div>
	<div class="project-section">
		<div style="display: flex; justify-content: space-between;">
			<h2>Personal Computer Science Projects</h2>
			<!-- <img src="images/star.png" /> -->
			<!-- <img src="images/img2.png" /> -->
		</div>
		<table>
			<tr>
				<th>Project</th>
				<th>Skills</th>
				<th>Date</th>
				<th>Description</th>
			</tr>
			<tr>
				<td>Computer Graphics</td>
				<td>Linear Algebra, Scripting, Modelling</td>
				<td>2023</td>
				<td>
					Created a multi-threaded application as a computer graphics
					project. An efficient, mathematicially defined raytracer was
					produced.
				</td>
			</tr>
			<tr>
				<td>Algorithms</td>
				<td>Optimisation, Multi-threading </td>
				<td>2022</td>
				<td>
					To investigate the efficiency of different algorithms I
					produced a C++ application utilising ImGui. This was
					intended to aid me on my Algorithms course.
				</td>
			</tr>
			<tr>
				<td>Personal Website</td>
				<td>Design, UIUX, Creative Coding</td>
				<td>2023</td>
				<td>
					My website implements design patterns and techniques using
					the framework Svelte, and previously Nuxt3, and libraries
					such as P5 and Three.js.
				</td>
			</tr>
			<tr>
				<td>Arduino Programming</td>
				<td>Soldering, Electronics</td>
				<td>2022</td>
				<td>
					A small boombox with a LED screen. It was used to play a
					hard-coded songs with the available 32 kilobytes on an
					Arduino Nano to entertain my flat.
				</td>
			</tr>
			<tr>
				<td>Steam Inventories</td>
				<td>Data analytics</td>
				<td>2021</td>
				<td>
					Using the Steam Web API with HTML requests, deserialising
					and parsing large quantities of inventoy information. Used
					to introduce myself to data analytics.
				</td>
			</tr>
		</table>
	</div>
	<div class="education-section">
		<div style="display: flex; justify-content: space-between;">
			<h2>Education</h2>
			<!-- <img src="images/flying.gif" /> -->
		</div>
		<table>
			<tr>
				<th>Location</th>
				<th>Date</th>
				<th>Description</th>
			</tr>
			<tr>
				<td>The University of Leeds</td>
				<td>2021, Ongoing</td>
				<td>
					I am currently enrolled at the University of Leeds,
					undertaking a Computer Science with Mathematics bachelors.
					Initially, I enrolled as a Computer Science student.
					However, I take pride in the mathematics based modules,
					resulting in me changing to a joint degree.
				</td>
			</tr>
			<tr>
				<td>The University of Waterloo</td>
				<td>2023</td>
				<td>
					My third year of university was taken abroad at the
					University of Waterloo, and award winning univeristy located
					in Ontario, Canada. During this period I travelled and
					engaged with the univeristys clubs and societies.
				</td>
			</tr>
		</table>
	</div>
	<div class="experience-section">
		<div style="display: flex; justify-content: space-between;">
			<h2>Experience</h2>
			<!-- <img src="images/A.gif" /> -->
		</div>
		<table>
			<tr>
				<th>Role</th>
				<th>Location</th>
				<th>Time</th>
				<th>Duties</th>
			</tr>
			<tr>
				<td>Bartender</td>
				<td>Belgrave Music Hall</td>
				<td>2022-2023</td>
				<td>
					Bartending, cleaning, preparing for large events, handling
					pizzas, BOH cleaning and organization, card payments.
				</td>
			</tr>
			<tr>
				<td>Cashier Assistant</td>
				<td>To The Rise Bakery</td>
				<td>Summer 2022 </td>
				<td
					>Preparing coffee, serving customers, presenting goods
					cleaning bakery equipment, preparing toasties</td
				>
			</tr>
			<tr>
				<td>Waiter</td>
				<td>BFI Bar and kitchen</td>
				<td>Summer 2020</td>
				<td
					>Table allocation, managing bookings and walk-ins, drink and
					food runner, dealing with customer complaints, BOH cleaning
					and organization, card payments.</td
				>
			</tr>
		</table>
	</div>
	<div class="commitments-section">
		<div style="display: flex; justify-content: space-between;">
			<h2>Commitments</h2>
			<!-- <img src="images/thumb.png" /> -->
		</div>
		<table>
			<tr>
				<th>Activity</th>
				<th>Time</th>
				<th>Details</th>
			</tr>
			<tr>
				<td>University of Leeds Hockey Club</td>
				<td>2022 - 2023</td>
				<td>Partook in the University of Leeds Hockey Club. </td>
			</tr>
			<tr>
				<td>Royal Air Force Air Cadets</td>
				<td>2017 - 2020</td>
				<td
					>Cadet. Climbed to role of Sergant. Won an award given by
					one of our sponsors, the Royal Company of Environmental
					Cleaners</td
				>
			</tr>
			<tr>
				<td>University of Waterloo Film Club</td>
				<td>2023</td>
				<td
					>Engaged in the University of Waterloo's film club.
					Sumbitted a film for the Jacob Owens Horror Short Film
					Contest</td
				>
			</tr>
			<tr>
				<td>Socratica</td>
				<td>2023</td>
				<td
					>Attended a weekenly weekend meeting, designed for students
					at the University of Waterloo to work on projects disjoint
					from their studies.</td
				>
			</tr>
		</table>
	</div>
	<Lines />
	<p
		style="text-align: center; border-top: 3px dashed darkblue; padding: 10px; border-bottom: 3px dashed darkgreen"
	>
		Without continuity disjoint paths cannot meet
	</p>
</section>

<style>
	section {
		padding: 2vw;
	}
	table {
		border: 1px solid darkblue;
	}
	th {
		border-right: 1px solid black;
		border-left: 1px solid black;
		border-bottom: 2px solid darkblue;
	}
	td {
		border-bottom: 2px solid darkblue;
		border-right: 1px solid black;
		border-left: 1px solid black;
		padding-left: 6px;
		padding-right: 6px;
	}
	img {
		align-self: flex-end;
		height: 2cm;
	}
	/* Title section */
	.title-section {
		display: flex;
		justify-content: space-between;
	}
	/* Contact section */
	.contact-section {
		justify-content: space-between;
	}
	.contact-section div {
		align-items: center;
		justify-content: space-between;
		display: flex;
		height: 3vh;
	}
	.contact-section .left {
		text-align: left;
		font-size: 2vh;
		padding: none;
	}
	.contact-section .right {
		text-align: right;
		font-size: 2vh;
		padding: none;
	}
	/* Statement section */
	.statement-section {
		text-align: left;
	}
	/* Projects Section  */
	.project-section {
		text-align: left;
	}
	/* Education Section */
	.education-section {
		text-align: left;
	}
	/* Experience Section */
	.experience-section {
		text-align: left;
	}
	/* Commitment Section */
	.commitments-section {
		text-align: left;
	}
</style>
