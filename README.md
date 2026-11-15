# My Learning Journal

# 02 11 2026

Today I brainstormed what components and prototype I wanted to make.
My current idea is to make a prototype around trying to escape a radioactive facility, trying to avoid areas that contain radiation, and making sure your health is high enough to survive high radiation areas. This would need components of:

- Player controller - 3D
- Health and damage system
- Interaction system
- 

This would be extremely exciting and fun to do.

# 15 11 2026 - COMPONENT 1 - HEALTH & DAMAGE SYSTEM

Making my first component, a health system.
Firstly, I wanted to calculate the distance between two objects, the enemy and the player camera.
For this it was neccessary to understand the distance formula.

<img width="287" height="67" alt="image" src="https://github.com/user-attachments/assets/0ffdef84-319a-4862-aa5f-6783c006f0c7" />

This is the first hurdle I've encountered, I'm trying to log every frame the X position of the character object, and its failed. The two possible fixes I have is searching within the Unity Documentation to attempt
to find the fix, or follow a tutorial for how to find position. After looking through unity discussions and so on, I realised I was using int instead of float, so replacing this fixed the issue!

<img width="715" height="626" alt="image" src="https://github.com/user-attachments/assets/644e9981-e141-46c5-8fb1-13c6a4ddce30" />
<img width="1316" height="797" alt="image" src="https://github.com/user-attachments/assets/cb54f10f-179a-477a-be8a-525b54027103" />

I successfully managed to use the distance formula to calculate the distance between the character and the enemy!!!
<img width="630" height="861" alt="image" src="https://github.com/user-attachments/assets/3f65ae29-6a10-47dd-9146-c7a4a8fbe2aa" />

The next step is to find when the enemy is close to the player, then cause damage. I will make both the damage and distance a public float so it can easily be changed.
To calculate damage, I will put an if statement in the update method to check the players distance to the enemy, and subtract a damage value each frame.
With checking if distance <= distance to check for, set take damage to true and subtract damage from health.

<img width="465" height="353" alt="image" src="https://github.com/user-attachments/assets/39985090-6470-4b1d-9999-ba67aaf708db" />

FOR TIME JOURNAL: 15/11/2026 / 3 hours / 2pm - 3pm, 9pm - 10pm / Created code to check distance between two objects using the distance formula, created a damage system that works if the distance is within a certain
amount.












