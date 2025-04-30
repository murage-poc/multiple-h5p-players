<script lang="ts">
    import { H5P } from "h5p-standalone"; // ES6

    let player1Anchor: HTMLDivElement;
    let player2Anchor: HTMLDivElement;
    let player3Anchor: HTMLDivElement;

    $effect(() => {
        //first h5p
        const options = {
            h5pJsonPath: "/h5p-test",
            frameJs: "/vendor/h5p/frame.bundle.js",
            frameCss: "/vendor/h5p/styles/h5p.css",
            export: true,
            icon: true,
            frame: true,
            downloadUrl: "/h5p-test.h5p",
        };

        new H5P(player1Anchor, options);

        //second h5p
        const options2 = {
            h5pJsonPath: "/course-presentation-one",
            frameJs: "/vendor/h5p/frame.bundle.js",
            frameCss: "/vendor/h5p/styles/h5p.css",
            export: false,
        };

        new H5P(player2Anchor, options2);

        //third h5p
        const options3 = {
            h5pJsonPath: "/fill-in-the-blanks-837",
            frameJs: "/vendor/h5p/frame.bundle.js",
            frameCss: "/vendor/h5p/styles/h5p.css",
            export: true,
            frame: true, 
            downloadUrl: "/fill-in-the-blanks-837.h5p",
        };

        new H5P(player3Anchor, options3);
    });
</script>

<h1>Welcome to Play Page</h1>

<div style="display: flex; gap: 8px">
    <a href="/">Home</a>
    <a href="/chapters">Chapters</a>
</div>

<div style="padding: 20px;">Please wait for content to load</div>

<div bind:this={player1Anchor} style="padding: 40px; margin-bottom: 16px; border: 1px solid;"></div>
<div bind:this={player2Anchor} style="padding: 40px; margin-bottom: 16px; border: 1px solid;"></div>
<div bind:this={player3Anchor} style="padding: 40px; margin-bottom: 16px; border: 1px solid;"></div>
