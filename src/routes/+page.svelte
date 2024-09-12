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
        <div class="books">
            <div class="image_div">
                <Lightbox>
                    <img src="images\Maanlichtverhalen.jpg" alt="Maanlichtverhalen">
                </Lightbox>
            </div>

            <p class="content">
                De bundel Maanlichtverhalen brengt u in een doolhof van ontmoetingen in clair-obscur.
                Maanlichtverhalen ontstaan meestal 's nachts. Een maanlichtverhaal beschrijft een ontmoeting met
                iemand die een wonderlijke ervaring heeft meegemaakt. De beleving van zo'n ontmoeting kan een
                gevoel oproepen dat het te maken heeft met een engel uit een andere dimensie. En dat de meeste
                verhalen in deze bundel goed aflopen, is een wonder op zich. Want zonneschijn is in het leven vaak
                op de bon.
                <br />
                <br />
                Bij de verwikkelingen die zich ontvouwen, speelt nu eens de invloed van een droom een rol, dan
                weer de hulp van intuïtie. Soms schiet de muze van het toeval te hulp. Al lezend dringt tot je door: er
                bestaat meer dan denken en voelen. Al sinds de Steentijd gebruikt de mens de vuistbijl van
                verbeeldingskracht en fantasie, om te overleven in de chaos. Beklemmend geeft veel eigentijdse
                literatuur ons een blik in een Beerput van narigheid en ellende. Hij wil laten zien dat de mens meer is
                dan een automaat. Met z'n vertelsels probeert auteur Hein Heijnen het kalf tijdig uit de put te halen -
                vóór het is verdronken.
                <br />
                <br />
                Een van de verhalen in Maanlichtverhalen is 'Kus des Doods', welke hieronder te lezen is. <br />
                <button on:click={toggleAccordion}>{openAccordion ? "Sluit 'Kus des Doods'": "Open 'Kus des Doods'"}</button>
                {#if openAccordion}
                
                    <h4>Kus des Doods</h4>
                    <p>
                        Hijgend komt een oude man naast me op het bankje zitten. Met het zweet op zijn voorhoofd zegt hij:
                        ‘Hier krijgt u mij voorlopig niet meer weg.’
                        ‘Leuk,’ zeg ik. ‘U ziet er uit of u heel wat mooie verhalen kunt vertellen.’
                        Hij legt zijn stok neer en zegt: ‘U vleit me. Als u het goed vindt vertel ik u een waar gebeurd drama
                        over mijn grootvader. Het is nog uit de vorige eeuw.’
                        ‘ik luister graag naar u,’antwoord ik.
                    </p>
                    <p>
                        Destijds werden zijn broer Joost en hij opgevoed door hun grootouders, begint hij. We hielden ons
                        echter vaak niet aan hun advies. De vloek van het ouderlijk gezag is dat het te laat wordt erkend.
                        In die tijd was zijn grootvader onderwijzer in Heerlen. De steenkoolmijn was nog vol in bedrijf. Op
                        een dag vertelde hij ons, zijn kleinzoons, een ervaring die hem zijn hele leven bijbleef:
                    </p>
                    <p>
                        Als jonge man wandelt hij op een doordeweekse dag naar de school waar hij lesgeeft. Net als nu is
                        het een mooie dag met zonnig weer. Iedereen draagt kleurrijke lichte kleding. Vaker dan anders
                        groeten onbekenden elkaar op straat. Met een glimlach en een wens. 
                    </p>
                    <p> 
                        Verder lopend ziet hij opeens een zestal paarden. Op een kluitje bij elkaar. Oude deels grijze dieren
                        bij wie de huid niet meer zo glanst. Afgeleefd, zo u wilt. Het valt hem op dat ze niet -- zoals anders--
                        mistroostig en geduldig blijven stilstaan. Door hun lijven gaan kleine schokjes. Ze wiegen heen en
                        weer. Ze huppelen en springen. Ze maken kleine danspasjes op de plaats. Deze paarden verheugen
                        zich ergens over. Ze zijn blij.
                    </p>
                    <p>
                        Met een schok dringt het tot mijn grootvader door waarover. Deze dieren hebben talloze lorries
                        met kolen door de gangen van de mijn gesleept. Verdoemd tot leven in het schemerduister. Vandaag
                        zijn ze uitgelaten vrolijk. Na jaren zijn ze voor het eerst weer boven de grond. Ze kunnen er niet stil
                        van blijven staan. Vol vreugde begroeten ze het licht van de zon.
                    </p>
                    <p>
                        Als mijn grootvader hun joligheid ziet, springen hem de tranen in de ogen. Dit zonlicht betekent
                        voor hen een kus des Doods. Morgen moeten ze naar de slacht. Bij het aanvoelen van hun dwaze
                        vrolijkheid begrijpt hij in een flits dat deze edele dieren ook gevoelens, emoties en pijn kunnen
                        ervaren—evenals wijzelf. Volgens hem hebben ze ook gevoel voor humor.
                    </p>
                    <p>
                        Op deze dag besluit mijn grootvader de overstap naar het vegetarisme te maken. Zijn hele verdere
                        leven at hij geen vlees of vis meer. Hij werd heel oud. Ach, mijnheer, u kunt vast begrijpen hoe wreed
                        sommige kinderen kunnen zijn. Destijds hadden Joost en ik moeite met dit ons opgedrongen
                        eetpatroon. Onze grootouders konden ons de oren van het hoofd kletsen, hoog springen, laag
                        springen—wij wilden vlees. In die tijd gingen we vaak mee-eten bij vrienden en kennissen. Eenmaal
                        uit huis hebben we de schade behoorlijk ingehaald.
                    </p>
                    <p>
                        Pas jaren later kwam het in de mode om slechts enkele dagen per week vlees te eten. Of zelfs
                        helemaal niet meer. Ook om paarden en koeien eervol met pensioen te sturen. Met verbazing en
                        spijt dacht hij toen bij mezelf: “Achteraf had mijn grootvader toch gelijk.”’ Opnieuw die vloek van het
                        ouderlijk gezag, weet je wel.         
                    </p>
                    <p>
                        Opeens kijkt de oude man op zijn horloge. Met de woorden dat hij naar een afspraak moet hier
                        dichtbij, pakt hij zijn stok en staat op. Bij het weglopen groet hij me en zegt: ‘Geloof me.
                        Paardenbiefstuk liet ik altijd liggen. Wegens hun gevoel voor humor.’ 
                    </p>
                    
                {/if}
                <br />
                <a href="https://libris.nl/a/hein-heijnen/maanlichtverhalen/501502880?#paperback-9789493288133"
                    >Maanlichtverhalen bij Libris <i class="material-icons">library_add</i></a
                >
            </p>
        </div>

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
