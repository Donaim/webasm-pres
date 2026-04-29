---
title: Software Packaging
theme: seriph
info: |
  ## Software Packaging
  A history of how procedures get packaged and deployed — from verse to WebAssembly.
class: text-left
drawings:
  persist: true
background: rgb(248,250,252)
mdc: true
zoom: 1.0
hideInToc: true
---

<div class="pt-14">
  <h1 style="font-size: 3em; line-height: 1.02; margin-top: 0.45rem; max-width: 42rem;">
    Software Packaging
  </h1>
  <p style="font-size: 1.3em; max-width: 41rem; margin-top: 1.3rem; line-height: 1.35;">
    A history of how procedures get packaged and deployed — from verse to WebAssembly.
  </p>
</div>
<div class="absolute bottom-8 left-0 right-0 grid grid-cols-6 gap-4 text-center text-sm opacity-75">
  <div>People</div>
  <div>Verse</div>
  <div>Living systems</div>
  <div>Cards</div>
  <div>Media</div>
  <div>URLs</div>
</div>

---

# Packaging is an old problem

<div class="pt-14 text-3xl leading-snug" style="max-width: 48rem;">
  This talk is a history of software packaging.
</div>

<div class="pt-10 text-3xl leading-snug" style="max-width: 49rem;">
  The history stretches further back than the word "software":
</div>

<div class="pt-10 text-4xl leading-tight" style="max-width: 50rem; color: rgb(8,145,178);">
  every method needs a host,
  <br>
  and some way to be reproduced elsewhere.
</div>

<div class="pt-12 text-xl leading-snug opacity-80" style="max-width: 46rem;">
  Long before code, people were already solving that problem.
</div>

---

# Before software, there were recipes

<div class="grid grid-cols-2 gap-10 pt-6 items-start">
<div>
  <div class="text-sm uppercase tracking-widest opacity-60 mb-1">A rhymed recipe</div>
  <div class="text-base italic leading-relaxed rounded-2xl px-5 py-5" style="border-left: 3px solid rgba(15,23,42,0.2); background: rgba(15,23,42,0.03);">
    Take &thorn;o chekyns and hew hom for &thorn;o seke,<br>
    All but &thorn;e hede and &thorn;e legges eke;<br>
    Take a handfulle of herb lovache,<br>
    And ano&thorn;er of persely, als<br>
    Of sage &thorn;at never was founde fals,<br>
    And no&thorn;er of lekes and alle hom wasshe;<br>
    &hellip;<br>
    Take powder of gynger and canel god wone,<br>
    Cast on &thorn;ese o&thorn;er thynges everychon;
  </div>
  <div class="text-sm opacity-70 mt-3">
    A recipe <em>For to make a compost</em> (a chicken-and-herb stew)
  </div>
</div>
<div>
  <div class="text-2xl leading-snug mb-5">A recipe is a <strong>portable procedure</strong>.</div>
  <div class="grid grid-cols-1 gap-2 text-base">
    <div class="rounded-xl px-4 py-3" style="border: 1px solid rgba(15,23,42,0.12);">inputs &rarr; ingredients</div>
    <div class="rounded-xl px-4 py-3" style="border: 1px solid rgba(15,23,42,0.12);">operations &rarr; chop, layer, boil, season</div>
    <div class="rounded-xl px-4 py-3" style="border: 1px solid rgba(15,23,42,0.12);">runtime &rarr; kitchen, tools, heat, vessel</div>
    <div class="rounded-xl px-4 py-3" style="border: 1px solid rgba(8,145,178,0.18); background: rgba(8,145,178,0.07);">output &rarr; a reproducible dish</div>
  </div>
  <div class="mt-5 text-lg leading-snug font-medium" style="max-width: 26rem;">
    The method travels, but execution still depends on the host environment.
  </div>
  <div class="text-sm opacity-60 mt-4">
    Verse made recipes easier to remember &mdash; but often less precise.
  </div>
</div>
</div>
<div class="absolute bottom-4 left-6 text-xs opacity-60">Liber Cure Cocorum, c.&nbsp;1420&ndash;1440, Sloane MS 1986</div>

---

# Shipping a live process

