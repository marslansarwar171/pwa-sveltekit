<script>
    import ReviewCard from "./ReviewCard.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";
    import Stars from "./Stars.svelte";

    let lim = true;

    let reviewsList = [
        {
            name: "John Doe",
            review: "I recently completed the HTML course at Web Academy, and it exceeded my expectations. The lessons were well-structured and easy to follow, with practical examples that helped me grasp the concepts quickly. The instructor's expertise and clear explanations made learning HTML a breeze. I highly recommend this course to anyone eager to dive into web development!",
            features: [
                "HTML",
                "CSS",
                "JavaScript",
            ],
        },
        {
            name: "Jane Smith",
            review: "The CSS course at Web Academy was fantastic! The content was comprehensive, covering both the basics and advanced techniques. The instructor's teaching style made complex concepts easy to understand. The hands-on exercises were invaluable in solidifying my understanding of CSS. I'm grateful for this course and can't wait to apply my newfound skills!",
            features: [
                "HTML",
                "CSS",
                "JavaScript",
            ],
        },
        {
            name: "Michael Brown",
            review: "I just completed the JavaScript course at Web Academy, and I'm thrilled with what I learned. The course provided a solid foundation in JavaScript, covering essential topics like variables, functions, and DOM manipulation. The instructor's explanations were clear and concise, and the coding exercises were challenging yet rewarding. I highly recommend this course to aspiring web developers!",
            features: [
                "HTML",
                "CSS",
                "JavaScript",
            ],
        },
        {
            name: "Sarah Williams",
            review: "The React course at Web Academy exceeded my expectations. The instructor's knowledge and teaching style were exceptional. The course covered React from the ground up, including components, state management, and routing. The hands-on projects were challenging but incredibly rewarding. I highly recommend this course to anyone looking to master React!",
            features: [
                "JavaScript",
                "React",
                "CSS",
            ],
        },
        {
            name: "David Lee",
            review: "I recently completed the Node.js course at Web Academy, and it was outstanding. The course covered everything from the basics to building full-fledged web applications. The instructor's explanations were clear, and the real-world examples helped me understand how to apply Node.js in practice. I'm grateful for this course and the skills it has given me.",
            features: [
                "JavaScript",
                "NodeJS",
                "Databases",
            ],
        },
        {
            name: "Ashley Johnson",
            review: "Web Academy's MongoDB course was exactly what I needed to learn this powerful NoSQL database. The course provided a comprehensive introduction to MongoDB, covering topics like data modeling, CRUD operations, and aggregation. The instructor's expertise and examples made the concepts easy to grasp. I highly recommend this course to anyone interested in MongoDB.",
            features: [
                "JavaScript",
                "NodeJS",
                "Databases",
            ],
        },
        {
            name: "Mark Robinson",
            review: "The course on PHP and MySQL was very informative and practical. The instructor taught me how to use PHP to create dynamic web pages and how to use MySQL to store and manipulate data. I learned how to build a web application that can handle user input, authentication, and database operations. This course is great for anyone who wants to learn how to create web applications using PHP and MySQL.",
            features: [
                "PHP",
                "MySQL",
                "Backend Development",
            ],
        },
    ];
</script>

<SectionWrapper id="reviews">
    <div
        class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
    >
        <div class="flex flex-col gap-2">
            <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
                Don't just take our word for it
            </p>
            <h3
                class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
            >
                See What <span class="text-indigo-400">Others</span> Have To Say
            </h3>
        </div>
        <div class="flex flex-col md:flex-row gap-8 w-fit mx-auto">
            <div class="flex flex-col gap-8">
                {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
                    <ReviewCard {reviewItem} left={true} {index} />
                {/each}
            </div>
            <div class="w-[1px] bg-slate-950 hidden md:flex"></div>
            <div class="flex flex-col gap-8">
                {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
                    <ReviewCard {reviewItem} {index} />
                {/each}
            </div>
        </div>
        <button on:click={() => (lim = !lim)} class="specialBtn">
            <p>{lim ? "Show More" : "Show Less"}</p>
        </button>
        <div class="flex flex-col gap-10">
            <p class="mx-auto text-lg sm:text-xl md:text-2xl font-semibold">
                Trusted by 2000+ Students
            </p>
            <Stars />
        </div>
    </div>
</SectionWrapper>
