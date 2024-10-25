<section class="carousel" id="sectionCarousel" data-scroll-speed="2">
    <h4>Favourite Music</h4>
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
                <img src="../images/covers/Hypechondriac.png" alt="Album Cover">
                <div class="album-info">
                    <p>HYPECHONDRIAC</p>
                    <p>BRAKENCE</p>
                    <p>2022</p>
                </div>
            </li>
            <li>
                <img src="../images/covers/ICYMI.png" alt="Album Cover">
                <div class="album-info">
                    <p>ICYMI</p>
                    <p>EDEN</p>
                    <p>2022</p>
                </div>
            </li>
            <li>
                <img src="../images/covers/The Alexander Technique.png" alt="Album Cover">
                <div class="album-info">
                    <p>THE ALEXANDER TECHNIQUE</p>
                    <p>REX ORANGE COUNTY</p>
                    <p>2024</p>
                </div>
            </li>
            <li>
                <img src="../images/covers/The First Time.png" alt="Album Cover">
                <div class="album-info">
                    <p>THE FIRST TIME</p>
                    <p>THE KID LAROI</p>
                    <p>2023</p>
                </div>
            </li>
            <li>
                <img src="../images/covers/Vertigo.png" alt="Album Cover">
                <div class="album-info">
                    <p>VERTIGO</p>
                    <p>EDEN</p>
                    <p>2018</p>
                </div>
            </li>
        </ul>
    </div>
</section>

<style>
    /* Carousel Section */
    section.carousel {
        margin-top: 10em;
    }
    
    section.carousel h4 {
        font-size: 8em;
        font-weight: 300;
        max-width: 450px;
    }

    /* Carousel ul styles */
    section.carousel ul {
        display: flex;
        overflow: scroll;
        scroll-snap-type: x mandatory;
    }

    section.carousel li {
        flex: 0 0 30vw;
        margin-block: 2em;
        text-align: center;
        scroll-snap-align: center;
    }

    section.carousel li img {
        height: 500px;
        width: 500px;
        object-fit: cover;
    }

    /* Carousel album styles */

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

    /* Mediq queries */
    @media screen and (max-width: 1750px) {
        .album-info p {
            font-size: 22.5px;
        }
        section.carousel li img {
            height: 400px;
            width: 400px;
            object-fit: cover;
        }
    }

    @media screen and (max-width: 1400px) {
        .album-info p {
            font-size: 15px;
        }
        section.carousel li img {
            height: 300px;
            width: 300px;
            object-fit: cover;
        }
    }

    @media screen and (max-width: 1100px) {
        .album-info p {
            font-size: 15px;
        }
        section.carousel li img {
            height: 250px;
            width: 250px;
            object-fit: cover;
        }
    }

    @media screen and (max-width: 900px) {
        .album-info p {
            font-size: 10px;
            letter-spacing: normal;
        }
        section.carousel li img {
            height: 200px;
            width: 200px;
            object-fit: cover;
        }

        section.carousel h4{
            font-size: 4em;
        }
    }

    @media screen and (max-width: 700px) {
        .album-info p {
            font-size: 10px;
        }
        section.carousel li img {
            height: 150px;
            width: 150px;
            object-fit: cover;
        }
    }

    @media screen and (max-width: 500px) {
        .album-info p {
            font-size: 10px;
            font-weight: 500;
            text-transform: none;
        }
        section.carousel li img {
            height: 125px;
            width: 125px;
            object-fit: cover;
        }
    }

    @media screen and (max-width: 450px) {
        section.carousel li img {
            height: 100px;
            width: 100px;
            object-fit: cover;
        }
    }

    /* Scroll-driven animation */
    @keyframes move {
        to {
            transform: translateX(calc(-100% + 100vw));
        }
    }

    @supports (animation-timeline: auto) {
        @media (prefers-reduced-motion: no-preference) {
            /* Set up the section's height for scrolling */
            section.carousel {
                height: 300vh;
                overflow: visible;
                view-timeline-name: --carousel-timeline;
                view-timeline-axis: block;
            }

            section.carousel h4 {
                margin-bottom: -18vh;
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
                width: 215vmax;
                height: 100vh;
                will-change: transform;
                animation: linear move forwards;
                animation-timeline: --carousel-timeline;
                animation-range: contain 10% contain 100%;
                overflow: auto;
                scroll-snap-type: none;
            }

            section.carousel li {
                list-style: none;
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: center;
                text-align: center;
            }

            @media screen and (max-width: 900px) {
                section.carousel ul {
                    width: 180vmax;
                }
            }

            @media screen and (max-width: 800px) {
                section.carousel ul {
                    width: 160vmax;
                }
            }

            @media screen and (max-width: 700px) {
                section.carousel ul {
                    width: 140vmax;
                }
            }

            @media screen and (max-width: 600px) {
                section.carousel ul {
                    width: 120vmax;
                }
            }

            @media screen and (max-width: 500px) {
                section.carousel ul {
                    width: 100vmax;
                }
            }
        }
    }
</style>
