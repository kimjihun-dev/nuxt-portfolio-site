<template>
    <footer class="footer">
        <div class="footer_inner">
            <p>kimjihun &copy; 2020</p>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'AppFooter',
}
</script>

<style>
.footer { margin-top: 5%; background: #444; }
.footer_inner { width: 100%; height: 100px; text-align: center; line-height: 100px; }
.footer_inner p { color: #fff; font-size: 15px; }

@media (max-width: 1024px) {
    .footer { margin-top: 2%; }
}
</style>