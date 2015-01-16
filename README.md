# myfile
A Python script to add/remove file name prefix/suffix

### Core functions: `myfile.py`
1. myfile.**searchByExt(***rootpath*, *ext***)**  
Find files in `rootpath` with a certain file extentison of `ext`, obtain their file paths, store those file paths into a `list`, and return it.

2. myfile.**modifyPrefix(***filelist*, *oldPrefix=''*, *newPrefix=''***)**  
For the files listed in `filelist`, change their file name prefix from `oldPrefix` to `newPrefix`. 

3. myfile.**modifySuffix(***filelist*, *oldSuffix=''*, *newSuffix=''***)**  
For the files listed in `filelist`, change their file name suffix from `oldSuffix` to `newSuffix`. 

### Sample code: `myfile_sample_code.py`
    # -*- coding: uft-8 -*-
    
    import myfile
    
    if __name__ == '__main__':
        rootpath = '~/Documents' # change this to a proper directory path
        ext = 'pdf' # change it to whatever file extension you need
        oldPrefix = '' # left empty when adding new prefix
        newPrefix = 'prefix-' # left empty when removing old prefix
        oldSuffix = '' # left empty when adding new suffix
        newSuffix = '-suffix' # left empty when removing old suffix
    
        results = myfile.searchByExt(rootpath, ext)
        myfile.modifyPrefix(results, oldPrefix, newPrefix)
        myfile.modifySuffix(results, oldSuffix, newSuffix)

### Further reading
1. [Python和正则表达式：给PDF文件批量添加前缀或后缀](http://research.irockbunny.com/post/100749403437/python-pdf)
