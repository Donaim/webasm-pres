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
  <div class="text-sm opacity-60 mb-4">Liber Cure Cocorum (c.&nbsp;1420&ndash;1440)</div>
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
    A recipe <em>For to make a compost</em>: a chicken-and-herb stew.
  </div>
</div>
<div>
  <div class="text-sm uppercase tracking-widest opacity-60 mb-4">Why this belongs in this talk</div>
  <div class="text-2xl leading-snug mb-5">A recipe is a <strong>portable procedure</strong>.</div>
  <div class="grid grid-cols-1 gap-2 text-base">
    <div class="rounded-xl px-4 py-3" style="border: 1px solid rgba(15,23,42,0.12);">inputs &rarr; ingredients</div>
    <div class="rounded-xl px-4 py-3" style="border: 1px solid rgba(15,23,42,0.12);">operations &rarr; chop, layer, boil, season</div>
    <div class="rounded-xl px-4 py-3" style="border: 1px solid rgba(15,23,42,0.12);">runtime &rarr; kitchen, tools, heat, vessel</div>
    <div class="rounded-xl px-4 py-3" style="border: 1px solid rgba(15,23,42,0.12);">hidden dependencies &rarr; the cook&rsquo;s tacit knowledge</div>
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
<div class="absolute bottom-4 right-6 text-xs opacity-60">Liber Cure Cocorum, c.&nbsp;1420&ndash;1440, Sloane MS 1986</div>

---

# Shipping a live process

<div class="grid grid-cols-2 gap-10 pt-8 items-start">
<div>
  <div class="rounded-3xl px-6 py-6" style="background: rgba(15,23,42,0.05); border: 1px solid rgba(15,23,42,0.12);">
    <div class="text-sm uppercase tracking-widest opacity-60 mb-3">1803</div>
    <div class="grid grid-cols-7 gap-2 text-center text-sm items-center">
      <div class="rounded-xl px-2 py-4" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(248,250,252,0.7);">child A</div>
      <div class="opacity-50">-&gt;</div>
      <div class="rounded-xl px-2 py-4" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(248,250,252,0.7);">child B</div>
      <div class="opacity-50">-&gt;</div>
      <div class="rounded-xl px-2 py-4" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(248,250,252,0.7);">child C</div>
      <div class="opacity-50">-&gt;</div>
      <div class="rounded-xl px-2 py-4" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(248,250,252,0.7);">child D</div>
    </div>
    <div class="mt-6 grid grid-cols-2 gap-3 text-center text-sm">
      <div class="rounded-xl px-4 py-4" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(248,250,252,0.7);">22 children</div>
      <div class="rounded-xl px-4 py-4" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(248,250,252,0.7);">arm-to-arm transfer</div>
      <div class="rounded-xl px-4 py-4" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(248,250,252,0.7);">live vaccine</div>
      <div class="rounded-xl px-4 py-4" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(248,250,252,0.7);">book + local institutions</div>
    </div>
  </div>
</div>
<div>
  <div class="text-4xl leading-tight" style="max-width: 30rem; color: rgb(153,27,27);">
    Transporting a viable instance of the procedure was the hard part.
  </div>
  <div class="pt-8 text-lg leading-snug" style="max-width: 33rem;">
    The Balmis expedition carried the vaccine as a running biological chain. Documentation and local setup traveled alongside the live material.
  </div>
</div>
</div>
<div class="absolute bottom-4 right-6 text-xs opacity-60">Balmis expedition accounts describe arm-to-arm transport across the ocean; PMC describes inoculation from fresh lesion material and the later pustule stage</div>

---

# From woven patterns to algebraical patterns

<div class="grid grid-cols-2 gap-10 pt-8 items-start">
<div>
  <div class="text-3xl leading-tight" style="max-width: 33rem;">
    Jacquard cards made a pattern detachable from the loom: stored, copied, transported, and replayed by a machine.
  </div>
  <div class="pt-8 text-lg leading-snug" style="max-width: 34rem;">
    Babbage borrowed that punched-card logic for the Analytical Engine. Lovelace saw the deeper shift: the same mechanism could control symbolic operations, not only textile patterns.
  </div>
