<template>
    <header>
        <div class="navbar h-14 text-auto">
            <div class="navbar-start">
                <NuxtLink to="/"><img class="h-24" src="assets/images/Logo_2.png" /></NuxtLink>
            </div>
            <div class="navbar-end text-white gap-10 mr-5 p-5">
                <a href="#" @click="scrollToPortfolio">
                    <div
                        class=" hover:bg-orange-400 hover:bg-opacity-80 px-5 py-2 rounded-lg transition-all ease-in-out duration-200">
                        Portfolio</div>
                </a>
                <a href="#" @click="scrollToAbout">
                    <div
                        class=" hover:bg-orange-400 hover:bg-opacity-80 px-5 py-2 rounded-lg transition-all ease-in-out duration-200">
                        About</div>
                </a>

                <a href="#" @click="scrollToContact">
                    <div
                        class=" hover:bg-orange-400 hover:bg-opacity-80 px-5 py-2 rounded-lg transition-all ease-in-out duration-200">
                        Contact</div>
                </a>

            </div>
        </div>
    </header>
    <div>
        <slot />
    </div>

    <footer>
        <div class="bg-neutral text-white h-10 flex justify-center">
            <div class="flex justify-center items-center">
                <p class="text-secondary-content">© 2016-2024 Ashish Verma Photography. All rights reserved.</p>
            </div>
        </div>
    </footer>
</template>

<script setup>

const scrollToPortfolio = () => {
    const portfolioSection = document.getElementById('portfolio');
    if (portfolioSection) {
        portfolioSection.scrollIntoView({
            behavior: 'smooth',
        });
    }
};

const scrollToAbout = () => {
    const aboutSection = document.getElementById('sec-2');
    if (aboutSection) {
        aboutSection.scrollIntoView({
            behavior: 'smooth',
        });
    }
};

const scrollToContact = () => {
    const contactSection = document.getElementById('contact');
    if (contactSection) {
        contactSection.scrollIntoView({
            behavior: 'smooth',
        });
    }
};


</script>

<style scoped></style>