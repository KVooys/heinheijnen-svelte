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
                Geïnspireerd door A. L. Snijders werkt Hein Heijnen aan een nieuwe bundel korte verhalen. De titel luidt: Maanlichtverhalen.
                Onderstaande knop opent een voorproefje. <br /> 
                <button on:click={toggleAccordion}>'Uw naam?'</button>
                {#if openAccordion}
                <p>
                    Het groene licht floept van oranje op rood, juist als ik er langs fiets.  <br /> 
                    Even later houdt een agent mij aan. ‘Mijnheer. U reed net door rood.’<br /> 
                    ‘Dag agent. Het was zonet echt groen,’ jok ik.<br /> 
                    ‘Ja, dat zeggen ze allemaal’ gromt hij. Het is een warme zomerdag. Hij zet zijn helm af en hangt hem aan het stuur van zijn motor. Nu zie ik dat hij een peervormig hoofd heeft met een puntige kin en zware borstelwenkbrauwen. Hij lijkt op Bert, een figuur uit een stripverhaal voor kinderen.  Onheilspellend haalt hij een notitieboekje tevoorschijn en een pen. <br /> 
                    ‘Uw naam?’<br /> 
                    ‘Mijn grootvader was ook agent. Hij ving dieven en inbrekers  – vaak met levensgevaar.’<br /> 
                    ‘Uw naam?’<br /> 
                    ‘Zijn naam was Zeger Zuurjager. Hoofdagent A. U kent zijn naam natuurlijk.’    <br /> 
                    De agent klapt zijn boekje dicht. ‘Had dat dan meteen gezegd. Die naam is legendarisch in het korps.’
                    ‘Kent u ook het verhaal over de insluiper die men ‘Sinterklaas’ noemde?Telkens drong hij een huis in, via de dakkapel. Dan beroofde hij de bewoners.’<br /> 
                    Nadenkend houdt de agent zijn hoofd scheef. Hij meent van niet. <br /> 
                    ‘Mijn grootvader zag een verdachte figuur bij een huis naar boven klimmen.  Hij belde er aan. De bewoner liet hem binnen. In de dakkapel wachtte Zeger de Sint op en sloeg hem in de boeien.’ <br /> 
                    ‘Een sterk verhaal,’ zegt de agent. <br /> 
                    ‘En kent u soms de geschiedenis van  Huize Avondrood’? Het was  een huis van lichte zeden.’<br /> 
                    De agent wappert zich met zijn boekje koelte toe. ‘Hoe zat dat precies?’<br /> 
                    ‘Op een gegeven moment klopt er een huilend kind aan: Lorna. Een verwaarloosd weeskind zonder familie.  Liefdevol nemen de dames in dat verdorven tehuis haar onder hun hoede. Na een tijdje zien ze haar als hun eigen kind. U raadt het al. Uiteindelijk wordt het een onweerstaanbare jonge vrouw met hetzelfde beroep als haar verzorgsters.
                    Een labiele zeebonk verklaart haar zijn liefde. Zij zegt hem dat zij daar niet van gediend is. De man eist echter dat zij haar ambacht vaarwel zegt en zonder uitstel een nieuw leven begint. Samen met hem. Zij weigert weer. Door het dolle heen en vloekend bedreigt hij haar met een slagersmes. Gillend vlucht zij naar buiten. Achtervolgd door de woesteling. Het lijkt wel een opera. Ten einde raad springt zij de gracht in, hoewel zij niet kan zwemmen.
                    Toevallig komt mijn grootvader net voorbij. Hij ziet de achtervolging. Met blote handen ontwapent hij de messentrekker. Daarna redt hij Lorna van de verdrinkingsdood. De driftkikker is er zó van onder de indruk dat hij tot inkeer komt. Later sluit hij zich nederig bij het Leger des Heils aan.<br /> 
                    ´Vervolgens raakt mijn grootvader smoorverliefd op Lorna. Hij beschouwt haar vorige leven als een afgedane zaak en is met haar getrouwd. Zij werd mijn lieve grootmoeder.’<br /> 
                    ‘Een verhaal voor een succesfilm,’ zegt de agent.   <br /> 
                    ’En weet u wel waarom grootvader Zeger nooit bevorderd werd tot rechercheur?´<br /> 
                    Verbaasd schudt hij ‘nee’. <br /> 
                    ‘Eens liet hij de gevreesde hoofdcommissaris ongehinderd door een rood stoplicht rijden. Deze roept hem echter op het matje. Hij beschuldigt hem van hielenlikken en plichtverzaking.’<br /> 
                    Opeens zegt de agent met barse stem:  ‘Die fout ga ik niet maken.’ Hij slaat zijn boekje weer open. <br /> 
                    ‘Uw naam?’<br /> 
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
