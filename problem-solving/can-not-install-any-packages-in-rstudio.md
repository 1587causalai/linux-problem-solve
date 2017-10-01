# I can't install any packages in R

lib = "/usr/local/lib/R/site-library"' is not writable


step 1: 

- google it and found answer [Library is not writable](https://stackoverflow.com/questions/32540919/library-is-not-writable)

```
Installing package into ‘/usr/local/lib/R/site-library’
(as ‘lib’ is unspecified)
Warning in install.packages :
  'lib = "/usr/local/lib/R/site-library"' is not writable
Would you like to use a personal library instead?  (y/n) y
Would you like to create a personal library
~/R/x86_64-pc-linux-gnu-library/3.2
to install packages into?  (y/n) y
Warning in install.packages :
  由于'权限不够'的原因，无法建立'/home/ghy/R/x86_64-pc-linux-gnu-library'文件目录
Error in install.packages : unable to create ‘~/R/x86_64-pc-linux-gnu-library/3.2’

```


step 2: start all over again.

reinstall my R studio and R. 


> It turns out to be a question of source.list !