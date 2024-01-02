<script>
    import ProductCard from "./ProductCard.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";
    let productFeatures = [
        {
            featureList: [
                "Select your Course",
                "Start Learning",
                "Complete Exercises",
                "Track your Progress",
            ],
            description:
                "Web Academy ensures all students have the information they need to learn skills and build web apps.",
            imgUrl: "assets/selection.png",
        },
        {
            featureList: [
                "Select your Course",
                "Start Learning",
                "Complete Exercises",
                "Track your Progress",
            ],
            description:
                "Build you skills and see your progress with our amazing tracking system.",
            imgUrl: "assets/training.png",
        },
        {
            featureList: [
                "Select your Course",
                "Start Learning",
                "Complete Exercises",
                "Track your Progress",
            ],
            description:
                "Learn as much information as you need to build blazing fast web apps according to clients needs",
            imgUrl: "assets/goal.png",
        },
    ];
</script>

<SectionWrapper id="product">
    <div
        class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14"
    >
        <div class="flex flex-col gap-2">
            <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
                Start your lifetime <span class="text-indigo-400"
                    >academy membership</span
                > today
            </p>
            <h3
                class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
            >
                Web For Everyone
            </h3>
        </div>

        {#each productFeatures as productFeature, index}
            <ProductCard {productFeature} {index}>
                {#if index === 0}
                    Experience a Web Dev <span
                        class="text-indigo-400 font-medium">master</span
                    > class
                {:else if index === 1}
                    Lay the foundations for <span
                        class="text-indigo-400 font-medium">modern</span
                    > Web Dev
                {:else}
                    Courses specific to modern <span
                        class="text-indigo-400 font-medium">Web Trends</span
                    >
                    and
                    <span class="text-indigo-400 font-medium">requirements</span>
                {/if}
            </ProductCard>
        {/each}
    </div>
</SectionWrapper>
