<script lang="ts">
    import Step from "./Step.svelte";

    let steps = [
        {
            href: "https://github.com/Harshal-dl/Portfolio",
            name: "Portfolio Website ",
            icon: "fa-solid fa-address-card",
        },
        {
            href: "https://github.com/Harshal-dl/Movie-Recommendation-System",
            name: " Popcornflix ",
            icon: "fa-solid fa-video",
        },
        {
            href: "https://github.com/Harshal-dl/Encodec",
            name: "Encodec ",
            icon: "fa-solid fa-file-circle-question",
        },
    ];

    let benefits = [
        {
            name: "a self taught developer",
            description:
                "I taught myself to code using free online resources and absolutely fell in love with the creativity and problem solving that is involved in developing and engineering innovative new online experiences. Starting of with JavaScript, HTML & CSS and evolving my knowledge base to include JavaScript frameworks, backend programming, design, cloud services and much much more.",
        },
        {
            name: "a product design & UX finatic",
            description:
                "Carefully crafting and designing amazing user experiences allows me to express and experiment with every morsel of creativity I have. I love the challenge of learning new design concepts and enabling users with amazing online experiences.",
        },
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <section
        id="introPage"
        class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
    >
        <div
            class="flex flex-col lg:justify-centre text-center lg-text-left gap-6 md:gap-8
            lg:gap-10"
        >
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-violet-400"
                    >Harshal
                </span>Lokhande
                <br />Full Stack
                <span class="poppins text-violet-400">Developer</span>
            </h2>

            <p class="text-base sm:text-lg md:text-xl">
                I am a passionate web developer with a strong foundation in data
                structures and algorithms using C++. I specialize in building
                dynamic and responsive web applications using React.js for the
                frontend and Node.js with Express.js for the backend. My
                expertise extends to database management with SQL (MySQL) and
                NoSQL (MongoDB) databases, allowing me to create robust and
                scalable applications. I am eager to expand my expertise by
                embracing new technology stacks.
            </p>
            <a
                class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-lg md:text-xl poppins
            relative overflow-hidden px-6 py-3 group rounded-full bg-white
            text-slate-950 cursor-pointer"
                href="https://www.linkedin.com/in/harshal-dl76/"
                target="_blank"
            >
                <div
                    class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20
            group-hover:translate-x-full z-0 duration-200"
                ></div>
                <h4 class="relative z-9">Get in touch &rarr;</h4>
            </a>
        </div>
        <div
            class="relative shadow-2xl grid place-items-center p-4 lg:self-center"
        >
            <img
                src="images/profile.png"
                alt="profile image"
                class="object-cover z-[2] w-64 h-64 sm:w-72 sm:h-72 md:w-80 md:h-80 rounded-full -mt-4 sm:-mt-6 md:-mt-8"
            />
        </div>
    </section>

    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text-2xl">
                A few of my creative endeavors.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-violet-400"> see</span> my work
                ?
            </h3>
        </div>
        <!-- <a
            href="https://www.youtube.com/watch?v=dQw4w9WgXcQ"
            target="_blank"
            class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200"
        >
            <i class="fa-regular fa-circle-play" />
            <p>Watch the video</p>
        </a> -->
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>
                    Portfolio website created with <strong
                        class="text-violet-400"
                        >SvelteKit & TailwindCSS!
                    </strong> Svelte is used to design the user interface and TailwindCSS
                    is used for the styling of the components.
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>
                    Popcornflix a movie recommender system build on <strong
                        class="text-violet-400"
                        >Jupyter Notebook!
                    </strong> Scikit-learn & TensorFlow are used to train machine
                    learning model. For frontend Html, Css and javascript are used
                </p>
            </Step>
            <Step step={steps[2]}>
                <p>
                    Encodec the file compressor build with <strong
                        class="text-violet-400"
                        >Html, Css & JavaScript!
                    </strong> Basic text file encoder and decoder demonstrating the huffman algorithm.
                    Only apllicable for file with .txt extention. 
                </p>
            </Step>

            <!-- <Step step={steps[2]}></Step> -->
        </div>
    </section>

    <section
        id="about"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16
    sm:gap-20 md:gap-24 relative"
    >
        <div
            class="flex flex-col gap-2 text-center relative
            before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute
            after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
        >
            <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-violet-400"> about</span> me
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
            I am . . .
        </p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                <div class="flex gap-6 sm:gap-8">
                    <p
                        class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500
                    font-semibold"
                    >
                        0{index + 1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">
                            {benefit.name}
                        </h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
    </section>
</main>
