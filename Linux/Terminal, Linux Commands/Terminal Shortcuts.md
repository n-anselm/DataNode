### Controlling the screen

- **`Ctrl + L`** = Clears the screen (same as the `clear` command).

- **`Ctrl + S`** = Pause all command output to the screen. If you have executed a command that produces verbose, long output, use this to pause the output scrolling down the screen.

- **`Ctrl + Q`** =     Resume output to the screen after pausing it with **`Ctrl+S`**.

---

### Move cursor on the command line

- **`Ctrl + A`** or **`Home`** = Moves the cursor to the start of the line.

- **`Ctrl + E`** or **`End`** = Moves the cursor to the end of the line.

- **`Ctrl + B`** or **`Left Arrow`** = Moves the cursor back one character at a time.

- **`Ctrl + F`** or **`Right Arrow`**  = Moves the cursor forward one character at a time.

- **`Ctrl + Left Arrow`** or **`Alt + B`** OR **`Esc`** and then **`B`** = Moves the cursor back one word at a time.

- **`Ctrl + Right Arrow`** or **`Alt + C`** OR **`Esc`** and then **`F`** = Moves the cursor forward one word at a time.

---

### Killing and yanking text

- **`Ctrl + K`** = Kill (cut) the text from the cursor to the end of the line.

- **`Ctrl + U`** = Kill (cut) the text from the cursor to the start of the line.

- **`Ctrl + Y`** = Yank (paste) the text that was yanked (cut).

---

### Deleting text

- **`Ctrl + W`** = Delete word by word to the start of the line.

- **`Ctrl + D`** or **`Delete`** = Remove or delete the character under the cursor.

- **`Ctrl + X`** and then **`Backspace`** = Removes all the text from the cursor to the beginning of the line.

---

### Search through history

- **`Up Arrow`** and **`Down Arrow`** = Pressing the up arrow retrieves the previous command. If you press it continuously, it takes you through multiple commands in history, so you can find the one you want. Use the down arrow to move in the reverse direction through the history.

- **`Ctrl + P`** and **`Ctrl + N`** = Alternatives to the **`Up Arrow`** and **`Down Arrow`**, respectively.

- **`Ctrl + R`** = Starts a reverse search through the bash history. Simply type characters that should be unique to the command you want to find in the history.

- **`Ctrl + S`** = Launches a forward search through the bash history.

- **`Ctrl + G`** = Quits reverse or forward search, through the bash history.

---

### Transpose text or change case

- **`Ctrl + T`** = Transposes the character before the cursor with the character under the cursor.

- **`Esc`** and then **`T`** = Transposes the two words immediately before (or under) the cursor.

- **`Esc`** and then **`U`** = Transforms the text from the cursor to the end of the word to uppercase.

- **`Esc`** and then **`L`** = Transforms the text from the cursor to the end of the word to lowercase.

- **`Esc`** and then **`C`** = Changes the letter under the cursor (or the first letter of the next word) to uppercase, leaving the rest of the word unchanged.

---

### Interacting with processes

- **`Ctrl + Z`** = Suspend the current foreground process. This sends the **SIGTSTP** signal to the process. You can get the process back to the foreground later using **`fg <process_name>`** (or **`%bg<process_number>`** like **`%1`**, **`%2`** and so on) command.

- **`Ctrl + C`** = Interrupt the current foreground process, by sending the **SIGINT** signal to it. The default behavior is to terminate a process gracefully, but the process can either honor or ignore it.

- **`Ctrl + D`** = Exit the bash shell (same as the **`exit`** command).

---

### Launch an editor

In a terminal press **`Ctrl + X`** and **`Ctrl + E`** to open an editor with an empty buffer. Bash will launch the editor that is defined by the $EDITOR environment variable.
