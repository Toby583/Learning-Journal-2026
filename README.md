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

# 16/11/2026

Today I am continuing component 1 by adding a health kit system, where I want to use collision detection to see if the player object comes into contact with an object tag "health_kit". I have faced a problem of
my code not working.

<img width="552" height="165" alt="image" src="https://github.com/user-attachments/assets/856982e3-76b3-4ae1-9d28-8086c371e601" />

I discovered that the issue was using OnCollisionEnter instead of OnTriggerEnter, since I was using On Trigger for the object, and also not using Compare Tag. It now works as it should.
What I've done so far is essentially the health and damage system, but I will tomorrow add some more features!

FOR TIME JOURNAL: 16/11/2026 / 1.5 hours / 7pm - 8:30pm / Continued working on damage and health system, adding code using on trigger enter to provide more health to the player when close to a health kit object.

# 16/11/2026

Today I completed the code for my component one, the scene contains a moveable character, using a very simple input actions tutorial: https://www.youtube.com/watch?v=q-VfsQQlji0 , an enemy that damages you if you get close, and some one time use medkits that will heal you! The next component I will be making is an interaction system.

<img width="977" height="698" alt="image" src="https://github.com/user-attachments/assets/f1422e0c-6afa-4d56-b79a-d21065af78f1" />


FOR TIME JOURNAL: 18/11/2026 / 1 hour / 4pm - 5pm / Finished component one, adding a very simple character movement and ui.

# 19 11 2026 - COMPONENT 2 - Interaction system

Now it is time to move onto my next component, an interaction system. To do this, my idea is to use an on trigger event and show a ui element combined with a bool set to true, allowing the player to interact
with the object. Before doing this, I created my GitHub repository. The first issue i have faced is the input not being registered:

<img width="598" height="351" alt="image" src="https://github.com/user-attachments/assets/ceb5585a-188a-41cc-9b47-cb151ef28ed2" />

FOR TIME JOURNAL: 19/11/2026 / 1 hour / Started working on component 1, an interaction system, hit a wall where the code didn't work.

# 20 11 2026 - COMPONENT 2 - Interaction system

The issue I faced yesterday with the interaction code I made is the input not being registered. I found the issue was OnTriggerEnter only gets called once, then after its called I should be able to 
press E to log a message, with it failing. My solution is to have an update where if ready to interact = true and input is true, then log the message. For the OnTriggerEnter event, I added an OnTriggerExit event aswell
with them containing ready to interact = true on enter, and ready to interact = false on exit.

This worked as I hoped it would:

<img width="637" height="575" alt="image" src="https://github.com/user-attachments/assets/4f849e90-7915-4d88-b1c8-1a0abb49197f" />

<img width="364" height="182" alt="image" src="https://github.com/user-attachments/assets/d7a9b976-37dc-4839-8bd3-c88d044ce426" />

The next thing I want to do is show a UI element when you're able to interact with the object for an example of how you could use this component. After making text appear when the player hits the collider of the interactable object, I created an example of an interaction
event, where using transform.translate, created code where the object moves up. An issue that came up was the object only moved up a little then stopped, after having another look I realized it was because the code
was placed inside of the if statement requiring two fields to be true, press E and have ready to interact be true. To fix this, I added a bool named is Moving, and made another if statement to check if this bool is true, then make the interactable object move up.

<img width="524" height="737" alt="image" src="https://github.com/user-attachments/assets/0f68dc0b-2d33-4bfa-a7b3-a4eb3b63bfaa" />

This is essentially the whole of the component, now I need to make sure it works correctly and write up the documentation for it.

FOR TIME JOURNAL: 20/11/2026 / 1 hour / Finished the code for component 2, working on documentation.

# 24 11 2026 - COMPONENT 2 - Interaction system

Today I wrote up the documentation for the interaction system, and made sure there were no bugs within the code. The next component I will be working on is moving platforms.

FOR TIME JOURNAL: 24/11/2026 / 1 hour / Wrote up documentation for Component 2 - Interaction

# 26 11 2026 - COMPONENT 3 - Moving Platforms

Today I am working on my next component of moving platforms, where my initial step was to create my repository on GitHub. 
To make the moving platforms, my memory of how it works is to place two points and make the platform move between those 2 positions.
I will be using transform.translate to code the movement.

The first problem I am facing is within my code it translates the platform forwards multiplied by speed, and when the platform collides with a point, I negative the speed to reverse the platform.
However, it isn't moving in the other direction, nor is it logging anything..

<img width="818" height="645" alt="image" src="https://github.com/user-attachments/assets/e1c45806-9219-458f-9092-9cdc8da49e1b" />

Quickly, I remembered the fix was to add a rigid body to the platform, making it work perfectly!
I will continue working on this tommorow

FOR TIME JOURNAL: 26/11/2026 / 1 hour / Started component 3 - Moving platforms

# 27 11 2026 - COMPONENT 3 - Moving Platforms

Today I continued working on the moving platforms component, where my next step is to make the player parented to the platform when standing on top of it. This is due to how the player wouldn't stay on the platform
and would fall off, so a fix is to make its parent the platform. Because the platform has a rigidbody and doesnt use gravity, but the player object does, it makes the platform tip from the players weight. To fix this,
I froze each axis on the platforms rigid body position and rotation constraints.

The code works perfectly and is controlled via a speed variable, the next step will be to write the documentation.

<img width="1146" height="696" alt="image" src="https://github.com/user-attachments/assets/8603ee0a-6f41-452f-aa10-076893579908" />
















