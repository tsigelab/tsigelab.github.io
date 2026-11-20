---
layout: page
title: predictor
permalink: /predictor/
description: Room-temperature surface tension of a polymer or a liquid from a single structure.
nav: true
nav_order: 1
---

Enter a **PSMILES** with two `*` for a polymer repeat unit (for example `*CC(C)*` for polypropylene), or a **SMILES** without `*` for a small-molecule liquid (for example `Cc1ccccc1` for toluene). The tool picks the matching graph neural network model and returns one prediction per submission.

<iframe id="predictor-frame" data-src="{{ site.predictor_url }}/~/+/?embed=true" title="Surface tension predictor" style="width: 100%; height: 820px; border: 0;"></iframe>
<script>
  (function () {
    var frame = document.getElementById("predictor-frame");
    var base = frame.getAttribute("data-src");
    var shown = null;
    function sync() {
      var theme = document.documentElement.getAttribute("data-theme") === "dark" ? "dark_theme" : "light_theme";
      if (theme !== shown) {
        shown = theme;
        frame.src = base + "&embed_options=" + theme;
      }
    }
    sync();
    new MutationObserver(sync).observe(document.documentElement, { attributes: true, attributeFilter: ["data-theme"] });
  })();
</script>

If the tool does not load, <a href="{{ site.predictor_url }}" target="_blank" rel="noopener">open it in a new tab</a>.
