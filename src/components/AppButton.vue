<template>
    <button
        :class="['button', { hovering: isHovering && showHoverEffect }]"
        :style="styleObject"
        @mouseover="isHovering = true"
        @mouseleave="isHovering = false"
    >
        <slot></slot>
    </button>
</template>

<script>
export default {
    name: "AppButton",
    props: {
        showShadow: {
            type: Boolean,
            default: true,
        },
        showHoverEffect: {
            type: Boolean,
            default: true,
        },
        minWidth: {
            type: String,
            default: "20rem",
        },
        fontSize: {
            type: String,
            default: "1.6rem",
        }
    },
    data() {
        return {
            styleObject: {
                boxShadow: this.showShadow
                    ? "0 13px 15px -13px rgb(150, 152, 166)"
                    : "",
                minWidth: this.minWidth,
                fontSize: this.fontSize,
            },
            isHovering: false,
        };
    },
};
</script>

<style lang="scss" scoped>
.button {
    font-family: "Be Vietnam", sans-serif;
    padding: 0 3.4rem;
    height: 5.5rem;
    border: none;
    border-radius: 3rem;
    outline: none;
    font-weight: 700;
    letter-spacing: 1px;
    color: rgba(255, 255, 255, 0.8);
    background: linear-gradient(to right, $green-lime, $cyan-bright);
    text-align: center;
    cursor: pointer;
    transition: background-color 0.3s, letter-spacing .3s;
    &.hovering {
        letter-spacing: 1.4px;
    }
}
</style>