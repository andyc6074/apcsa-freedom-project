# Entry 3
##### 2/5/24

### Context
As I have been learning my tool for some time. I have spent a bit of time deciding on what type of game I should work on and what are the mechanics. After sitting down and thinking for a while, I have no luck in deciding on what the type is, however, the mechanic is more straightforward for me. I want my game to be based on light and shadow, "day" and "night" modes. Ok, past the general planning, I will be talking about the tinkering.

### How have I been learning
The way I learn a new feature is by looking at tutorials or any forms, which could be videos or websites. I follow through the steps then I change the value to see what has changed and what else affects what.
#### Example- Camera tracking
What I am trying to learn is Camera tracking for the player or in general, I learned there could be multiple ways of doing it but some are better than others.

option 1-parent class:
it will trail behind due to it being in the child's class, however, when the parent spins even a bit, it will move uncontrollably.


option 2- follow back:
 By using a script to make the camera follow the camera instead, we can eliminate that issue.
```C#
public Transform player;
    // this variable allow us to reference the Vector3(the 3 mean it is in 3 direction) PlayerMovement so we can use it
    public Vector3 offset;
    // Update is called once per frame
    void Update()
    {
        //Debug.Log(player.position);
        transform.position = player.position + offset;
    }
    //Transform* = to tell the computer to change the object vectors

    //We could put in a number here and try to change it, an easier way is to create an option where you can in a value from the main menu.

```
#### Example- Collision
I learn how to check for collision and how to reference other scripts.
```C#
public class PlayerCollision: MonoBehaviour
{
    //This line of code allows us to reference the script PlayerMovement so we can use it
    public PlayerMovement movement;


    private void OnCollisionEnter(Collision CollisionInfo){

        //Debug.Log("we hit something");
        //if make it so we can get some sort of information. and in this case, we chose tags.
        //the reason we chose tag is that, when checking on a bigger scale, it is much easier for the computer to check for tags instead of something like the name.
        if (CollisionInfo.collider.tag == "obstacle")
        {
            //Debug.Log("we hit obs");
            movement.enabled = false;
        }
    }
}

```
### MVP Goal
I want to figure out how to work with the gameplay sense such as continuous gameplay and keep track of scores.

How to make a Video Game playlist-(https://www.youtube.com/watch?v=j48LtUkZRjU&list=PLPV2KyIb3jR5QFsefuO2RlAgWEz6EvVi6&index=1)


[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
