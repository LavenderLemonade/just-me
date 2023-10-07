<script>
    import Step from "./Step.svelte";
    import myPic from "../me.jpg";

    let steps = [
        {
            name: "Frog Chores App",
            icon: "fa-solid fa-frog",
            href: "https://github.com/LavenderLemonade/frog-chores",
        },
        {
            name: "Anime Girl API Practice",
            icon: "fa-solid fa-face-grin-hearts",
            href: "https://github.com/LavenderLemonade/waifu-page",
        },

        {
            name: "Portfolio Site",
            icon: "fa-solid fa-book-atlas",
            href: "#introPage",
        },
    ];

    let benefits = [
        {
            name: "growth-oriented",
            description:
                "Moving from Biomedical Engineering into Software Development was one of the biggest changes of my life, and one that I'm proud of. I love building things and helping people and coding lets me do that while exploring my creative side! ",
        },
        {
            name: "a lover of challenges",
            description:
                "What does JavaScript have in common with Monster Hunter? They're both hard to figure out without a guide. Fortunately, I love a good challenge, and I've never found a dragon I couldn't slay with the right amount of prep! ",
        },
        {
            name: "an enthusiastic collaborator",
            description:
                "I never shy away from group projects! If anything, I love being able to learn alongside other people. I'm big on asking questions, and bigger on maintaining effective communication.",
        },
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <section
        id="introPage"
        class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
    >
        <div
            class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md: gap-8 lg:gap-10"
        >
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-orange-400"> Sam </span>
                Elliott <br /> Full Stack
                <span class="poppins text-orange-400"> Developer!</span>
            </h2>
            <p class="text-base sm:text-lg mg:text-xl">
                My <span class="text-orange-400"> favorite languages </span> include
                JavaScript
            </p>

            <a
                href="https://www.linkedin.com/in/its-me-sam/"
                class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer"
            >
                <div
                    class="absolute top-0 right-full w-full h-full bg-orange-400 opacity-90 group-hover:translate-x-full z-0 duration-200"
                />
                <h4 class="relative z-9">Get in touch! &rarr;</h4></a
            >
        </div>

        <div class="relative shadow-2xl grid place-items-center">
            <!-- svelte-ignore a11y-img-redundant-alt -->
            <img
                src={myPic}
                alt="profile image"
                class="object-cover z-[2] max-h-[70vh"
            />
        </div>
    </section>

    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                A couple projects I've worked on!
            </h6>

            <h3 class="font-semibold text-3xl sm:text-4xl mg:text-5xl">
                Wanna see <span class="poppins text-orange-400"> what </span>
                I've been
                <span class="poppins text-orange-400"> working on? </span>
            </h3>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>
                    This is a simple app to ask if you've done your chores!
                    Prototyped with
                    <strong class="text-orange-400"> Figma </strong>
                    and built in
                    <strong class="text-orange-400"> React </strong>
                    as a way to get my feet wet!
                </p>
            </Step>

            <Step step={steps[1]}>
                <p>
                    This is an app that lets the user scroll through images of
                    anime girls! Utilizing
                    <strong class="text-orange-400"> Axios </strong>
                    to access the API and the page is built in
                    <strong class="text-orange-400"> React </strong>
                    as a fun learning project!
                </p>
            </Step>

            <Step step={steps[2]}>
                <p>
                    The very site you're looking at! I taught myself to use
                    <strong class="text-orange-400"> Sveltekit </strong>
                    as well as
                    <strong class="text-orange-400"> Tailwind CSS </strong>
                    to build this bad boy!
                </p>
            </Step>
        </div>
    </section>

    <section
        id="about"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
        <div
            class="flex flec-cop gap-2 text-center relative before:absolute before:top-0
        before:left-0 before:w-2/3 before:h-1.5 before:bg-orange-700 after:absolute
        after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-orange-700 py-4"
        >
            <h6 class="text-lg sm:-xl md:text-2xl">Wanna know more?</h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit
                <span class="poppins text-orange-400"> about </span>
                me.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
            I am. . .
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
        <h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">
            The <span class="text-orange-400 poppins"> Complete </span> Package!
        </h5>
        <div
            class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full"
        >
            <table class="bg-white text-slate-700 rounded text-center">
                <thead class="border-b border-solid border-slate-200">
                    <tr class="">
                        <th />
                        <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
                        <th
                            class="whitespace-nowrap bg-orange-700 text-white p-2 px-4"
                            >Me</th
                        >
                    </tr>
                </thead>
                <tbody>
                    <tr class="border-b border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                        >
                            Dedication</td
                        >
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>

                    <tr class="border-b border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                        >
                            Critical Thought</td
                        >
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>

                    <tr class="border-b border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                        >
                            Interpersonal Skills</td
                        >
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>

                    <tr class="border-b border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                        >
                            Coding Ability</td
                        >
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                </tbody>
            </table>
        </div>

        <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
            <p>Scroll to see more &rarr;</p>
        </div>

        <p class="mx-auto">So why not invest?</p>
    </section>
</main>
