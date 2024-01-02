<script>
    import SectionWrapper from "./SectionWrapper.svelte";
    let faqs = [
        {
            question: "What is web development?",
            ans: "Web development refers to the process of creating websites or web applications. It involves a combination of programming, design, and other technical skills to build and maintain functional and visually appealing websites that are accessible on the internet.",
        },
        {
            question: "What are the essential programming languages for web development?",
            ans: "The essential programming languages for web development include HTML (Hypertext Markup Language) for creating the structure and content of web pages, CSS (Cascading Style Sheets) for styling and layout, and JavaScript for adding interactivity and dynamic elements to websites. Additional languages and frameworks like Python, PHP, Ruby, and frameworks like React, Angular, or Django may also be used depending on the specific requirements.",
        },
        {
            question: "What are the differences between front-end and back-end web development?",
            ans: "Front-end web development focuses on creating the user interface and user experience of a website. It involves working with HTML, CSS, and JavaScript to design and implement the visual elements that users interact with directly. Back-end web development, on the other hand, involves server-side programming and database management. It handles tasks like server configuration, database integration, and server-side logic to ensure the proper functioning of a website.",
        },
        {
            question: "How do I start learning web development?",
            ans: "To start learning web development, you can begin by familiarizing yourself with HTML, CSS, and JavaScript. There are numerous online resources, tutorials, and courses available that can help you learn these languages. Practice by building simple web pages and gradually move on to more complex projects. It's also helpful to explore frameworks and libraries like Bootstrap or React to enhance your skills.",
        },
        {
            question: "What are some important skills for a web developer?",
            ans: "Important skills for a web developer include proficiency in HTML, CSS, and JavaScript, as well as knowledge of programming concepts and algorithms. Understanding responsive design, version control systems like Git, and familiarity with web development tools and frameworks are also beneficial. Additionally, problem-solving abilities, attention to detail, and continuous learning are essential traits for a successful web developer.",
        },
        {
            question: "What is the difference between a website and a web application?",
            ans: "A website typically consists of static web pages that provide information or content to visitors, while a web application is more interactive and dynamic. Web applications often have user accounts, databases, and more complex functionality, such as online shopping, social media platforms, or productivity tools.",
        },
        {
            question: "What is responsive web design?",
            ans: "Responsive web design is an approach to designing and building websites that ensure optimal viewing and interaction across various devices and screen sizes. It involves using flexible layouts, fluid grids, and media queries to adapt the content and design elements to fit different screen resolutions, enabling a seamless user experience on desktops, tablets, and mobile devices.",
        },
        {
            question: "What is the role of frameworks in web development?",
            ans: "Frameworks in web development provide pre-written code, libraries, and tools that help developers streamline the development process. They offer a foundation for building web applications, handle common tasks, and provide a structure that promotes code organization and maintainability. Examples of popular web development frameworks include Ruby on Rails, Django, Laravel, and Express.js.",
        },
        {
            question: "What is SEO, and why is it important for web development?",
            ans: "SEO, or Search Engine Optimization, refers to the practice of optimizing websites to rank higher in search engine results pages. It involves improving website performance, content quality, and adhering to certain technical requirements that search engines consider when determining rankings. SEO is crucial for web development as it helps increase organic traffic and visibility, making websites more discoverable to potential visitors.",
        },
        {
            question:
                "How can I make my website more secure?",
            ans: "Ensuring website security is essential to protect user data and prevent unauthorized access or attacks. Some best practices include using secure passwords, encrypting sensitive data, implementing user authentication and authorization mechanisms, keeping software and plugins up to date, performing regular security audits, and using SSL certificates to enable secure communication between the website and users.",
        },
    ];
</script>

<SectionWrapper id="faqs">
    <div
        class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
    >
        <div class="flex flex-col gap-2">
            <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
                For all your questions and queries
            </p>
            <h3
                class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
            >
                Frequently Asked Questions
            </h3>
        </div>
        <div class="flex flex-col gap-8 sm:gap-10 md:gap-14 w-full">
            {#each faqs as faq}
                <div
                    class="flex flex-col gap-2 text-left max-w-[800px] w-full mx-auto relative p-4 px-6"
                >
                    <div
                        class="absolute top-0 left-0 w-1/3 h-[1px] bg-slate-950 -translate-x-4"
                    ></div>
                    <div
                        class="absolute top-0 left-0 h-2/3 w-[1px] bg-slate-950 -translate-y-4"
                    ></div>
                    <h4 class="text-lg sm:text-xl md:text-2xl pt-2">
                        {faq.question}
                    </h4>
                    <p class="pl-2">{faq.ans}</p>
                </div>
            {/each}
        </div>
    </div>
</SectionWrapper>
