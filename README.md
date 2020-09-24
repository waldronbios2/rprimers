# rprimers


For posterity:

I fetched the primers dependencies from a renv.lock file like this,
then inserted pkgs.txt into my DESCRIPTION. It's a lot of dependencies
but I think that's OK. I realize the primers may not all work without
restoring the same versions that rstudio-education fixed, but let's
cross that bridge later. In the meantime it would be annoying to be
stuck with R 3.6.3.


```bash
grep Package primers/renv.lock  | sed -e 's/      "Package": "/    /' | sed -e 's/",/,/' | uniq | sort > pkgs.txt 
```
