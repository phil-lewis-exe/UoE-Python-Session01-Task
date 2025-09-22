<style>
details { padding-top: 1em; padding-bottom:1em;}
details summary {text-transform: uppercase; font-size: 0.8em; text-transform: uppercase; font-weight: bold; }
</style>

# Session 01: Practice Activity 

You should now have read through the Session 1 activities. These cover the first two chapters in Crash Course in Python, and also how to work in the CodeSpaces web IDE.

This exercise is set up to let you try out those skills: how to open your workspace; create a Python file; write code to store information and do calculations; and save your work to your GitHub repository.

## Forking the Repository & Launching Your Codespace

Before you can start coding, you need to create your own copy of the course repository. This is called "forking". Forking allows you to experiment and save your work without affecting the original project.

1. **Go to the repository page that contains an empty workspace for you to use for the lecture activities:** [https://github.com/phil-lewis-exe/UoE-Python-Codespace](https://github.com/phil-lewis-exe/UoE-Python-Codespace)

2. **Fork the Repository:** In the top-right corner of the page, click the **Fork** button.

3. **Create Your Fork:** You will be taken to the "Create a new fork" page.
   * Make sure your own GitHub username is selected as the **Owner**.
   * You can leave the **Repository name** and other settings as they are.
   * Click the green **Create fork** button. GitHub will take a moment to create your personal copy.

4. **Launch Codespaces:** Once your fork is created, you'll be on the main page for *your* copy of the repository.
   * Click the green **Code** button.
   * Select the **Codespaces** tab.
   * Click **Create codespace on main** to launch your cloud-based VS Code editor. This might take a minute or two to build for the first time.

## Navigating Your Workspace in the Terminal

Your Codespace provides a ready-to-use development environment. The terminal is a powerful tool for navigating this environment and managing files.

1. **Open the Integrated Terminal:** Your Codespace should open with a terminal panel already at the bottom.

2. **Find Your Current Location:** In Codespaces, the terminal starts with the working directory set to the main project folder. To verify this, type the `pwd` command into the terminal and press `Enter`. The `pwd` command stands for 'print working directory'.
   ```bash
   pwd
   ```
   You should see an output something like `/workspaces/UoE-Python-CodeSpace`.

3. **List the Directory Contents:** To see what's in your current directory, use the `ls` command, which stands for 'list'.
   ```bash
   ls
   ```
   You will see a list of files and directories, which should include the `WORKSPACE` directory.

4. **Change into the Workspace Directory:** Now, let's move into the main `WORKSPACE` directory for your course. Use the `cd` command, which stands for 'change directory'.
   ```bash
   cd WORKSPACE
   ```

5. **Navigate into the Session Folder:** You can use the `ls` command to see the contents of this directory. It is suggested that you work for this exercise in the `Session01` folder. Type the `cd` command again to move into that directory.
   ```bash
   cd Session01
   ```

6. **Verify Your New Location:** It's good practice to check you are where you think you are. Run the `pwd` command again.
   ```bash
   pwd
   ```
   The output should now be `/workspaces/UoE-Python-CodeSpace/WORKSPACE/Session01`.

7. **Create Your Python File:** You are now in the correct directory to create your file for this exercise. Use the `touch` command to create a new, empty Python file named `cinema_ex.py`.
   ```bash
   touch cinema_ex.py
   ```

8. **Confirm File Creation:** To be sure the file was created, use the `ls` command one more time.
   ```bash
   ls
   ```
   You should now see your new `cinema_ex.py` file listed in the terminal.

## Opening Your File in the Editor

Now that you've created the file via the terminal, let's open it in the editor.

1. **Use the Explorer:** On the left-hand side of your VS Code window, you'll see the "Explorer" panel, which shows the complete file structure of your `UoE-Python-CodeSpace` project.

2. **Find Your File:** If they're not already expanded, click the arrows next to the `WORKSPACE` directory and then the `Session01` directory to see their contents.

3. **Open the File:** Click on `cinema_ex.py`. It will open in the main editor panel, ready for you to write code.

## Writing and Running Your First Code

Let's write a line of code to make sure everything is working.

1. **Write the Print Statement:** In the editor panel for `cinema_ex.py`, type a `print()` function that displays the welcome message: "Welcome to the University of Exeter cinema!".

   <details>
   <summary>SHOW MODEL ANSWER</summary>

      ```python
      print("Welcome to the University of Exeter cinema!")
      ```

   </details>

2. **Automatic Saving:** In Codespaces, the editor saves all changes to your files as you make them. You don't need to manually save.

3. **Try out the `cat` command.** In the linux terminal we can display the contents of a file using the `cat` command. Run the command below and you can see the code you wrote in the editor has been saved in the file.
   ```bash
   cat cinema_ex.py
   ```

4. **Run the File:** Go back to your integrated terminal (which should still be in the `Session01` directory). To run your script, type `python` followed by the name of your file.
   ```bash
   python cinema_ex.py
   ```

5. **Check the Output:** You should see your welcome message printed directly in the terminal.
   ```
   Welcome to the University of Exeter cinema!
   ```

## Using Variables and F-Strings

Variables store information. F-strings let us easily format and display that information.

1. **Add Variables and F-String:** In your `cinema_ex.py` file, first define two variables. Set `weekday` to `"Saturday"` and `title` to `"Ferris Bueller's Day Off"`. Then, use a `print` function with an f-string to display their contents in a sentence.

   <details>
   <summary>SHOW MODEL ANSWER</summary>


      ```python
      # Film and day information
      weekday = "Saturday"
      title = "Ferris Bueller's Day Off"
      
      # Use an f-string to display the variables
      print(f"Today is {weekday}, and the film showing is {title}")
      ```

   </details>

2. **Run Again:** Your file is saved automatically. Run it again from the terminal using the same command as before.

   <details>
   <summary>SHOW MODEL ANSWER</summary>

   ```bash
   python cinema_ex.py
   ```
   You should now see the new message displaying the content of your variables.
   ```
   Welcome to the University of Exeter cinema!
   Today is Saturday, and the film showing is Ferris Bueller's Day Off
   ```
   
   </details>

## Calculating Attendance

Now let's track ticket sales and see how many seats are left.

1. **Add Attendance Variables:** In your script, add the variables `capacity`, `n_adult`, `n_child`, and `n_student`. These should store the cinema's capacity, which is 200, and the current number of tickets sold: 12 adult tickets, 0 child tickets, and 97 student tickets.

   <details>
   <summary>SHOW MODEL ANSWER</summary>


   ```python
   # Attendance information
   capacity = 200
   n_adult = 12
   n_child = 0
   n_student = 97
   ```

   </details>

2. **Calculate and Display Totals:** Next, add code to calculate the `total_tickets_sold` by adding the three ticket types together. Then, calculate the `seats_remaining`. Finally, print both of these results using f-strings.

      <details>
      <summary>SHOW MODEL ANSWER</summary>

      ```python
      total_tickets_sold = n_adult + n_child + n_student
      seats_remaining = capacity - total_tickets_sold
      
      print(f"Total tickets sold: {total_tickets_sold}")
      print(f"Seats remaining: {seats_remaining}")
      ```

      </details>

3. **Run and Check:** Run the file again from the terminal to see your new calculations.

   ```
   Total tickets sold: 109
   Seats remaining: 91
   ```

## Calculating Takings

Finally, let's calculate the total cash taken from ticket sales.

1. **Add Price Variables:** First, add the variables `price_adult`, `price_child`, and `price_student` to your script. These should store the price for each ticket type: 9.99 for an adult ticket, 4.99 for a child ticket, and 5.99 for a student ticket.

   <details>
   <summary>SHOW MODEL ANSWER</summary>


      ```python
      # Ticket price information
      price_adult = 9.99
      price_child = 4.99
      price_student = 5.99
      ```

   </details>

2. **Calculate Total Cash:** Now, create a `cash_taken` variable. To calculate its value, multiply each ticket count variable by its corresponding price variable, and add the results together. Finally, print the result in a user-friendly message, formatting it to two decimal places.

   *Note: You can use `:.2f` inside the f-string so it formats the number to two decimal places, which is useful for currency e.g. will show £10.80 and not £10.8*

   <details>
   <summary>SHOW MODEL ANSWER</summary>

   ```python
   cash_taken = (n_adult * price_adult) + (n_child * price_child) + (n_student * price_student)
   
   print(f"Cash taken: £{cash_taken:.2f}")
   ```

   </details>



3. **Run and Check:** Run the file one last time.
   Your final output should look like this:
   ```
   Welcome to the University of Exeter cinema!
   Today is Saturday, and the film showing is Ferris Bueller's Day Off
   Total tickets sold: 109
   Seats remaining: 91
   Cash taken: £700.91
   ```

You have successfully navigated your workspace, written a Python script that uses variables, and performed calculations. Great work!

## Committing Your Changes to GitHub via the Terminal

The final step is to save your work back to your forked repository on GitHub. We will do this using `git` commands in the terminal. This process is called "committing" and "pushing". As shown in the CodeSpaces video tutorial you can save files to GitHub using the toolbar, but it is often useful to be able to do this using terminal commands.

1. **Check the Status:** First, let's see what changes Git has tracked. In your terminal, type the `git status` command.
   ```bash
   git status
   ```
   This will show you that `cinema_ex.py` has been "modified" or is an "untracked file".

2. **Stage Your Changes:** Before you can commit a file, you need to add it to the "staging area". This tells Git exactly which changes you want to include in the next snapshot.
   * To add one specific file, you would use: `git add cinema_ex.py`
   * If you have changed multiple files and want to stage them all, it's more efficient to use a period (`.`), which means "all files in the current directory and subdirectories".
   ```bash
   git add .
   ```

3. **Commit the Changes:** Now, take a snapshot of the staged changes. This is called a commit. It's important to include a descriptive message about the work you did using the `-m` flag.
   ```bash
   git commit -m "Complete Session 1 cinema exercise"
   ```
   Git will confirm that the commit has been made.

4. **Push to GitHub:** The commit is saved locally in your Codespace. The final step is to "push" it up to your personal forked repository on GitHub.com.
   ```bash
   git push
   ```
You can now go to your forked repository on the GitHub website, navigate to the `WORKSPACE/Session01` folder, and you will see your `cinema_ex.py` file saved there with your commit message.

## **Appendix: Windows Terminal Commands**

CodeSpaces is based on the VS Code IDE application. If working in the terminal in VS Code on a Windows laptop, the system commands are different:

| **Linux Command** | **Windows PowerShell Command** | **Description** | 
| :--- | :--- | :--- |
| `pwd` | `gl` | **Prints the current working directory.** | 
| `ls` | `dir` | **Lists the contents of the directory.** | 
| `touch file.py` | `New-Item file.py` | **Creates a new, empty file.** | 
| `cat file.py` | `type file.py` | **Displays the contents of a file.** | 
| `cd` | `cd` | **Change directory (this one is the same!).** | 
