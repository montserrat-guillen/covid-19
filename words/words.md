<div class="section">
    <div>
    	<iframe id="splash" width="960" height="480" src="banners/splash.html"></iframe>
        <div style="top: 70px;font-size: 75px;font-weight: bold;">
        	I ara què passarà?
       	</div>
		<div style="font-weight: 500;top: 140px;left: 10px;font-size: 29px;">
			El futur del COVID-19 explicat amb Simulacions Interactives
		</div>
		<div style="font-weight: 100;top: 189px;left: 10px;font-size: 19px;line-height: 21px;">
			<b>
				🕐 30 min veure/llegir
				&nbsp;&middot;&nbsp;
			</b>
			by
			<a href="https://scholar.google.com/citations?user=_wHMGkUAAAAJ&amp;hl=en">Marcel Salathé</a>
			(epidemiòleg)
			&
			<a href="https://ncase.me/">Nicky Case</a>
			(art/codi)
		</div>
	</div>
</div>

"Només cal tenir por a la por mateixa". Consell per tontos.

És clar, potser que no acumulem paper de WC - però si els polítics tenen por a la por, tendiran a minitmitzar els perills reals per a evitar la "histèria col·lectiva". La por no és el problema, sinó com "canalitzem" aquesta por. La por ens dona energia per a afrontar el perills actuals i preparar-nos per als què vindran.

Honradament, nosaltres (Marcel, epidemiòleg + Nicky, art/codi) estem preocupats. I pensem que tu també!. Per això hem decidit posar-nos a canalitzar la nostra por a través d'aquestes **simulacions interactives**,  i fer que *tu* transformis la por en coneixement:

* **Els Darrers Mesos** (epidemiologia bàsica,  model SEIR, R & R<sub>0</sub>)
* **Els Pròxims Mesos** (confinaments, seguiment de contactes, mascaretes)
* **Els Pròxims Anys** (pèrdua de la inmunitat? cap vacuna?)

L'objectiu d'aquesta guia (publicada el dia 1 de Maig de 2020, clica aquesta nota a peu de página!→[^timestamp]) és donar-te esperança *i* fer-te agafar por. Per a guanyar el COVID-19 **d'una forma que també protegim la nostra salut mental i financera**, necessitem optimisme per a dissenyar plans, i pessimisme per a idear un pla B. Com va dir un cop Gladys Bronwyn Stern, *“L'optimista inventa l'avió i el pessimista el paracaigudes.”*

[^timestamp]: Aquestes notes a peu de pàgina contenen referències, links i commentaris extres. Com aquest!
    
    **Aquesta guia va ser publicada el dia 1 de maig de 2020.** Hi ha molts detalls que quedaran obsolets, però tenim confiança que cobreix el 95% dels possibles escenaris futurs, i que l'epidemiologia bàsica sempre serà útil.

Per tant, corda't el cinturó, que s'acosten turbulències!

<div class="section chapter">
    <div>
		<img src="banners/curve.png" height=480 style="position: absolute;"/>
        <div>The Last Few Months</div>
    </div>
</div>

Els pilots utilitzen simuladors per evitar que s'estrellin els avions.

**Els epidemiòlegs utilitzen simuladors per evitar que s'estrelli la humanitat.**

Per tant, fem primer un "simulador de vol per epidèmies" que sigui molt, *molt* senzill. En aquesta simulació les <icon i></icon> persones infeccioses poden tranformar les <icon s></icon> persones susceptibles en més <icon i></icon> persones infeccioses:

![](pics/spread.png)

S'estima que, *al principi* de l'esclat del COVID-19, el virus salta d'un <icon i></icon> a un altre  <icon s></icon> cada 4 dies, *de promige*.[^serial_interval] (recorda, hi ha molta variació)

[^serial_interval]: “L'interval [serial] mitjà era de 3.96 dies (95% CI 3.53–4.39 days)”. [Du Z, Xu X, Wu Y, Wang L, Cowling BJ, Ancel Meyers L](https://wwwnc.cdc.gov/eid/article/26/6/20-0357_article) (Avís: Els articles en pre-publicació no es consideren versions finals)

Si simulem "el doble cada 4 dies" *i res més*, en una població que comença només amb un 0.001% <span class="nowrap"><icon i></icon>,</span> què passa?

**Clica a sobre de "Inici" per a veure la simulació! Pots tornar-la a veure després amb paràmetres diferents:** (detalls tècnics: [^caveats])

[^caveats]: **Recorda: totes aquestes simulacions són super simplidicades, amb finalitat didàctica.**
    
    Una simplificació: Quan en aquesta simulació diem "Infecta 1 persona nova cada X dies", en realitat s'incremente el nombre d'infectats per 1/X cada dia. El mateix per a altres paràmetres d'aquesta simulació - "Es recupara cada X dies" redueix el nombre d'infectats d'un 1/X cada dia.
    De fet *no són* exactament el mateix, però s'assemblen prou i per al cas, això és menys opac que fixar les taxes de transmissió/recuperació directament.

<div class="sim">
		<iframe src="sim?stage=epi-1" width="800" height="540"></iframe>
</div>

Aquesta és la **corba de creixement exponencial.** Comença fluix, i després explota. "Oh només és una grip" fins a "Oh vaja, les grips no provoquen que hi hagi *fosses comuns a grans ciutats*". 

![](pics/exponential.png)

Però, aquesta simulació és falsa. El creixement exponencial, per sort, no es pot mantenir per sempre. Una cosa que para l'expansió del  virus és si *els altres ja el tenen*:

![](pics/susceptibles.png)

Com més <span class="nowrap"><icon i></icon>s</span> hi ha, més de pressa els <span class="nowrap"><icon s></icon>s</span> es tornrn <span class="nowrap"><icon i></icon>s,</span> **però com menys <span class="nowrap"><icon s></icon>s</span> hi ha, més *tarden* els <span class="nowrap"><icon s></icon>s</span> a ser <span class="nowrap"><icon i></icon>s.</span>**

Com pot ser que això canviÏ el creixement de l'epidèmia? Veiem-ho:

<div class="sim">
		<iframe src="sim?stage=epi-2" width="800" height="540"></iframe>
</div>

Aquesta és la **corba de creixement** en forma d'"S". Comença fluix, explota, i després es frena de nou.

Però, aquesta simulació *encara* és incorrecta. Ens falta el fet que <icon i></icon> la gent infecciosa podria deixar de ser-ho, perquè 1) es recupera, o 2) es "recupera amb els pulmons danyats" o 3) mor.

Per simplificar, anem a suposar que totes les <icon i></icon> persones infeccioses es recuperen <icon r></icon>. (només recorda que en realitat, algunes es moren). <span class="nowrap"><icon r></icon>s</span> no es poden tornar a nfectar, i posem per cas que – *per ara!* – queden inmunitzades per sempre. 