<div class="grid grid-cols-2 gap-10 pt-6 items-start">
<div>
  <img src="/assets/balmis.png" alt="Painting of the Balmis expedition" class="rounded-2xl w-full" style="object-fit: cover; object-position: center top;">
</div>
<div>
  <div class="text-4xl leading-tight" style="max-width: 30rem; color: rgb(153,27,27);">
    Transporting a viable instance of the procedure was the hard part.
  </div>
  <div class="pt-6 text-lg leading-snug" style="max-width: 33rem;">
    In 1803 the Balmis expedition carried the smallpox vaccine across the Atlantic as a running biological chain: 22 children, each inoculated arm-to-arm in turn. Documentation and local institutions traveled alongside the live material.
  </div>
</div>
</div>
<div class="absolute bottom-4 right-6 text-xs opacity-60">Balmis expedition 1803 &mdash; arm-to-arm chain kept the vaccine alive across the ocean</div>

---

# From woven patterns to algebraical patterns

<div class="grid grid-cols-2 gap-10 pt-6 items-start">
<div>
  <img src="/assets/jacquard-loom.jpg" alt="Jacquard loom engraving, 1801" class="rounded-2xl w-full" style="max-height: 26rem; object-fit: cover; object-position: center;">
</div>
<div>
  <div class="pt-6 text-lg leading-snug" style="max-width: 34rem;">
    Babbage borrowed that punched-card logic for the Analytical Engine. Lovelace saw the deeper shift: the same mechanism could control symbolic operations, not only textile patterns.
  </div>
  <div class="mt-6 rounded-2xl px-5 py-5" style="background: rgba(8,145,178,0.07); border: 1px solid rgba(8,145,178,0.18);">
    The punched card began as a way to make a procedure detachable from the craft that first embodied it.
  </div>
  <br>
  <div class="pt-5 text-xl italic leading-snug" style="border-left: 3px solid rgba(8,145,178,0.4); padding-left: 1rem; max-width: 33rem;">
    &ldquo;The Analytical Engine weaves algebraical patterns just as the Jacquard-loom weaves flowers and leaves.&rdquo;
  </div>
</div>
</div>

<!--

  Jacquard cards made a pattern detachable from the loom: stored, copied, transported, and replayed by a machine.

-->

---

# Magazines were once app stores

<div class="grid grid-cols-2 gap-10 pt-6 items-start">
<div>
  <img src="/assets/magazine-listing.jpg" class="rounded-2xl w-full" style="max-height: 26rem; object-fit: cover; object-position: top;">
</div>
<div>
  <div class="text-3xl leading-tight" style="max-width: 32rem;">
    Home-computer users got software by reading it off paper and typing it in.
  </div>
  <div class="pt-6 text-lg leading-snug" style="max-width: 33rem;">
    A magazine listing could be the distribution channel. The workaround was human re-entry: line by line, keyword by keyword, then save to cassette and hope the save worked.
  </div>
  <ul class="mt-6 grid grid-cols-1 gap-3">
    <li class="rounded-2xl">The printed listing was the artifact</li>
    <li class="rounded-2xl">Shortcut tools helped speed up typing</li>
    <li class="rounded-2xl">Cassette save errors were minor tragedy</li>
  </ul>
</div>
</div>

---

# Package managers: install software by name

<div class="grid grid-cols-2 gap-10 pt-8 items-start">
<div>
  <div class="text-3xl leading-tight" style="max-width: 33rem;">
    Software becomes discoverable and installable from a shared repository, rather than handed over as a pile of files.
  </div>
  <div class="pt-8 text-lg leading-snug" style="max-width: 34rem;">
    A package describes itself: its name, version, everything else it needs, and where to get it. The repository holds those descriptions; the machine does the fetching.
  </div>
</div>
<div>
  <div class="rounded-2xl px-5 py-6" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">
    <div class="text-sm uppercase tracking-widest opacity-60 mb-3">What travels now</div>
    <div class="grid grid-cols-1 gap-3">
      <div class="rounded-xl px-4 py-3" style="border: 1px solid rgba(15,23,42,0.12);">A name and a version number</div>
      <div class="rounded-xl px-4 py-3" style="border: 1px solid rgba(15,23,42,0.12);">A list of everything else it needs</div>
      <div class="rounded-xl px-4 py-3" style="border: 1px solid rgba(8,145,178,0.18); background: rgba(8,145,178,0.07);">A link into a shared, maintained collection</div>
    </div>
  </div>
