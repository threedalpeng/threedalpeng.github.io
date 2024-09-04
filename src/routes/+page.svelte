<script>
	import profile from '$assets/profile.jpg';
	import githubmark from '$assets/github-mark.svg';
</script>

<div class="flex flex-col items-center gap-8 bg-slate-50 p-8">
	<div class="flex flex-row gap-8">
		<img
			class="aspect-auto h-40 rounded-full object-cover object-center"
			src={profile}
			alt="My Profile"
		/>
		<div>
			<p>Hello! My name is</p>
			<p class="text-3xl font-bold">Kim Jeong-won</p>
			<p>
				I am a undergraduate student in the Department of Computer Science and Engineering at
				Sungkyunkwan University.
			</p>
			<p>My interests include AI-integrated Services/Game, AI Agents, Computer Graphics, and XR</p>
			<h1 class="mt-2 font-semibold">Contact:</h1>
			<div>
				<a href="mailto:threedalpeng@gmail.com">
					<button class="btn btn-sm">📧 threedalpeng@gmail.com</button>
				</a>
				<a href="mailto:dalpengx3@g.skku.edu">
					<button class="btn btn-sm">📧 dalpengx3@g.skku.edu</button>
				</a>
				<a href="https://github.com/threedalpeng" target="_blank">
					<button class="btn btn-sm py-0">
						<img class="h-1/2" src={githubmark} alt="Github Logo" /> Github</button
					>
				</a>
			</div>
		</div>
	</div>

	<div class="w-[80ch] columns-1 break-inside-avoid gap-4 px-16 py-4 xl:w-[160ch] xl:columns-2">
		<div class="card mb-4 inline-block w-full bg-base-100 shadow-lg">
			<div
				class="card-body prose prose-sm w-full max-w-none prose-p:mb-0 prose-ul:my-0 prose-ul:list-disc"
			>
				<h2 class="card-title">Projects</h2>
				<h3>Team</h3>
				<p>
					<span class="font-semibold"
						>ShibaMarket : Interactive commodity trading game with LLM-based agents</span
					>
					<br />Team Leader | 2024.06 ~
				</p>
				<ul>
					<li>
						Now creating a game that utilizes LLM Agent's expressiveness and judgment for
						interactions with NPCs
					</li>
					<li>Targeting a launch by the end of 2024</li>
				</ul>
				<p>
					<span class="font-semibold"
						>RealBang : 3D room generation AI models and viewer based on Novel View Synthesis
					</span>
					<br />Team Member | 2023.05 ~ 2024.01
					<br />
					<a href="https://github.com/orgs/Real-Bang/repositories" target="_blank">Github Link</a>
				</p>
				<ul>
					<li>A project for Spark 11st and Co-Deep Learning</li>
					<li>
						Compared the performance metrics of the available NeRF and 3D Gaussian Splatting models
						for room-scanned videos
					</li>
					<li>Streamed the AI-rendered images from the server to a client viewer</li>
					<li>Awarded 2nd place(최우수상) in the Co-Deep Learning Project, SKKU</li>
				</ul>
				<p>
					<span class="font-semibold"
						>Automated Summarization and Authoring Assistant for Product Review Data</span
					>
					<br />Team member | 2020.12 ~ 2021.02
					<br />
					<a href="https://github.com/threedalpeng/skku-coop-GIT-GPT-SERVER" target="_blank"
						>Github Link (Webapp)</a
					>
				</p>
				<ul>
					<li>Industry-University Coop Project with Goodmorning Information Technology</li>
					<li>Finetuned KoBERT on cosmetics review data crawled from various review sites</li>
					<li>
						Developed a next-sentence suggestion feature based on the previous sentence and
						pre-entered words
					</li>
				</ul>
				<p>
					<span class="font-semibold"
						>PreVentra : AI-detected Virus Infection Prevention System</span
					>
					<br />Team member | 2020.04 ~ 2020.12
					<br /><a href="https://github.com/threedalpeng/2020-sw-skku-GIT" target="_blank"
						>Github Link (AI Server)</a
					>,
					<a href="https://github.com/threedalpeng/2020-sw-skku-GIT-server" target="_blank"
						>Github Link (Webapp)</a
					>
				</p>
				<ul>
					<li>Industry-University Coop Project with Goodmorning Information Technology</li>
					<li>Set up the system for training and inferencing using YOLOv4 model</li>
					<li>
						Processed real-time video streams and scheduled the conversion of recorded data into
						stats
					</li>
					<li>
						Awarded 3rd place(우수상) in the 2020 Sol·Jik Challenge, Ministry of Science and ICT
					</li>
				</ul>
				<p>
					<span class="font-semibold">Lecture Projects and Others</span>
				</p>
				<ul>
					<li>
						Speech Enhancement using AI and Improvement of its Baseline Performance, AI Project,
						SKKU, Spring 2024(<a
							href="https://github.com/skku-aiproject-team2/skku-aiproject-speech-enhancement"
							>Github</a
						>)
					</li>
					<li>
						CLab:U - Interactive Clab and Lab Search Service using RAG, Introduction to Software
						Engineering, SKKU, Spring 2024(<a
							href="https://github.com/orgs/SKKU-SWE-2024s-Team9/repositories">Github</a
						>)
					</li>
					<li>
						Designing a Remote Couple Messanger &lt;Dove&gt;, Introduction to Human-Computer
						Interaction, SKKU, Spring 2024
					</li>
					<li>
						SpaceSwim Game Development Project, Computer Graphics, SKKU, Spring 2021(<a
							href="https://github.com/threedalpeng/SKKU-2021-Spring-CG-T1">Github</a
						>)
					</li>
					<li>
						PACMAN Game Development Project, Java Programming Lab, SKKU, Spring 2020(<a
							href="https://github.com/threedalpeng/Pacman_Java">Github</a
						>)
					</li>
				</ul>
				<h3>Personal</h3>
				<p>
					<span class="font-semibold">jazzy-dalpeng</span> (<a
						href="https://github.com/threedalpeng/JazzyDalpeng"
						target="_blank">Github Link</a
					>, working on progress)
				</p>
				<ul>
					<li>Jazz Guitar practice helper</li>
					<li>Integrates and syncs a canvas renderer and an audio player loop</li>
					<li>Built using SvelteKit (w. Svelte5) and custom HTML5 Canvas library</li>
				</ul>
				<p>
					<span class="font-semibold">dalpeng</span> (<a
						href="https://github.com/threedalpeng/dalpeng"
						target="_blank">Github Link</a
					>)
				</p>
				<ul>
					<li>
						Implements core system of game engine, including: Game loop, Component system, Linear
						algebra math library, Physically based rendering, Deferred rendering...
					</li>
					<li>Designed modern-web-frontend-like scripting features</li>
					<li>Built using WebGL2 and TypeScript</li>
				</ul>
			</div>
		</div>

		<div class="card mb-4 inline-block w-full bg-base-100 shadow-lg">
			<div
				class="card-body prose prose-sm w-full max-w-none prose-p:mb-0 prose-ul:my-0 prose-ul:list-disc"
			>
				<h2 class="card-title">Education & Work</h2>
				<h3>Education</h3>
				<p>
					<span class="font-semibold">2019.03 ~ : Sungkyunkwan University</span>
				</p>
				<ul class="mt-0">
					<p class="mt-0">
						Major : <span class="font-medium">Computer Science and Engineering</span>
					</p>
					<p class="mt-0">Major GPA : <span class="font-medium">4.14 / 4.5</span></p>
				</ul>
				<p class="font-medium">Participated Programs</p>
				<ul class="mt-0">
					<li>Toy Project Supporting Program</li>
					<li>Sungkyun SW Mentoring</li>
					<li>Co-Deep Learning</li>
					<li>SPARK 11st</li>
					<li>Industry-University Cooperation</li>
				</ul>
				<p class="font-medium">Clubs</p>
				<ul class="mt-0">
					<li>Metaverse/XR Club MAV, joining as a committee member and a mentor, 2023 ~</li>
					<li>Algorithm/Problem Solving Club NPC, joined as a committee member, 2020 ~ 2021</li>
					<li>Classical Music Club Eumchiheon, 2019 ~</li>
				</ul>
				<p>You can find my resources for presonal study:</p>
				<ul class="mt-0">
					<li><a href="/presentations">My Presentations</a></li>
					<li>
						<a href="https://threedalpeng.com" target="_blank">My Blog Post(Not Published Yet..)</a>
					</li>
				</ul>
				<h3>Work Experience</h3>
				<p>
					<span class="font-semibold">2023.07 ~ 2023.09: MUTI</span>
				</p>
				<ul>
					<li>Interned as an Android app developer</li>
					<li>Developed an AR demo Android app, using Jetpack Compose and ArCore</li>
				</ul>
				<p>
					<span class="font-semibold">2021.09 ~ 2023.04: ROK Air Force</span>
				</p>
				<ul>
					<li>
						Served in Air Force Intelligence Information Systems Management Group as a software
						developer (대한민국 공군 정보체계관리단 소프트웨어개발병)
					</li>
					<li>
						Developed and managed multiple Air Force Intranet services, mainly using Spring,
						OracleDB, and Vue
					</li>
				</ul>
			</div>
		</div>

		<div class="card mb-4 inline-block w-full bg-base-100 shadow-lg">
			<div
				class="card-body prose prose-sm w-full max-w-none prose-p:mb-0 prose-ul:my-0 prose-ul:list-disc"
			>
				<h2 class="card-title">Achievements and Certifications</h2>
				<h3>Achievements</h3>
				<ul>
					<li>
						2024.01: <span class="font-semibold">2nd place(최우수상)</span> in Co-Deep Learning Project,
						SKKU
					</li>
					<li>
						2020.12: <span class="font-semibold">3rd place(우수상)</span> in the 2020 Sol·Jik Challenge,
						Ministry of Science and ICT(과기부 주관 2020 솔·직 챌린지)
					</li>
				</ul>
				<h3>Scholarships</h3>
				<ul>
					<li>2023 Fall: Co-Deep Learning</li>
				</ul>
				<h3>Certifications</h3>
				<ul>
					<li>2024.08: 960 TOEIC score</li>
				</ul>
			</div>
		</div>
		<div class="card mb-4 inline-block w-full bg-base-100 shadow-lg">
			<div
				class="card-body prose prose-sm w-full max-w-none prose-p:mb-0 prose-ul:my-0 prose-ul:list-disc"
			>
				<h2 class="card-title">Tech Skills</h2>
				<p><span class="font-semibold">Web/App Client</span></p>
				<ul>
					<li>Next.js (w. React), for many official web projects</li>
					<li>Vue, while working on ROK Air Force</li>
					<li>SvelteKit (w. Svelte), for many personal projects, including this page!</li>
					<li>Jetpack Compose for Android</li>
					<li>Unity for game development</li>
				</ul>
				<p><span class="font-semibold">Computer Graphics & XR</span></p>
				<ul>
					<li>OpenGL & WebGL2</li>
					<li>Android ArCore</li>
				</ul>
				<p>I know core concepts of backend and have experiences using...</p>
				<ul>
					<li>Spring, Express(Node.js), FastAPI...</li>
					<li>Oracle, MySQL, PostgreSQL...</li>
				</ul>
				<p>I also worked with some AI models or services</p>
				<ul>
					<li>Utilized YOLO, BERT, NeRF, 3D Gaussian Splatting...</li>
					<li>Integrated systems with ChatGPT and MidJourney</li>
				</ul>
			</div>
		</div>
	</div>
</div>
