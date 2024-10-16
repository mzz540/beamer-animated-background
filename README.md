## Beamer Animated Background using TikZ and Animate

This project creates an animated background for Beamer presentations using TikZ to generate randomized color grids and Animate to loop through frames, creating a dynamic effect. The background changes each time the code is executed, as colors and opacity are randomly generated.

# Project Overview
1. Frame Generation (`background.tex`):

  - Randomly generates colored blocks using six predefined colors.
  - Each time you compile the code, the arrangement of colors and opacity changes, simulating motion in the final animation.
  - This code generates a series of frames (e.g., `frame_0.pdf`, `frame_1.pdf`, etc.).

2. Animation (`animation.tex`):

  - Uses the frames generated from background.tex to create a continuous animation in a Beamer presentation.
  - The animateinline package is used to cycle through the frames automatically.

# Customization
  - Colors and Opacity: You can change the colors or adjust the opacity of the blocks in `background.tex` by editing the predefined color codes and opacity values.
    
  - Grid Size: Modify the block size and grid spacing by adjusting the loops in `background.tex`:

```
Latex
\foreach \x in {0,0.2,...,15.75} { % Horizontal grid spacing
\foreach \y in {0,0.2,...,11.75} { % Vertical grid spacing
```

  - Frame Rate: You can control the speed of the animation by changing the rate value in `animation.tex`:
```
Latex
\begin{animateinline}[autoplay,loop,rate=0.5]{3}
```

  
