<template>
    <div class="page-footer">
        <p>© 2024 Designed by <a class="footer-name" href="https://github.com/MarSeventh" target="_blank">SanyueQi</a>
            <a :href="footerLink" target="_blank">
                <font-awesome-icon icon="paper-plane" class="footer-link-icon"/>
            </a>
            Modified by <a class="footer-name" href="https://blog.2000223.xyz/" target="_blank">LWind</a>
        </p>
    </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
    name: 'Footer',
    computed: {
        ...mapGetters(['userConfig']),
        footerLink() {
            return this.userConfig?.footerLink || 'https://sanyue.site'
        }
    }
}
</script>

<style scoped>
.page-footer {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100vw;
    color: rgb(66, 66, 66);
    font-size: large;
    user-select: none;
}
.footer-name {
    color: #409eff;
    font-weight: bold;
    text-decoration: none;
}
.footer-link-icon {
    color: #409EFF;
    margin-left: 5px;
}
</style>