<template>
    <div class="footer">
        <p class="footer__text">© 2019 Elizabeth Setton. All Rights Reserved</p>
    </div>
</template>

<style lang="scss">
    // @import "@/styles/_variables.scss";
    // @import "@/styles/_mixins.scss";
    /////////// COLORS ///////////

$color-purple-light: #c9cfe5;
$color-purple-lighter: #a397b7;
$color-purple-dark: #a691b6;

$color-heading: #6f506f;

$color-border: 1px solid #c9cfe5;
$color-background: #f9f7f6;


/////////// TYPOGRAPHY ///////////

$font-size-smallest: 1rem;
$font-size-small: 1.3rem;
$font-size-medium2: 1.4rem;
$font-size-medium1: 1.6rem;
$font-size-big: 1.9rem;

/////////// GENERAL ///////////

$general-box-shadow: 0px 5px 8px 0px rgba(0, 0, 0, 0.14);
@mixin respond($breakpoint) {
    @if $breakpoint == phone-small {
        @media (max-width: 33.5em) {@content}; //540px
    }
    @if $breakpoint == phone-medium {
        @media (max-width: 38.5em) {@content}; //600px
    }
    @if $breakpoint == phone-big {
        @media (max-width: 43.8em) {@content}; //700px
    }
    @if $breakpoint == tab-port {
        @media (max-width: 56.25em) {@content}; //900px
    }
    @if $breakpoint == tab-land {
        @media (max-width: 75em) {@content}; //1200px
    }
    @if $breakpoint == big-desktop {
        @media (min-width: 112.5em) {@content}; //1800px
    }

}



    .footer {
        grid-column: 1 / 7;
        grid-row: 16 / 17;
        display: flex;
        background-color: $color-purple-light;
        color: $color-heading;
        justify-content: center;
        align-items: center;
        font-size: $font-size-small;

        &__text {
            padding: 0.7rem !important;

            @include respond(phone-small) {
                font-size: $font-size-smallest;
            }
        }
    }
</style>