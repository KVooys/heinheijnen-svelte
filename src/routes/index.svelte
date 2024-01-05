<script>
	import { Lightbox } from 'svelte-lightbox';
    import translations from '../translations.json';

    let language_toggle = "nl";
    let selectedTranslation = translations[0];
    let openAccordion = false;

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

    function toggleAccordion() {
        if (openAccordion) {
            openAccordion = false;
        }
        else {
            openAccordion = true;
        }
    }
</script>

<div class="flex-container">
    <div class="title">
        <h2>Hein Heijnen</h2>
    </div>

	<div class="booknav">
        <h3>Maanlichtverhalen</h3>                    
            <p>
                De auteur Hein Heijnen werkt aan een nieuwe bundel levensverhalen. Telkens één A-viertje. Daarin vindt vaak een ontmoeting plaats, die het alledaagse overschrijdt. <br />
                De titel is: 'Maanlichtverhalen'. De uitgever is Rinus van Warven te Kampen. De bundel verschijnt medio 2024 en is <a href="https://libris.nl/boek?authortitle=hein-heijnen/maanlichtverhalen--9789493288133#">hier</a> te reserveren. <br />
                Op vrijdag 16 februari 2024 is een feestelijke boekpresentatie in <a href="https://maps.app.goo.gl/p88Znhx1o743k8vu9">boekhandel Linnaeus</a> op de Middenweg in Amsterdam Watergraafsmeer, vanaf 18.00 tot circa 20.00 uur.  <br />
                <br />
                Een van deze verhalen is 'Weeshuis', welke hieronder te lezen is. <br />
                <button on:click={toggleAccordion}>{openAccordion ? "Sluit 'Weeshuis'": "Open 'Weeshuis'"}</button>
                {#if openAccordion}
                
                    <h4>Weeshuis</h4>
                    <p>
                    Bij mijn wandeling met een volle kinderwagen spreekt een jeugdig stel me aan op straat. Met haar
                    grote neus en haar lange piekhaar heeft zij wel iets van een heks. Hij lijkt een Italiaan of Griek door
                    zijn donkere krullenbol. Toch zie ik de volle maan al schemeren op zijn kruin.
                    In de kinderwagen zitten mijn twee geadopteerde jongetjes.
                    </p>
                    <p>
                    De feeks roept: ‘Jeetje. Wat een mooie kindertjes. Komen ze uit Zanzibar? <br />
                    Zij is al de vierde vragensteller van de dag. Deze donkere kindertjes hebben de aantrekkingskracht
                    van een achtbaan op de kermis.
                    </p>
                    <p>
                    Langzamerhand begin ik buikpijn te krijgen van alle aandacht. ‘Nee hoor,‘ zeg ik. ‘We haalden ze uit
                    een weeshuis in Stockholm.’ <br />
                    ‘Hé ?! Scandinavië ?’ <br />
                    ‘Ja. Destijds werd het schaap Dolly met veel succes gekloond. Nog wel uit haar eigen huidcellen. Dat
                    bracht de hoogleraar Romeo Strindberg op het idee iets dergelijks met mensen te gaan doen. Om
                    precies te zijn: hij wilde het materiaal van overleden genieën bewerken. Hij droomde ervan ze
                    postuum te kunnen klonen. Hun stoffelijke resten zijn de relieken van cultuurprofeten. Ze vormen
                    een brug tussen ons en deze grote geesten. Op allerlei begraafplaatsen en in diverse kerken slaagde
                    hij erin monsters van hun overblijfselen te nemen. ’
                    </p>
                    <p>
                    ‘Was het niet lastig om iets bruikbaars uit die resten te verkrijgen?’ vraagt ze praktisch. <br />
                    ‘Ja. Neem bijvoorbeeld Dimitri Sjostakovitsj. Bij nacht en ontij moest zijn kist heimelijk geopend
                    worden om zijn lichaamscellen eruit op te diepen.’
                    </p>
                    <p>
                    ‘Maar na zoveel jaar,’ blijft ze tegen werpen, ‘zal alles wel vergaan zijn, behalve de botresten.’<br />
                    ‘Dat valt enorm mee. Gelukkig vond de professor een revolutionaire methode om de huid van het
                    overschot weer op te peppen. Hij dompelt hem vierentwintig uur in een verjongingsbad van eigen
                    vinding. Tussen haakjes: eenmaal per jaar gaan hij en zijn medewerkers ook in dat bad zitten. Om
                    hun rimpelig uiterlijk en hun verlepte huid een shot van jeugd en frisheid toe te dienen. Hoe dan ook:
                    nu staat hij aan het hoofd van een weeshuis met gekloonde kinderen van hoogbegaafde mensen.’
                    ‘Aan wie moeten we dan denken ?’<br />
                    ‘Bijvoorbeeld aan Einstein, Picasso, Maria Callas. Alleen ingewijden weten van welk megatalent ze
                    afkomstig zijn.’
                    </p>
                    <p>
                    Ze wijst naar de kindertjes. ‘Mag ik vragen wie… – om zo te zeggen - hun ideële vader is ?’<br />
                    ‘Privacy hoor. Toch kan ik wel verklappen dat het om Nelson Mandela gaat. Deze jongens kunnen
                    beiden dromen over een loopbaan als grote vredestichters.’<br />
                    ‘Heeft deze gang van zaken niet een groot bezwaar? Ontstaat er door dat kloongedoe niet een
                    vaderloze maatschappij?’<br />
                    ‘Ach nee. Dat zou juist heel mooi zijn: hofmakerij en seks alleen voor je plezier.’<br />
                    Hierop beweert de heks met schelle stem dat draagmoeders altijd nodig zullen blijven.<br />
                    ‘Natuurlijk’ zeg ik lachend. ‘Zonder ons, vrouwen, zou het leven voor de gewone man een hel zijn.’
                    De twee druipen af. Gelukkig kon ik ze afschepen met een ter plekke verzonnen fantasieverhaal.
                    Even later komt mijn lieve vriendin aanlopen. Met een benieuwd gezicht vraagt ze wat ik dat
                    nieuwsgierige stel in hemelsnaam op de mouw heb gespeld.
                    </p><p>
                    ‘Waarom wil je dat weten?’<br />
                    ‘Die Italiaan sputterde dat hij nog nooit in zijn leven zo’n wartaal had gehoord. ‘Het is kukeleku,’
                    riep hij—tegen zijn voorhoofd tikkend.<br />
                    Toch wil ze zelfs het adres van een professor in Zweden aan je vragen. Ze snauwde hem toe: ‘Die
                    mediterrane genen van jou vertrouw ik voor geen cent.’                    
                    </p>
                {/if}
            </p>

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
                {selectedTranslation.lang == "Nederlands" ? "Deutsch" : "Nederlands"}
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
