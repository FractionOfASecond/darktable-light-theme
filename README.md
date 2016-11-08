#Light theme for Darktable

All this is ugly hacking, but it works for me. Maybe will work for you.
Not everything looks like it should, but it is fine for me. 
The result is here <https://raw.githubusercontent.com/ip413/darktable-light-theme/master/dartable-light.gif>.  
I prefer this than dark darktable, and I don't want to spend
more time on this.

You have two options:  
1. change source code, recompile, install, change css style (more clean)  
2. change style, change plugin (very ugly and risky, but who knows, maybe will work)

I was working on version 2.2.0rc0+20~g791ada8-dirty, commit 791ada866085fbd10a8a6bbe1e080409fa8a13cf.

1  
1.0. Get darktable source code <https://github.com/darktable-org/darktable>  
1.1. Replace src/views/darkroom.c with file from this repo (only chage is different arguments for cairo_set_source_rgb).  
1.2. Recompile project with command from <https://github.com/darktable-org/darktable> (if you have problems with dependencies you could use this: apt-get build-dep darktable)  
1.3. You could need to remove old darktable by: sudo apt remove darktable  
1.4. Make link to you current binary file in /opt/darktable/bin/darktable  
1.5. Replace file /opt/darktable/share/darktable/darktable.css with mine   
Run darktable and enjoy white theme

2  
I didn't check this option, but if you already have version 2.2.0rc0+20~g791ada8-dirty or any similar, it could work.  
If not... there could be some crash.  
If you don't have you directory "/opt/darktable/", you could have those files in "/usr/share/darktable/".  
2.1. Replace file /opt/darktable/lib/darktable/views/libdarkroom.so with mine  
2.2. Do 1.5  
Run darktable
