# P01_International_Malnutrition_Study_-Python_-_SQL-
<h2><strong><em>Data Analyst Certification by OpenClassrooms, in partnership with&nbsp;ENSAE-ENSAI</em></strong></h2>
<p><em>Studying malnutrition using Python and SQL on data from FAO</em></p>
<p><em>Skills:</em></p>
<ul>
    <li style="font-style: italic;"><em>Perform complex queries in SQL</em></li>
    <li style="font-style: italic;"><em>Apply relational algebra in R or Python</em></li>
    <li style="font-style: italic;"><em>Use specialized libraries for Data Science</em></li>
    <li style="font-style: italic;"><em>Master the basics of R or Python</em></li>
    <li style="font-style: italic;"><em>Use technical documentation</em></li>
    <li style="font-style: italic;"><em>Recover data from an identified source</em></li>
</ul>
<div>
    <div>
        <div>
            <div>
                <h1>Projet 01 - R&eacute;alisez une &eacute;tude de sant&eacute; publique</h1>
            </div>
        </div>
    </div>
</div>
<h3>Mise en situation</h3>
<p>Vous &ecirc;tes int&eacute;gr&eacute; &agrave; une nouvelle &eacute;quipe de chercheurs de la&nbsp;<a href="https://fr.wikipedia.org/wiki/Organisation_des_Nations_unies_pour_l%27alimentation_et_l%27agriculture">Food and Agriculture Organization of the United Nations (FAO)</a>, l&apos;un des organes qui compose l&apos;ONU et dont l&apos;objectif est d&apos; &laquo; aider &agrave; construire un monde lib&eacute;r&eacute; de la faim &raquo;.</p>
<p>Votre &eacute;quipe est charg&eacute;e de r&eacute;aliser une &eacute;tude de grande ampleur sur le th&egrave;me de la sous-nutrition dans le monde.</p>
<p>Le probl&egrave;me de la faim est complexe et peut avoir de multiples causes, diff&eacute;rentes selon les pays. L&rsquo;&eacute;tape pr&eacute;liminaire de cette &eacute;tude sera donc d&rsquo;&eacute;tablir un &ldquo;&eacute;tat de l&rsquo;art&rdquo; des recherches d&eacute;j&agrave; publi&eacute;es, mais &eacute;galement de mener une &eacute;tude statistique destin&eacute;e &agrave; orienter les recherches vers des pays particuliers, et de mettre en lumi&egrave;re diff&eacute;rentes causes de la faim. Ainsi, une poign&eacute;e de data analysts (dont vous !) a &eacute;t&eacute; s&eacute;lectionn&eacute;e pour mener cette &eacute;tape pr&eacute;liminaire. Lors de la premi&egrave;re r&eacute;union, vous avez &eacute;t&eacute; d&eacute;sign&eacute; pour mettre une place la base de donn&eacute;es que votre &eacute;quipe pourra requ&ecirc;ter (en SQL) &agrave; souhait pour r&eacute;aliser cette &eacute;tude statistique.</p>
<h3>Les donn&eacute;es</h3>
<p>Les donn&eacute;es sont disponibles sur&nbsp;<a href="https://s3.eu-west-1.amazonaws.com/course.oc-static.com/projects/DAN_V1_P3/data.zip">ce lien</a> et sont constitu&eacute;es de 5 fichiers:</p>
<ul>
    <li>fr_animaux.csv : multiples indicateurs de production des produits animaux en 2013</li>
    <li>fr_population.csv: population mondiale par pays en 2013</li>
    <li>fr_vegetaux.csv: multiples indicateurs de production des produits v&eacute;g&eacute;taux en 2013</li>
    <li>fr_céréales.csv: quantit&eacute; de c&eacute;r&eacute;ales produites au niveau mondial en 2013 &nbsp; &nbsp;</li>
    <li>fr_sousalimentation.csv: nombre de personnes sous aliment&eacute;es dans le monde de 2013 &agrave; 2017.</li>
