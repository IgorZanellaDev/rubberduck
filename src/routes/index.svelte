<script context="module">
	import Prism from 'prismjs';

	const highlight = (code, syntax) => Prism.highlight(code, Prism.languages[syntax], syntax);

</script>

<script lang="ts">
	import { Column, Button, Link,  Content, Grid, ImageLoader, Row, TextArea, Select, SelectItem } from 'carbon-components-svelte';
	import { onMount } from 'svelte';
	import { AVAILABLE_SYNTAX } from '../constants/syntax';
	import "prismjs/themes/prism-okaidia.css";
	import 'prismjs/components/prism-abap.js';
	import 'prismjs/components/prism-abnf.js';
	import 'prismjs/components/prism-actionscript.js';
	import 'prismjs/components/prism-ada.js';
	import 'prismjs/components/prism-agda.js';
	import 'prismjs/components/prism-al.js';
	import 'prismjs/components/prism-antlr4.js';
	import 'prismjs/components/prism-apacheconf.js';
	import 'prismjs/components/prism-apex.js';
	import 'prismjs/components/prism-apl.js';
	import 'prismjs/components/prism-applescript.js';
	import 'prismjs/components/prism-aql.js';
	import 'prismjs/components/prism-arff.js';
	import 'prismjs/components/prism-asciidoc.js';
	import 'prismjs/components/prism-asm6502.js';
	import 'prismjs/components/prism-aspnet.js';
	import 'prismjs/components/prism-autohotkey.js';
	import 'prismjs/components/prism-autoit.js';
	import 'prismjs/components/prism-bash.js';
	import 'prismjs/components/prism-basic.js';
	import 'prismjs/components/prism-batch.js';
	import 'prismjs/components/prism-bbcode.js';
	import 'prismjs/components/prism-birb.js';
	import 'prismjs/components/prism-bnf.js';
	import 'prismjs/components/prism-brainfuck.js';
	import 'prismjs/components/prism-brightscript.js';
	import 'prismjs/components/prism-bro.js';
	import 'prismjs/components/prism-bsl.js';
	import 'prismjs/components/prism-c.js';
	import 'prismjs/components/prism-cfscript.js';
	import 'prismjs/components/prism-cil.js';
	import 'prismjs/components/prism-clike.js';
	import 'prismjs/components/prism-clojure.js';
	import 'prismjs/components/prism-cmake.js';
	import 'prismjs/components/prism-cobol.js';
	import 'prismjs/components/prism-coffeescript.js';
	import 'prismjs/components/prism-concurnas.js';
	import 'prismjs/components/prism-coq.js';
	import 'prismjs/components/prism-cpp.js';
	import 'prismjs/components/prism-csharp.js';
	import 'prismjs/components/prism-csp.js';
	import 'prismjs/components/prism-css.js';
	import 'prismjs/components/prism-css-extras.js';
	import 'prismjs/components/prism-csv.js';
	import 'prismjs/components/prism-cypher.js';
	import 'prismjs/components/prism-d.js';
	import 'prismjs/components/prism-dart.js';
	import 'prismjs/components/prism-dataweave.js';
	import 'prismjs/components/prism-dax.js';
	import 'prismjs/components/prism-dhall.js';
	import 'prismjs/components/prism-diff.js';
	import 'prismjs/components/prism-dns-zone-file.js';
	import 'prismjs/components/prism-docker.js';
	import 'prismjs/components/prism-dot.js';
	import 'prismjs/components/prism-ebnf.js';
	import 'prismjs/components/prism-editorconfig.js';
	import 'prismjs/components/prism-eiffel.js';
	import 'prismjs/components/prism-ejs.js';
	import 'prismjs/components/prism-elixir.js';
	import 'prismjs/components/prism-elm.js';
	import 'prismjs/components/prism-erb.js';
	import 'prismjs/components/prism-erlang.js';
	import 'prismjs/components/prism-etlua.js';
	import 'prismjs/components/prism-excel-formula.js';
	import 'prismjs/components/prism-factor.js';
	import 'prismjs/components/prism-false.js';
	import 'prismjs/components/prism-firestore-security-rules.js';
	import 'prismjs/components/prism-flow.js';
	import 'prismjs/components/prism-fortran.js';
	import 'prismjs/components/prism-fsharp.js';
	import 'prismjs/components/prism-ftl.js';
	import 'prismjs/components/prism-gcode.js';
	import 'prismjs/components/prism-gdscript.js';
	import 'prismjs/components/prism-gedcom.js';
	import 'prismjs/components/prism-gherkin.js';
	import 'prismjs/components/prism-git.js';
	import 'prismjs/components/prism-glsl.js';
	import 'prismjs/components/prism-gml.js';
	import 'prismjs/components/prism-go.js';
	import 'prismjs/components/prism-graphql.js';
	import 'prismjs/components/prism-groovy.js';
	import 'prismjs/components/prism-haml.js';
	import 'prismjs/components/prism-handlebars.js';
	import 'prismjs/components/prism-hcl.js';
	import 'prismjs/components/prism-haskell.js';
	import 'prismjs/components/prism-haxe.js';
	import 'prismjs/components/prism-hlsl.js';
	import 'prismjs/components/prism-hpkp.js';
	import 'prismjs/components/prism-hsts.js';
	import 'prismjs/components/prism-http.js';
	import 'prismjs/components/prism-ichigojam.js';
	import 'prismjs/components/prism-icon.js';
	import 'prismjs/components/prism-icu-message-format.js';
	import 'prismjs/components/prism-idris.js';
	import 'prismjs/components/prism-iecst.js';
	import 'prismjs/components/prism-ignore.js';
	import 'prismjs/components/prism-inform7.js';
	import 'prismjs/components/prism-ini.js';
	import 'prismjs/components/prism-io.js';
	import 'prismjs/components/prism-j.js';
	import 'prismjs/components/prism-java.js';
	import 'prismjs/components/prism-javadoclike.js';
	import 'prismjs/components/prism-javascript.js';
	import 'prismjs/components/prism-javastacktrace.js';
	import 'prismjs/components/prism-jexl.js';
	import 'prismjs/components/prism-jolie.js';
	import 'prismjs/components/prism-jq.js';
	import 'prismjs/components/prism-js-extras.js';
	import 'prismjs/components/prism-js-templates.js';
	import 'prismjs/components/prism-json.js';
	import 'prismjs/components/prism-json5.js';
	import 'prismjs/components/prism-jsonp.js';
	import 'prismjs/components/prism-jsstacktrace.js';
	import 'prismjs/components/prism-jsx.js';
	import 'prismjs/components/prism-julia.js';
	import 'prismjs/components/prism-keyman.js';
	import 'prismjs/components/prism-kotlin.js';
	import 'prismjs/components/prism-kumir.js';
	import 'prismjs/components/prism-latex.js';
	import 'prismjs/components/prism-latte.js';
	import 'prismjs/components/prism-less.js';
	import 'prismjs/components/prism-lilypond.js';
	import 'prismjs/components/prism-liquid.js';
	import 'prismjs/components/prism-lisp.js';
	import 'prismjs/components/prism-livescript.js';
	import 'prismjs/components/prism-llvm.js';
	import 'prismjs/components/prism-log.js';
	import 'prismjs/components/prism-lolcode.js';
	import 'prismjs/components/prism-lua.js';
	import 'prismjs/components/prism-makefile.js';
	import 'prismjs/components/prism-markdown.js';
	import 'prismjs/components/prism-markup.js';
	import 'prismjs/components/prism-markup-templating.js';
	import 'prismjs/components/prism-matlab.js';
	import 'prismjs/components/prism-mel.js';
	import 'prismjs/components/prism-mizar.js';
	import 'prismjs/components/prism-mongodb.js';
	import 'prismjs/components/prism-monkey.js';
	import 'prismjs/components/prism-moonscript.js';
	import 'prismjs/components/prism-n1ql.js';
	import 'prismjs/components/prism-n4js.js';
	import 'prismjs/components/prism-nand2tetris-hdl.js';
	import 'prismjs/components/prism-naniscript.js';
	import 'prismjs/components/prism-neon.js';
	import 'prismjs/components/prism-nasm.js';
	import 'prismjs/components/prism-nevod.js';
	import 'prismjs/components/prism-nginx.js';
	import 'prismjs/components/prism-nim.js';
	import 'prismjs/components/prism-nix.js';
	import 'prismjs/components/prism-nsis.js';
	import 'prismjs/components/prism-objectivec.js';
	import 'prismjs/components/prism-ocaml.js';
	import 'prismjs/components/prism-openqasm.js';
	import 'prismjs/components/prism-oz.js';
	import 'prismjs/components/prism-parigp.js';
	import 'prismjs/components/prism-parser.js';
	import 'prismjs/components/prism-pascal.js';
	import 'prismjs/components/prism-pascaligo.js';
	import 'prismjs/components/prism-pcaxis.js';
	import 'prismjs/components/prism-peoplecode.js';
	import 'prismjs/components/prism-perl.js';
	import 'prismjs/components/prism-php.js';
	import 'prismjs/components/prism-php-extras.js';
	import 'prismjs/components/prism-powerquery.js';
	import 'prismjs/components/prism-powershell.js';
	import 'prismjs/components/prism-processing.js';
	import 'prismjs/components/prism-prolog.js';
	import 'prismjs/components/prism-promql.js';
	import 'prismjs/components/prism-properties.js';
	import 'prismjs/components/prism-protobuf.js';
	import 'prismjs/components/prism-psl.js';
	import 'prismjs/components/prism-pug.js';
	import 'prismjs/components/prism-puppet.js';
	import 'prismjs/components/prism-pure.js';
	import 'prismjs/components/prism-purebasic.js';
	import 'prismjs/components/prism-python.js';
	import 'prismjs/components/prism-q.js';
	import 'prismjs/components/prism-qml.js';
	import 'prismjs/components/prism-qore.js';
	import 'prismjs/components/prism-qsharp.js';
	import 'prismjs/components/prism-r.js';
	import 'prismjs/components/prism-reason.js';
	import 'prismjs/components/prism-regex.js';
	import 'prismjs/components/prism-rego.js';
	import 'prismjs/components/prism-renpy.js';
	import 'prismjs/components/prism-rest.js';
	import 'prismjs/components/prism-rip.js';
	import 'prismjs/components/prism-roboconf.js';
	import 'prismjs/components/prism-robotframework.js';
	import 'prismjs/components/prism-ruby.js';
	import 'prismjs/components/prism-rust.js';
	import 'prismjs/components/prism-sas.js';
	import 'prismjs/components/prism-sass.js';
	import 'prismjs/components/prism-scheme.js';
	import 'prismjs/components/prism-scss.js';
	import 'prismjs/components/prism-shell-session.js';
	import 'prismjs/components/prism-smali.js';
	import 'prismjs/components/prism-smalltalk.js';
	import 'prismjs/components/prism-smarty.js';
	import 'prismjs/components/prism-sml.js';
	import 'prismjs/components/prism-solidity.js';
	import 'prismjs/components/prism-solution-file.js';
	import 'prismjs/components/prism-soy.js';
	import 'prismjs/components/prism-splunk-spl.js';
	import 'prismjs/components/prism-sqf.js';
	import 'prismjs/components/prism-sql.js';
	import 'prismjs/components/prism-squirrel.js';
	import 'prismjs/components/prism-stan.js';
	import 'prismjs/components/prism-stylus.js';
	import 'prismjs/components/prism-swift.js';
	import 'prismjs/components/prism-tap.js';
	import 'prismjs/components/prism-tcl.js';
	import 'prismjs/components/prism-textile.js';
	import 'prismjs/components/prism-toml.js';
	import 'prismjs/components/prism-tt2.js';
	import 'prismjs/components/prism-turtle.js';
	import 'prismjs/components/prism-twig.js';
	import 'prismjs/components/prism-typescript.js';
	import 'prismjs/components/prism-typoscript.js';
	import 'prismjs/components/prism-unrealscript.js';
	import 'prismjs/components/prism-uri.js';
	import 'prismjs/components/prism-v.js';
	import 'prismjs/components/prism-vala.js';
	import 'prismjs/components/prism-velocity.js';
	import 'prismjs/components/prism-verilog.js';
	import 'prismjs/components/prism-vhdl.js';
	import 'prismjs/components/prism-vim.js';
	import 'prismjs/components/prism-visual-basic.js';
	import 'prismjs/components/prism-warpscript.js';
	import 'prismjs/components/prism-wasm.js';
	import 'prismjs/components/prism-wiki.js';
	import 'prismjs/components/prism-wolfram.js';
	import 'prismjs/components/prism-xeora.js';
	import 'prismjs/components/prism-xml-doc.js';
	import 'prismjs/components/prism-xojo.js';
	import 'prismjs/components/prism-xquery.js';
	import 'prismjs/components/prism-yaml.js';
	import 'prismjs/components/prism-yang.js';
	import 'prismjs/components/prism-zig.js';
	import Restart16 from "carbon-icons-svelte/lib/Restart16";

	const DEFAULT_CODE = "let test = \"hello\";";
	const DEFAULT_SYNTAX = "javascript";

	let code = DEFAULT_CODE;
	let syntax = "";

	let CodeJar;
	onMount(async () => {
		syntax = "javascript";
		({CodeJar} = await import("@novacbn/svelte-codejar"));
	});

	const handleClearCode = () => {
		code = DEFAULT_CODE;
		syntax = DEFAULT_SYNTAX;
	};
