<script lang="ts">
    import { H5P } from "h5p-standalone"; // ES6

    let player1Anchor: HTMLDivElement;
    let player2Anchor: HTMLDivElement;

    $effect(() => {
        //first h5p
        const options = {
            id: "po",
            h5pJsonPath: "/h5p-test",
            frameJs: "/vendor/h5p/frame.bundle.js",
            frameCss: "/vendor/h5p/styles/h5p.css",
            export: true,
            icon: true,
            downloadUrl: "/h5p-test.h5p",
        };

        new H5P(player1Anchor, options);

        //second h5p
        const options2 = {
            id: "some",
            h5pJsonPath: "/course-presentation-one",
            frameJs: "/vendor/h5p/frame.bundle.js",
            frameCss: "/vendor/h5p/styles/h5p.css",
            export: false,
        };

        new H5P(player2Anchor, options2);
    });
</script>

<h1>Welcome to Play Page</h1>

<a href="/">Home</a>

<a href="/chapters">Chapters</a>

<div bind:this={player1Anchor}></div>
<div bind:this={player2Anchor}></div>
