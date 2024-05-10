# Ex06-Redirecting-the-Scene

## Aim:
To Redirecting the scene in the unity engine.

## Algorithm:
Step 1:
To open the unity engine.

Step 2:
Create a new 3D project.

Step 3:
Create plane and name it as ground and create cube and name it as player.

Step 4:
Add WinText in Hierarchy.

Step 5:
Create a C# Script and name it as playercontroller and add the script to player.

Step 6:
Use the R button to change the level2

Step 7
Print the Output and end the program.

## Program:
## NAME : THRIKESWAR
## REGISTER NUMBER : 212222230162

```c#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;


public class cube : MonoBehaviour
{
    Rigidbody rb;
    public GameObject WinText;
    // Start is called before the first frame update
    void Start()
    {
        rb=GetComponent<Rigidbody>();
    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("Level 2");
        }
    }
    private void OnCollisionEnter(Collision Other)
    {
        if (Other.gameObject.tag=="Destroy")
        {
            Destroy(Other.gameObject);
            WinText.SetActive(true);
        }
    }
}
```

## Output:
![img1](https://github.com/Naveensrinivasan07/Ex06-Redirecting-the-Scene/assets/119475891/9a686992-51ac-4cff-9c97-f95009f40ce3)
![img2](https://github.com/Naveensrinivasan07/Ex06-Redirecting-the-Scene/assets/119475891/2bdce292-620f-4ff4-897d-1da2df2a6898)
![img3](https://github.com/Naveensrinivasan07/Ex06-Redirecting-the-Scene/assets/119475891/f50c7e40-e5ab-4abc-b66b-3c965b7f0dd1)

## Result:

The above C# coding is successfully redirecting the scene in the unity engine.
