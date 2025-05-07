# Exp.No:35  
## TOWER OF HANOI

---

### AIM  
To write a Python program to implement **Tower of Hanoi** and display all the moves of the disks using a recursive function.  
Consider the names of the tower pegs as A, B, C. Get the number of disks value from the user.

---

### ALGORITHM  

1. **Start the program.**
2. **Input** the number of disks `n`.
3. **Print** the number of disks.
4. Define a **recursive function** `TowerOfHanoi(n, source, destination, auxiliary)`:
   - If `n == 1`:
     - Print: "Move disk from source to destination".
   - Else:
     - Call `TowerOfHanoi(n - 1, source, auxiliary, destination)`  
       → Move `n-1` disks from source to auxiliary using destination as helper.
     - Print: "Move disk from source to destination"  
       → Move the largest disk to the destination.
     - Call `TowerOfHanoi(n - 1, auxiliary, destination, source)`  
       → Move `n-1` disks from auxiliary to destination using source as helper.
5. Call `TowerOfHanoi(n, 'A', 'C', 'B')` to start the process.
6. **End the program.**

---

### PROGRAM  

```
#Reg.NO-212223060119
#Name-Kavindra T G
def TowerOfHanoi(n, source, destination, auxiliary):
    if n == 1:
        print(f"Move disk 1 from {source} to {destination}")
        return
    TowerOfHanoi(n - 1, source, auxiliary, destination)
    print(f"Move disk {n} from {source} to {destination}")
    TowerOfHanoi(n - 1, auxiliary, destination, source)

n = int(input("Enter the number of disks: "))
print(f"Number of disks: {n}")
TowerOfHanoi(n, 'A', 'C', 'B')



```

### OUTPUT
![image](https://github.com/user-attachments/assets/30360199-3e1d-4286-86b4-3b5e19ca6f47)



### RESULT
Thus, the python program to implement **Tower of Hanoi** and display all the moves of the disks using a recursive function.  
Consider the names of the tower pegs as A, B, C. Get the number of disks value from the user has been executed and verified successfully.
