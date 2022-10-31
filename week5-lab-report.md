# Week 3 Lab Report

## find command

### find . -type d
```
chengqian@Chengs-MacBook-Air skill-demo1 % find . -type d
.
./lib
./technical
./technical/government
./technical/government/About_LSC
./technical/government/Env_Prot_Agen
./technical/government/Alcohol_Problems
./technical/government/Gen_Account_Office
./technical/government/Post_Rate_Comm
./technical/government/Media
./technical/plos
./technical/biomed
./technical/911report
```

```

```


### find . -type -f -size -1024c
```
chengqian@Chengs-MacBook-Air skill-demo1 % find . -type f -size -1024c
./README.md
./test.sh
./start.sh
./technical/plos/pmed.0020191.txt
./technical/plos/pmed.0020226.txt
```

### find ./technical/911report -name "*.txt"
```
chengqian@Chengs-MacBook-Air skill-demo1 % find ./technical/911report -name "*.txt"
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-13.1.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-3.txt
./technical/911report/chapter-2.txt
./technical/911report/chapter-1.txt
./technical/911report/chapter-5.txt
./technical/911report/chapter-6.txt
./technical/911report/chapter-7.txt
./technical/911report/chapter-9.txt
./technical/911report/chapter-8.txt
./technical/911report/preface.txt
./technical/911report/chapter-12.txt
./technical/911report/chapter-10.txt
./technical/911report/chapter-11.txt
```
