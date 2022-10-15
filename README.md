# Simulating Impacts -- A Very Specific Physics Engine

<p align="center">
  <img width="50%" src="https://lh6.googleusercontent.com/DkLHuv10JCAyICOj3ImhsTpJaDbn0RaNpXyIfQzSSsb2jv20-AaIMsX0qlhzOCnBM5OkStYnizrvu6v2NLso7hprXU1WBev-RSdMsfnm5vjQXws8YyHcfV2k-0D_rEVw9lyfbERm7lW_-ns_IxHfgwpDDpcxKTV4LczA1DiDtQfkTZcDO0f6GFp5GA" alt="Die In a Box GIF"/>
</p>

ME314 (Theory of Machine Dynamics) was an introductory course in rigid multi-body dynamics. It culminated in an independent final project that brought together a lot of what was foundational to the course:

- Analyzing **rotating rigid body geometries**
- Using **Lagrange** equations to derive **equations of motion** 
- Enforcing **geometrical constraints** and applying **external driving forces**
- Solving **impact dynamic** equations
- And leveraging Numpy and Scipy for **numerical methods simulation** of mechanical systems

Such was my “die in a box” simulation project – which was effectively a very specific very limited physics engine of a die falling in gravity and colliding with the internal walls of a box, itself being shaken.

## Die In a Box Formulation

See [Project Writeup](https://github.com/kjwelbeck3/me314_DieInABox/blob/main/ME314%20Final%20Project%20Writeup-%20Die%20in%20a%20Cup%20.pdf) for 

- a Model Drawing of respective coordinate frames and relative transforms;  
- a description of the approach to constraints
- and the Euler-Lagrange and impact update equations

See [Jupyter Notebook](https://github.com/kjwelbeck3/me314_DieInABox/blob/main/ME314_Die%20in%20Cup_KojoWelbeck.ipynb) for implementation details

## Simulation Results

The die in the cup begins at rest and drops under gravity until one corner impacts the bottom of the cup, which is itself being driven by an external force. Both cup and die react upon impact and continue to collide multiple times during the simulation/animation as they both translate and rotate continually. The die only impacts the internal walls of the cup at its (the die’s) corners, per the initial conditions: q_die = (0, 0, pi/4), q_cup=(0, 0, -pi/15) 

See [Video](https://github.com/kjwelbeck3/me314_DieInABox/blob/main/DieInACup.mp4)