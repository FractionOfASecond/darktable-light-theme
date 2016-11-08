#Light theme for Darktable

All this is ugly hacking, but it works for me. Maybe will work for you.<br>
Not everything looks like it should, but it is fine for me.<br>
The result is here <https://raw.githubusercontent.com/ip413/darktable-light-theme/master/darktable-light.gif>.<br>
I prefer this than dark darktable, and I don't want to spend<br>
more time on this trying to make it perfect.<br>

##You have three options:
1. change source code, recompile, install, change css style (more clean)<br>
2. change style, change plugin (very ugly and risky, but who knows, maybe will work)<br>
3. change style (the most clean option, but without white background in darkroom, under photo)<br>
<br><br>
I was working on version 2.0.7-dirty, commit d2bec77e44ed83769a154180abf6b612537ff16f, this is version was used to create release 2.0.7.

###1
1.0. Get darktable source code <https://github.com/darktable-org/darktable><br>
1.1. Replace src/views/darkroom.c with file from this repo (only change is different arguments for cairo_set_source_rgb).<br>
1.2. Recompile project with command from <https://github.com/darktable-org/darktable> (if you have problems with dependencies you could use this: apt-get build-dep darktable)<br>
1.3. You could need to remove old darktable by: sudo apt remove darktable<br>
1.4. Make link to you current binary file in /opt/darktable/bin/darktable<br>
1.5. Replace file /opt/darktable/share/darktable/darktable.css with mine (or, the path could be /usr/share/darktable)<br>
Run darktable and enjoy white theme<br>

###2
I didn't check this option, but if you already have version 2.0.7 or any similar, it could work.<br>
If not... there could be some crash.<br>
If you don't have directory "/opt/darktable/", you could have those files in "/usr/share/darktable/".<br>
2.1. Replace file /opt/darktable/lib/darktable/views/libdarkroom.so with mine<br>
2.2. Do 1.5<br>
Run darktable

###3
3.1. do 1.5<br>
Run darktable
<br><br>
If something gone wrong try to remove /usr/share/darktable, /opt/darktable, ~/.config/darktable and repeat 1 sequences.
