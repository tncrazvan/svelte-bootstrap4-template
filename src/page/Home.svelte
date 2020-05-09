<script>
	import {onMount} from 'svelte';
	import PrintableDocument from './../shared/component/printable/PrintableDocument.svelte';
	import PrintableDocumentRoot from './../shared/component/printable/PrintableDocumentRoot.svelte';
	import NewPage from './../shared/component/printable/NewPage.svelte';
	import IconButton from './../shared/component/button/IconButton.svelte';
	import { fly } from 'svelte/transition';
	let doc;
</script>
<div transition:fly={{ x: -100, duration: 200 }} class="page">
<IconButton click={()=>{doc.show()}} text="Preview" icon="print"}/>
	<PrintableDocument title={"Hello PDF"} bind:this={doc}>
		<PrintableDocumentRoot>
			<NewPage>
				<h1><a href="https://it.wikipedia.org/wiki/Hypertext_Transfer_Protocol">HTTP</a></h1>
				<div id="toc" class="toc" role="navigation" aria-labelledby="mw-toc-heading"><input type="checkbox" role="button" id="toctogglecheckbox" class="toctogglecheckbox" style="display:none"><div class="toctitle" lang="it" dir="ltr"><h2 id="mw-toc-heading">Indice</h2><span class="toctogglespan"><label class="toctogglelabel" for="toctogglecheckbox"></label></span></div>
<ul>
<li class="toclevel-1 tocsection-1"><a href="#Storia"><span class="tocnumber">1</span> <span class="toctext">Storia</span></a></li>
<li class="toclevel-1 tocsection-2"><a href="#Funzionamento"><span class="tocnumber">2</span> <span class="toctext">Funzionamento</span></a>
<ul>
<li class="toclevel-2 tocsection-3"><a href="#Messaggio_di_richiesta"><span class="tocnumber">2.1</span> <span class="toctext">Messaggio di richiesta</span></a>
<ul>
<li class="toclevel-3 tocsection-4"><a href="#Riga_di_richiesta"><span class="tocnumber">2.1.1</span> <span class="toctext">Riga di richiesta</span></a></li>
<li class="toclevel-3 tocsection-5"><a href="#Gli_header_della_richiesta"><span class="tocnumber">2.1.2</span> <span class="toctext">Gli header della richiesta</span></a></li>
</ul>
</li>
<li class="toclevel-2 tocsection-6"><a href="#Messaggio_di_risposta"><span class="tocnumber">2.2</span> <span class="toctext">Messaggio di risposta</span></a>
<ul>
<li class="toclevel-3 tocsection-7"><a href="#Riga_di_stato"><span class="tocnumber">2.2.1</span> <span class="toctext">Riga di stato</span></a></li>
<li class="toclevel-3 tocsection-8"><a href="#Gli_header_della_risposta"><span class="tocnumber">2.2.2</span> <span class="toctext">Gli header della risposta</span></a></li>
</ul>
</li>
<li class="toclevel-2 tocsection-9"><a href="#Tipo_di_connessione"><span class="tocnumber">2.3</span> <span class="toctext">Tipo di connessione</span></a></li>
</ul>
</li>
<li class="toclevel-1 tocsection-10"><a href="#Esempi_di_messaggi_HTTP"><span class="tocnumber">3</span> <span class="toctext">Esempi di messaggi HTTP</span></a>
<ul>
<li class="toclevel-2 tocsection-11"><a href="#Richiesta_GET_e_risposta_di_successo"><span class="tocnumber">3.1</span> <span class="toctext">Richiesta GET e risposta di successo</span></a></li>
<li class="toclevel-2 tocsection-12"><a href="#Richiesta_GET_e_risposta_di_redirezione_permanente"><span class="tocnumber">3.2</span> <span class="toctext">Richiesta GET e risposta di redirezione permanente</span></a></li>
<li class="toclevel-2 tocsection-13"><a href="#Richiesta_POST_e_risposta_di_redirezione_temporanea"><span class="tocnumber">3.3</span> <span class="toctext">Richiesta POST e risposta di redirezione temporanea</span></a></li>
<li class="toclevel-2 tocsection-14"><a href="#Richieste_utili_nella_versione_1.0"><span class="tocnumber">3.4</span> <span class="toctext">Richieste utili nella versione 1.0</span></a>
<ul>
<li class="toclevel-3 tocsection-15"><a href="#GET_/_HTTP/1.0"><span class="tocnumber">3.4.1</span> <span class="toctext">GET / HTTP/1.0</span></a></li>
<li class="toclevel-3 tocsection-16"><a href="#HEAD_/_HTTP/1.0"><span class="tocnumber">3.4.2</span> <span class="toctext">HEAD / HTTP/1.0</span></a></li>
</ul>
</li>
</ul>
</li>
<li class="toclevel-1 tocsection-17"><a href="#Versioni_sicure"><span class="tocnumber">4</span> <span class="toctext">Versioni <i>sicure</i></span></a></li>
<li class="toclevel-1 tocsection-18"><a href="#Streaming_HTTP"><span class="tocnumber">5</span> <span class="toctext">Streaming HTTP</span></a></li>
<li class="toclevel-1 tocsection-19"><a href="#Note"><span class="tocnumber">6</span> <span class="toctext">Note</span></a></li>
<li class="toclevel-1 tocsection-20"><a href="#Bibliografia"><span class="tocnumber">7</span> <span class="toctext">Bibliografia</span></a></li>
<li class="toclevel-1 tocsection-21"><a href="#Voci_correlate"><span class="tocnumber">8</span> <span class="toctext">Voci correlate</span></a></li>
<li class="toclevel-1 tocsection-22"><a href="#Altri_progetti"><span class="tocnumber">9</span> <span class="toctext">Altri progetti</span></a></li>
<li class="toclevel-1 tocsection-23"><a href="#Collegamenti_esterni"><span class="tocnumber">10</span> <span class="toctext">Collegamenti esterni</span></a></li>
</ul>
</div>
			</NewPage>
		</PrintableDocumentRoot>
	</PrintableDocument>
</div>