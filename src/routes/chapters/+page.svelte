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
            frame: true, 
            downloadUrl: '/course-presentation-one.h5p',
        };

        new H5P(playerAnchor, options2);
    });
</script>

<h1>Welcome to Chapters</h1>
<div style="display: flex; gap: 8px">
    <a href="/">Home</a>
    <a href="/play">Play Page</a>
</div>


<div style="padding: 20px;">Please wait for content to load</div>

<div bind:this={playerAnchor} style="padding: 40px; margin-bottom: 16px; border: 1px solid;"></div>