</div>
<div>
  <div class="grid grid-cols-4 gap-2 text-center text-sm font-bold">
    <div class="rounded-xl px-2 py-5" style="border: 1px solid rgba(15,23,42,0.12);">card</div>
    <div class="rounded-xl px-2 py-5" style="border: 1px solid rgba(15,23,42,0.12);">card</div>
    <div class="rounded-xl px-2 py-5" style="border: 1px solid rgba(15,23,42,0.12);">card</div>
    <div class="rounded-xl px-2 py-5" style="border: 1px solid rgba(15,23,42,0.12);">card</div>
  </div>
  <div class="mt-6 rounded-2xl px-5 py-5" style="background: rgba(8,145,178,0.07); border: 1px solid rgba(8,145,178,0.18);">
    The punched card began as a way to make a procedure detachable from the craft that first embodied it.
  </div>
  <div class="pt-6 text-xl italic leading-snug" style="border-left: 3px solid rgba(8,145,178,0.4); padding-left: 1rem; max-width: 33rem;">
    "The Analytical Engine weaves algebraical patterns just as the Jacquard-loom weaves flowers and leaves."
  </div>
</div>
</div>
<div class="absolute bottom-4 right-6 left-10 text-xs opacity-60">CHM: punched-card control begins in Jacquard textile machinery; Lovelace 1843: the Analytical Engine &ldquo;weaves algebraical patterns just as the Jacquard-loom weaves flowers and leaves&rdquo;</div>

---

# Magazines were once app stores

<div class="grid grid-cols-2 gap-10 pt-8 items-start">
<div>
  <div class="text-3xl leading-tight" style="max-width: 32rem;">
    Home-computer users got software by reading it off paper and typing it in.
  </div>
  <div class="pt-8 text-lg leading-snug" style="max-width: 33rem;">
    A magazine listing could be the distribution channel. The workaround was human re-entry: line by line, keyword by keyword, then save to cassette and hope the save worked.
  </div>
</div>
<div class="grid grid-cols-1 gap-4 text-center">
  <div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">Artifact: the printed listing</div>
  <div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">Shortcut tools to speed up typing it all in</div>
  <div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(153,27,27,0.06);">Failure mode: cassette save errors as minor tragedy</div>
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

<div class="grid grid-cols-5 gap-8 pt-8 items-start">
<div class="col-span-3">
  <div class="text-3xl leading-tight" style="max-width: 34rem;">
    The browser becomes another strange container.
    The "Mosaic" Browser is the turning point.
  </div>
  <div class="pt-8 text-lg leading-snug" style="max-width: 34rem;">
    NCSA's big move was simple and enormous: pictures appeared automatically alongside text. After that, the browser keeps accumulating capabilities that make it feel more and more like a multimedia system.
  </div>
</div>
</div>
<div class="absolute bottom-4 right-6 text-xs opacity-60">NCSA Mosaic: first published browser to automatically display pictures with text</div>

---

# The browser starts running code

<div class="grid grid-cols-2 gap-10 pt-8 items-start">
<div>
  <div class="text-2xl leading-snug" style="max-width: 32rem;">
    Before JavaScript, the server owns all computation.
    Every interaction is a round-trip: click, wait, new page.
    The browser is a <em>display terminal</em> for someone else's machine.
  </div>
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

# The browser becomes a platform

<div class="grid grid-cols-3 gap-4 pt-6">
<div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">
  <div class="text-sm uppercase tracking-widest opacity-60 mb-2">Canvas · WebGL · WebGPU</div>
  <div class="text-lg leading-snug">2D pixel drawing, GPU-accelerated 3D, massively parallel compute</div>
</div>
<div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">
  <div class="text-sm uppercase tracking-widest opacity-60 mb-2">Web Workers</div>
  <div class="text-lg leading-snug">Heavy computation moves off the UI thread; the page stays responsive</div>
</div>
<div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">
  <div class="text-sm uppercase tracking-widest opacity-60 mb-2">IndexedDB · localStorage</div>
  <div class="text-lg leading-snug">Structured persistent state without a server round-trip</div>
</div>
<div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">
  <div class="text-sm uppercase tracking-widest opacity-60 mb-2">WebSockets · WebRTC</div>
  <div class="text-lg leading-snug">Persistent two-way and peer-to-peer connections, not just request-response</div>
</div>
<div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">
  <div class="text-sm uppercase tracking-widest opacity-60 mb-2">Service Workers · Cache API</div>
  <div class="text-lg leading-snug">Intercept every network request; the app keeps running when the network disappears</div>
