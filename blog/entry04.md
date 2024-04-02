# Entry 4
##### 2/4/24

### Context
As I have been learning my tool for some time. I have spent some time deciding what type of game I should work on and what the mechanics are. After sitting down and thinking for a while, I have no luck in deciding on what the type is, however, the mechanic is more straightforward for me. I want my game to be based on light and shadow, "day" and "night" modes. Ok, past the general planning, I will be talking about the tinkering.

### How have I been learning
The way I learn a new feature is by looking at tutorials or any forms, which could be videos or websites. I follow through the steps then I change the value to see what has changed and what else affects what.


#### Example- prefabs
Prefabs are a special type of component that allows fully configured GameObjects to be saved in the Project for reuse.

Prefabs are used if you want to use multiple of the same object at the same time.

 If you affect one prefab object, each of the same objects will change along with it. (Remember to apply when changing something on the prefab.)

#### Example- movement+
to make the movement more smoother we will have to change some things. The reason for this is speed build-up, so when changing the direction you will need to build up enough to first do so.

```C#
void FixedUpdate()
{
    //added a forward force
    rb.AddForce(0, 0, forwardForce * Time.deltaTime);

    if (Input.GetKey("d"))
    {
        rb.AddForce(sidewayForce * Time.deltaTime, 0, 0, ForceMode.VelocityChange);
    }

    if (Input.GetKey("a"))
    {
        rb.AddForce(-sidewayForce * Time.deltaTime, 0, 0, ForceMode.VelocityChange);
    }
}
//VelocityChange changes the velocity vector directly without the need to speed down or speed up.
```

### MVP Goal
I want to figure out how to work with the UI and possibly the game over screen.

How to make a Video Game playlist-(https://www.youtube.com/watch?v=j48LtUkZRjU&list=PLPV2KyIb3jR5QFsefuO2RlAgWEz6EvVi6&index=1)

[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