</div>
</div>
<div class="absolute bottom-4 right-6 text-xs opacity-60">Debian project; GNU Guix: package collections make software distribution reproducible and declarative</div>

---

# Containers: ship the whole environment

<div class="grid grid-cols-2 gap-10 pt-8 items-start">
<div>
  <div class="text-3xl leading-tight" style="max-width: 33rem;">
    A container bundles everything the software needs: the program, its tools, and its settings. A registry stores and distributes those bundles.
  </div>
  <div class="pt-8 text-lg leading-snug" style="max-width: 34rem;">
    The software then runs the same way everywhere &mdash; regardless of what is already installed on the host machine.
  </div>
</div>
<div>
  <div class="grid grid-cols-1 gap-3">
    <div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">Package managers: install what you need, on the machine you&rsquo;re on</div>
    <div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">Containers: ship the whole assembled environment, ready to run</div>
    <div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(8,145,178,0.18); background: rgba(8,145,178,0.07);">Download the container, run it &mdash; no installation steps needed</div>
  </div>
</div>
</div>
<div class="absolute bottom-4 right-6 text-xs opacity-60">Docker documentation: an image is a read-only template of instructions for creating a container</div>

---

# 1993: the browser stops being plain text

<div class="grid grid-cols-2 gap-10 pt-6 items-start">
<div>
  <div class="text-sm uppercase tracking-widest opacity-60 mb-3">The web before Mosaic</div>
  <a href="https://info.cern.ch/hypertext/WWW/TheProject.html" target="_blank">
    <img src="/assets/first-website.png" alt="First website at CERN, still live at info.cern.ch" class="rounded-2xl w-full" style="border: 1px solid rgba(15,23,42,0.14);">
  </a>
  <div class="text-sm opacity-60 mt-2">The first website, still live at <code>info.cern.ch</code> &mdash; plain text and hyperlinks, nothing else.</div>
</div>
<div>
  <div class="text-3xl leading-tight" style="max-width: 34rem;">
    Mosaic is the turning point where the browser starts becoming a software platform.
  </div>
  <div class="pt-6 text-lg leading-snug" style="max-width: 34rem;">
    NCSA&rsquo;s big move was simple and enormous: pictures appeared automatically alongside text. After that, the browser keeps accumulating capabilities that make it feel more and more like a general host for software.
  </div>
  <div class="mt-6 rounded-2xl px-5 py-5" style="background: rgba(15,23,42,0.05); border: 1px solid rgba(15,23,42,0.12);">
    The browser stops being a page of linked text and starts becoming a software delivery mechanism.
  </div>
</div>
</div>

---

# The browser grows into a platform

<div class="pt-6">
<div class="text-xl opacity-70 mb-8">Built for reading documents, the browser slowly became something much more powerful:</div>
<div class="flex items-center gap-2 flex-wrap mb-10">
  <div class="rounded-2xl px-5 py-4 text-center text-lg" style="border: 1px solid rgba(15,23,42,0.2); background: rgba(15,23,42,0.04); min-width: 9rem;">Document reader</div>
  <div class="text-2xl opacity-40">&rarr;</div>
  <div class="rounded-2xl px-5 py-4 text-center text-lg" style="border: 1px solid rgba(15,23,42,0.2); background: rgba(15,23,42,0.04); min-width: 9rem;">Interactive page</div>
  <div class="text-2xl opacity-40">&rarr;</div>
  <div class="rounded-2xl px-5 py-4 text-center text-lg" style="border: 1px solid rgba(15,23,42,0.2); background: rgba(15,23,42,0.04); min-width: 9rem;">Graphics &amp; storage</div>
  <div class="text-2xl opacity-40">&rarr;</div>
  <div class="rounded-2xl px-5 py-4 text-center text-lg" style="border: 1px solid rgba(15,23,42,0.2); background: rgba(15,23,42,0.04); min-width: 9rem;">Offline &amp; local files</div>
  <div class="text-2xl opacity-40">&rarr;</div>
  <div class="rounded-2xl px-5 py-4 text-center text-lg font-semibold" style="border: 1px solid rgba(8,145,178,0.35); background: rgba(8,145,178,0.1); min-width: 9rem;">Serious software platform</div>
