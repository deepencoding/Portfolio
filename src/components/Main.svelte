<script>
    import Step from "./Step.svelte";
    let steps = [
        {name: 'Face-Clipper', icon: 'fa-solid fa-face-kiss-beam', href: 'https://github.com/deepencoding/Face-Clipper'},
        {name: 'PacAttack', icon: 'fa-solid fa-ghost', href: 'https://github.com/deepencoding/PacAttack'},
        {name: 'IndeXpress', icon: 'fa-solid fa-book-open-reader', href: 'https://github.com/deepencoding/IndeXpress'},
    ]
    let benefits = [
        {name: 'technically versatile', description:'I have experience building diverse software solutions, from developing a face detection pipeline for ML datasets to creating interactive graphics applications and efficient parsers, showcasing my adaptability and technical depth.'},
        {name: 'a performance-driven solver', description:'I focus on writing optimized code that enhances performance, such as improving system efficiency with concurrency, algorithmic enhancements, and effective design patterns.'},
        {name: 'adaptable, impactful and friendly!', description:'I quickly adapt to new technologies, consistently deliver meaningful contributions, and foster a positive, collaborative environment that helps teams thrive.'},
    ]
</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I am <span class="ebgaramound text-violet-400">Deepanshu</span><br/>Software
                <span class="ebgaramound text-violet-400">Engineer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-violet-400">favorite tech</span> includes C++ (GCC, CMake, SFML, DearImGui, OpenCV) and Rust!
            </p>
            <a class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-ls md:text-xl ebgaramound relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer" href="https://x.com/deepencoding" target="_blank">
                <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"></div>
                <h4 class="relative z-9">Get in touch &rarr;</h4>
            </a>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img src={"images/profile.png"} alt="A full moon" class="object-cover z-[2] max-h-[70vh]"/>
        </div>
    </section>

    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center ">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                A few of my creative Endeavors.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="ebgaramound text-violet-400">see</span> my work?
            </h3>
        </div>
        <!--TODO: Make videos to showcase here bro.
            <a href="#" target="_blank" class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover: border-violet-700 duration-200">
            <i class="fa-regular fa-circle-play"></i>
            <p>Watch the video</p>
        </a>-->
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>A <strong class="text-violet-400">GStreamer</strong> pipeline and <strong class="text-violet-400">OpenCV</strong>-based face detection system that efficiently processed MP4 videos, extracting over 10,000 frames in <strong class="text-violet-400">under 2 minutes</strong> and automating dataset preparation for machine learning.</p>
            </Step>
            <Step step={steps[1]}>
                <p>A Pac-Man-inspired game using <strong class="text-violet-400">SFML</strong> with collision detection, dynamic Ghost AI, and progressive scoring and much more.</p>
            </Step>
            <Step step={steps[2]}>
                <p>A concurrent word indexing application in <strong class="text-violet-400">C++</strong> that efficiently parses directories, processing <strong class="text-violet-400">over 1.1 Million</strong> characters in <strong class="text-violet-400">under 5 seconds</strong> using a custom thread pool.</p>
            </Step>
        </div>
    </section>
    <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4">
            <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="ebgaramound text-violet-400">about</span> me.
            </h3>
        </div>
        <p class="mx-auto ebgaramound font-semibold text-lg sm:text-xl md:text-2xl">I am . . .</p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                <div class="flex gap-6 sm:gap-8">
                    <p class="ebgaramound text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
                        0{index+1}
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
        <h5 class="text-2xl sm:text-3xl font-semibold text-center ebgaramound">Jack of all trades <strong class="text-violet-400 ebgaramound">(with mastery)</strong></h5>
        <p class="mx-auto ">SO WHY NOT INVEST?</p>
    </section>
</main>