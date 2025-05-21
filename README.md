# Ex06-Redirecting-the-Scene

## Aim:
To Redirecting the scene in the unity engine.

## Algorithm:
Step 1: To open the unity engine.

Step 2: Create a new 3D project.

Step 3: Create plane and name it as ground and create cube and name it as player.

Step 4: Add WinText in Hierarchy.

Step 5: Create a C# Script and name it as playercontroller and add the script to player.

Step 6: Use the R button to change the level2.

Step 7 Print the Output and end the program.

## Program:
## DEVELOPED BY : AHALYA S
## REG NO : 212223230006

```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;
public class coding : MonoBehaviour
{
    Rigidbody rb;
    public GameObject WinText;
    // Start is called once before the first execution of Update after the MonoBehaviour is created
    void Start()
    {
        rb = GetComponent<Rigidbody>(); 
    }

    // Update is called once per frame
    void Update()
    {
        if(Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("level2");
        }
    }
    private void OnTriggerEnter(Collider other)
    {
        if(other.gameObject.tag == "Cube")
        {
            Destroy(other.gameObject);
            WinText.SetActive(true);
        }
    }
}
```


## Output:

![Screenshot 2025-05-21 141033](https://github.com/user-attachments/assets/67424f1d-16a9-4880-9e02-0a3900b7a129)


![Screenshot 2025-05-21 141056](https://github.com/user-attachments/assets/c928ad3c-2535-4604-9adf-96ef12b3fbe5)


![Screenshot 2025-05-21 141116](https://github.com/user-attachments/assets/8b71d9ca-1025-41a0-be01-d8df513281fe)


## Result:
The above C# coding is successfully redirecting the scene in the unity engine.
