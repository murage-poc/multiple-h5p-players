<script lang="ts">
    import { H5P } from "h5p-standalone"; // ES6

    let playerAnchor: HTMLDivElement;

    $effect(() => {
            const options2 = {
            h5pJsonPath: "/course-presentation-one",
            frameJs: "/vendor/h5p/frame.bundle.js",
            frameCss: "/vendor/h5p/styles/h5p.css",
            export: true,
            icon: true,
            downloadUrl: '/course-presentation-one.h5p',
        };

        new H5P(playerAnchor, options2);
    });
</script>

<h1>Welcome to Chapters</h1>
<a href="/">Home</a>

<a href="/play">Play Page</a>

<div bind:this={playerAnchor}></div>

