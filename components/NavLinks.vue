<template name="NavLinks">
    <div>
        <ul class="nav_links">
          <li>
            <a href="#hero">Home</a>
          </li>
          <li>
            <a href="#about-me">About me</a>
          </li>
          <li>
            <a href="#work">Work</a>
          </li>
        </ul>
    </div>
</template>
<script>
// JS
export default  {
    
}
</script>

<style lang="scss" scoped>
/* CSS */
@use '~/assets/variables' as *;
@import 'assets/mixins';

.nav_links {
        @media (max-width: 490px) {
            display: none;
        }

        li {
            list-style: none;
            display: inline;
            margin-left: 2.5rem;

            a {
                position: relative;
                
                text-decoration: none;
                color: #e5e5e5;
                font-weight: bold;
                @include transitionBack;

                &:hover{
                    text-shadow: 0 3px 5px $primary-color;
                }

                &::after {
                    content: '';
                    position: absolute;
                    top: 120%;
                    left: 50%;
                    transform: translate(-50%, -50%);
                    width: 0px;
                    height: 2.5px;

                    @include transitionBack;
                }

                &:hover::after {
                    background-color: $cta-color;
                    width: 75px;
                    top: 115%;
                    border-radius: 5px;
                }
            }
        }
    }


</style>