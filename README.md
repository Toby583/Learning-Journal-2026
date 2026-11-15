# My Learning Journal

# 02 11 2026

Today I brainstormed what components and prototype I wanted to make.
My current idea is to make a prototype around trying to save a crashing military plane, following a checklist for what to press within the cockpit, and the cabin, to save the aircraft. This would need components of:

- Player controller - 2D/3D
- Interaction system
- Screen shake
- Health system

This would be extremely exciting and fun to do.

# 15 11 2026

Making my first component, without any tutorials, a health system.
My first hurdle was trying to calculate the distance between two objects, the enemy and the player camera
For this I wanted to understand the distance formula using Pythagorean theorem a2 + b2 = c2 in coordinate geometry

<img width="287" height="67" alt="image" src="https://github.com/user-attachments/assets/0ffdef84-319a-4862-aa5f-6783c006f0c7" />

This is the first hurdle I've encountered, I'm trying to log every frame the X position of the character object, and its failed. The two possible fixes I have is searching within the Unity Documentation to attempt
to find the fix, or follow a tutorial for how to find position. After looking through unity discussions and so on, I realised I was using int instead of float, so replacing this fixed the issue!

<img width="715" height="626" alt="image" src="https://github.com/user-attachments/assets/644e9981-e141-46c5-8fb1-13c6a4ddce30" />
<img width="1316" height="797" alt="image" src="https://github.com/user-attachments/assets/cb54f10f-179a-477a-be8a-525b54027103" />

I successfully managed to use the Pythagorean theorem to calculate the distance between the character and the enemy!!!
<img width="630" height="861" alt="image" src="https://github.com/user-attachments/assets/3f65ae29-6a10-47dd-9146-c7a4a8fbe2aa" />

The next step is to find when the enemy is close to the player, then cause damage. I will make both the damage and distance a public float so it can easily be changed.