</div>
<div class="grid grid-cols-2 gap-6">
  <div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(153,27,27,0.2); background: rgba(153,27,27,0.04);">
    <div class="text-sm uppercase tracking-widest opacity-60 mb-2">Plugin detour (1990s&ndash;2010s)</div>
    <div class="text-base leading-snug opacity-80">Flash, Java applets, and similar plug-ins tried to fill the gap &mdash; and worked for a while. But each required a separate install, and each was eventually abandoned.</div>
  </div>
  <div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(8,145,178,0.18); background: rgba(8,145,178,0.07);">
    <div class="text-sm uppercase tracking-widest opacity-60 mb-2">The built-in path</div>
    <div class="text-base leading-snug">The browser kept getting more capable on its own. Today it can run serious software without any plug-in &mdash; if the code can reach it.</div>
  </div>
</div>
</div>
<div class="absolute bottom-4 right-6 text-xs opacity-60">Flash retired 2020; Java plug-in removed from major browsers by 2017</div>

---

# The browser starts running code

<div class="grid grid-cols-2 gap-10 pt-8 items-start">
<div>
  <div class="text-2xl leading-snug" style="max-width: 32rem;">
    Before JavaScript, the server owns all computation.
    Every interaction is a round-trip: click, wait, new page.
    The browser is a <em>display terminal</em> for someone else's machine.
  </div>
  <br>
  <div class="pt-8 rounded-2xl px-6 py-5" style="background: rgba(8,145,178,0.07); border: 1px solid rgba(8,145,178,0.18); max-width: 32rem;">
    JavaScript ships a runtime with the page.
    Computation runs on the user's machine.
    The server becomes optional for most interactions.
  </div>
</div>
<div class="grid grid-cols-1 gap-3">
  <div class="rounded-2xl px-5 py-4" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">
    <div class="text-xs uppercase tracking-widest opacity-60 mb-1">Form validation</div>
    <div class="text-lg">The form tells you what is wrong before one byte leaves your machine</div>
  </div>
  <div class="rounded-2xl px-5 py-4" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">
    <div class="text-xs uppercase tracking-widest opacity-60 mb-1">Games</div>
    <div class="text-lg">Entire games run in the browser with the server completely absent</div>
  </div>
  <div class="rounded-2xl px-5 py-4" style="border: 1px solid rgba(8,145,178,0.18); background: rgba(8,145,178,0.07);">
    <div class="text-xs uppercase tracking-widest opacity-60 mb-1">Packaging shift</div>
    <div class="text-lg">The URL now delivers executable code, not just a document</div>
  </div>
</div>
</div>
<div class="absolute bottom-4 right-6 text-xs opacity-60">JavaScript created at Netscape in ten days in 1995; its long-term effect was to move computation from servers into URL-delivered pages</div>

<!--
Objection, and a real one: executable code arriving through what had been a passive viewer is a fundamentally different security risk. System administrators immediately pushed back. The browser had no sandbox when JavaScript shipped — the same-origin policy was added afterward as a patch under pressure. Java applets and Flash drew the same criticism louder. Every new browser capability since has had to answer the same question first: who controls what the code is allowed to do?
-->

---

# What WebAssembly finally changes

<div class="pt-6 text-3xl leading-tight font-semibold" style="max-width: 46rem;">
  A link can now deliver serious software without making people install it.
</div>
<div class="grid grid-cols-3 gap-5 pt-8">
<div class="rounded-2xl px-5 py-6" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">
  <div class="text-sm uppercase tracking-widest opacity-60 mb-3">Open a link, not an installer</div>
  <div class="text-lg leading-snug">The user gets the current version immediately.</div>
</div>
<div class="rounded-2xl px-5 py-6" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">
  <div class="text-sm uppercase tracking-widest opacity-60 mb-3">Run locally when privacy matters</div>
  <div class="text-lg leading-snug">Files can stay on the user&rsquo;s machine.</div>
