<script>
export default {
    name: 'swiper-item',
    render() {
        return this.$slots.default[0]
    },
    mounted() {
        this.$el.classList.add('swiper-slide')
    }
}
</script>