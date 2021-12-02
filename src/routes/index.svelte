<script>
	import { Lightbox, LightboxImage, LightboxGallery } from 'svelte-lightbox';
    import translations from '../translations.json';

    let language_toggle = "nl";
    let selectedTranslation = translations[0];

    function toggleLanguage() {
        if (language_toggle == "nl"){
            language_toggle = "de";
            selectedTranslation = translations[1];

        }
        else { 
            language_toggle = "nl";
            selectedTranslation = translations[0];
        }
    }
</script>

<div class="flex-container">
	<!-- <div class="navbar"> -->
		<div class="title">
			<h2>Hein Heijnen</h2>
		</div>
		<!-- <div class="menu">
			<a href="#books" id="booksbutton"><i class="material-icons">library_books</i> Boeken </a>
			<a href="#about" id="aboutbutton"><i class="material-icons">info</i> Auteur </a>
			<a href="#contact" id="contactbutton"><i class="material-icons">contact_mail</i> Contact </a>
		</div> -->
	<!-- </div> -->

	<div class="booknav">
		<h3>Toverdrankjes voor geluk</h3>

		<div class="books">
			<div class="image_div">
                <Lightbox>
                    <img src="images\Toverdrankjes.jpg" alt="Toverdrankjes">
                </Lightbox>
			</div>

			<p class="content">
				De bundel Toverdrankjes voor Geluk bevat 20 duetten, een samenspel van Hein Heijnen en Merik
				van der Torren. Elk duet bestaat uit een verhaal gevolgd door een passend gedicht. De sfeer
				is meestal opgewekt-weemoedig. In de meeste verhalen speelt de troost door muziek een rol.
				Volgens de filosoof Plato dringt niets zo diep door in het binnenste van de ziel als ritme
				en melodie. Hier en daar blinken vonkjes van tegendraadse humor, waarmee de schrijvers ons
				bijlichten op zoek naar identiteit en geluk.
				<br />
				<a href="https://www.bol.com/nl/p/toverdrankjes-voor-geluk/9200000081928113/"
					>Toverdrankjes voor geluk op bol.com <i class="material-icons">library_add</i></a
				>
			</p>
		</div>

		<div lang="nl" id="rokkade">
			<h3>{selectedTranslation.title}</h3>
			<button on:click={toggleLanguage}>
                {selectedTranslation.lang}
            </button>
			<br />
			<br />
			<div class="books">
				<div class="image_div">
                    <Lightbox>
                        <img src="images\{selectedTranslation.imageUrl}" alt={selectedTranslation.imageAlt}>
                    </Lightbox>
				</div>

				<p class="content">
					{selectedTranslation.content1}
					<br />
					<br />
					{selectedTranslation.content2}
					<br />
                    {#if selectedTranslation.storeUrl}
                    <a href={selectedTranslation.storeUrl}>{selectedTranslation.storeDescription}<i
                        class="material-icons">library_add</i></a>                                        
                    {:else}
                    <br />
                    {selectedTranslation.storeDescription}
                    {/if}                    
				</p>
			</div>
		</div>
	</div>

	<div class="about">
		<h3>Over de auteur</h3>
		Van jongs af aan ontmoette Hein Heijnen zonderlinge figuren in wie hij zich herkende. Liefdevol schetst
		hij ze in zijn flitsverhalen. Hij speelt iedere dag piano, ook in een trio dat de blues en songs
		uit The American Songbook brengt.In 2014 verscheen zijn schaakroman Rokade. Momenteel werkt Hein
		Heijnen aan een bundel korte verhalen.
	</div>

	<div class="contact">
		<h3>Contact</h3>
		E-mail: <a href="mailto:hein.vanderkroon@gmail.com">hein.vanderkroon@gmail.com</a>
	</div>
</div>
