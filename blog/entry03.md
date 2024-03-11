# Entry 3
##### 2/5/24

### Context
As I have been learing my tool for some time. I have focas a bit of time decideing on what type game I should work on and what are the mecanices. After siting down and thinking for a while, I have no luck in decide on what the type, however the mechanic is more strait forward for me. I want to my game to based on light and shadow, "day" and "night" modes. Ok, pass the gernal planing, I will be talking about the tinkering.

### How I been learning
They way I learn a new feature is by look at tutatral any forms, could be vidieo or websites. I follow trough the steps then I change value to see what that has change and what else effect what.
#### Example- Camera tracking
What I am trying to learn is Camera tracking for the player or in genral, I learn there could be mutple way of doing it but some are better then other.

option 1-parent class:
it will tain behind however due to it being in the child class, the the parent move even a bit, it will move unctrollable.


option 2- follow back:
 By using a scipt to make the cammera follow cammera instead, we can elmite that issue.
```C#
public Transform player;
    // this varible allow us to refence the Vector3(the 3 mean it is in 3 direction) PlayerMovement so we can use it
    public Vector3 offset;
    // Update is called once per frame
    void Update()
    {
        //Debug.Log(player.position);
        transform.position = player.position + offset;
    }
    //Transform* = to tell the computer to change the object vectors

    //We could put in a number here and try to change it, a easer way is to create a option where you can in a value from the main menu.

```
#### Example- Collision
I learn how to check for collision and how to refence other scripts.
```C#
public class PlayerCollision : MonoBehaviour
{
    // this line of code allow us to refence the script PlayerMovement so we can use it
    public PlayerMovement movement;


    private void OnCollisionEnter(Collision CollisionInfo){

        //Debug.Log("we hit something");
        //if make it so we can get some sort of information. and in this case we chose tags.
        //the reason we chose tag is because, when checking on a bigger scale, it is much easier to for the computer to check for tags instead of somthing like name.
        if (CollisionInfo.collider.tag == "obstacle")
        {
            //Debug.Log("we hit obs");
            movement.enabled = false;
        }
    }
}

```
### MVP Goal
I want to figure out how to work with the the gameplay sence such as contunious gameplay and keep track of scores.

How to make a Video Game playlist-(https://www.youtube.com/watch?v=j48LtUkZRjU&list=PLPV2KyIb3jR5QFsefuO2RlAgWEz6EvVi6&index=1)


[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
