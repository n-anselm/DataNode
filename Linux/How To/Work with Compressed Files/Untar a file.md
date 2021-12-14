### Extract a ```.tar.gz``` or ```.tgz``` file

If your tar file is compressed using a gZip compressor, use this command:

    tar xvzf file.tar.gz

The options are pretty straightforward for this:  
  
**x:** This tells tar to extract the files.  
  
**v:** This option will list all of the files one by one in the archive. The “v” stands for “verbose."  
  
**z:** The z option is very important and tells the tar command to uncompress the file (gzip).  
  
**f:** This option tells tar that you are going to give it a file name to work with.

---

### Extract a ```.tar.bz2``` or ```.tbz``` file

If the tar file is compressed using a bZip2 compressor, use this command:

    tar xvjf file.tar.tbz

This is just about the same as the gzip decompression. The major difference is that the z option has been replaced by the j option.  
  
If you remember, the z option was the uncompress (specifically gzip) flag, so it makes sense that this would be switched out.  
  
**j:** This will decompress a bzip2 file.

---

### Extract a file using the ```dtrx``` function

To install ```dtrx```, use this command:

    sudo apt-get install dtrx
	
Standing for the “Do the Right eXtraction,” ```dtrx``` works as you would hope. The command should be simple for both gZip and bZip2 files:

```
dtrx file.tar.gz
```

```
dtrx file.tar.bz2
```
