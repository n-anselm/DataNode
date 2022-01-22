### Replace character(s) in a string
	string.replace('to_replace', 'replacement')

---
### Play an audio file
```
from playsound import playsound
playsound('/path/to/sound.wav')
```

---

### Run an \[external] shell command
	subprocess.run(["command", "argument(s)"])

---
### Get type of variable
	type(variable)

or

	isinstance(object, type)

The `type` function outputs the type.
The `isinstance` function outputs a boolean.

isinstance example:

	print(isinstance(string_var, str))
	Output>>> True

Check if type of variable is a string with type function:

	if type(variable) is str:
		print('True')

---

### Exit program
	exit()

or

	quit()

or

	sys.exit("The program stopped.")
