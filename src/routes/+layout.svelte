<script lang="ts">
    import "../app.css";
</script>

<div class="bg-gray-400 text-white py-4">
    <nav>
        <ul class="flex justify-center gap-3">
            <li><a href="/">Home</a></li>
            <li><a href="/layout">layout</a></li>
        </ul>
    </nav>
</div>

<div class="p-5 border rounded my-5 mx-auto w-4/5">
    <slot />
</div>

<footer class="text-center text-white text-xl bg-purple-500 py-4">
    Footer
</footer>