</script>


<style>
	.image-container {
      display: inline-block;
			max-width: 600px;
			max-height: 600px;
	}
</style>

<Content>
	<Grid>
		<Row>
			<Column md={4} lg={10} style="display: flex; justify-content: center">
				<div class="image-container">
					<ImageLoader src="rubber-duck.png" style="max-width: 100%; height:auto;"/>
				</div>
			</Column>
			<Column md={4} lg={6}>
				<h2 style="margin-bottom: 8px">Let's solve your problem</h2>
				<TextArea labelText="Explain your algorithm to the duck" placeholder="Enter your explanation..." style="min-height: 180px; margin-bottom: .5rem"/>
				{#if CodeJar}
					<label class="bx--label">Write your code here</label>
					<svelte:component this={CodeJar} {syntax} {highlight} value={code} on:change={(e) => code = e.detail.value} style="margin-top: 0; background: #262626;"/>
					<Row>
						<Column sm={3} md={6} lg={13}>
								<Select labelText="Syntax" selected={syntax} bind:value={syntax} on:change={(e) => syntax = e.detail}>
									{#each AVAILABLE_SYNTAX as syntax}
										<SelectItem value={syntax.value} text={syntax.name}/>
									{/each}
								</Select>
						</Column>
						<Column style="display: flex; align-items: flex-end; justify-content: center;" sm={1} md={2} lg={3}>
							<Button kind="tertiary" size="md" iconDescription="Clear code" icon={Restart16} on:click={handleClearCode}/>
						</Column>
					</Row>
				{/if}
			</Column>
		</Row>
		<Row>
			<Column>
				<h2 id="what-is-rubber-duck">What is Rubber Duck?</h2>
				<p>
					In software engineering, rubber duck debugging is a method of debugging code.
					The name is a reference to a story in the book The Pragmatic Programmer in which a programmer would carry around a rubber duck and debug their code by forcing themselves to explain it, line-by-line, to the duck.
					Many other terms exist for this technique, often involving different (usually) inanimate objects, or pets such as a dog or a cat.<br/>
					Many programmers have had the experience of explaining a problem to someone else, possibly even to someone who knows nothing about programming, and then hitting upon the solution in the process of explaining the problem.
					In describing what the code is supposed to do and observing what it actually does, any incongruity between these two becomes apparent.
					More generally, teaching a subject forces its evaluation from different perspectives and can provide a deeper understanding.
					By using an inanimate object, the programmer can try to accomplish this without having to interrupt anyone else.
				</p>
				<p>
					Source: <Link size="lg" href="https://en.wikipedia.org/wiki/Rubber_duck_debugging" target="_blank" rel="noopener noreferrer">Wikipedia</Link>
				</p>
			</Column>
		</Row>
	</Grid>
</Content>