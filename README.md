# LaTeX Thesis Template
A template for theses (Projectwork, Bachelor, Master, Phd, etc.) at the TU Wien (Vienna University of Technology). Some basic content is included exemplarily.

## General Tips
- Split the sections of the thesis into separate files if possible (which speeds up compilation time by commenting the parts which are not being worked on)
- Write the text first before layouting
- Use version control and make frequent backups.
- Objects creating data (programs, scripts, etc.) may be included in the file structure which comes handy especially when applying version control. In this layout these would be placed in the folders called *generators* in each folder of the corresponding section 

## LaTeX Tips
- Enable shell-escape when utilising gnuplot or inkscape by adding **-shell-escape -interaction=nonstopmode %source** in the compiler options of the TeX distribution
- Use *tikz standalone* when there are significant amount of figures generated by tikz. This speeds up the compilation time
- When running out of memory during compilation the following may help when working with windows

  Open a command line (cmd), type **initexmf --edit-config-file=pdflatex** and hit enter. Replace the contents of the file with, e.g.,
  > main_memory=5000000  
  > extra_mem_bot=5000000  
  > font_mem_size=5000000  
  > pool_size=5000000  
  > buf_size=5000000  

  save the file and execute **initexmf --dump=pdflatex** in the command line. This will increase the memory size of TeX for the process of compilation