# Lab Report 5 - Putting it All Together
## Part 1 - Debugging Scenario

**Student Post:**

<br/>

Hello! I've been stuck on this Java program for a while now and was wondering if anyone had any insight/advice. The program is supposed to process user profiles from a list and print out the names and emails of the users. However, when I run the program, it throws a `NullPointerException`. For context, the program is supposed to iterate through an array of `UserProfile` objects and read/print user data. I'm pretty sure all the objects in `UserProfile` have a name and email. If one of the objects were missing a name and email or doesn't even exist, would that be the cause of the error? Additionally, how would I fix my code so that this error doesn't occur again? Below is a screenshot of the error.

<br/>

![image](https://github.com/QuocBaoNNguyen/cse15l-lab-reports/assets/156359008/c1c337c2-b68e-42f9-b61a-c5192115baa8)

<br/>

**TA Response**

<br/>

Hi! Generally, a `NullPointerException` would occur when you try to access a method or object that is null. It is very much a possibility that one of the profiles in `UserProfile` is null or that the object itself exists but the property you're trying to access is null. Maybe try double checking that all the elements in your `UserProfile` array and the properties of the elements are initialized correctly. An approach to fix your code would be to add a null check at the beginning of your code so that it knows how to handle nulls would let you know if anything object or property being accessed is null.

<br/>

**Student Response**

<br/>

Thank you for the advice! After some work, I added null checks to my code and found that the bug was that one of the `UserProfile` objects was actually null. I now understand the importance of checking for null objects/ methods!

<br/>

![image](https://github.com/QuocBaoNNguyen/cse15l-lab-reports/assets/156359008/e41ca888-7f6b-4749-93f0-8b4c57f061cc)

<br/>

**Setup Information**

<br/>

File and Directory Structure:



UserProfile.java- Defines the `UserProfile` class and initiates the name and email properties
ProcessProfiles.java- Program that processes and prints the user profile data(name and email)
run.sh- Bash script that will compile and run the `ProcessProfiles.java` program
All are in the `/home` directory

<br/>

**Contents of `UserProfile.java` Before:**

<br/>

```
public class UserProfile {
    private String name;
    private String email;

    public UserProfile(String name, String email) {
        this.name = name;
        this.email = email;
    }

    public String getName() {
        return name;
    }

    public String getEmail() {
        return email;
    }
}
```

<br/>

**Contents of `ProcessProfiles.java` Before:**

<br/>

```
public class ProcessProfiles {
    public static void main(String[] args) {
        UserProfile[] userProfiles = new UserProfile[3];
        userProfiles[0] = new UserProfile("John Doe", "john@example.com");
        userProfiles[1] = null; // This causes the NullPointerException
        userProfiles[2] = new UserProfile("Jane Smith", "jane@example.com");

        for (UserProfile user : userProfiles) {
            System.out.println(user.getName() + " - " + user.getEmail()); // Error occurs here
        }
    }
}
```

<br/>

**Full Bug Triggering Command Line:**

<br/>

```
javac ProcessProfiles.java
java ProcessProfiles
```

<br/>

**Description of Fixing Bug:**

<br/>

In order to fix the bug, make sure that each `UserProfile` object and the properties that are being accessed are not null before trying to access them. This can be done by adding a null check at the beginning of the code such as the one below.

<br/>

```
for (UserProfile user : userProfiles){
            if (user == null){
                System.out.println("An object in the array is null!");
                return;
            }
        }

        for (UserProfile user : userProfiles){
            if (user.getName() == null || user.getEmail() == null){
                System.out.println("A property of an object of the array is null!");
                return;
            }
        }
```

<br/>

## Part 2- Reflection

<br/>

reflection...

















