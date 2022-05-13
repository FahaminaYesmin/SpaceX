<script>
    let src = "/img/spacex-logo.jpg";
    let current = "home";
    // Burger menus
    document.addEventListener("DOMContentLoaded", function () {
        // open
        const burger = document.querySelectorAll(".navbar-burger");
        const menu = document.querySelectorAll(".navbar-menu");

        if (burger.length && menu.length) {
            for (var i = 0; i < burger.length; i++) {
                burger[i].addEventListener("click", function () {
                    for (var j = 0; j < menu.length; j++) {
                        menu[j].classList.toggle("hidden");
                    }
                });
            }
        }

        // close
        const close = document.querySelectorAll(".navbar-close");
        const backdrop = document.querySelectorAll(".navbar-backdrop");

        if (close.length) {
            for (var i = 0; i < close.length; i++) {
                close[i].addEventListener("click", function () {
                    for (var j = 0; j < menu.length; j++) {
                        menu[j].classList.toggle("hidden");
                    }
                });
            }
        }

        if (backdrop.length) {
            for (var i = 0; i < backdrop.length; i++) {
                backdrop[i].addEventListener("click", function () {
                    for (var j = 0; j < menu.length; j++) {
                        menu[j].classList.toggle("hidden");
                    }
                });
            }
        }
    });
</script>

<header class="fixed w-full top-0">
    <nav
        class="relative flex justify-between items-center bg-transparent w-11/12 m-auto"
    >
        <a class="text-3xl font-bold leading-none" href="#/">
            <img {src} alt="headerlogo" class="w-1/4" />
        </a>
        <div class="lg:hidden">
            <button class="navbar-burger flex items-center text-blue-600 p-3">
                <svg
                    class="block h-4 w-4 fill-current"
                    viewBox="0 0 20 20"
                    xmlns="http://www.w3.org/2000/svg"
                >
                    <title>Mobile menu</title>
                    <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
                </svg>
            </button>
        </div>
        <ul
            class="hidden justify-end w-full absolute top-1/2 left-1/2 transform -translate-y-1/2 -translate-x-1/2 lg:flex lg:mx-auto lg:flex lg:items-center lg:space-x-6"
        >
            <li>
                <a
                    href="#/"
                    class={current === "home" ? "selected" : ""}
                    on:click={() => (current = "home")}>Home</a
                >
            </li>
            <li>
                <a
                    href="#/company"
                    class={current === "company" ? "selected" : ""}
                    on:click={() => (current = "company")}
                    >Company Information</a
                >
            </li>

            <li>
                <a
                    href="#/launch"
                    class={current === "launch" ? "selected" : ""}
                    on:click={() => (current = "launch")}>Launch</a
                >
            </li>

            <li>
                <a
                    href="#/launch-pad"
                    class={current === "launchpad" ? "selected" : ""}
                    on:click={() => (current = "launchpad")}>Launch Pads</a
                >
            </li>
        </ul>
    </nav>
    <div class="navbar-menu relative z-50 hidden">
        <div class="navbar-backdrop fixed inset-0 bg-gray-800 opacity-25" />
        <nav
            class="fixed top-0 left-0 bottom-0 flex flex-col w-5/6 max-w-sm py-6 px-6 bg-black border-r overflow-y-auto"
        >
            <div class="flex items-center mb-8">
                <a class="mr-auto text-3xl font-bold leading-none" href="#/">
                    Logo
                </a>
                <button class="navbar-close">
                    <svg
                        class="h-6 w-6 text-gray-400 cursor-pointer hover:text-gray-500"
                        xmlns="http://www.w3.org/2000/svg"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke="currentColor"
                    >
                        <path
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            stroke-width="2"
                            d="M6 18L18 6M6 6l12 12"
                        />
                    </svg>
                </button>
            </div>
            <div>
                <ul>
                    <li class="mb-1">
                        <a
                            class="block p-4 text-sm font-semibold text-white-400 hover:bg-blue-50 hover:text-blue-600 rounded"
                            href="#/">Home 2</a
                        >
                    </li>
                    <li class="mb-1">
                        <a
                            class="block p-4 text-sm font-semibold text-gray-400 hover:bg-blue-50 hover:text-blue-600 rounded"
                            href="#/company">Company Information</a
                        >
                    </li>
                    <li class="mb-1">
                        <a
                            class="block p-4 text-sm font-semibold text-gray-400 hover:bg-blue-50 hover:text-blue-600 rounded"
                            href="#/launch">Launch</a
                        >
                    </li>
                    <li class="mb-1">
                        <a
                            class="block p-4 text-sm font-semibold text-gray-400 hover:bg-blue-50 hover:text-blue-600 rounded"
                            href="#/launch-pads">Launch Pads</a
                        >
                    </li>
                </ul>
            </div>
        </nav>
    </div>
</header>

<style>
    header a {
        color: #fff !important;
    }
    header li .selected {
        color: #ff3e00 !important;
    }
</style>
