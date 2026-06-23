---
title-slide: false
bibliography: references.bib
csl: vancouver.csl
citeproc: true
theme: serif
background-color: "#ffffff"
transition: slide
navigationMode: linear
hash: true
---

:::: {.columns}
::: {.column width="50%"}

## Sample slides
#### PlaceHolderName
#### Universiti Malaysia Perlis
#### [placeholder@email.com](mailto:placeholder@email.com)

<audio id="bg-music" src="media/audio/sb.m4a" loop></audio>

<div id="audio-credit"
     style="position: absolute; bottom: 40px; right: 20px; font-size: 0.6em; opacity: 0.6;">
  Music: “Adrift” by Scott Buckley (CC BY 4.0)
</div>

<script>
  document.addEventListener('DOMContentLoaded', () => {
    const audio = document.getElementById('bg-music');
    const credit = document.getElementById('audio-credit');

    // hide credit by default
    credit.style.display = 'none';

    const test = new Audio('media/audio/bgm.mp3');

    test.addEventListener('canplaythrough', () => {
      // bgm.mp3 exists → use it, keep credit hidden
      audio.src = 'media/audio/bgm.mp3';
    }, { once: true });

    test.addEventListener('error', () => {
      // bgm.mp3 missing → sb.m4a will play → show credit
      credit.style.display = 'block';
    }, { once: true });

    document.addEventListener('click', () => {
      if (Reveal.getIndices().h === 0) {
        audio.volume = 0.5;
        audio.play();
      }
    }, { once: true });

    Reveal.on('slidechanged', (event) => {
      if (event.indexh > 0) { audio.pause(); }
      else { audio.play(); }
    });
  });
</script>

:::

::: {.column width="50%"}
![](media/pics/logo1.png)
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Slide one
**Key Concepts:**
- Energy conservation per @carnot1824.
- $\Delta U = Q - W$
:::

::: {.column width="50%"}
![](media/pics/sample.png)
:::
::::

---

<span class="slide-title" data-title="My Hidden Slide Name"></span>

![](media/pics/wide.jpeg)

---

:::: {.columns}
::: {.column width="50%"}
### The Master Equation
The fundamental relation of thermodynamics:

$$\Delta U = Q - W$$

The work done $W$ is positive when the system expands against an external pressure.
:::

::: {.column width="50%"}
<video data-src="media/videos/sample.mp4" data-autoplay loop muted width="100%"></video>
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Visualizing the Gas Law
**Interactive Model:**

- P, V, and T relationships.
- Use the slider to adjust pressure.
- Observe the phase boundary.
:::

::: {.column width="50%"}
<iframe 
  data-src="media/plots/sample.html" 
  width="100%" 
  height="500px" 
  style="border:none;" 
  scrolling="no">
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 1 Resistance Analysis

- **Temperature**: Highly Significant ($p = 0.0000$)
- **Pressure**: Highly Significant ($p = 0.0000$)
- **Interaction**: Not Significant ($p = 0.7222$)

Both factors independently reduce resistance. Since the goal is minimizing resistance below the USL of 10, higher settings of both parameters appear beneficial.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/m1_resistance.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

# Cross-Machine Comparison

:::::: {.columns}
::: {.column width="50%"}
### Resistance Trends
Comparing Machines 1, 2, and 3:

- **Machine 1** shows the lowest overall Resistance levels.
- **Machine 2** consistently exhibits higher Resistance regardless of settings.
- Increasing **Pressure** and **Temperature** generally reduces Resistance across all units.
- The USL (10) is met more consistently by Machine 1.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/all_machines_resistance.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::::

---

# Conclusion: Interaction Effects

- **Primary Drivers:** Pressure and Temperature are the main drivers of quality.
- **Interaction P*T:** Across the manufacturing process, the interaction term is non-significant ($p > 0.05$).
- **Recommendation:** Optimize Pressure and Temperature independently to minimize Resistance. Machine 1 is the preferred unit for meeting the "lower is better" criteria.

---
# Bibliography
<div id="refs"></div>