</ul>
<h3>Votre mission</h3>
<p>Vous &ecirc;tes pr&ecirc;t ? Alors c&apos;est parti !</p>
<aside>
    <p>Si vous r&eacute;alisez ce projet en Python, il est vivement conseill&eacute; d&apos;utiliser un notebook Jupyter, et de savoir utiliser les librairies Python pour la data science.&nbsp;<a href="https://openclassrooms.com/fr/courses/4452741-decouvrez-les-librairies-python-pour-la-data-science"><strong>Ce cours</strong></a> vous y aidera. (Les chapitres sur Monty Hall et le Th&eacute;or&egrave;me central limite sortent du scope de ce projet, mais les autres sont fait pour vous !)</p>
</aside>
<h4><strong>Identifiez les grandes tendances</strong></h4>
<p>Une fois les fichiers CSV t&eacute;l&eacute;charg&eacute;s, il vous faudra les charger dans R ou Python, afin d&rsquo;identifier les grandes tendances et vous familiariser avec le jeu de donn&eacute;es.</p>
<p>Pour chacune des tables t&eacute;l&eacute;charg&eacute;es, identifiez les possibles cl&eacute;s primaires, et testez-les (pour plus d&apos;informations, voici&nbsp;<a href="https://openclassrooms.com/courses/initiez-vous-a-lalgebre-relationnelle-avec-le-langage-sql/ne-perdez-pas-de-vue-vos-cles">un chapitre</a> du cours &ldquo;<strong>Initiez-vous &agrave; l&rsquo;alg&egrave;bre relationnelle avec le langage SQL</strong>&rdquo;). Cette &eacute;tape vous permettra de comprendre la &quot;structure&quot; de vos tables, et vous sera utile lorsque vous aurez &agrave; effectuer des jointures.</p>
<p>On commence !</p>
<p>Cr&eacute;ez un dataframe contenant les informations de population de chaque pays. Calculez le nombre total d&rsquo;humains sur la plan&egrave;te. Critiquez votre r&eacute;sultat. En cas d&rsquo;anomalie, analysez et effectuer les corrections n&eacute;cessaires.</p>
<div>
    <p>Question 1 : donnez le r&eacute;sultat de votre calcul pour l&apos;ann&eacute;e 2013.</p>
</div>
<p>Parmi les documents sur les Bilans alimentaires que vous avez t&eacute;l&eacute;charg&eacute;s, il y a des informations redondantes. En effet, pour un pays donn&eacute;, certaines de ces informations peuvent se calculer &agrave; partir d&apos;autres :</p>
<ul>
    <li>Production&nbsp;</li>
    <li>Importations</li>
    <li>Exportations&nbsp;</li>
    <li>Variation de stock&nbsp;</li>
    <li>Disponibilit&eacute; int&eacute;rieure&nbsp;</li>
    <li>Semences&nbsp;</li>
    <li>Pertes&nbsp;</li>
    <li>Nourriture, aussi appel&eacute;e Disponibilit&eacute; alimentaire&nbsp;</li>
    <li>Aliments pour animaux&nbsp;</li>
    <li>Traitement</li>
    <li>Autres utilisations&nbsp;</li>
