<section class="carousel" id="sectionCarousel" data-scroll-speed="2">
    <h2>Favourite Music</h2>
    <div class="carousel-sticky">
        <ul>
            <li>
                <img src="../images/covers/Apricot Princess.png" alt="Album Cover">
                <div class="album-info">
                    <p>APRICOT PRINCESS</p>
                    <p>REX ORANGE COUNTY</p>
                    <p>2017</p>
                </div>
            </li>
            <li>
                <img src="../images/covers/Blonde.png" alt="Album Cover">
                <div class="album-info">
                    <p>BLONDE</p>
                    <p>FRANK OCEAN</p>
                    <p>2016</p>
                </div>
            </li>
            <li>
                <img src="../images/covers/Hypecondriac.png" alt="Album Cover">
                <div class="album-info">
                    <p>HYPECONDRIAC</p>
                    <p>BRAKENCE</p>
                    <p>2019</p>
                </div>
            </li>
            <li>
                <img src="../images/covers/ICYMI.png" alt="Album Cover">
                <div class="album-info">
                    <p>ICYMI</p>
                    <p>EDEN</p>
                    <p>2021</p>
                </div>
            </li>
            <li>
                <img src="../images/covers/The Alexander Technique.png" alt="Album Cover">
                <div class="album-info">
                    <p>THE ALEXANDER TECHNIQUE</p>
                    <p>REX ORANGE COUNTY</p>
                    <p>2020</p>
                </div>
            </li>
            <li>
                <img src="../images/covers/The First Time.png" alt="Album Cover">
                <div class="album-info">
                    <p>THE FIRST TIME</p>
                    <p>THE KID LAROI</p>
                    <p>2021</p>
                </div>
            </li>
            <li>
                <img src="../images/covers/Vertigo.png" alt="Album Cover">
                <div class="album-info">
                    <p>VERTIGO</p>
                    <p>EDEN</p>
                    <p>2021</p>
                </div>
            </li>
        </ul>
    </div>
</section>

<style>
    /* Carousel Section */
    section.carousel h2 {
        font-size: 8em;
        font-weight: 300;
        max-width: 450px;
        margin-left: 1.5em;
    }

    /* Set up the section's height for scrolling */
    section.carousel {
        height: 300vh;
        overflow: visible;
        view-timeline-name: --carousel-timeline;
        view-timeline-axis: block;
    }

    /* Sticky Wrapper to hold the carousel in place */
    .carousel-sticky {
        position: sticky;
        top: 0;
        height: 100vh;
        width: 100vw;
        overflow-x: hidden;
    }

    /* Carousel ul styles */
    section.carousel ul {
        display: flex;
        width: 215vmax; /* Stretch horizontally to fit all items */
        height: 100vh;
        will-change: transform;
        animation: linear move forwards;
        animation-timeline: --carousel-timeline;
        animation-range: contain 0% contain 100%;
    }

    section.carousel li {
        list-style: none;
        flex: 0 0 30vw; /* Each item takes a portion of the viewport */
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;
    }

    section.carousel li img {
        height: 500px;
        width: 500px;
        object-fit: cover;
    }

    .album-info {
        color: white;
        padding: 20px;
        width: 100%;
    }

    .album-info p {
        margin: 10px 0;
        font-weight: bold;
        text-transform: uppercase;
        letter-spacing: 2px;
        font-size: 30px;
    }

    /* Scroll-driven animation */
    @keyframes move {
        to {
            transform: translateX(calc(-100% + 100vw));
        }
    }
</style>