Amb el COVID-19, s'estima que ets icon i></icon> infecciós durant 10 dies, *de mitjana*.[^infectiousness] Aixo vol dir que alguns afortunats es recuperaran abans de 10 dies, uns altres després. **Aquí tenim la pinta que té, amb una simulació que *començag* amb el  100%  de <span class="nowrap"><icon i></icon>:</span>**

[^infectiousness]: “La mediana del periode comunicable \[...\] era 9.5 dies.” [Hu, Z., Song, C., Xu, C. et al](https://link.springer.com/article/10.1007/s11427-020-1661-4) Si, ja sabem que la "mediana" noe és el mateix que la "mitjana". Per a finalitats didàctiques, són prou iguals.

<div class="sim">
		<iframe src="sim?stage=epi-3" width="800" height="540"></iframe>
</div>

TAixò és el contrari que el creixement exponencial, la **corba de decreixement exponencial.**

I ara, què passa si simules un creixement logístics amb forma d'"S" *amb* recuperació?

![](pics/graphs_q.png)

Veiem-ho!

<b style='color:#ff4040'>La corba vermella</b> és la dels casos *actuals* <span class="nowrap"><icon i></icon>,</span>    
<b style='color:#999999'>La corba gris</b> és el *total* de casos (actuals + recuperats <span class="nowrap"><icon r></icon>),</span>
que comença just al 0.001% <span class="nowrap"><icon i></icon>:</span>

<div class="sim">
		<iframe src="sim?stage=epi-4" width="800" height="540"></iframe>
</div>

I *aquí tenim* d'on ve la famosa corba! No té forma de campana, no tan sols és una corba "log-normal". IO té cap nom. Però l'hem vist infinitat de vegades, i sempre implorant que s'aplanés.

Aquest és el **Model SIR**,[^sir]    
(<icon s></icon>**S**usceptible <icon i></icon>**I**nfeccióss <icon r></icon>**R**ecuperat)      
el *segon* concepte més important de l'epidemiologia bàsica:

[^sir]: Per a més explicacions tècniques del Model SIR, veieu [the Institute for Disease Modeling](https://www.idmod.org/docs/hiv/model-sir.html#) i [Wikipedia](https://en.wikipedia.org/wiki/Compartmental_models_in_epidemiology#The_SIR_model)

![](pics/sir.png)

**NOTA: Les simulacions que es fan servir per prendre de decisions de polítiques públiques son molt, *molt* més elaborades que aquesta!** Però el Model SIR ja serveix per treure onclusions generals, encara que li faltin els matisos.

Doncs, som-hi, posem-li un matís més: abans que un <icon s></icon> es torni un <span class="nowrap"><icon i></icon>,</span>, perimer ha de passar a ser un <icon e></icon> Exposat. Aixo vol dir que té e virusperò que no el pot passar encara - infec*tat*, però no infec*ciós*.

![](pics/seir.png)

(Aquesta variant s'anomena el **Model SEIR**[^seir], on la lletra "E" vol dir <icon e></icon> "Exposat". Fixa't que aquest *no és* el significat habitual de la paraula "exposet", que vol dir que pot tenir el virus o no. En aquesta definició tècnica, "Exposat" vol dir que no hi ha cap dubte que el tens. La terminologia científica és dolenta.)

[^seir]: Per a més explicacions tèniques del Model SEIR, veieu [the Institute for Disease Modeling](https://www.idmod.org/docs/hiv/model-seir.html) i [Wikipedia](https://en.wikipedia.org/wiki/Compartmental_models_in_epidemiology#The_SEIR_model)

Per al COVID-19, s'estima que estàs <icon e></icon> infectat-però-no-encara-infecciós durant 3 dies, *en mitjana*.[^latent] Què passa si ho afegim a la simulació?

[^latent]: “Suposant una distribució del periode d'incubació de mitjana 5.2 dies a partir d'un estudi separat de cass de COVID-19, hem deduit que la capactat d'infecció començava a partir del 2.3 dies  (95% CI, 0.8–3.0 days) abans de l'inici dels símptomes" (Traduim: Suposant que els símptomes comencen als 5 dies, la capacitat d'infecció comença 2 dies abans = LA capacitat d'infecció comença al dia 3) [He, X., Lau, E.H.Y., Wu, P. et al.](https://www.nature.com/articles/s41591-020-0869-5)

<b style='color:#ff4040'>La corba vermella <b style='color:#FF9393'>+ rosa</b> curve</b> son els casos *actuals* (infecciosos <icon i></icon> + exposats <span class="nowrap"><icon e></icon>),</span>    
<b style='color:#888'>LA corba gris</b> son els *total* de casos (actuals + recuperats <span class="nowrap"><icon r></icon>):</span>

<div class="sim">
		<iframe src="sim?stage=epi-5" width="800" height="540"></iframe>
</div>

No hi ha gaires canvis! El temps que estàs <icon e></icon> Exposat canvia la ratio de <span class="nowrap"><icon e></icon>-a-<icon i></icon>,</span> i *quan* els casos actuals arriben al pic... pero l'*alçada* del pic i els casos totals, es queden igual.

Per què passa? Pel *primer* concepte i el més important de l'epidemiologia bàsica:

![](pics/r.png)

Abreviació del "nombre Reproductiu". És el nmbre *promig* de persones que un <icon i></icon> infecta *abans* de recuperar-se (or morir).

![](pics/r2.png)

**R** canvia en el decurs de l'epidèmia, si ens immunitzem més  i fem més intervencions.

**R<sub>0</sub>** és e que val R *al princpi de l'epidèmia, abans de la immunitat o les intervencions*. R<sub>0</sub> reflecteix sobretot la capacitat del mateix virus, però canvia d'un lloc a un altre. Per exemple,  R<sub>0</sub> és més alt a les ciutats amb més densitat de població que a les àrees rurals i disperses.

(La majoria dels articles nous - in inclús alguns articles de recerca! – confonen R i R<sub>0</sub>. Aquí també, la terminologia científica és dolenta)

L'R<sub>0</sub> per a "la" gripa estacional està al voltant d'1.28[^r0_flu]. Això vol dir que, al *principi* d'una epidèmia de grip, cada <icon i></icon> infecta 1.28 persones *de promig.* (Si sona estrany que o sigui un nombre enter, recorda que una mare "promig" té 2.4 fills. I no hi ha fraccions de nens corrent pel món.)

[^r0_flu]: “El valor medià per R en la grip estacional era  1.28 (RIQ: 1.19–1.37)” [Biggerstaff, M., Cauchemez, S., Reed, C. et al.](https://bmcinfectdis.biomedcentral.com/articles/10.1186/1471-2334-14-480)

L'R<sub>0</sub> pel COVID-19 es va estimar que estava al voltant de 2.2,[^r0_covid] però un estudi *encara-no-finalitzat* estima que era  5.7(!) a Wuhan.[^r0_wuhan]

[^r0_covid]: “Hem estimat que el número bàsica de reproducció R0 deL 2019-nCoV està al voltant de 2.2 (interval d'alta densitat al 90%: 1.4–3.8)” [Riou J, Althaus CL.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7001239/)

[^r0_wuhan]: “Hem calculat un valor medià per R0 de 5.7 (95% IC 3.8–8.9)” [Sanche S, Lin YT, Xu C, Romero-Severson E, Hengartner N, Ke R.](https://wwwnc.cdc.gov/eid/article/26/7/20-0282_article)

A la nostra simulació – *al principi & en promig* – un <icon i></icon> infecta algú cada 4 dies, durant 10 dies. "4 dies" encaixa dins els "10 dies" dues vegades i mitja. Això vol dir que – *al primcipi & em promig* – cada <icon i></icon> infecta 2.5 persones. Per tant, R<sub>0</sub> = 2.5. (caveats:[^r0_caveats_sim])

[^r0_caveats_sim]: Això val si creus que ets igual d'infecciós durant tot el teu "periode infecciós". Un altre cop, simplificacions didàctiques.

**Juga amb aquesta calculadora d'R<sub>0</sub>, per veure com R<sub>0</sub> depèn dels temps de recuperació i d'infecció:**

<div class="sim">
		<iframe src="sim?stage=epi-6a&format=calc" width="285" height="255"></iframe>
</div>


Però recorda, com menys <span class="nowrap"><icon s></icon>s</span> hi ha, més a *poc a poc* els <span class="nowrap"><icon s></icon>s</span> passen a <span class="nowrap"><icon i></icon>s.</span> El nombre de reproducció *actual* (R) no només depèn del nombre de reproducció *basic* (R<sub>0</sub>), sinó *també* de quanta gent ja no és  <icon s></icon> Susceptible. (Per exemple, perquè es recupera & aconsegueix immunitat natural.)

<div class="sim">
		<iframe src="sim?stage=epi-6b&format=calc" width="285" height="390"></iframe>
</div>

Quan ja hi ha prou gent que té immunitat, R < 1, i el virus es conté! Això s'anomena **immunitat de grup**. Per a les grips, aquesta immunitat s'aconsegueix *amb una vacuna*. Mirar d'aconseguir "immunitat natural de grup" deixant que la gent s'infecti és una idea *horrible*. (Però no per les raons que creus! Ho explicarem després.)

Ara, tornem a jugar amb el Model SEIR, però mirem R<sub>0</sub>, R al llarg del temps i el nivell de la immunitat de grup:

<div class="sim">
		<iframe src="sim?stage=epi-7" width="800" height="540"></iframe>
</div>


**NOTA: El total de casos *no atura* al nivell de la immunitat de grup, la supera!** I creua el nivell en el moment *exacte* que els casos actuals arriben al pic. (Això passa independenyment dels ajustos que triïs – prova-ho tu mateix!)

Això passa perquè quan hi ha més <span class="nowrap">non-<icon s></icon>s</span> del nivell de la immunitat de grup, tens R < 1. I quan  R < 1, no augmenten més els casos nous: un pic.

**Si hi ha una única lliçó que t'has d'emportar d'aquesta guia, aquí la tens!** – és un diagrama extremadament complex, per tant pren-te una mica de temps per a absorvir-lo:

![](pics/r3.png)

**Signfica que: NO cal evitar tots els contagis, ni tan sols la gran majoria, per aturar el COVID-19**

És una paradoxa, el COVID-19 és extremadament contagiós, però per a controlar-lo, "només" cal que evitem més del 60% de contagis. El 60%?! Si això fos la nota d'un examen, seria un suspens clar. Però si R<sub>0</sub> = 2.5, ci el retallem un 61% tenims R = 0.975, que és R < 1, virus controlat! (fórmula exacta:[^exact_formula])

[^exact_formula]: Recorda que  diem que R = R<sub>0</sub> *  és la taxa de transmissió permesa. Recorda també que la taxa de tramissió permesa = 1 - taxa de transmissió per a l'*aturada*.
    
    Per tant, per obtenir R<1, has de tenir R<sub>0</sub> * TransmissionsPermeses < 1.

    Per tant, TransmissionsPermeses < 1/R<sub>0</sub>

    Per tant, 1 - TransmissionsAturades < 1/R<sub>0</sub>
   
    Llavors, TransmissionsAturades > 1 - 1/R<sub>0</sub>
    
    I en conseqüència, cal parar més de l'**1 - 1/R<sub>0</sub>**  de les transmissions per a obtenir R < 1 i controlar el virus!

![](pics/r4.png)


(Si creus que R<sub>0</sub> o els altres nombres de les nostres simulacions són massa baixos/alts, està bé, estàs posant a prova les nostres hipótesis! Hi ha un mode *caixa d'eines* al final d'aquesta guia, on podràs posar els teus *propis* números, i simular què passa.)

*Cada* intervenció COVID-19 de la què hagis sentit a parlar - rentat de mans, distanciament social/físic, confinaments, auto-isolació, seguiment de contactes & quanrentenes, mascaretes, inclosa la "immunitat de grup", *totes* fan el mateix:

Aconseguir R < 1.

Així que ara, usem el nostre "simulador de vol d'eidèmies" per entendre-ho: Com es podem fer que R < 1 d'una forma que **també es protegeixi la nostra salut mental *i* financera?**

Agafa't fort per a un aterratget d'emergència...

<div class="section chapter">
    <div>
		<img src="banners/curve.png" height=480 style="position: absolute;"/>
        <div>The Next Few Months</div>
    </div>
</div>

... podria haver estat pitjor. Aquí hi ha un univers paral·lel que haurem evitat:

###Scenario 0: No fer absolutament res

Aproximadament 1 de cada 20 perones infectades de COVID-19 han d'anar a l'UCI (Unitat de Cures Intensives.[^icu_covid]  A un país ric com els EUA, hi ha 1 llit per cada 3400 persones.[^icu_us] Per tant, als EUA es pot soportar una situació de 20 persones infectades *simultàniament* ce cada 3400 - o, el 0.6% de la població.

[^icu_covid]: ["Percentatge de casos COVID-19 als Estats Units entre el 12 de febrer i el 16 de març de 2020 que van necessitar ingressar a una unitat de cures intensives (UCI) per hrup d'edat""](https://www.statista.com/statistics/1105420/covid-icu-admission-rates-us-by-age-group/). Entre el 4.9% i l'11.5% de *tots* els casos COVID-19 van requerir entrar a l'UCI. Si prenem generosament el rang inferior, és un 5%, és a dir 1 de cada 20. Cal tenir en compte que aquest total és específic de l'estructura d'edats dels EUA, i que serà més alt en paísos amb una població més envellida, més baix en paísos amb un població més jove.

[^icu_us]: “Número de llits UCI = 96,596”. A partir de [the Society of Critical Care Medicine](https://sccm.org/Blog/March-2020/United-States-Resource-Availability-for-COVID-19) La població dels EUA era 328,200,000 al 2019. 96,596 dels 328,200,000 = aproximadament 1 de cada 3400. 

Inclús si *tripliquéssim* aquesta capacitat fins al 2%, aquí tenim el què hauria passat *si no haguéssim fet res:*

<div class="sim">
		<iframe src="sim?stage=int-1&format=lines" width="800" height="540"></iframe>
</div>

Gens bo.

Això és el que l'informe [the March 16 Imperial College report](http://www.imperial.ac.uk/mrc-global-infectious-disease-analysis/covid-19/report-9-impact-of-npis-on-covid-19/) va concloure: si no fem res, ens falten UCIs, i tenim a més del 80% de la població infectada. 
(recorda: el total de casos *supera* la immunitat de grup)

Inclús si només el 0.5% dels infectats es mor  una hipòtesi generosa quan ja no queden UCIs - en un país gran com els EUA, amb 300 milions d'habitants, 0.5% del 80% de 300 milions = arribem a 1.2 milions de morts...*SI no haguéssim fet res*

(Molts mitjans socials i de comunicació van dir que "s'infectarien el 80%" igualment *sense* el "SI NO FEM RES". La por es va canalitzar en cliks, no en aprenentatge. *Buf.*)


###Scenario 1: Aplanar la Corba / Immunitat de Grup

El pla "Aplanar la Corba" va ser aclamat per totes les organitzacions de salut pública, mentre que el pla "Immunitat de Grup* original del Regne Unit va ser criticat. Eren *el mateix pla*. Només que el Regne Unit el va comunicar malamet.[^yong]

[^yong]: “Diu que la finalittat és la mateixa que als altre països: aplanar la corba esglaonant l'inici de les infeccions. Com a conseqUència, tot el país aconsegueix la immunitat de grup; és un efecte secundari, no un objectiu  [...]  El pla d'acció del govern contra el coronavirus que hi ha a la xarxa, no esmenta per res la immunitat de grup.”
    
    Extret de [The Atlantic article by Ed Yong](https://www.theatlantic.com/health/archive/2020/03/coronavirus-pandemic-herd-immunity-uk-boris-johnson/608065/)

Els dos plans, malgrat tot, tenien un defecte literalment fatal.

Primer, mmirem a les dues formes d'"aplanar la corba": rentat de mans & distanciament físic.

Incrementar el rentat de mans atura els refredats & grips en els països de renda alta en aprox. un 5%[^handwashing], mentre que un confinament global de la ciutat de Londres va tallar es contactes d'aprox. un 70%[^london]. Per tant, suposarem que el rentat de mans redueix R *fins a ^un 25% i el distanciament el pot reduir *fins a* un 70%.

[^handwashing]: “Els vuit estudis indiquen que el rentat de mans reueix el risc d'infecció respiratòria, amb reduccions d'entre un 6% i un 44% [valor agrupat 24% (95% IC 6–40%)].” Nosaltres hem arrodonit el valor agrupat al 25% en aquestes simulacions per a simplificar. [Rabie, T. and Curtis, V.](https://onlinelibrary.wiley.com/doi/full/10.1111/j.1365-3156.2006.01568.x) Nota: com es diu en aquesta meta-anàlisi, la qualitat dels estudis del rentat de mans (al menys en el païsso de rendes altes) és horrible.

[^london]: “Vàrem trobar una reducció del 73% en el nombre mitjà de contactes diaris observats per participants. Això seria suficient per a reduir R0 del valor de 2.6 abans del confinament fins a 0.62 (0.37 - 0.89) durant el confinament”. Nosaltres ho hem arrodonit al 70% a les nostres simulacions per simplificar [Jarvis and Zandvoort et al](https://cmmid.github.io/topics/covid19/comix-impact-of-physical-distance-measures-on-transmission-in-the-UK.html)

**Juga amb aquesta calucladora per veure com % dels <span class="nowrap">no-<icon s></icon>,</span> el rentat de mans i el distanciament redueixen  R:** ( aquesta calculadora visulaitza els seus efectes *relatius*, i per això quan una creix *sembla* que decreixi l'efecte de les altres.[^log_caveat])

[^log_caveat]: Aquesta distorció desapareixeria si féssim una gràfica de l'R en una escala logarítmica... però aleshores hauriem d'explicar les *escales logarítmiques.*

<div class="sim">
		<iframe src="sim?stage=int-2a&format=calc" width="285" height="260"></iframe>
</div>




Now, let's simulate what happens to a COVID-19 epidemic if, starting March 2020, we had increased handwashing but only *mild* physical distancing – so that R is lower, but still above 1:

<div class="sim">
		<iframe src="sim?stage=int-2&format=lines" width="800" height="540"></iframe>
</div>

Three notes:

1. This *reduces* total cases! **Even if you don't get R < 1, reducing R still saves lives, by reducing the 'overshoot' above herd immunity.** Lots of folks think "Flatten The Curve" spreads out cases without reducing the total. This is impossible in *any* Epidemiology 101 model. But because the news reported "80%+ will be infected" as inevitable, folks thought total cases will be the same no matter what. *Sigh.*

2. Due to the extra interventions, current cases peak *before* herd immunity is reached. In fact, in this simulation, total cases only overshoots *a tiny bit* above herd immunity – the UK's plan! At that point, R < 1, you can let go of all other interventions, and COVID-19 stays contained! Well, except for one problem...

3. You still run out of ICUs. For several months. (and remember, we *already* tripled ICUs for these simulations)

That was the other finding of the March 16 Imperial College report, which convinced the UK to abandon its original plan. Any attempt at **mitigation** (reduce R, but R > 1) will fail. The only way out is **suppression** (reduce R so that R < 1).

![](pics/mitigation_vs_suppression.png)

That is, don't merely "flatten" the curve, *crush* the curve. For example, with a...

###Scenario 2: Months-Long Lockdown

Let's see what happens if we *crush* the curve with a 5-month lockdown, reduce <icon i></icon> to nearly nothing, then finally – *finally* – return to normal life:

<div class="sim">
		<iframe src="sim?stage=int-3&format=lines" width="800" height="540"></iframe>
</div>

Oh.

This is the "second wave" everyone's talking about. As soon as we remove the lockdown, we get R > 1 again. So, a single leftover <icon i></icon> (or imported <span class="nowrap"><icon i></icon>)</span> can cause a spike in cases that's almost as bad as if we'd done Scenario 0: Absolutely Nothing.

**A lockdown isn't a cure, it's just a restart.**

So, what, do we just lockdown again & again?

###Scenario 3: Intermittent Lockdown

This solution was first suggested by the March 16 Imperial College report, and later again by a Harvard paper.[^lockdown_harvard]

[^lockdown_harvard]: “Absent other interventions, a key metric for the success of social distancing is whether critical care capacities are exceeded. To avoid this, prolonged or intermittent social distancing may be necessary into 2022.” [Kissler and Tedijanto et al](https://science.sciencemag.org/content/early/2020/04/14/science.abb5793)

**Here's a simulation:** (After playing the "recorded scenario", you can try simulating your *own* lockdown schedule, by changing the sliders *while* the simulation is running! Remember you can pause & continue the sim, and change the simulation speed)

<div class="sim">
		<iframe src="sim?stage=int-4&format=lines" width="800" height="540"></iframe>
</div>

This *would* keep cases below ICU capacity! And it's *much* better than an 18-month lockdown until a vaccine is available. We just need to... shut down for a few months, open up for a few months, and repeat until a vaccine is available. (And if there's no vaccine, repeat until herd immunity is reached... in 2022.)

Look, it's nice to draw a line saying "ICU capacity", but there's lots of important things we *can't* simulate here. Like:

**Mental Health:** Loneliness is one of the biggest risk factors for depression, anxiety, and suicide. And it's as associated with an early death as smoking 15 cigarettes a day.[^loneliness]

[^loneliness]: See [Figure 6 from Holt-Lunstad & Smith 2010](https://journals.sagepub.com/doi/abs/10.1177/1745691614568352). Of course, big disclaimer that they found a *correlation*. But unless you want to try randomly assigning people to be lonely for life, observational evidence is all you're gonna get.

**Financial Health:** "What about the economy" sounds like you care more about dollars than lives, but "the economy" isn't just stocks: it's people's ability to provide food & shelter for their loved ones, to invest in their kids' futures, and enjoy arts, foods, videogames – the stuff that makes life worth living. And besides, poverty *itself* has horrible impacts on mental and physical health.

Not saying we *shouldn't* lock down again! We'll look at "circuit breaker" lockdowns later. Still, it's not ideal.

But wait... haven't Taiwan and South Korea *already* contained COVID-19? For 4 whole months, *without* long-term lockdowns?

How?

###Scenario 4: Test, Trace, Isolate

*"Sure, we \*could've\* done what Taiwan & South Korea did at the start, but it's too late now. We missed the start."*

But that's exactly it! “A lockdown isn't a cure, it's just a restart”... **and a fresh start is what we need.**

To understand how Taiwan & South Korea contained COVID-19, we need to understand the exact timeline of a typical COVID-19 infection[^timeline]:

[^timeline]: **3 days on average to infectiousness:** “Assuming an incubation period distribution of mean 5.2 days from a separate study of early COVID-19 cases, we inferred that infectiousness started from 2.3 days (95% CI, 0.8–3.0 days) before symptom onset” (translation: Assuming symptoms start at 5 days, infectiousness starts 2 days before = Infectiousness starts at 3 days) [He, X., Lau, E.H.Y., Wu, P. et al.](https://www.nature.com/articles/s41591-020-0869-5)  
    
    **4 days on average to infecting someone else:** “The mean [serial] interval was 3.96 days (95% CI 3.53–4.39 days)” [Du Z, Xu X, Wu Y, Wang L, Cowling BJ, Ancel Meyers L](https://wwwnc.cdc.gov/eid/article/26/6/20-0357_article)
    
    **5 days on average to feeling symptoms:** “The median incubation period was estimated to be 5.1 days (95% CI, 4.5 to 5.8 days)” [Lauer SA, Grantz KH, Bi Q, et al](https://annals.org/AIM/FULLARTICLE/2762808/INCUBATION-PERIOD-CORONAVIRUS-DISEASE-2019-COVID-19-FROM-PUBLICLY-REPORTED)

![](pics/timeline1.png)

If cases only self-isolate when they know they're sick (that is, they feel symptoms), the virus can still spread:

![](pics/timeline2.png)

And in fact, 44% of all transmissions are like this: *pre*-symptomatic! [^pre_symp]

[^pre_symp]: “We estimated that 44% (95% confidence interval, 25–69%) of secondary cases were infected during the index cases’ presymptomatic stage” [He, X., Lau, E.H.Y., Wu, P. et al](https://www.nature.com/articles/s41591-020-0869-5)

But, if we find *and quarantine* a symptomatic case's recent close contacts... we stop the spread, by staying one step ahead!

![](pics/timeline3.png)

This is called **contact tracing**. It's an old idea, was used at an unprecedented scale to contain Ebola[^ebola], and now it's core part of how Taiwan & South Korea are containing COVID-19!

[^ebola]: “Contact tracing was a critical intervention in Liberia and represented one of the largest contact tracing efforts during an epidemic in history.” [Swanson KC, Altare C, Wesseh CS, et al.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6152989/)

(It also lets us use our limited tests more efficiently, to find pre-symptomatic <span class="nowrap"><icon i></icon>s</span> without needing to test almost everyone.)

Traditionally, contacts are found with in-person interviews, but those *alone* are too slow for COVID-19's ~48 hour window. That's why contact tracers need help, and be supported by – *NOT* replaced by – contact tracing apps.

(This idea didn't come from "techies": using an app to fight COVID-19 was first proposed by [a team of Oxford epidemiologists](https://science.sciencemag.org/content/early/2020/04/09/science.abb6936).)

Wait, apps that trace who you've been in contact with?... Does that mean giving up privacy, giving in to Big Brother?

Heck no! **[DP-3T](https://github.com/DP-3T/documents#decentralized-privacy-preserving-proximity-tracing)**, a team of epidemiologists & cryptographers (including one of us, Marcel Salathé) is *already* making a contact tracing app – with code available to the public – that reveals **no info about your identity, location, who your contacts are, or even *how many contacts* you've had.**

Here's how it works:

![](pics/dp3t.png)

([Here's the full comic](https://ncase.me/contact-tracing/). Details about "pranking"/false positives/etc in footnote:[^dp3t_details])

[^dp3t_details]: To prevent "pranking" (people falsely claiming to be infected), the DP-3T Protocol requires that the hospital first give you a One-Time Passcode that lets you upload your messages.
    
    False positives are a problem in both manual & digital contact tracing. Still, we can reduce false positives in 2 ways: 1) By notifying Bobs only if they heard, say, 30+ min worth of messages, not just one message in passing. And 2) If the app *does* think Bob's been exposed, it can refer Bob to a *manual* contact tracer, for an in-depth follow-up interview.
    
    For other issues like data bandwidth, source integrity, and other security issues, check out [the open-source DP-3T whitepapers!](https://github.com/DP-3T/documents#decentralized-privacy-preserving-proximity-tracing)

Along with similar teams like TCN Protocol[^tcn] and MIT PACT[^pact], they've inspired Apple & Google to bake privacy-first contact tracing directly into Android/iOS.[^gapple] (Don't trust Google/Apple? Good! The beauty of this system is it doesn't *need* trust!) Soon, your local public health agency may ask you to download an app. If it's privacy-first with publicly-available code, please do!

[^tcn]: [Temporary Contact Numbers, a decentralized, privacy-first contact tracing protocol](https://github.com/TCNCoalition/TCN#tcn-protocol)

[^pact]: [PACT: Private Automated Contact Tracing](https://pact.mit.edu/)

[^gapple]: [Apple and Google partner on COVID-19 contact tracing technology ](https://www.apple.com/ca/newsroom/2020/04/apple-and-google-partner-on-covid-19-contact-tracing-technology/). Note they're not making the apps *themselves*, just creating the systems that will *support* those apps.

But what about folks without smartphones? Or infections through doorknobs? Or "true" asymptomatic cases? Contact tracing apps can't catch all transmissions... *and that's okay!* We don't need to catch *all* transmissions, just 60%+ to get R < 1.

(Footnote rant about the confusion between pre-symptomatic vs "true" asymptomatic – "true" asymptomatics are rare:[^rant])

[^rant]: Lots of news reports – and honestly, many research papers – did not distinguish between "cases who showed no symptoms when we tested them" (pre-symptomatic) and "cases who showed no symptoms *ever*" (true asymptomatic). The only way you could tell the difference is by following up with cases later.
   
    Which is what [this study](https://wwwnc.cdc.gov/eid/article/26/8/20-1274_article) did. (Disclaimer: "Early release articles are not considered as final versions.") In a call center in South Korea that had a COVID-19 outbreak, "only 4 (1.9%) remained asymptomatic within 14 days of quarantine, and none of their household contacts acquired secondary infections."
    
    So that means "true asymptomatics" are rare, and catching the disease from a true asymptomatic may be even rarer!

Isolating *symptomatic* cases would reduce R by up to 40%, and quarantining their *pre/a-symptomatic* contacts would reduce R by up to 50%[^oxford]:

[^oxford]: From the same Oxford study that first recommended apps to fight COVID-19: [Luca Ferretti & Chris Wymant et al](https://science.sciencemag.org/content/early/2020/04/09/science.abb6936/tab-figures-data) See Figure 2. Assuming R<sub>0</sub> = 2.0, they found that:    
    
    * Symptomatics contribute R = 0.8 (40%)
    * Pre-symptomatics contribute R = 0.9 (45%)
    * Asymptomatics contribute R = 0.1 (5%, though their model has uncertainty and it could be much lower)
    * Environmental stuff like doorknobs contribute R = 0.2 (10%)

    And add up the pre- & a-symptomatic contacts (45% + 5%) and you get 50% of R!

<div class="sim">
		<iframe src="sim?stage=int-4a&format=calc" width="285" height="340"></iframe>
</div>

Thus, even without 100% contact quarantining, we can get R < 1 *without a lockdown!* Much better for our mental & financial health. (As for the cost to folks who have to self-isolate/quarantine, *governments should support them* – pay for the tests, job protection, subsidized paid leave, etc. Still way cheaper than intermittent lockdown.)

We then keep R < 1 until we have a vaccine, which turns susceptible <span class="nowrap"><icon s></icon>s</span> into immune <span class="nowrap"><icon r></icon>s.</span> Herd immunity, the *right* way:

<div class="sim">
		<iframe src="sim?stage=int-4b&format=calc" width="285" height="230"></iframe>
</div>

(Note: this calculator pretends the vaccines are 100% effective. Just remember that in reality, you'd have to compensate by vaccinating *more* than "herd immunity", to *actually* get herd immunity)

Okay, enough talk. Here's a simulation of:

1. A few-month lockdown, until we can...
2. Switch to "Test, Trace, Isolate" until we can...
3. Vaccinate enough people, which means...
4. We win.

<div class="sim">
		<iframe src="sim?stage=int-5&format=lines" width="800" height="540"></iframe>
</div>

So that's it! That's how we make an emergency landing on this plane.

That's how we beat COVID-19.

...

But what if things *still* go wrong? Things have gone horribly wrong already. That's fear, and that's good! Fear gives us energy to create *backup plans*.

The pessimist invents the parachute.

###Scenario 4+: Masks For All, Summer, Circuit Breakers

What if R<sub>0</sub> is way higher than we thought, and the above interventions, even with mild distancing, *still* aren't enough to get R < 1?

Remember, even if we can't get R < 1, reducing R still reduces the "overshoot" in total cases, thus saving lives. But still, R < 1 is the ideal, so here's a few other ways to reduce R:

**Masks For All:**

*"Wait,"* you might ask, *"I thought face masks don't stop you from getting sick?"*

You're right. Masks don't stop you from getting sick[^incoming]... they stop you from getting *others* sick.

[^incoming]: “None of these surgical masks exhibited adequate filter performance and facial fit characteristics to be considered respiratory protection devices.” [Tara Oberg & Lisa M. Brosseau](https://www.sciencedirect.com/science/article/pii/S0196655307007742)

[^outgoing]: “The overall 3.4 fold reduction [70% reduction] in aerosol copy numbers we observed combined with a nearly complete elimination of large droplet spray demonstrated by Johnson et al. suggests that surgical masks worn by infected persons could have a clinically significant impact on transmission.” [Milton DK, Fabian MP, Cowling BJ, Grantham ML, McDevitt JJ](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3591312/)

[^homemade]: [Davies, A., Thompson, K., Giri, K., Kafatos, G., Walker, J., & Bennett, A](https://www.cambridge.org/core/journals/disaster-medicine-and-public-health-preparedness/article/testing-the-efficacy-of-homemade-masks-would-they-protect-in-an-influenza-pandemic/0921A05A69A9419C862FA2F35F819D55) See Table 1: a 100% cotton T-shirt has around 2/3 the filtration efficiency as a surgical mask, for the two bacterial aerosols they tested.

![](pics/masks.png)

To put a number on it: surgical masks *on the infectious person* reduce cold & flu viruses in aerosols by 70%.[^outgoing] Reducing transmissions by 70% would be as large an impact as a lockdown!

However, we don't know for sure the impact of masks on COVID-19 *specifically*. In science, one should only publish a finding if you're 95% sure of it. (...should.[^replication]) Masks, as of May 1st 2020, are less than "95% sure".

[^replication]: Any actual scientist who read that last sentence is probably laugh-crying right now. See: [p-hacking](https://en.wikipedia.org/wiki/Data_dredging), [the replication crisis](https://en.wikipedia.org/wiki/Replication_crisis))

However, pandemics are like poker. **Make bets only when you're 95% sure, and you'll lose everything at stake.** As a recent article on masks in the British Medical Journal notes,[^precautionary] we *have* to make cost/benefit analyses under uncertainty. Like so:

[^precautionary]: “It is time to apply the precautionary principle” [Trisha Greenhalgh et al \[PDF\]](https://www.bmj.com/content/bmj/369/bmj.m1435.full.pdf)

Cost: If homemade cloth masks (which are ~2/3 as effective as surgical masks[^homemade]), super cheap. If surgical masks, more expensive but still pretty cheap.

Benefit: Even if it's a 50–50 chance of surgical masks reducing transmission by 0% or 70%, the average "expected value" is still 35%, same as a half-lockdown! So let's guess-timate that surgical masks reduce R by up to 35%, discounted for our uncertainty. (Again, you can challenge our assumptions by turning the sliders up/down)

<div class="sim">
		<iframe src="sim?stage=int-6a&format=calc" width="285" height="380"></iframe>
</div>

(other arguments for/against masks:[^mask_args])

[^mask_args]: **"We need to save supplies for hospitals."** *Absolutely agreed.* But that's more of an argument for increasing mask production, not rationing. In the meantime, we can make cloth masks.

   **"They're hard to wear correctly."** It's also hard to wash your hands according to the WHO Guidelines – seriously, "Step 3) right palm over left dorsum"?! – but we still recommend handwashing, because imperfect is still better than nothing.
   
   **"It'll make people more reckless with handwashing & social distancing."** Sure, and safety belts make people ignore stop signs, and flossing makes people eat rocks. But seriously, we'd argue the opposite: masks are a *constant physical reminder* to be careful – and in East Asia, masks are also a symbol of solidarity!
    
    

Masks *alone* won't get R < 1. But if handwashing & "Test, Trace, Isolate" only gets us to R = 1.10, having just 1/3 of people wear masks would tip that over to R < 1, virus contained!

**Summer:**

Okay, this isn't an "intervention" we can control, but it will help! Some news outlets report that summer won't do anything to COVID-19. They're half right: summer won't get R < 1, but it *will* reduce R.

For COVID-19, every extra 1° Celsius (1.8° Fahrenheit) makes R drop by 1.2%.[^heat] The summer-winter difference in New York City is 26°C (47°F),[^nyc_heat] so summer will make R drop by ~31%.

[^heat]: “One-degree Celsius increase in temperature [...] lower[s] R by 0.0225” and “The average R-value of these 100 cities is 1.83”. 0.0225 ÷ 1.83 = ~1.2%. [Wang, Jingyuan and Tang, Ke and Feng, Kai and Lv, Weifeng](https://papers.ssrn.com/sol3/Papers.cfm?abstract_id=3551767)

[^nyc_heat]: In 2019 at Central Park, hottest month (July) was 79.6°F, coldest month (Jan) was 32.5°F. Difference is 47.1°F, or ~26°C. [PDF from Weather.gov](https://www.weather.gov/media/okx/Climate/CentralPark/monthlyannualtemp.pdf)

<div class="sim">
		<iframe src="sim?stage=int-6b&format=calc" width="285" height="220"></iframe>
</div>

Summer alone won't make R < 1, but if we have limited resources, we can scale back some interventions in the summer – so we can scale them *higher* in the winter.

**A "Circuit Breaker" Lockdown:**

And if all that *still* isn't enough to get R < 1... we can do another lockdown.

But we wouldn't have to be 2-months-closed / 1-month-open over & over! Because R is reduced, we'd only need one or two more "circuit breaker" lockdowns before a vaccine is available. (Singapore had to do this recently, "despite" having controlled COVID-19 for 4 months. That's not failure: this *is* what success takes.)

Here's a simulation of a "lazy case" scenario:

1. Lockdown, then
2. A moderate amount of hygiene & "Test, Trace, Isolate", with a mild amount of "Masks For All", then...
3. One more "circuit breaker" lockdown before a vaccine's found.

<div class="sim">
		<iframe src="sim?stage=int-7&format=lines&height=620" width="800" height="620"></iframe>
</div>

Not to mention all the *other* interventions we could do, to further push R down:

* Travel restrictions/quarantines
* Temperature checks at malls & schools
* Deep-cleaning public spaces
* [Replacing hand-shaking with foot-bumping](https://twitter.com/V_actually/status/1233785527788285953)
* And all else human ingenuity shall bring

. . .

We hope these plans give you hope. 

**Even under a pessimistic scenario, it *is* possible to beat COVID-19, while protecting our mental and financial health.** Use the lockdown as a "reset button", keep R < 1 with case isolation + privacy-protecting contact tracing + at *least* cloth masks for all... and life can get back to a normal-ish!

Sure, you may have dried-out hands. But you'll get to invite a date out to a comics bookstore! You'll get to go out with friends to watch the latest Hollywood cash-grab. You'll get to people-watch at a library, taking joy in people going about the simple business of *being alive.*

Even under the worst-case scenario... life perseveres.

So now, let's plan for some *worse* worst-case scenarios. Water landing, get your life jacket, and please follow the lights to the emergency exits:

<div class="section chapter">
    <div>
		<img src="banners/curve.png" height=480 style="position: absolute;"/>
        <div>The Next Few Years</div>
    </div>
</div>

You get COVID-19, and recover. Or you get the COVID-19 vaccine. Either way, you're now immune...

...*for how long?*

* COVID-19 is most closely related to SARS, which gave its survivors 2 years of immunity.[^SARS immunity]
* The coronaviruses that cause "the" common cold give you 8 months of immunity.[^cold immunity]
* There's reports of folks recovering from COVID-19, then testing positive again, but it's unclear if these are false positives.[^unclear]
* One *not-yet-peer-reviewed* study on monkeys showed immunity to the COVID-19 coronavirus for at least 28 days.[^monkeys]

But for COVID-19 *in humans*, as of May 1st 2020, "how long" is the big unknown.

[^SARS immunity]: “SARS-specific antibodies were maintained for an average of 2 years [...] Thus, SARS patients might be susceptible to reinfection ≥3 years after initial exposure.” [Wu LP, Wang NC, Chang YH, et al.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2851497/) "Sadly" we'll never know how long SARS immunity would have really lasted, since we eradicated it so quickly.

[^cold immunity]: “We found no significant difference between the probability of testing positive at least once and the probability of a recurrence for the beta-coronaviruses HKU1 and OC43 at 34 weeks after enrollment/first infection.” [Marta Galanti & Jeffrey Shaman (PDF)](http://www.columbia.edu/~jls106/galanti_shaman_ms_supp.pdf)

[^unclear]: “Once a person fights off a virus, viral particles tend to linger for some time. These cannot cause infections, but they can trigger a positive test.” [from STAT News by Andrew Joseph](https://www.statnews.com/2020/04/20/everything-we-know-about-coronavirus-immunity-and-antibodies-and-plenty-we-still-dont/)

[^monkeys]: From [Bao et al.](https://www.biorxiv.org/content/10.1101/2020.03.13.990226v1.abstract) *Disclaimer: This article is a preprint and has not been certified by peer review (yet).* Also, to emphasize: they only tested re-infection 28 days later. 

For these simulations, let's say it's 1 year.
**Here's a simulation starting with 100% <span class="nowrap"><icon r></icon>**,</span> exponentially decaying into susceptible, no-immunity <span class="nowrap"><icon s></icon>s</span> after 1 year, on *average*, with variation:

<div class="sim">
		<iframe src="sim?stage=yrs-1&format=lines&height=600" width="800" height="600"></iframe>
</div>

Return of the exponential decay!

This is the **SEIRS Model**. The final "S" stands for <icon s></icon> Susceptible, again.

![](pics/seirs.png)

Now, let's simulate a COVID-19 outbreak, over 10 years, with no interventions... *if immunity only lasts a year:*

<div class="sim">
		<iframe src="sim?stage=yrs-2&format=lines&height=600" width="800" height="600"></iframe>
</div>

In previous simulations, we only had *one* ICU-overwhelming spike. Now, we have several, *and* <icon i></icon> cases come to a rest *permanently at* ICU capacity. (Which, remember, we *tripled* for these simulations)

R = 1, it's **endemic.**

Thankfully, because summer reduces R, it'll make the situation better:

<div class="sim">
		<iframe src="sim?stage=yrs-3&format=lines&height=640" width="800" height="640"></iframe>
</div>

Oh.

Counterintuitively, summer makes the spikes worse *and* regular! This is because summer reduces new <span class="nowrap"><icon i></icon>s,</span> but that in turn reduces new immune <span class="nowrap"><icon r></icon>s.</span> Which means immunity plummets in the summer, *creating* large regular spikes in the winter.

Thankfully, the solution to this is pretty straightforward – just vaccinate people every fall/winter, like we do with flu shots:

**(After playing the recording, try simulating your own vaccination campaigns! Remember you can pause/continue the sim at any time)**

<div class="sim">
		<iframe src="sim?stage=yrs-4&format=lines" width="800" height="540"></iframe>
</div>

But here's the scarier question:

What if there's no vaccine for *years*? Or *ever?*

**To be clear: this is unlikely.** Most epidemiologists expect a vaccine in 1 to 2 years. Sure, there's never been a vaccine for any of the other coronaviruses before, but that's because SARS was eradicated quickly, and "the" common cold wasn't worth the investment. 

Still, infectious disease researchers have expressed worries: What if we can't make enough?[^vax_enough] What if we rush it, and it's not safe?[^vax_safe]

[^vax_enough]: “If a coronavirus vaccine arrives, can the world make enough?” [by Roxanne Khamsi, on Nature](https://www.nature.com/articles/d41586-020-01063-8)

[^vax_safe]: “Don’t rush to deploy COVID-19 vaccines and drugs without sufficient safety guarantees” [by Shibo Jiang, on Nature](https://www.nature.com/articles/d41586-020-00751-9)

Even in the nightmare "no-vaccine" scenario, we still have 3 ways out. From most to least terrible:

1) Do intermittent or loose R < 1 interventions, to reach "natural herd immunity". (Warning: this will result in many deaths & damaged lungs. *And* won't work if immunity doesn't last.)

2) Do the R < 1 interventions forever. Contact tracing & wearing masks just becomes a new norm in the post-COVID-19 world, like how STI tests & wearing condoms became a new norm in the post-HIV world.

3) Do the R < 1 interventions until we develop treatments that make COVID-19 way, way less likely to need critical care. (Which we should be doing *anyway!*) Reducing ICU use by 10x is the same as increasing our ICU capacity by 10x:

**Here's a simulation of *no* lasting immunity, *no* vaccine, and not even any interventions – just slowly increasing capacity to survive the long-term spikes:**

<div class="sim">
		<iframe src="sim?stage=yrs-5&format=lines" width="800" height="540"></iframe>
</div>

Even under the *worst* worst-case scenario... life perseveres.

. . .

Maybe you'd like to challenge our assumptions, and try different R<sub>0</sub>'s or numbers. Or try simulating your *own* combination of intervention plans!

**Here's an (optional) Sandbox Mode, with *everything* available. (scroll to see all controls) Simulate & play around to your heart's content:**

<div class="sim">
		<iframe src="sim?stage=SB&format=sb" width="800" height="540"></iframe>
</div>

This basic "epidemic flight simulator" has taught us so much. It's let us answer questions about the past few months, next few months, and next few years.

So finally, let's return to...

<div class="section chapter">
    <div>
		<img src="banners/curve.png" height=480 style="position: absolute;"/>
        <div>The Now</div>
    </div>
</div>

Plane's sunk. We've scrambled onto the life rafts. It's time to find dry land.[^dry_land]

[^dry_land]: Dry land metaphor [from Marc Lipsitch & Yonatan Grad, on STAT News](https://www.statnews.com/2020/04/01/navigating-covid-19-pandemic/)

Teams of epidemiologists and policymakers ([left](https://www.americanprogress.org/issues/healthcare/news/2020/04/03/482613/national-state-plan-end-coronavirus-crisis/), [right](https://www.aei.org/research-products/report/national-coronavirus-response-a-road-map-to-reopening/ ), and [multi-partisan](https://ethics.harvard.edu/covid-roadmap)) have come to a consensus on how to beat COVID-19, while protecting our lives *and* liberties.

Here's the rough idea, with some (less-consensus) backup plans:

![](pics/plan.png)

So what does this mean for YOU, right now?

**For everyone:** Respect the lockdown so we can get out of Phase I asap. Keep washing those hands. Make your own masks. Download a *privacy-protecting* contact tracing app when those are available next month. Stay healthy, physically & mentally! And write your local policymaker to get off their butt and...

**For policymakers:** Make laws to support folks who have to self-isolate/quarantine. Hire more manual contact tracers, *supported* by privacy-protecting contact tracing apps. Direct more funds into the stuff we should be building, like...

**For builders:** Build tests. Build ventilators. Build personal protective equipment for hospitals. Build tests. Build masks. Build apps. Build antivirals, prophylactics, and other treatments that aren't vaccines. Build vaccines. Build tests. Build tests. Build tests. Build hope. 

Don't downplay fear to build up hope. Our fear should *team up* with our hope, like the inventors of airplanes & parachutes. Preparing for horrible futures is how we *create* a hopeful future.

The only thing to fear is the idea that the only thing to fear is fear itself.
