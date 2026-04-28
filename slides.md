---
title: Packaging Methods
theme: seriph
info: |
  ## Packaging Methods
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
    Packaging Methods
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

<div class="grid grid-cols-2 gap-6 pt-6 items-stretch">
<div class="rounded-2xl px-6 py-6" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">
  <div class="text-sm uppercase tracking-widest opacity-60 mb-3">A rule you can sing</div>
  <div class="text-2xl leading-tight" style="max-width: 24rem;">
    When the cuckoo comes to the bare thorn,<br>
    Sell your cow and buy your corn;<br>
    But when she comes to the full bit,<br>
    Sell your corn and buy your sheep.
  </div>
  <div class="mt-8 rounded-xl px-4 py-4 text-lg" style="background: rgba(8,145,178,0.07); border: 1px solid rgba(8,145,178,0.18); display: inline-block;">
    Condition -&gt; decision rule
  </div>
</div>
<div class="rounded-2xl px-6 py-6" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">
  <div class="text-sm uppercase tracking-widest opacity-60 mb-3">A workflow song</div>
  <div style="font-size: 0.85em; line-height: 1.4; max-width: 28rem;">
    <div style="font-size: 1.05em; line-height: 1.5;">
      七月流火、八月萑苇。<br>
      蚕月条桑、取彼斧斨、以伐远扬、猗彼女桑。<br>
      七月鸣鵙、八月载绩。<br>
      载玄载黄、我朱孔阳、为公子裳。
    </div>
    <div class="mt-3 italic opacity-80" style="line-height: 1.5;">
      In the seventh month, the Fire Star marks the season;<br>
      in the silkworm month they strip the mulberry branches and take up their axes.<br>
      When the shrike calls in the seventh month,<br>
      spinning begins in the eighth —<br>
      dark and yellow cloth, bright red, for the robes of the princes.
    </div>
  </div>
  <div class="mt-4 rounded-xl px-4 py-4 text-lg" style="background: rgba(8,145,178,0.07); border: 1px solid rgba(8,145,178,0.18); display: inline-block;">
    A seasonal labor sequence in verse
  </div>
</div>
</div>
<!-- <div class="absolute bottom-4 right-6 text-xs opacity-60">Presscom: the cuckoo rhyme is preserved as an agricultural proverb; Berkshire: Qi Yue is treated as a farming-calendar poem listing seasonal work</div> -->

---

## Long before cheap, universal manuals, procedures often had to fit inside one's head.

<br>

## Rhythm, rhyme, and repeated performance made them portable.

<br>

## Verse is compression: portable, replayable, and memory-efficient.

<div class="absolute bottom-4 right-6 text-xs opacity-60">OUP: instructional verse and medical verse were long used for memorability and portability</div>

---

# Smuggling the runtime

<div class="grid grid-cols-2 gap-10 pt-8 items-start">
<div>
  <div class="rounded-3xl px-6 py-6" style="background: rgba(15,23,42,0.05); border: 1px solid rgba(15,23,42,0.12);">
    <div class="text-sm uppercase tracking-widest opacity-60 mb-3">Silk to Byzantium</div>
    <div class="text-xl leading-snug" style="max-width: 29rem;">
      Silk was not just a recipe. To deploy sericulture elsewhere, the Empire needed:
    </div>
    <div class="mt-6 grid grid-cols-1 gap-3">
      <div class="rounded-xl px-4 py-4" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(248,250,252,0.7);">the living eggs</div>
      <div class="rounded-xl px-4 py-4" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(248,250,252,0.7);">the mulberry-based feeding context</div>
      <div class="rounded-xl px-4 py-4" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(248,250,252,0.7);">the know-how to keep the system alive</div>
    </div>
  </div>
</div>
<div>
  <div class="text-4xl leading-tight" style="max-width: 28rem; color: rgb(8,145,178);">
    The runtime had to be smuggled.
  </div>
  <div class="pt-8 text-lg leading-snug" style="max-width: 32rem;">
    Eggs, warmth, mulberry leaves, and know-how all had to travel together.
  </div>
</div>
</div>

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
  <div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">Hack: helper tools to speed BASIC keyword entry</div>
  <div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(153,27,27,0.06);">Failure mode: cassette save errors as minor tragedy</div>
</div>
</div>

---

# Package repositories let software travel by reference

<div class="grid grid-cols-2 gap-10 pt-8 items-start">
<div>
  <div class="text-3xl leading-tight" style="max-width: 33rem;">
    With package repositories software becomes discoverable and installable from a shared repository rather than handed over as a pile of files.
  </div>
  <div class="pt-8 text-lg leading-snug" style="max-width: 34rem;">
    A Debian package is a description: what the software is, what it depends on, and how to obtain and compose everything it needs to run. The repository holds those descriptions; the machine does the fetching and building.
  </div>
