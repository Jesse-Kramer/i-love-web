<section>
    <ul>
        <li>
            <img src="../images/covers/Apricot Princess.png" alt="">
            <p>Apricot Princess</p>
            <p>Rex Orange County</p>
            <p>Number 1</p>
        </li>
        <li>
            <img src="../images/covers/Blonde.png" alt="">
            <p>Blonde</p>
            <p>Frank Ocean</p>
            <p>Number 2</p>
        </li>
        <li>
            <img src="../images/covers/Hypecondriac.png" alt="">
            <p>Hypecondriac</p>
            <p>Brakence</p>
            <p>Number 3</p>
        </li>
        <li>
            <img src="../images/covers/ICYMI.png" alt="">
            <p>ICYMI</p>
            <p>Eden</p>
            <p>Number 4</p>
        </li>
        <li>
            <img src="../images/covers/The Alexander Technique.png" alt="">
            <p>The Alexander Technique</p>
            <p>Rex Orange County</p>
            <p>Number 5</p>
        </li>
        <li>
            <img src="../images/covers/The First Time.png" alt="">
            <p>The First Time</p>
            <p>The Kid Laroi</p>
            <p>Number 6</p>
        </li>
        <li>
            <img src="../images/covers/Vertigo.png" alt="">
            <p>Vertigo</p>
            <p>Eden</p>
            <p>Number 7</p>
        </li>
    </ul>
    <button class="prevBtn" aria-label="Vorige slide">
        <img src="../images/icons/Arrow_left.svg" alt="">
    </button>
    <button class="nextBtn" aria-label="Volgende slide">
        <img src="../images/icons/Arrow_right.svg" alt="">
    </button>
</section>

<style>
    button {
        color: inherit;
        background-color: inherit;
        border: none;
    }

    /* Carousel Section */
	section ul {
		display: flex;
		overflow: auto;
		scroll-snap-type: x mandatory;
	}

	section li {
		margin-block: 2em;
		text-align: center;
		scroll-snap-align: center;
	}

	section li img {
        height: 400px;
        width: 400px;
        object-fit: cover;
	}

	/* Scrollbar Support */
	section.carousel ul::-webkit-scrollbar {
		display: none;
	}

	@supports (scrollbar-width: none) {
		section.carousel ul{
			scrollbar-width: none;
		}
	}
</style>