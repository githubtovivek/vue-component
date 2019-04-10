<template>
    <div class="row">
        <div class="col-xs-6">
            <div>
                <p>All Servers are managed here</p>
            </div>
        </div>
        <div class="col-xs-6">
            <app-footer-links>
                <div slot="contact">
                    <a >Contact US</a>
                </div>
                <div slot="media">
                    <a href="#">faceBook</a>
                    <a href="#">Twitter</a>
                </div>
            </app-footer-links>
        </div>
    </div>
</template>

<script>
import footerLinks from "./FooterLinks.vue";

export default {
  components: {
    "app-footer-links": footerLinks
  }
};
</script>

