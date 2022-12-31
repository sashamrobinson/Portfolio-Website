<template>
    <div id="static">
        <header>
            <div>
                <HomeButton class="align homeButton"/>
            </div>
            <div>
                <MenuButton class="align menuButton"/>
                <MenuButtonIcon class="align menuButton" />
            </div>
        </header>
        <hr>
    </div>
</template>

<script>
import HomeButton from './HomeButton'
import MenuButton from './MenuButton'
import MenuButtonIcon from './MenuButtonIcon'

export default {
    name: 'Header',
    components: {
        HomeButton,
        MenuButton,
        MenuButtonIcon
    }
}
</script>

<style>
#static {
    position: sticky;
    top: 0;
}
header {
    display: flex;
    justify-content: space-between;
    align-items: center; 
}

hr {
    width: 99%;
    border: 0.025em solid white;
    opacity: 50%;
}
.align {
  display: inline-block;
  vertical-align: middle;
  padding: 0.5rem 1rem;
}

.homeButton {
    left: 2em;
    top: 2em;
}

.menuButton {
    right: 2em;
}

</style>