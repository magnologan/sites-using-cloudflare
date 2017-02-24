# List of Sites affected by Cloudflare's #Cloudbleed HTTPS Traffic Leak

This is a (work-in-progress) list of domains affected by the [CloudBleed HTTPS traffic leak](https://blog.cloudflare.com/incident-report-on-memory-leak-caused-by-cloudflare-parser-bug/).
Original vuln [thread](https://bugs.chromium.org/p/project-zero/issues/detail?id=1139) by Google Project Zero.

Cloudflare has not provided an official list of affected domains, and likely will not due to privacy concerns.  I'm compiling an unofficial list here so you know what passwords to change.

## Impact

**Between 2016-09-22 - 2017-02-18 passwords, private messages, API keys, and other sensitive data were leaked by Cloudflare to random requesters.**
Data was cached by search engines, and may have been collected by random adversaries over the past few months.

 "The greatest period of impact was from February 13 and February 18 with around 1 in every 3,300,000 HTTP requests through Cloudflare potentially resulting in memory leakage (that’s about 0.00003% of requests), potential of 100k-200k paged with private data leaked every day" -- [source](https://news.ycombinator.com/item?id=13719518)

You can see some of the leaked data yourself in search engine caches: https://duckduckgo.com/?q=+%7B%22scheme%22%3A%22http%22%7D+CF-Host-Origin-IP&t=h_&ia=web

## What should I do?

Check your password managers and **change all your passwords**, especially those on these affected sites.
Rotate API keys & secrets, and confirm you have 2-FA set up for important accounts.
Theoretically sites not in this list can also be affected (because an affected site could have made an API request to a non-affected one), so to be safe you should probably change all your important passwords.

**Submit PR's to add domains that you know are using cloudflare**

I'm working on running a DNS scraper that will add thousands more domains to this list automatically, so check back periodically for updates as we find more domains.

Some sources:
 - https://stackshare.io/cloudflare
 - https://wappalyzer.com/applications/cloudflare
 - DNS scraper I'm running on Alexa top 10,000 sites (grepping for cloudflare in results)
 - https://www.cloudflare.com/ips/  (going to find sites that resolve to these IPs next)
 - http://www.crimeflare.com/cfs.html (scrape of all cloudflare customers)

I'd rather be safe than sorry so I've included any domain here that remotely touches cloudflare.
If I've made a mistake and you believe your site is not affected, submit a PR and I will merge it ASAP, I don't want to hurt anyone's reputation unecessarily.

You can also ping me on twitter [@theSquashSH](https://twitter.com/thesquashsh) and I'll respond as soon as I can.


## Full List

**Download the [full list.zip](https://github.com/pirate/sites-using-cloudflare/raw/master/sorted_unique.zip) (21mb)**

4,287,625 potentially affected domains.  Download this file, unzip it, then run `grep domaintocheck.com < sorted_unique_cf.txt` to see if a domain is present.


## Notable Sites

- authy.com
- coinbase.com
- betterment.com
- transferwise.com
- prosper.com
- digitalocean.com
- patreon.com
- bitpay.com
- news.ycombinator.com
- producthunt.com
- stackoverflow.com
- medium.com
- reddit.com
- 4chan.org
- yelp.com
- okcupid.com
- zendesk.com
- uber.com
- namecheap.com
- poloniex.com
- localbitcoins.com
- kraken.com
- 23andme.com
- fastmail.com (does not proxy TLS, probably safe from this attack)
- 1password.com ([not affected](https://discussions.agilebits.com/discussion/comment/356869/#Comment_356869))

## Alexa Top 10,000 affected sites:

- upwork.com
- codepen.io
- fiverr.com
- thepiratebay.org
- extratorrent.com
- getbootstrap.com
- jquery.com
- laravel.com
- laracasts.com
- seriouseats.com
- bitdefender.com
- ziprecruiter.com
- glassdoor.com
- pastebin.com
- fitbit.com
- discordapp.com
- change.org
- feedly.com
- zoho.com
- irccloud.com


- 000webhost.com
- 1001freefonts.com
- 101greatgoals.com
- 10minutemail.com
- 123telugu.com
- 1hhhh.net
- 1jux.net
- 1news.az
- 1sale.com
- 1stwebdesigner.com
- 24horas.cl
- 24sata.hr
- 2ch-c.net
- 2ch.hk
- 2ch.net
- 2ip.ru
- 3bmeteo.com
- 4chan.org
- 4dsply.com
- 4pda.ru
- 4tube.com
- 5giay.vn
- 800notes.com
- 96down.com
- abidjan.net
- abs-cbnnews.com
- adafruit.com
- add-anime.net
- addicted2success.com
- addictinginfo.org
- addmefast.com
- addtoany.com
- adf.ly
- adfoc.us
- ads-id.com
- adult-empire.com
- advfn.com
- adxpansion.com
- aflam4you.tv
- aflamneek.com
- aftabir.com
- agilebits.com
- ahlamontada.com
- ahlynews.com
- ahnegao.com.br
- aitnews.com
- aksam.com.tr
- aktifhaber.com
- al-akhbar.com
- aleqt.com
- alexaboostup.com
- alfajertv.com
- alfavita.gr
- alhilal.com
- alison.com
- alistapart.com
- aljaras.com
- allanalpass.com
- all.biz
- allkpop.com
- allmyvideos.net
- alltop.com
- almaany.com
- almasryalyoum.com
- almesryoon.com
- alnaharegypt.com
- alphacoders.com
- alrakoba.net
- alternativeto.net
- alternet.org
- alwafd.org
- alwatanvoice.com
- alweeam.com.sa
- amadershomoybd.com
- amarujala.com
- amino.dk
- anandabazar.com
- androidauthority.com
- androidcentral.com
- androidpolice.com
- angloinfo.com
- anime44.com
- animeflv.net
- animeid.tv
- animenewsnetwork.com
- anipo.jp
- anitube.se
- ann.az
- annunci69.it
- antarvasna.com
- antena3.ro
- antyweb.pl
- any.gs
- ap7am.com
- apherald.com
- apne.tv
- aporrea.org
- appadvice.com
- appbrain.com
- appstorm.net
- arabsh.com
- archive.is
- argentinawarez.com
- arioo.com
- aristeguinoticias.com
- armorgames.com
- arouraios.gr
- articlesnatch.com
- ashleymadison.com
- ashleyrnadison.com
- atlas.sk
- attracta.com
- atwiki.jp
- authorstream.com
- avaaz.org
- avaz.ba
- avazutracking.net
- avito.ma
- avito.ru
- avn.info.ve
- azertag.com
- aznews.az
- azyya.com
- b1.org
- bab.la
- babyoye.com
- backlinks.com
- bakufu.jp
- bancdebinary.com
- banglanews24.com
- barstoolsports.com
- bbspink.com
- bc.vc
- bdr130.net
- beeg.com
- behindwoods.com
- belboon.com
- bestblackhatforum.com
- bezaat.com
- bicaps.com
- bigrock.in
- bikroy.com
- billiger.de
- billionuploads.com
- binaryoptionsnewbies.com
- binsearch.info
- bitcoincharts.com
- bitshare.com
- bitsnoop.com
- bizsugar.com
- blackhatteam.com
- blackhatworld.com
- blankrefer.com
- bleepingcomputer.com
- blekko.com
- blinklist.com
- blip.tv
- blockchain.info
- blogcatalog.com
- blogfa.com
- blogs.com
- boards.ie
- boo-box.com
- boxden.com
- boxingscene.com
- brainpickings.org
- brainyquote.com
- brandyourself.com
- brasil247.com
- briian.com
- broadwayworld.com
- bronto.com
- brooonzyah.net
- brusheezy.com
- btc-e.com
- bubblews.com
- bufferapp.com
- bukkit.org
- burbuja.info
- burnews.com
- business2blogger.com
- businessforhome.org
- buzztheme.net
- camplace.com
- cancan.ro
- careers360.com
- car.gr
- catracalivre.com.br
- cbox.ws
- cda.pl
- ce4arab.com
- celebuzz.com
- charter97.org
- chatrandom.com
- cheathappens.com
- chinavasion.com
- chomikuj.pl
- christian-dogma.com
- cima4u.com
- ciudad.com.ar
- ck101.com
- clasicooo.com
- classifiedads.com
- cleanfiles.net
- clickbank.com
- clickbank.net
- clip.vn
- clixsense.com
- cloudflare.com
- clubedohardware.com.br
- cmse.ru
- codepen.io
- codeschool.com
- coinbase.com
- col3negoriginal.lk
- colourlovers.com
- comicbookmovie.com
- compucalitv.com
- copacet.com
- cpalead.com
- cpasbien.com
- cpasbien.me
- crackberry.com
- creativecommons.org
- cricfree.tv
- crictime.com
- crocko.com
- crosswalk.com
- crunchbase.com
- crunchyroll.com
- cs-cart.com
- cssdeck.com
- cucirca.eu
- curse.com
- cyanogenmod.org
- cyberchimps.com
- cyberpresse.ca
- dailycaller.com
- daisycon.com
- dangerousminds.net
- dardarkom.com
- dashnet.org
- davidicke.com
- davidwalsh.name
- dawanda.com
- dawn.com
- de10.com.mx
- deadline.com
- defaultsear.ch
- defencenet.gr
- definebabe.com
- demandforce.com
- demotywatory.pl
- deperu.com
- desidime.com
- designboom.com
- designfloat.com
- designtaxi.com
- desirulez.net
- desi-tashan.com
- desitorrents.com
- desmotivaciones.es
- destructoid.com
- deutsche-wirtschafts-nachrichten.de
- dev-point.com
- dhakatimes24.com
- diariocontraste.com
- diariodemorelos.com
- diario.mx
- diary.ru
- dicelacancion.com
- diffen.com
- digikala.com
- digitalocean.com
- digital-photography-school.com
- digitalpoint.com
- discuss.com.hk
- divxplanet.com
- divxstage.eu
- dizi-mag.com
- djmaza.info
- dlink.com
- dl-protect.com
- dnevnik.hr
- doba.com
- doisongphapluat.com
- doityourself.com
- doostiha.ir
- dostor.org
- dota2lounge.com
- downloadatoz.com
- downloadming.me
- downloads.nl
- dpstream.net
- drakulastream.eu
- dramasonline.com
- dreamamateurs.com
- dreamincode.net
- dreamteammoney.com
- dreamtemplate.com
- droid-life.com
- drudgereport.com
- dryicons.com
- dsdomination.com
- duedil.com
- dumpert.nl
- dx.com
- eatlocalgrown.com
- ebs.in
- e-cigarette-forum.com
- econsultancy.com
- edublogs.org
- e-estekhdam.com
- efukt.com
- egaliteetreconciliation.fr
- egyup.com
- el-ahly.com
- elance.com
- el-balad.com
- elbilad.net
- elbotola.com
- eldia.com.ar
- elephantjournal.com
- elespectador.com
- elfagr.org
- elheddaf.com
- elitepvpers.com
- elitetorrent.net
- elkhabar.com
- elpais.com.uy
- elshaab.org
- elwatannews.com
- el-wlid.com
- emailmeform.com
- emoneyspace.com
- e-monsite.com
- encuentra24.com
- englishforums.com
- enjoydressup.com
- enwdgts.com
- epidemz.net
- erepublik.com
- ero-advertising.com
- ethnos.gr
- etxt.ru
- excellentbux.net
- expatriates.com
- experts-exchange.com
- explosm.net
- express.com.pk
- express.pk
- extabit.com
- extratorrent.cc
- extratorrent.com
- eyny.com
- ezilon.com
- eztv.it
- fabthemes.com
- fakenamegenerator.com
- fakku.net
- fanpop.com
- fansided.com
- fansshare.com
- fanswong.com
- fantasy8.com
- fap.to
- fatakat.com
- feedio.net
- feedly.com
- fenopy.se
- ffffound.com
- filecloud.io
- filelist.ro
- filenuke.com
- filesfetcher.com
- filgoal.com
- filmey.com
- filmifullizle.com
- fishki.net
- fiverr.com
- fok.nl
- fontspace.com
- forbes.ru
- forex4you.org
- forexpeacearmy.com
- forgifs.com
- foro20.com
- foroactivo.com
- forobeta.com
- forocoches.com
- forosdelweb.com
- forumactif.com
- forumactif.org
- forum.hr
- forumophilia.com
- forumotion.com
- fotka.pl
- fotolog.net
- foundationapi.com
- fragrantica.com
- frandroid.com
- freakshare.com
- freekaamaal.com
- freelanceswitch.com
- freeonlinegames.com
- freepatriot.org
- freepornvs.com
- free-press-release.com
- free-tv-video-online.me
- freewebs.com
- freshdesignweb.com
- fresherslive.com
- frmtr.com
- frombar.com
- fsiblog.com
- fssnet.co.in
- fuckbooknet.net
- fullhdfilmizle.org
- fun698.com
- funnyjunk.com
- funnymama.com
- fuskator.com
- futhead.com
- fux.com
- gaaks.com
- game321.com
- gameblog.fr
- game-debate.com
- gamefront.com
- gamer.com.tw
- games.la
- gamestorrents.com
- gametracker.com
- gamevicio.com
- gamme.com.tw
- geenstijl.nl
- genteflow.com
- geo.tv
- getbootstrap.com
- getcashforsurveys.com
- getfireshot.com
- getglue.com
- gezginler.net
- gezinti.com
- gfxtra.com
- gfy.com
- ghanaweb.com
- ghost.org
- gigaom.com
- gigporno.com
- gistmania.com
- glassdoor.com
- globalewallet.com
- globovision.com
- gmane.org
- godvine.com
- gofuckbiz.com
- gogoanime.com
- goldenline.pl
- goldesel.to
- goldporntube.com
- goldprice.org
- gooddrama.net
- good.is
- goodsearch.com
- gossiplankanews.com
- gottabemobile.com
- graaam.com
- grasscity.com
- greenwichmeantime.com
- grindtv.com
- gsmhosting.com
- gsmspain.com
- gtaforums.com
- gulli.com
- gun.az
- gyazo.com
- h2porn.com
- hackforums.net
- haivl.com
- haivl.tv
- hamariweb.com
- hammihan.com
- haqqin.az
- hardsextube.com
- hardwareluxx.de
- hawamer.com
- hawkhost.com
- hayah.cc
- hdfcbank.com
- healthkart.com
- heavy-r.com
- hespress.com
- hibapress.com
- hightrafficacademy.com
- hihi2.com
- hiphopdx.com
- hir.ma
- hitleap.com
- hizliresim.com
- hkgolden.com
- hobbyking.com
- hockeysfuture.com
- holiday-weather.com
- hostgator.com.br
- hostgator.in
- hostingflame.org
- hotair.com
- hotarabchat.com
- hotfrog.com
- hottube.me
- hotukdeals.com
- howtoforge.com
- hubpages.com
- hugedomains.com
- hugefiles.net
- humblebundle.com
- humoron.com
- hvg.hu
- icefilms.info
- iconarchive.com
- identi.li
- idlebrain.com
- iitv.info
- ijreview.com
- ikman.lk
- ilbe.com
- ilyke.net
- imagecurl.org
- imageporter.com
- imagetwist.com
- imgchili.com
- imgchili.net
- imgdino.com
- imgserve.net
- imgtiger.com
- imore.com
- impiego24.it
- inbound.org
- index.hr
- index-of-mp3s.com
- india-forums.com
- indiafreestuff.in
- indiangilma.com
- indianpornvideos.com
- indiansexstories.net
- indowebster.com
- inews.gr
- infibeam.com
- infolinks.com
- informationng.com
- informe21.com
- inkedmag.com
- inlinkz.com
- inquirer.net
- insight.ly
- instantcheckmate.com
- intercambiosvirtuales.org
- intereconomia.com
- internethaber.com
- interpals.net
- ioffer.com
- iol.co.za
- iphoneogram.com
- iphones.ru
- ipiccy.com
- iptorrents.com
- islammemo.cc
- italiafilm.tv
- it-ebooks.info
- ittefaq.com.bd
- ixl.com
- jagobd.com
- jang.com.pk
- javascript.ru
- jeanmarcmorandini.com
- j.gs
- jne.co.id
- joemonster.org
- johnchow.com
- jonloomer.com
- joomla.fr
- joomlart.com
- joomshaper.com
- jotform.com
- jquery.com
- jquerymobile.com
- jqueryui.com
- jusbrasil.com.br
- justunfollow.com
- jutarnji.hr
- jvzoo.com
- kaban.tv
- kalahari.com
- kanui.com.br
- karnaval.com
- katproxy.com
- keep2share.cc
- khabarfarsi.com
- khmerload.com
- kingworldnews.com
- kinogo.net
- kinox.to
- kinozal.tv
- kleiderkreisel.de
- klicktel.de
- klix.ba
- kn3.net
- komikid.com
- korabia.com
- kora-online.tv
- korben.info
- krucil.net
- ktonanovenkogo.ru
- kure.tv
- kwejk.pl
- lankacnews.com
- lapatilla.com
- laravel.com
- largeporntube.com
- latribune.fr
- laughingsquid.com
- layalina.com
- lebuteur.com
- legiaodosherois.com.br
- lenskart.com
- levelup.com
- lewrockwell.com
- libertagia.com
- life.com.tw
- light-dark.net
- liilas.com
- lik.cl
- like4like.org
- likesasap.com
- likes.com
- limetorrents.com
- linkbucks.com
- linkcollider.com
- linkconnector.com
- linkcrypt.ws
- linksmanagement.com
- listcovery.com
- listverse.com
- livememe.com
- lolinez.com
- lolnexus.com
- looti.net
- lumfile.com
- m5zn.com
- mafiashare.net
- makeameme.org
- makeupandbeauty.com
- makezine.com
- malaysiakini.com
- malwaretips.com
- managewp.com
- mangafox.me
- mangahere.com
- mangapanda.com
- mangareader.net
- mangastream.com
- manoto1.com
- maplestage.com
- marathonbet.com
- marketglory.com
- marunadanmalayali.com
- matchesfashion.com
- mathsisfun.com
- matthewwoodward.co.uk
- maultalk.com
- maxicep.com
- mazika2day.com
- mediapart.fr
- mediatakeout.com
- mediatraffic.com
- medium.com
- megashare.info
- members.webs.com
- memecenter.com
- memedad.com
- meme-lol.com
- menshealth.com
- merca20.com
- mforos.com
- mg.co.za
- micromaxinfo.com
- microworkers.com
- mindmeister.com
- mindtools.com
- minecraftforum.net
- minijuegos.com
- minutebuzz.com
- mitbbs.com
- mixcloud.com
- mixedmartialarts.com
- mkyong.com
- mmo-champion.com
- mobafire.com
- mobilism.org
- moddb.com
- moneymakergroup.com
- monova.org
- moodle.org
- morguefile.com
- moveon.org
- movie4k.to
- movie-blog.org
- movieweb.com
- mp3skull.com
- mp3xd.com
- mstaml.com
- musavat.com
- mybb.com
- mybroadband.co.za
- mydealz.de
- mydigitallife.info
- myegy.com
- mygully.com
- mylikes.com
- mymodernmet.com
- mynewsdesk.com
- myorderbox.com
- mysavings.com
- mysmartprice.com
- myvidster.com
- n4g.com
- n4hr.com
- naijapals.com
- naij.com
- nairaland.com
- namepros.com
- naosalvo.com.br
- nationalreview.com
- natunbarta.com
- ncrypt.in
- neswangy.net
- netbarg.com
- network-tools.com
- newgrounds.com
- news.am
- newtvworld.com
- nexusmods.com
- nguoiduatin.vn
- nicozon.net
- ninisite.com
- niusnews.com
- nmisr.com
- nodejs.org
- notdoppler.com
- notebookcheck.net
- noticiaaldia.com
- noticierodigital.com
- novafile.com
- nowgamez.com
- nrc.nl
- nuevoloquo.com
- nulled.cc
- nullrefer.com
- nur.kz
- nyaa.se
- ocioso.com.br
- odesk.com
- offervault.com
- ofreegames.com
- ojooo.com
- omegle.com
- on.cc
- onedio.com
- onlinekhabar.com
- onlinesoccermanager.com
- online-stopwatch.com
- oodle.com
- opencart.com
- openclassrooms.com
- opensubtitles.org
- opinionlab.com
- opposingviews.com
- optimizepress.com
- optionbit.com
- orgasmatrix.com
- osdir.com
- pagina12.com.ar
- pandodaily.com
- paperblog.com
- pastebin.com
- patient.co.uk
- paxum.com
- pbagora.com.br
- pcadvisor.co.uk
- pccomponentes.com
- pcgames.de
- pcgameshardware.de
- pcinpact.com
- pdfonline.com
- peb.pl
- peerfly.com
- peliculas4.com
- peliculasyonkis.com
- penguinvids.com
- penny-arcade.com
- persiantools.com
- petapixel.com
- phimvang.com
- phpbb.com
- picstopin.com
- pijamasurf.com
- pik.ba
- pimpandhost.com
- pingdom.com
- pirateproxy.net
- pirateproxy.se
- piratestreaming.tv
- pixhost.org
- pjmedia.com
- planetminecraft.com
- played.to
- playvid.com
- playxn.com
- plugrush.com
- plus28.com
- popcash.net
- poringa.net
- pornbb.org
- pornerbros.com
- pornper.com
- porntube.com
- porntubevidz.com
- pornup.me
- portalnet.cl
- postplanner.com
- prefiles.com
- premiere.fr
- premiumwp.com
- prevention.com
- primewire.ag
- privatehomeclips.com
- priyo.com
- prlog.ru
- prntscr.com
- problogger.net
- proboards.com
- proceso.com.mx
- promiflash.de
- promptfile.com
- propakistani.pk
- proprofs.com
- psychcentral.com
- ptt.cc
- pubdirecte.com
- publika.az
- puls24.mk
- punchng.com
- purpleporno.com
- putlocker.bz
- putlocker.com
- putlocker.ws
- puu.sh
- q8yat.com
- qafqazinfo.az
- q-ask.com
- qatarliving.com
- qaynar.info
- q.gs
- questionablecontent.net
- r10.net
- racing-games.com
- radiojavan.com
- rahnama.com
- random.org
- ranker.com
- rapgenius.com
- rapradar.com
- rassd.com
- raventools.com
- rawstory.com
- reactiongifs.com
- readms.com
- realfarmacy.com
- realitatea.net
- redbubble.com
- re-direcciona.me
- reduxmediia.com
- relink.us
- resellerclub.com
- residentadvisor.net
- rghost.ru
- ripoffreport.com
- robtex.com
- rockpapershotgun.com
- roro44.com
- rosbalt.ru
- rozee.pk
- rubias19.com
- runetki.com
- runetki.tv
- runnersworld.com
- rus.ec
- ryushare.com
- sa.ae
- saaid.net
- sabq.org
- sadistic.pl
- saharareporters.com
- samanyoluhaber.com
- sankakucomplex.com
- say7.info
- sayidaty.net
- scamadviser.com
- scriptmafia.org
- sdpnoticias.com
- searchengines.ru
- searchere.info
- searchquotes.com
- sedty.com
- seemorgh.com
- seenive.com
- semprot.com
- seneweb.com
- seozenlaunch.com
- sergey-mavrodi.com
- sergeymavrodi.com
- sergey-mavrodi-mmm.net
- serials.ws
- serienjunkies.org
- series.ly
- seriesyonkis.com
- seriouseats.com
- serviporno.com
- seslisozluk.net
- sethgodin.typepad.com
- sexytube.me
- shahvani.com
- shareasale.com
- share-links.biz
- share-online.biz
- sheknows.com
- shiftdelete.net
- shoghlanty.com
- shorouknews.com
- shortp.com
- shoutmeloud.com
- sia.az
- siasat.pk
- siliconrus.com
- simplyrecipes.com
- sinembargo.mx
- sipse.com
- sitedeals.nl
- sitetalk.com
- siyahgazete.com
- skidrowcrack.com
- skidrowgames.net
- skladchik.com
- skyscrapercity.com
- slaati.com
- slashfilm.com
- slate.fr
- slimspots.com
- sm3na.com
- smallbiztrends.com
- smallseotools.com
- smartinsights.com
- smartpassiveincome.com
- smartprix.com
- smosh.com
- snapwidget.com
- soccermanager.com
- soccersuck.com
- socialadr.com
- socialblade.com
- socialmediabar.com
- socialmediaexaminer.com
- socialmediatoday.com
- socialtriggers.com
- softarchive.net
- solidtrustpay.com
- someecards.com
- somethingawful.com
- somuch.com
- songlyrics.com
- songspk.cc
- songspk.name
- soompi.com
- sooperarticles.com
- sopitas.com
- source-wave.com
- sourtimes.org
- spankbang.com
- spi0n.com
- spin.com
- sportcategory.com
- sportdog.gr
- spotscenered.info
- sprashivai.ru
- ssense.com
- stadelahly.com
- stadt-bremerhaven.de
- stafaband.info
- stagram.com
- standardmedia.co.ke
- stansberryresearch.com
- stargazete.com
- starsue.net
- statcounter.com
- statmyweb.com
- statscrop.com
- stepashka.com
- stereogum.com
- stocktwits.com
- stopforumspam.com
- storenvy.com
- streamhunter.eu
- stream-tv.me
- stuffgate.com
- submissionwebdirectory.com
- subscene.com
- subtitulos.es
- sudaneseonline.com
- sunmaker.com
- super.ae
- surveygizmo.com
- swalif.net
- systweak.com
- t411.me
- talkarcades.com
- tamindir.com
- taringa.net
- taxheaven.gr
- te3p.com
- teamliquid.net
- techdirt.com
- techinasia.com
- tech-wd.com
- tecmundo.com.br
- teespring.com
- telelistas.net
- template-help.com
- templatemonster.com
- tfl.gov.uk
- tgju.org
- th3professional.com
- thaqafnafsak.com
- thebump.com
- the-bux.net
- thedailybeast.com
- theelevationgroup.com
- thefrisky.com
- thehackernews.com
- thejournal.ie
- theladbible.com
- themalaysianinsider.com
- theme-fusion.com
- theme-junkie.com
- themelock.com
- themobileindian.com
- thenationonlineng.net
- thenews.com.pk
- thenewstribe.com
- thepoke.co.uk
- theregister.co.uk
- thestudentroom.co.uk
- thesuperficial.com
- thethao247.vn
- thetoptens.com
- theync.com
- thingiverse.com
- thisav.com
- thisoldhouse.com
- tickld.com
- tielabs.com
- tineye.com
- tinhte.vn
- tipsandtricks-hq.com
- tmart.com
- tn.com.ar
- tnr.com
- todayhumor.co.kr
- tomshw.it
- top-channel.tv
- topdocumentaryfilms.com
- topix.com
- toprankblog.com
- torlock.com
- torrentbutler.eu
- torrentcrazy.com
- torrentday.com
- torrentdownloads.me
- torrentfreak.com
- torrenthound.com
- torrentleech.org
- torrentreactor.net
- torrents.net
- townhall.com
- tracklab101.com
- tradetracker.com
- trafficbroker.com
- trafficestimate.com
- trafficfactory.biz
- trafficg.com
- traidnt.net
- tribune.com.pk
- trndsys.co
- trojmiasto.pl
- trueactivist.com
- truthaboutabs.com
- tubeplus.me
- tukif.com
- tunisia-sat.com
- tureng.com
- tutorialzine.com
- tutsplus.com
- tuvaro.com
- tvboxnow.com
- tvrage.com
- tv-series.me
- tw116.com
- twentytwowords.com
- twitchy.com
- typepad.com
- udemy.com
- uludagsozluk.com
- unitezz.com
- uploadboy.com
- uppit.com
- uptobox.com
- usingenglish.com
- utrace.de
- utusan.com.my
- uwants.com
- vanguardngr.com
- vavel.com
- vcommission.com
- vecernji.hr
- vecteezy.com
- vetogate.com
- vid2c.com
- videarn.com
- video.az
- videomega.tv
- videopremium.tv
- videoyoum7.com
- vidspot.net
- viralnova.com
- vivas.fi
- vladtv.com
- vodly.to
- vodonet.net
- voetbalzone.nl
- vozforums.com
- vr-zone.com
- w3resource.com
- w4.com
- warez-bb.org
- warriorplus.com
- waseet.net
- washingtontimes.com
- watch32.com
- watchcartoononline.com
- watchfreemovies.ch
- watchseries.lt
- watchseries-online.eu
- wattpad.com
- waveapps.com
- wayn.com
- wearehairy.com
- webconfs.com
- webdesignerdepot.com
- webdesignledger.com
- webgains.com
- webhostbox.net
- webhostingtalk.com
- webmastersitesi.com
- web-opinions.com
- webresourcesdepot.com
- webs.com
- wed168.com.tw
- wehkamp.nl
- weknowmemes.com
- weloveshopping.com
- whatculture.com
- whatismyip.com
- whatsmyserp.com
- whirlpool.net.au
- whocallsme.com
- whoishostingthis.com
- whoismind.com
- wikiwiki.jp
- wiziq.com
- wiziwig.tv
- wjunction.com
- wmmail.ru
- womenshealthmag.com
- worldtimebuddy.com
- worldtimeserver.com
- worthofweb.com
- wpcentral.com
- wpengine.com
- wphub.com
- wplocker.com
- wpmu.org
- x-art.com
- xat.com
- xbmc.org
- xenforo.com
- xxxbunker.com
- xxxkinky.com
- yam.com
- yazete.com
- yepi.com
- yeppudaa.com
- yeslibertin.com
- yola.com
- yoo7.com
- yougetpaidfast.com
- yougetsignal.com
- youm7.com
- yourbittorrent.com
- youtradefx.com
- youtube-mp3.org
- yucatan.com.mx
- yuku.com
- z6.com
- zakon.kz
- zalukaj.tv
- zamalekfans.com
- zaman.com.tr
- zemanta.com
- zemtv.com
- zenhabits.net
- zero10.net
- zetaboards.com
- ziprecruiter.com
- zone-telechargement.com
- zoominfo.com
- zoomit.ir
- zurb.com
- zwaar.net
