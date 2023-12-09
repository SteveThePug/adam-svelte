<script>
    import { page } from "$app/stores";
</script>

<footer>
    <a href="https://github.com/SteveThePug" class="footer-link">SteveThePug</a>
</footer>

<style>
    footer {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100vw; /* Set the width to 100% */
        overflow: hidden;
    }
    .footer-link {
        padding: 10px;
        flex: 1;
        text-align: left;
        font-size: 3vh;
        color: white;
        font-variation-settings: "ELSH" 1;
        font-variation-settings: "ELSH" 2;
        font-variation-settings: "wght" 400;
        align-self: center;
        text-align: center;
    }
    .footer-link:hover {
        text-decoration: none;
        font-variation-settings: "ELSH" 15;
        font-variation-settings: "ELSH" 45;
        font-variation-settings: "wght" 800;
    }
</style>