</div>
<div>
  <div class="rounded-2xl px-5 py-6" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">
    <div class="text-sm uppercase tracking-widest opacity-60 mb-3">What travels now</div>
    <div class="grid grid-cols-1 gap-3">
      <div class="rounded-xl px-4 py-3" style="border: 1px solid rgba(15,23,42,0.12);">A named, versioned artifact</div>
      <div class="rounded-xl px-4 py-3" style="border: 1px solid rgba(15,23,42,0.12);">A dependency description</div>
      <div class="rounded-xl px-4 py-3" style="border: 1px solid rgba(8,145,178,0.18); background: rgba(8,145,178,0.07);">A pointer into a shared, maintained source</div>
    </div>
  </div>
</div>
</div>
<div class="absolute bottom-4 right-6 text-xs opacity-60">Debian project; GNU Guix: package collections make software distribution reproducible and declarative</div>

---

# Containers ship more of the runtime with the code

<div class="grid grid-cols-2 gap-10 pt-8 items-start">
<div>
  <div class="text-3xl leading-tight" style="max-width: 33rem;">
    A container image packages files, binaries, libraries, and configuration together. A registry stores and distributes those images.
  </div>
  <div class="pt-8 text-lg leading-snug" style="max-width: 34rem;">
    Containers bundle a much larger chunk of the runnable environment itself, making deployment far less dependent on what is already installed.
  </div>
</div>
<div>
  <div class="grid grid-cols-1 gap-3">
    <div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">Package systems: distribute recipes and dependency graphs</div>
    <div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(15,23,42,0.12); background: rgba(15,23,42,0.04);">Containers: distribute a far thicker runnable bundle</div>
    <div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(8,145,178,0.18); background: rgba(8,145,178,0.07);">docker pull &rarr; docker run &mdash; the runtime arrives with the code</div>
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
    Mosaic is the turning point.
  </div>
  <div class="pt-8 text-lg leading-snug" style="max-width: 34rem;">
    NCSA's big move was simple and enormous: pictures appeared automatically alongside text. After that, the browser keeps accumulating capabilities that make it feel more and more like a general host for software.
  </div>
</div>
<div class="col-span-2 rounded-2xl px-6 py-6" style="background: rgba(15,23,42,0.05); border: 1px solid rgba(15,23,42,0.12);">
  <div class="text-sm uppercase tracking-widest opacity-60 mb-3">Mutation</div>
  <div class="text-xl leading-snug">
    The browser stops being a page of linked text and starts becoming a software platform.
  </div>
</div>
</div>
<div class="absolute bottom-4 right-6 text-xs opacity-60">NCSA Mosaic: first published browser to automatically display pictures with text</div>

---

# The browser learns behavior

<div class="grid grid-cols-2 gap-10 pt-8 items-start">
<div>
  <div class="text-3xl leading-tight" style="max-width: 32rem;">
    First JavaScript makes the page react.
    Then XHR and Ajax teach it to change without turning the page.
  </div>
  <div class="pt-8 text-lg leading-snug" style="max-width: 33rem;">
    That is when the browser becomes a programmable environment.
  </div>
</div>
<div class="grid grid-cols-1 gap-4 text-center">
  <div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(15,23,42,0.12);">1995: page scripts react to clicks and forms</div>
  <div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(15,23,42,0.12);">XHR: fetch data without a full refresh</div>
  <div class="rounded-2xl px-5 py-5" style="border: 1px solid rgba(8,145,178,0.18); background: rgba(8,145,178,0.07);">Ajax: only part of the page changes, but the app keeps going</div>
</div>
</div>
<div class="absolute bottom-4 right-6 text-xs opacity-60">JavaScript created at Netscape in 1995; XHR and Ajax enabled partial-page updates</div>

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
    <li>URL delivery is already the easiest way to distribute a client</li>
  </ul>
</div>
<div>
  <div class="text-sm uppercase tracking-widest opacity-60 mb-3">New with Wasm</div>
  <ul class="list-disc text-lg leading-snug" style="padding-left: 1.2rem; max-width: 31rem;">
    <li>More of the existing compute core can travel inside that package</li>
    <li>Fewer tools need a server just to avoid installation pain</li>
    <li>Fewer teams need a rewrite-from-scratch browser version</li>
  </ul>
</div>
</div>
<div class="mt-10 rounded-2xl px-6 py-5" style="background: rgba(8,145,178,0.07); border: 1px solid rgba(8,145,178,0.18); max-width: 49rem;">
What makes WebAssembly interesting here is that this increasingly OS-like browser environment can now host larger pieces of existing software inside a browser-delivered tool.
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
