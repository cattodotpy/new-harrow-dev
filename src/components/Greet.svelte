<script>
    export let name = "John Doe";

    // morning, afternoon, evening, night
    let timeOfDay = "morning";
    const currentHour = new Date().getHours();

    if (currentHour >= 12 && currentHour < 17) {
        timeOfDay = "afternoon";
    } else if (currentHour >= 17 && currentHour < 20) {
        timeOfDay = "evening";
    } else if (currentHour >= 20 || currentHour < 6) {
        timeOfDay = "night";
    }

    const greeting = `Good ${timeOfDay}`;
</script>

<h1 class="text-4xl font-extrabold tracking-tight sm:text-5xl md:text-6xl">
    <span class="block text-center">{greeting}!</span>
    <span class="block">I'm <span class="text-amber-200">{name}</span></span>
</h1>