</div>
<div class="rounded-2xl px-5 py-6" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">
  <div class="text-sm uppercase tracking-widest opacity-60 mb-3">Bring existing tools to the browser</div>
  <div class="text-lg leading-snug">More proven analysis code can travel to the web without being rewritten from scratch.</div>
</div>
</div>
<div class="mt-8 rounded-2xl px-6 py-5" style="background: rgba(8,145,178,0.07); border: 1px solid rgba(8,145,178,0.18); max-width: 52rem;">
  WebAssembly helps the browser become a delivery box for real tools: easy to share, safer to run, and still local when the data should stay local.
</div>
<div class="absolute bottom-4 right-6 text-xs opacity-60">MDN: Wasm lets code from many languages run in modern browsers without a plug-in</div>

---

# ReCall, QAI, and the new packaging option

<div class="grid grid-cols-3 gap-5 pt-8 text-center items-stretch">
<div class="rounded-2xl px-5 py-6" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">
  <div class="text-sm uppercase tracking-widest opacity-60 mb-3">Installed client</div>
  <div class="text-2xl font-bold mb-4">ReCall</div>
  <div class="text-base leading-snug">Strong local control, but every machine becomes a deployment story.</div>
</div>
<div class="rounded-2xl px-5 py-6" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">
  <div class="text-sm uppercase tracking-widest opacity-60 mb-3">Central service</div>
  <div class="text-2xl font-bold mb-4">QAI</div>
  <div class="text-base leading-snug">Shared control and policy, but the work happens in a managed central system.</div>
</div>
<div class="rounded-2xl px-5 py-6" style="border: 1px solid rgba(8,145,178,0.18); background: rgba(8,145,178,0.07);">
  <div class="text-sm uppercase tracking-widest opacity-60 mb-3">Browser-delivered local client</div>
  <div class="text-2xl font-bold mb-4">New option</div>
  <div class="text-base leading-snug">Open a URL, use the current version, and still keep the sensitive files on the analyst's side.</div>
</div>
</div>
<div class="pt-8 text-xl" style="max-width: 47rem;">
That third box matters when distribution is painful, confidentiality matters, and the tool behaves more like an instrument than a shared workflow hub.
</div>

---
layout: iframe-right
url: https://cfe-lab.github.io/CFEIntact/app/
---

# CFEIntact, as the tool itself

<ul class="list-disc text-lg leading-snug pt-8" style="padding-left: 1.2rem; max-width: 22rem;">
<li>Reached by URL</li>
<li>Real lab-relevant biology task</li>
<li>Runs on the user&rsquo;s own machine</li>
<li>Sensitive files stay user-side</li>
</ul>
<div class="mt-6 text-sm opacity-60" style="word-break: break-all;">
https://cfe-lab.github.io/CFEIntact/app/
</div>

---

# What should we package this way next?

<div class="grid grid-cols-2 gap-4 pt-8 text-center">
  <div class="rounded-2xl px-5 py-6" style="border: 1px solid rgba(15,23,42,0.12);">
    Alignment viewer that runs in the browser
  </div>
  <div class="rounded-2xl px-5 py-6" style="border: 1px solid rgba(15,23,42,0.12);">
    BLAST-like sequence search
  </div>
  <div class="rounded-2xl px-5 py-6" style="border: 1px solid rgba(15,23,42,0.12);">
    Phylogenetic tree builder
  </div>
  <div class="rounded-2xl px-5 py-6" style="border: 1px solid rgba(15,23,42,0.12);">
    Most of BBLabs
  </div>
</div>
<div class="mt-8 rounded-2xl px-6 py-5" style="background: rgba(8,145,178,0.07); border: 1px solid rgba(8,145,178,0.18); max-width: 48rem;">
These are good candidates when installation hurts more than the algorithm, and when server centralization buys less than local privacy and easy distribution.
</div>

---

# Closing takeaway

<div class="pt-12 text-4xl leading-tight" style="max-width: 49rem;">
The browser is the latest in a long line of strange containers people have invented to move a method.
</div>
<div class="pt-10 text-3xl leading-tight" style="max-width: 49rem;">
WebAssembly is one reason more of our existing lab software can now fit inside it.
</div>
