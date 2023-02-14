<template>
    <header class="header-block">
        <div class="header-wrapper">
            <div class="header-right">
                <img class="header__logo" src="@/assets/logo.svg" alt="logo">
                <nav class="header-menu">
                    <ul class="header-menu__list">
                        <li class="header-menu__item"><a href="">NavItem1</a></li>
                        <li class="header-menu__item"><a href="">NavItem2</a></li>
                        <li class="header-menu__item header-menu__item_selected"><a href="">NavItem3</a></li>
                    </ul>
                </nav>
            </div>
            <div class="header-left">
                <button class="header__button">Button</button>
            </div>
        </div>
    </header>
</template>

<script>

export default {
    name: 'Header'
}
</script>
