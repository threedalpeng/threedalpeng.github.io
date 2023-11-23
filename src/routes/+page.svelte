<script>
	import profile from '$lib/assets/profile.jpg';
	import githubmark from '$lib/assets/github-mark.svg';
</script>

<div class="bg-slate-50 flex flex-col p-8 gap-8 items-center">
	<div class="flex flex-row gap-8">
		<img
			class="h-40 aspect-square rounded-full object-cover object-center"
			src={profile}
			alt="My Profile"
		/>
		<div>
			<p>Hello! My name is</p>
			<p class="text-3xl font-bold">Kim Jeong-won</p>
			<p>I am a student at Sungkyunkwan University, and a software major.</p>
			<p>
				I'm interested in Frontend Architecture, AI-integrated Service, Computer Graphics, and
				VR/AR/MR
			</p>
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

	<div class="columns-1 md:columns-2 break-inside-avoid gap-4 px-16 py-4">
		<div class="card bg-base-100 shadow-lg inline-block w-full mb-4">
			<div class="card-body prose prose-sm prose-ul:list-disc prose-p:mb-0 prose-ul:mb-0">
				<h2 class="card-title">Skills</h2>
				<h3>Web and App Frontend Framework</h3>
				<ul>
					<li>Next.js (w. React), for many official web projects</li>
					<li>Vue, while working on ROK Air Force</li>
					<li>SvelteKit (w. Svelte), for many private projects, including this page!</li>
					<li>Jetpack Compose for Android</li>
				</ul>
				<h3>Computer Graphics & Metaverse Development</h3>
				<ul>
					<li>OpenGL & WebGL2</li>
					<li>Unity Game Engine</li>
					<li>Android ArCore</li>
				</ul>
				<p>I know basic concepts of backend and have experiences using...</p>
				<ul><li>Spring, Express(Node.js), FastAPI...</li></ul>
				<p>I also worked with some AI models like...</p>
				<ul><li>YOLO, BERT, NeRF... and other AI Services</li></ul>
			</div>
		</div>

		<div class="card bg-base-100 shadow-lg inline-block w-full mb-4">
			<div class="card-body prose prose-sm prose-ul:list-disc prose-p:mb-0 prose-ul:mb-0">
				<h2 class="card-title">Projects</h2>
				<ul>
					<li>
						Dalpeng(<a href="https://github.com/threedalpeng/dalpeng" target="_blank">Github Link</a
						>):<br /> Tried to implement core system of game engine, including: Game Loop, Entity-Component
						System, Linear Algebra math library, Physically Based Rendering, deferred rendering, modern-web-frontend-like
						Scripting features
					</li>
					<li>
						JazzyDalpeng(<a href="https://github.com/threedalpeng/JazzyDalpeng" target="_blank"
							>Github Link</a
						>):<br /> Working on progress! My practice helper for jazz guitar, using Svelte, HTML5 Canvas
						and some audio features features.
					</li>
				</ul>
				<p>I have lots of other works and if interested, please check out my Github!</p>
			</div>
		</div>

		<div class="card bg-base-100 shadow-lg inline-block w-full mb-4">
			<div class="card-body prose prose-sm prose-ul:list-disc prose-p:mb-0 prose-ul:mb-0">
				<h2 class="card-title">Education & Work</h2>
				<h3>Education</h3>
				<p>
					2019~: Sungkyunkwan University
					<br />participated in many program:
				</p>
				<ul class="mt-0">
					<li>Industry-University Cooperation</li>
					<li>SPARK</li>
					<li>Co-Deep Learning</li>
				</ul>
				<p>You can find my resources for presonal study:</p>
				<ul class="mt-0">
					<li><a href="/presentations">My Presentations</a></li>
					<li><a href="https://threedalpeng.com" target="_blank">My Blog Post(Not Published Yet..)</a></li>
				</ul>
				<h3>Work Experience</h3>
				<ul>
					<li>
						2021.09 ~ 2023.04: <br />
						대한민국 공군 정보체계관리단 소프트웨어개발병 복무
					</li>
				</ul>
			</div>
		</div>

		<div class="card bg-base-100 shadow-lg inline-block w-full mb-4">
			<div class="card-body prose prose-sm prose-ul:list-disc prose-p:mb-0 prose-ul:mb-0">
				<h2 class="card-title">Achievements and Certifications</h2>
				<h3>Achievements</h3>
				<ul>
					<li>2020.12: 과기부 주관 2020 솔직챌린지 공모전 우수상 수상</li>
				</ul>
				<h3>Certifications</h3>
				<ul>
					<li>2018.01: 900 TOEIC score</li>
				</ul>
			</div>
		</div>
	</div>
</div>
