# Set keyboard layout & swap ctrl/win
in `/.config/hypr/hyprland.conf` change
```bash
input{
	kb_layout = latam
	kb_options = ctrl:swap_lwin_lctl
}
```
# Add Teleport source
in `.config/fish/config.fish`
```bash
source /home/asmot/Apps/Teleport/adapters/tp.fish
```

# Display ascii art 
Ensure that a sl is located in the config.fish directory with the name `ascii_art` that point to the directory with all the ascii art you want to display
This is meant to be placed in the config.fish file
```bash
# Display Ascii_art 
	# List all text files in the directory
	set ascii_art_dir "$__fish_config_dir/ascii_art/"
	set files (find $ascii_art_dir -maxdepth 1 -type f -name "*.txt")
	# Check if there are any files
	if test (count $files) -eq 0
		echo "No text files found in the current directory."
		exit 1
	end
	# Select a random file
	set random_index (random 1 (count $files))
	set random_file $files[$random_index]
	#Display the contents of the random file
	cat $random_file
	exit 0
```