</ul>
<div>
    <p>Question 2 : Identifiez ces redondances, en donnant votre r&eacute;ponse sous forme de formule math&eacute;matique (pas besoin de coder ici <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABMAAAATCAMAAAEyifZoAAAAY1BMVEVxUy7/wWn/6pj/tl3/0Xz/3Yn//a7/+an/2YT/x3D/tFr/9qX/7p3/1X//vWX/+6z/umHmolD/9KP/5JH/7Jr//7D/uF//znf/y3T/4Y3/xG3Xl0v/sliodjr///8AAAD///+O7quOAAAAIXRSTlP//////////////////////////////////////////wCfwdAhAAAA1ElEQVQYV12PR3JEQQxC+TnO/MkOEg33P6UXbZfLfitKUBKCZSgSTsNGCDrB2zgLPrE0sGVDY9sYrSKEhYWGc5Vhq91xkg3rG0NDezyWS6ZgXVgKzzJsW7Jt2JZUFfcWtOEOz2Pow5CKVCThukmTtAau922bz68MqO/JUlJwXEopGYbNzIb/NtuWmJmsZ6vb3YDp1g54i5oTb/qlowzxMUmSWGdJQdf7Po3P8djn96bpMkMQ+2H+uA/9QpKZKwWLzSdLhXlmfV2xJknytcSffhHx0+8LuWUjlhWB48QAAAAASUVORK5CYII=" title=":soleil:" alt=":soleil:">&nbsp;). C&apos;est une &eacute;quation &agrave; 3 termes de type&nbsp;\(a_1 + a2 + [...] = b_1 + b_2 + [...] = c_1 + c_2 + [...]\)&nbsp;) faisant intervenir chacune des 11 quantit&eacute;s donn&eacute;es ci dessus. Illustrez cette &eacute;quation avec l&apos;exemple du bl&eacute; en France. Pour avoir un indice, cliquez sur &quot;D&eacute;finitions et Standards&quot; sur&nbsp;<a href="http://www.fao.org/faostat/fr/#data/FBS">la page de t&eacute;l&eacute;chargement</a> des donn&eacute;es.</p>
</div>
<div>
    <p>Question 3 : Calculez (pour chaque pays et chaque produit) la disponibilit&eacute; alimentaire en kcal puis en kg de prot&eacute;ines.</p>
</div>
<aside>
    <p>Vous ferez cela &agrave; partir de ces informations :</p>
    <ul>
        <li>Population de chaque pays ;</li>
        <li>Disponibilit&eacute; alimentaire donn&eacute;e pour chaque produit et pour chaque pays en kcal/personne/jour.</li>
        <li>Disponibilit&eacute; alimentaire en prot&eacute;ines donn&eacute;e pour chaque produit et pour chaque pays en g/personne/jour.</li>
    </ul>
</aside>
<div>
    <p>Question 4 : A partir de ces derni&egrave;res informations, et &agrave; partir du poids de la disponibilit&eacute; alimentaire (pour chaque pays et chaque produit), calculez pour chaque produit le ratio &quot;&eacute;nergie/poids&quot;, que vous donnerez en kcal/kg. Vous pouvez v&eacute;rifier la coh&eacute;rence de votre calcul en comparant ce ratio aux donn&eacute;es disponibles sur internet, par exemple en cherchant la&nbsp;<a href="https://fr.wikipedia.org/wiki/%C5%92uf_(aliment)"><strong>valeur calorique d&apos;un oeuf</strong></a>.</p>
</div>
<aside>
    <p>Indication : La disponibilit&eacute; alimentaire en kcal/personne/jour est calcul&eacute;e par la FAO en multipliant la quantit&eacute; Nourriture par le ratio &eacute;nergie/poids (en kcal/kg), puis en le divisant par la population du pays puis par 365. Ici, on vous demande juste de retrouver le ratio &eacute;nergie/poids que la FAO a utilis&eacute; dans son calcul.</p>
</aside>
<p>En suivant la m&ecirc;me m&eacute;thodologie, calculez &eacute;galement le pourcentage de prot&eacute;ines de chaque produit (pour chaque pays). Ce pourcentage est obtenu en calculant le ratio &quot;poids de prot&eacute;ines/poids total&quot; (attention aux unit&eacute;s utilis&eacute;es). Vous pouvez v&eacute;rifier la coh&eacute;rence de votre calcul en comparant ce ratio aux donn&eacute;es disponibles sur internet, par exemple en cherchant la teneur en prot&eacute;ines de l&apos;<a href="https://fr.wikipedia.org/wiki/Avoine_cultiv%C3%A9e">avoine</a>.</p>
<div>
    <p>Question 5 : Citez 5 aliments parmi les 20 aliments les plus caloriques, en utilisant le ratio &eacute;nergie/poids.</p>
    <p>&Eacute;tonnamment, il arrive que ce ratio soit diff&eacute;rent en fonction du pays. Il faudra donc r&eacute;aliser pour chaque aliment une moyenne sur les diff&eacute;rents pays. Vous cr&eacute;erez donc une nouvelle table gr&acirc;ce &agrave; une agr&eacute;gation.<strong>&nbsp;Attention &agrave; bien retirer les valeurs &eacute;gales &agrave; 0 afin de ne pas fausser le calcul de la moyenne</strong>.</p>
    <p>Citez 5 aliments parmi les 20 aliments les plus riches en prot&eacute;ines.</p>
</div>
<aside>
    <p>Pour approfondir la r&eacute;flexion, il est important de se documenter sur la qualit&eacute; des prot&eacute;ines, notamment sur l&apos;indice PDCAAS. Voici les articles Wikipedia correspondant :&nbsp;<a href="https://fr.wikipedia.org/wiki/Score_chimique_corrig%C3%A9_de_la_digestibilit%C3%A9"><strong>fran&ccedil;ais</strong></a>,&nbsp;<a href="https://en.wikipedia.org/wiki/Protein_Digestibility_Corrected_Amino_Acid_Score"><strong>anglais</strong></a>. Cet aspect n&apos;est pas demand&eacute; dans la soutenance, c&apos;est juste pour la culture g&eacute;n&eacute;rale.</p>
</aside>
<div>
    <p>Question 6 : Calculez, pour les produits v&eacute;g&eacute;taux&nbsp;<strong>uniquement</strong>, la disponibilit&eacute; int&eacute;rieure mondiale exprim&eacute;e en kcal.</p>
</div>
<div>
    <p>&nbsp;Question 7 : Combien d&apos;humains pourraient &ecirc;tre nourris si toute la disponibilit&eacute; int&eacute;rieure mondiale de produits v&eacute;g&eacute;taux &eacute;tait utilis&eacute;e pour de la nourriture ? Donnez les r&eacute;sultats en termes de calories, puis de prot&eacute;ines, et exprimez ensuite ces 2 r&eacute;sultats en pourcentage de la population mondiale.</p>
</div>
<div>
    <p>Question 8 : Combien d&apos;humains pourraient &ecirc;tre nourris si toute la disponibilit&eacute; alimentaire en produits v&eacute;g&eacute;taux, la nourriture v&eacute;g&eacute;tale destin&eacute;e aux animaux et les pertes de produits v&eacute;g&eacute;taux &eacute;taient utilis&eacute;s pour de la nourriture ? Donnez les r&eacute;sultats en termes de calories, puis de prot&eacute;ines, et exprimez ensuite ces 2 r&eacute;sultats en pourcentage de la population mondiale.</p>
</div>
<div>
    <p>Question 9 : Combien d&apos;humains pourraient &ecirc;tre nourris avec la disponibilit&eacute; alimentaire mondiale ? Donnez les r&eacute;sultats en termes de calories, puis de prot&eacute;ines, et exprimez ensuite ces 2 r&eacute;sultats en pourcentage de la population mondiale.</p>
</div>
<div>
    <p>&nbsp;Question 10 : A partir des donn&eacute;es t&eacute;l&eacute;charg&eacute;es qui concernent la sous-nutrition, r&eacute;pondez &agrave; cette question : Quelle proportion de la population mondiale est consid&eacute;r&eacute;e comme &eacute;tant en sous-nutrition ?</p>
</div>
<p>&Eacute;tablissez la liste des produits (ainsi que leur code) consid&eacute;r&eacute;s comme des c&eacute;r&eacute;ales selon la FAO.</p>
<p>Rep&eacute;rez dans vos donn&eacute;es les informations concernant les c&eacute;r&eacute;ales (par exemple en cr&eacute;ant une colonne de type bool&eacute;en nomm&eacute;e &quot;is_cereal&quot;).</p>
<div>
    <p>Question 11 : En ne prenant en compte que les c&eacute;r&eacute;ales destin&eacute;es &agrave; l&apos;alimentation (humaine et animale), quelle proportion (en termes de poids) est destin&eacute;e &agrave; l&apos;alimentation animale ?</p>
</div>
<p>S&eacute;lectionnez parmi les donn&eacute;es des bilans alimentaires les informations relatives aux pays dans lesquels la FAO recense des personnes en sous-nutrition.</p>
<p>Rep&eacute;rez les 15 produits les plus export&eacute;s par ce groupe de pays.</p>
<p>Parmi les donn&eacute;es des bilans alimentaires au niveau mondial, s&eacute;lectionnez les 200 plus grandes importations de ces produits (1 importation = une quantit&eacute; d&apos;un produit donn&eacute; import&eacute;e par un pays donn&eacute;)</p>
<p>Groupez ces importations par produit, afin d&apos;avoir une table contenant 1 ligne pour chacun des 15 produits. Ensuite, calculez pour chaque produit les 2 quantit&eacute;s suivantes :</p>
<ul>
    <li>le ratio entre la quantit&eacute; destin&eacute;s aux &quot;Autres utilisations&quot; (Other uses) et la disponibilit&eacute; int&eacute;rieure.</li>
    <li>le ratio entre la quantit&eacute; destin&eacute;e &agrave; la nourriture animale et la quantit&eacute; destin&eacute;e &agrave; la nourriture (animale + humaine)</li>
</ul>
<div>
    <p>Question 12 : Donnez les 3 produits qui ont la plus grande valeur pour chacun des 2 ratios (vous aurez donc 6 produits &agrave; citer).</p>
</div>
<div>
    <p>Question 13 : Combien de tonnes de c&eacute;r&eacute;ales pourraient &ecirc;tre lib&eacute;r&eacute;es si les USA diminuaient leur production de produits animaux de 10% ?</p>
</div>
<div>
    <p>Question 14 : En Tha&iuml;lande, quelle proportion de manioc produit est export&eacute;e ? Quelle est la proportion de personnes en sous-nutrition ?</p>
</div>
<p>&nbsp;</p>
<h4>Entrez vos donn&eacute;es dans une base de donn&eacute;es relationnelle</h4>
<p>Bon, finis les calculs math&eacute;matiques&nbsp;<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABMAAAATCAMAAAEyifZoAAAAb1BMVEX/tFr/wWn/x3D/3Yn/+an/1X//0Xz/6pj/uF//xG1ZgP//5JH/7p3/vWX/9qX/znfmolD/9KM7af//2YT/7Jr/86L/+6z/4Y3/umGUlJQkUun/y3T/tl3//a7//7DXl0uodjr/slj///8AAAD///9MsirYAAAAJXRSTlP///////////////////////////////////////////////8AP89CTwAAAORJREFUGBkFwYVhBEEQA0EdPzP7FmbV+cfoKmFkhwgESk2exMm2mLroBAbZ7tDSvp3Vn9dAhIzAy+E9GcQj5fyc+kAelt1v94uw8Ge142gEYAMIsA0I6mG5VxBr8stzQR5zTsPfxrqc8rd5q6LL/nRrt00UeZ77T0RYFMvhgqBGdBUE2AYEgF0jotoACPB6HV/jdRnu52JAuF6Tc87pOUzertXI9TGmnFtLrZ37fo1q+bI/jGlnN/vWrRHFcp2H+3s/zP1xVUSoWrh22629UdgRx2oEuCgiImLTFwMCwK6llGoD8A9QhyaoQuuUoQAAAABJRU5ErkJggg==" title=":'(" alt=":'(">, passons &agrave; de la technique, de la vraie !</p>
<p>Transformez vos donn&eacute;es en un format propice &agrave; l&rsquo;utilisation souhait&eacute;e par les utilisateurs finaux, qui utiliserons votre base via le langage SQL. Une fois les donn&eacute;es correctement format&eacute;es, vous les int&eacute;grerez dans une base de donn&eacute;es.</p>
<aside>
    <p>Le choix de la technologie utilis&eacute;e est libre. Vous en trouverez un petit tour d&apos;horizon dans le chapitre&nbsp;<a href="https://openclassrooms.com/fr/courses/1946386-comprendre-le-web/6874684-decouvrez-les-bases-de-donnees"><strong>Les bases de donn&eacute;es</strong></a> du cours&nbsp;<em>Comprendre le web</em>.</p>
    <p>Si vous n&apos;avez jamais utilis&eacute; de syst&egrave;me de gestion de base de donn&eacute;es relationnelles (SGBR), nous vous conseillons d&apos;utiliser&nbsp;<em>SQL-lite</em>. Pour savoir comment l&apos;utiliser, la vid&eacute;o de&nbsp;<a href="https://openclassrooms.com/courses/initiez-vous-a-lalgebre-relationnelle-avec-le-langage-sql/comprenez-les-bases-de-donnees-sql"><strong>ce chapitre</strong></a> peut vous &ecirc;tre utile.</p>
    <p>Si vous &ecirc;tes plus aventurier , un cours sur&nbsp;<a href="https://openclassrooms.com/courses/administrez-vos-bases-de-donnees-avec-mysql"><strong>la technologie&nbsp;</strong><strong><em>MySQL</em></strong></a> est &eacute;galement disponible sur OpenClassrooms : les chapitres utiles seront les 10 premiers (de&nbsp;<em>Introduction</em> &agrave;&nbsp;<em>Suppression et modification de donn&eacute;es</em>).</p>
</aside>
<aside>
    <p>Pour exporter un dataframe de R ou Python vers une base de donn&eacute;es, l&apos;une des solutions est de passer via un fichier CSV. Sous Python, utilisez to_csv :</p>
    <p>&nbsp;</p>
    <pre><code><div><div><div>df.to_csv(&quot;export.csv&quot;, index = False)</div></div></div></code></pre>
    <p>Sous R, utilisez write.csv :</p>
    <pre><code><div><div><div>write.csv(df, file = &quot;export.csv&quot;, row.names=FALSE)</div></div></div></code></pre>
    <p>Ensuite, en fonction de votre SGBDR, recherchez comment importer un fichier CSV dans une table. Pour ceci, votre moteur de recherche internet est votre meilleur ami (par exemple, recherchez :&nbsp;<em>&quot;import a csv file into PostgreSQL&quot;</em>).</p>
    <p>Si vous utilisez le SGBDR SQLite, et que vous le manipulez gr&acirc;ce au logiciel SQLiteStudio, alors cliquez sur &quot;Outils&quot; puis sur &quot;Importer&quot; (&agrave; faire une fois que votre base de donn&eacute;es est cr&eacute;&eacute;e, comme indiqu&eacute; sur cette&nbsp;<a href="https://openclassrooms.com/courses/initiez-vous-a-lalgebre-relationnelle-avec-le-langage-sql/comprenez-les-bases-de-donnees-sql">vid&eacute;o</a>) :</p>
    <p><img src="https://user.oc-static.com/upload/2018/03/01/15199010719158_skeluc.png" alt=""></p>
    <p>Une autre solution, plus &eacute;l&eacute;gante, consiste &agrave; utiliser une librairie Python ou R permettant de se connecter directement &agrave; votre SGBDR, comme par exemple les librairies&nbsp;<em>RMySQL</em>,&nbsp;<em>psycopg2</em>, etc.</p>
</aside>
<p>Votre base devra contenir ces diff&eacute;rentes tables :</p>
<ul>
    <li>Une table appel&eacute;e&nbsp;<strong>population</strong>, contenant l<em>a population de chaque pays pour 2013. Elle devra contenir 4 c</em>olonnes :&nbsp;<strong>pays</strong>,&nbsp;<strong>code_pays</strong>,&nbsp;<strong>annee</strong>,&nbsp;<strong>population</strong>.</li>
</ul>
<div>
    <p>Question 15 : Proposez une cl&eacute; primaire pertinente pour cette table.</p>
</div>
<ul>
    <li>Une table appel&eacute;e&nbsp;<strong>dispo_alim</strong>contenant pour chaque pays et pour chaque produit en 2013, les informations suivantes:<ul>
            <li>la nature du produit (deux valeurs possibles : &ldquo;animal&rdquo; ou &ldquo;v&eacute;g&eacute;tal&rdquo;)</li>
            <li>disponibilit&eacute; alimentaire en tonnes</li>
            <li>disponibilit&eacute; alimentaire en Kcal/personne/jour</li>
            <li>disponibilit&eacute; alimentaire de prot&eacute;ines en g/personne/jour</li>
            <li>disponibilit&eacute; alimentaire de mati&egrave;res grasses en g/personne/jour</li>
        </ul>
    </li>
    <li>Elle devra contenir ces colonnes : pays, code_pays, annee, produit, code_produit, origin, dispo_alim_tonnes, dispo_alim_kcal_p_j, dispo_prot, dispo_mat_gr</li>
</ul>
<div>
    <p>Question 16 : Proposez une cl&eacute; primaire pertinente pour cette table.</p>
</div>
<ul>
    <li>Une table appel&eacute;e&nbsp;<strong>equilibre_prod</strong>contenant pour chaque pays et pour chaque produit en 2013, les quantit&eacute;s suivantes :<ul>
            <li>disponibilit&eacute; int&eacute;rieure</li>
            <li>aliments pour animaux</li>
            <li>semences</li>
            <li>pertes</li>
            <li>transform&eacute;s</li>
            <li>nourriture</li>
            <li>autres utilisations</li>
        </ul>
    </li>
    <li>Elle devra contenir ces colonnes : pays, code_pays, annee, produit, code_produit, dispo_int, alim_ani, semences, pertes, transfo, nourriture, autres_utilisations.</li>
</ul>
<div>
    <p>Question 17 : Proposez une cl&eacute; primaire pertinente pour cette table.</p>
</div>
<ul>
    <li>Une table appel&eacute;e&nbsp;<strong>sous_nutrition</strong>, contenant le nombre de personnes en sous-alimentation pour chaque pays en 2013. Elle devra contenir 4 colonnes :&nbsp;<strong>pays</strong>,&nbsp;<strong>code_pays</strong>,&nbsp;<strong>annee</strong>,&nbsp;<strong>nb_personnes</strong>.</li>
</ul>
<div>
    <p>Question 18 : Vous vous en doutez... proposez encore une fois une cl&eacute; primaire pertinente pour cette table !</p>
</div>
<div>
    <p>Question 19 : &Eacute;crivez les requ&ecirc;tes SQL permettant de conna&icirc;tre&hellip;</p>
    <ul>
        <li>Les 10 pays ayant le plus haut ratio&nbsp;<strong>disponibilit&eacute; alimentaire/habitant&nbsp;</strong>en termes de prot&eacute;ines (en kg) par habitant,&nbsp;<strong>puis</strong> en termes de kcal par habitant.</li>
        <li>Pour l&apos;ann&eacute;e 2013, les 10 pays ayant le plus faible ratio&nbsp;<strong>disponibilit&eacute; alimentaire/habitant</strong> en termes de prot&eacute;ines (en kg) par habitant.</li>
        <li>La quantit&eacute; totale (en kg) de produits perdus par pays en 2013.</li>
        <li>Les 10 pays pour lesquels la proportion de personnes sous-aliment&eacute;es est la plus forte.</li>
        <li>Les 10 produits pour lesquels le ratio&nbsp;<strong>Autres utilisations/Disponibilit&eacute; int&eacute;rieure</strong> est le plus &eacute;lev&eacute;.</li>
    </ul>
</div>
<div>
    <p>Question 20 : pour quelques-uns des produits identifi&eacute;s dans cette derni&egrave;re requ&ecirc;te SQL, supposez quelles sont ces &quot;autres utilisations&quot; possibles (recherchez sur Internet !)</p>
</div>
<h4>&nbsp;</h4>
<h4>Enrichissez votre analyse</h4>
<p>Lors de votre pr&eacute;sentation, vous pr&eacute;senterez les pistes &eacute;tudi&eacute;es jusqu&apos;&agrave; maintenant gr&acirc;ce aux donn&eacute;es de la FAO. En r&eacute;alit&eacute;, vous n&apos;&ecirc;tes pas le/la premier&middot;e &agrave; &eacute;tudier ce ph&eacute;nom&egrave;ne (bien heureusement!). Veillez donc &agrave; bien confirmer vos intuitions par des recherches sur internet : votre mentor vous fournira des sources.</p>
<p>Pour une bonne analyse, le data analyst doit comprendre le domaine qu&apos;il &eacute;tudie. On appelle cela les &nbsp;&quot;connaissances m&eacute;tier&quot;. A partir des sources fournies par votre mentor, il vous sera donc &eacute;galement demand&eacute; de citer d&apos;autres causes de la faim, et d&apos;enrichir votre analyse de nouveaux chiffres. Si vous &ecirc;tes motiv&eacute;s, vous pouvez m&ecirc;me v&eacute;rifier certains des chiffres cit&eacute;es dans les sources &agrave; partir des donn&eacute;es de la FAO.&nbsp;<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABMAAAATCAMAAAEyifZoAAAAbFBMVEX/wWn/tFr/2YT/6pj/+an/3Yn/0Xz/7p3/vWX/uF//xG3/////9qX/umH/+6z/5JH/1X//znf/7Jr/9KPmolD/4Y3/86KUlJSkd0L/y3RqSCD/tl3/x3DXl0v//a7//7Codjr/slgAAAD///8cVNK0AAAAJHRSTlP//////////////////////////////////////////////wBYLA0NAAAA5ElEQVQYV11PRXLFUAAi7vK1kjwB7n/HLjJdtDsYGASWIRGmYSMK2uE5loJ3ELBlQ7GCUaUNwnk7aJiFDFtV99plw/eY0ns6aaip1vu5kIK1HBJ7GbYt2TZsS7pQ7qoy2/AR09q0wVCdUpy+BuE5p1RrLAKe2zyX/cAAte25kBQcFokMhp1J5H/JtqVMMl+1l3o86rV+VE15C5dP+RFTSim+m/02HlmG8r2On99KsfvQeR7Mgp5bV8cU166cJhxkEJTbpnxtTXv2R0GyyIKVMY7qh4Ik2efrusLFOZzhz74Qwu++HxuXJSXJNKbZAAAAAElFTkSuQmCC" title=";)" alt=";)"></p>
<p>Notamment, cherchez les r&eacute;ponses &agrave; ces questions :</p>
<ul>
    <li>Combien de personnes d&eacute;c&egrave;dent des causes de la faim ?</li>
    <li>Quelles sont les pr&eacute;visions de population mondiale en 2050 ?</li>
</ul>
<p>&nbsp;</p>
<h3>Livrables&nbsp;</h3>
<p>Voici les livrables attendus, que vous transmettrez dans une archive ZIP :</p>
<ul>
    <li>Le&nbsp;<strong>code</strong> en R ou en Python qui vous a permis de calculer chacune des r&eacute;ponses aux questions 1 &agrave; 14.</li>
    <li>Le&nbsp;<strong>code</strong> en R, Python et/ou SQL vous ayant permis d&apos;enregistrer les donn&eacute;es dans la base de donn&eacute;es</li>
    <li>Les&nbsp;<strong>requ&ecirc;tes SQL</strong> vous ayant permis de r&eacute;pondre aux questions 15 &agrave; 20.&nbsp;</li>
</ul>
