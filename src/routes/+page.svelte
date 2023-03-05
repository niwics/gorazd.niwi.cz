<script>
    const year = new Date().getFullYear()

    const referenceWebs = {
        'https://www.iklubovna.cz': ['iklubovna', 'iKlubovna.cz', 'Children community website'],
        'http://www.niwi.cz': ['niwi', 'Niwi.cz', 'Author\'s personal website'],
        'https://geo.niwi.cz': ['geo', 'GEO symbols', 'Database of Czech geodetic symbols'],
        'https://www.spjf.cz': ['spjf', 'SPJF', 'Children organisation'],
        'https://www.dlouhodobka.cz': ['dlouhodobka', 'Dlouhodobky', 'Long-term games for children teams'],
        'http://obchod.spjf.cz': ['obchod', 'E-shop SPJF', 'SPJF organisation e-shop']
    }
</script>

<style>
    :global(body) {
        background-color: #333333;
        font-family: Arial, Helvetica, sans-serif;
        color: #CCCCCC;
    }

    #layout {
        margin: 0 auto;
        font-size: 15px;
    }

    #top {
        position: relative;
    }
    #top img {
        max-width: 100%;
        height: auto;
    }
    #top-box {
        position: absolute;
        top: 10%;
        right: 4%;
        text-align: center;
    }
    h1 {
        margin: 0 0 0.2em 0;
        padding: 0;
        font-size: 3.4em; /* fallback */
        font-size: 5.5vw;
        color: #ff9600;
        text-shadow: rgba(1, 1, 1, 0.45) 2px 2px 3px;
    }
    #top-box strong {
        font-size: 1.6em; /* fallback */
        font-size: 2.8vw;
        color: #333333;
    }

    a.links {
        position: absolute;
        padding: 0.3em 0.5em;
        font-size: 2.2em; /* fallback */
        font-size: 4.6vw;
        background-color: rgba(0, 0, 0, 0.33);
        text-decoration: none;
    }
    a.links:hover {
        background-color: rgba(0, 0, 0, 0.7);
    }
    #link-about {
        top: 55%;
        right: 4%;
    }
    #link-install {
        bottom: 10%;
        right: 4%;
    }
    #link-download {
        top: 55%;
        left: 4%;
    }
    #link-references {
        bottom: 10%;
        left: 4%;
    }

    #layout #mid-right, #layout #content.left-only {
    }

    #layout #content {
        line-height: 1.4em;
    }
    #layout #content-inner {
        min-height: 600px;
        padding: .5em 3em 2em 3em;
        background-color: rgba(0, 0, 0, 0.33);
    }

    #layout #footer {
        clear: both;
        padding: 8px;
        background-color: rgba(0, 0, 0, 0.1);
        color: #55a2ef;
    }
    #layout #footer {
        color: #777777;
    }
    #layout #footer a {
        color: #555555;
    }

    /* Style for small devices: right col on the bottom */
    @media (max-width: 440px) {
        #layout {
            width: 440px;
        }
    }
    /* Style for really huge devices: restrict max width */
    @media (min-width: 1200px) {
        #layout {
            width: 1200px;
        }
        h1 {
            font-size: 4.3em;
        }
        #top-box strong {
            font-size: 2.1em;
        }
        a.links {
            font-size: 3.5em;
        }
    }

    /*
    --
    Basic page elements
    --
    */
    h2 {
        margin: 1.3em 0 0.7em 0;
        padding-bottom: 0.2em;
        border-bottom: 2px dotted #555555;
        font-size: 2.25em;
        color: #c0eb3f;
    }

    a {
        color: #c0eb3f;
    }
    a:hover {
        color: white;
    }

    img {
        max-width: 100%;
        height: auto;
    }

    /* Forms */
    form.gsfb-form#generate-init fieldset {
        background-color: inherit;
    }
    form.gsfb-form#generate-init legend {
        color: white;
    }

    /* References */
    .reference-box {
        display: inline-block;
        width: 180px;
        height: 220px;
        margin: 1em;
        padding: 1em;
        border: 3px solid #2A2A2A;
        border-radius: 15px;
        line-height: 1.6em;
        text-align: center;
        vertical-align: top;
        text-decoration: none;
    }
    .reference-box:hover {
        background-color: #2A2A2A;
    }
    .reference-box h3 {
        height: 1.2em;
        margin: 0 0 0.5em 0;
        font-weight: bold;
    }
    .reference-box img {
        width: 150px;
    }
    .reference-box:hover img {
        -webkit-filter: drop-shadow(8px 4px 8px rgba(0,0,0,1.0));
        filter: drop-shadow(8px 4px 8px rgba(0,0,0,1.0));
    }

    .copyright {
        display: inline-block;
        vertical-align: middle;
    }
</style>

<div id="layout">
    <div id="top">
        <img src="/top.jpg" alt="Gorazd system landscape">
        <div id="top-box">
        <h1>Gorazd system</h1>
        <strong>Open-source PHP framework and <abbr title="Content Management System">CMS</abbr></strong>
        </div>
        <a href="#about" class="links" id="link-about">About</a>
        <a href="#installation" class="links" id="link-install">How to install</a>
        <a href="#references" class="links" id="link-references">References</a>
        <a href="#download" class="links" id="link-download">Download</a>
    </div>

    <h2 id="about">What is Gorazd System?</h2>
    PHP framework and CMS (Content Management System).

    <h2 id="installation">Installation</h2>
    <img src="/installation.png" alt="Installtion instructions">

    <h2 id="references">Which websites runs on Gorazd System?</h2>
    {#each Object.entries(referenceWebs) as [web, params]}
        <a href={web} class="reference-box">
            <h3>{params[1]}</h3>
            <img src="/references/{params[0]}.jpg" alt="Website homepage"><br>{params[2]}
        </a>
    {/each}
    <p>... and several smaller websites.</p>

    <h2 id="download">Download</h2>
    <a href="https://github.com/niwics">GitHub - niwics</a>

    <div id="footer">
        <div class="copyright">&copy; <a href="http://www.niwi.cz">niwi</a> {year} |
            <a href="http://gorazd.niwi.cz" title="Redakční systém Gorazd">RS Gorazd</a></div>
    </div>
</div>