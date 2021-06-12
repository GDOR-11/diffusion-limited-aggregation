# diffusion-limited-aggregation
A diffusion limited aggregation algorithm using what i like to call randomized ray marching with quadtrees
<br><br>
ok let's see what each term on this sentence means
<br><br>
diffusion limited aggregation is just a bunch of particles moving around randomly and when they hit the DLA they get stuck (therefore being added to the DLA), and the DLA starts with one static particle.
<br><br>
randomized ray marching is just what i used to make the random motion faster, basically the particle calculates its distance to the DLA (using quadtrees), moves that distance with a random angle an repeats this until it gets close enough to the DLA
<br><br>
quadtrees is a data structure, where there is a big rectangle (covering the whole screen), and this rectangle gets subdivided in the quadrants where the DLA is at, and each one of these quadrants (that are olso rectangles) also gets subdivided, and again and again up to a certain limit.
<br>
quadtrees help a lot when you want to calculate the distance from a particle to the DLA, because you can check the particles in the little rectangles in a smart way such that ou don't check far particles, only the needed ones
<br><br><br>
note that these topics are horribly explained to make them "easier" to understand, if you want to really understand these topics look at the wikipedia pages on <a href = 'https://en.wikipedia.org/wiki/Diffusion-limited_aggregation'>diffusion limited aggregation</a>(very small) and <a href = 'https://en.wikipedia.org/wiki/Quadtree'>quadtrees</a>(very big). unfortunately i invented randomized ray marching exactly for this purpose then there aren't any wikipedia pages :(
