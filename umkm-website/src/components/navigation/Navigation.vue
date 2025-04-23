<script>
export default {
    data () {
        return {
            showNavbar: true,
            lastScrollPosition: 0
        }
    },
    mounted () {
        window.addEventListener('scroll', this.onScroll)
    },
    beforeDestroy () {
        window.removeEventListener('scroll', this.onScroll)
    },
    methods: {
        onScroll () {
            const currentScrollPosition = window.pageYOffset || document.documentElement.scrollTop
            if (currentScrollPosition < 0) {
                return
            }
            
            if (Math.abs(currentScrollPosition - this.lastScrollPosition) < 60) {
                return
            }
            this.showNavbar = currentScrollPosition < this.lastScrollPosition
            this.lastScrollPosition = currentScrollPosition
        }
    }
}
</script>

<template>
    <header class="flex justify-center items-center w-full h-[66px] top-0 fixed">
        <nav v-if="showNavbar" class="navbar border-b-4 border-gray-100 w-full h-full bg-white flex justify-around items-center" :class="{ 'navbar--hidden': !showNavbar }">
            <div class="menu flex justify-center items-center">
                <div class="flex justify-center items-center mr-[70px]">
                    <img src="../../assets/image 13.png" alt="brand" width="42px" height="42px">
                </div>
                    <li class="flex justify-between items-center gap-4">
                        <a href="#">Home</a>
                        <a href="#">About</a>
                        <a href="#">Menu</a>
                        <a href="#">Contact</a>
                    </li>
            </div>
            <div class="flex justify-between items-center">
                <form class="w-[200px] h-[35px]">
                    <div>
                        <input
                            placeholder="Search..."
                            type="text" 
                            name="text"
                            autocomplete="off"
                            id="search-input"
                            class="w-[200px] h-[35px] bg-none p-4 rounded-3xl outline" 
                        />
                    </div>
                </form>
                <div class="flex justify-center items-center ml-4">
                    <a href="#" class="flex gap-1">
                        <span class="font-bold text-[#704FE6]">EN</span>
                        <span class="font-bold text-[#704FE6]">|</span>
                        <span class="font-bold text-[#704fe66f]">IDN</span>
                    </a>
                </div>
            </div>
        </nav>
    </header>
</template>