</div>
<div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(8,145,178,0.18); background: rgba(8,145,178,0.07);">
  <div class="text-sm uppercase tracking-widest opacity-60 mb-2">File access · Web Audio · USB · Geolocation</div>
  <div class="text-lg leading-snug">The browser reaches into the machine and the physical world</div>
</div>
</div>
<div class="mt-8 text-xl leading-snug" style="max-width: 49rem;">
The accumulated result: a user-space operating environment delivered through a URL.
</div>
<div class="absolute bottom-4 right-6 text-xs opacity-60">Canvas 2004, Web Workers 2010, IndexedDB 2011, WebRTC 2012, Service Workers 2015, WebGPU 2023 — each capability would have seemed out of place in a document viewer</div>

---

# The browser kept trying to smuggle in a runtime

<div class="grid grid-cols-4 gap-4 pt-8 text-center items-stretch">
<div class="rounded-2xl px-4 py-6" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">
  <div class="text-sm uppercase tracking-widest opacity-60 mb-3">Java applets</div>
  <div class="text-lg">Bring a whole JVM into the page</div>
</div>
<div class="rounded-2xl px-4 py-6" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">
  <div class="text-sm uppercase tracking-widest opacity-60 mb-3">Flash</div>
  <div class="text-lg">A parallel plug-in world for rich apps</div>
</div>
<div class="rounded-2xl px-4 py-6" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">
  <div class="text-sm uppercase tracking-widest opacity-60 mb-3">NaCl / PNaCl</div>
  <div class="text-lg">Native-ish code, but trapped in one browser's story</div>
</div>
<div class="rounded-2xl px-4 py-6" style="border: 1px solid rgba(153,27,27,0.18); background: rgba(153,27,27,0.07);">
  <div class="text-sm uppercase tracking-widest opacity-60 mb-3">asm.js</div>
  <div class="text-lg">Compiled code disguised as weird JavaScript</div>
</div>
</div>
<div class="mt-10 rounded-2xl px-6 py-5" style="background: rgba(8,145,178,0.07); border: 1px solid rgba(8,145,178,0.18); max-width: 48rem;">
Different hacks, same desire: once the browser had become a richer host environment, people kept trying to smuggle in larger runtimes and more serious software.
</div>
<div class="absolute bottom-4 right-6 text-xs opacity-60">Oracle: applets and Java deployment stack removed; MDN: asm.js deprecated in favor of WebAssembly</div>

---

# What WebAssembly finally changes

<div class="grid grid-cols-2 gap-10 pt-8 items-start">
<div>
  <div class="text-sm uppercase tracking-widest opacity-60 mb-3">Already true</div>
  <ul class="list-disc text-lg leading-snug" style="padding-left: 1.2rem; max-width: 31rem;">
    <li>The browser already has UI, networking, graphics, storage, and background execution</li>
    <li>Biology already has serious browser software</li>
    <li>Sharing a URL is already the easiest way to give someone a tool</li>
  </ul>
</div>
<div>
  <div class="text-sm uppercase tracking-widest opacity-60 mb-3">New with Wasm</div>
  <ul class="list-disc text-lg leading-snug" style="padding-left: 1.2rem; max-width: 31rem;">
    <li>More of our existing analysis code can run in the browser without a full rewrite</li>
    <li>Fewer tools need a server just to avoid installation pain</li>
    <li>Fewer teams need to rebuild their tool from scratch just to offer a browser version</li>
  </ul>
</div>
</div>
<div class="mt-10 rounded-2xl px-6 py-5" style="background: rgba(8,145,178,0.07); border: 1px solid rgba(8,145,178,0.18); max-width: 49rem;">
The browser is now capable enough to host serious software. WebAssembly is what lets existing code &mdash; written in any language &mdash; travel inside a URL without a full rewrite.
</div>
<div class="absolute bottom-4 right-6 text-xs opacity-60">MDN: Wasm complements JavaScript and lets code from multiple languages run in modern browsers</div>

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
<div class="mt-8 rounded-2xl px-6 py-5" style="background: rgba(8,145,178,0.07); border: 1px solid rgba(8,145,178,0.18);">
The project still documents Docker as the easiest installation path. The browser-hosted version is a meaningful packaging shift.
</div>
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
