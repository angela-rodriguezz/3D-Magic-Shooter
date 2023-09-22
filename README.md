# 3D-Magic-Shooter

![](https://github.com/angela-rodriguezz/3D-Magic-Shooter/blob/master/3d%20gif.gif)

A first person, 3D platformer and shooter with elemental attacks using Unity's particle system. Programmed the code for player movement, enemies, attacks, and animations. 

## Game Design
The main goal is to gain the highest score from shooting each of the particles. The more particles you eliminate, the higher the score and the more health you are rewarded to make it easier to survive.

## Gameplay Mechanics

There are two different attack animations to use. Both attacks remove health from the playable character. The red particle attack removes more health, but deals more damage and the pink particle attack removes less health for a smaller attack damage.

## Programming Lessons
Some important coding features I now will implement in my projects are the #region and Tooltip feature. Previously, I simply generated the variable without any labels. However, the Tooltip aids in the ability to debug and recall each of the UI features you are implementing within the game. Additionally the #region allows for the categorization of certain parts of code that adds to the readability of the code.

Additionally, my first introduction to Coroutines and random spawning of enemies within a 3D space. I needed to generate the enemies randomly and to always spawn infinitely. However, there couldn't be a fast generation or that will impact performance and make the game too difficult.

``` ruby
private IEnumerator Spawn(int enemyInd)
{
    ...
    while (alwaysSpawn || i < info.NumberToSpawn)
    {
        yield return new WaitForSeconds(info.TimeToNextSpawn);
        float xVal = m_Bounds.x / 2;
        float yVal = m_Bounds.y / 2;
        float zVal = m_Bounds.z / 2;

        Vector3 spawnPos = new Vector3(
            Random.Range(-xVal, xVal),
            Random.Range(-yVal, yVal),
            Random.Range(-zVal, zVal));
        spawnPos += transform.position;
        Instantiate(info.EnemyGO, spawnPos, Quaternion.identity);
        ...
    }
```

## Lessons

From this project, I have realized the imporance in the organization in features of my code and intend to implement several of the features I learned in this project in the future.

## Playable Demo
[Play Here 🖥️](http://www.angelarodriguezz.me/3D-Magic-Shooter/)
