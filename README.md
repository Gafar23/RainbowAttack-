### Script
You can execute the Demo bash script it will do everything for you
```
$ bash Demo.sh
```
or
```
$ chmod +x ./Demo.sh
$ ./Demo.sh
```
### Or
you can do the following if you do not want to use my bash script

### Compilation
```
$ make all
```
### Execution
#### Generation of the Rainbow Table
```
$ ./executable/rainbow_table_gen <nb_of_chains> <length_of_chains> <pwd_size> <rainbow_table_path>
```

##### Where
> - **nb_of_chains** is the number of heads and tails that you want to generate
> - **length_of_chains** is the length of the chains (head -> tail) of the Rainbow Table
> - **pwd_size** is the allowed size of the head (head need to be the same size as the size of password that you want to crack)
> - **rainbow_table_path** is the name of the output file where the heads and the tails will be stored 
>or you can enters separately each file where
>heads is the name of the output file where the heads will be stored,
>tails is the name of the output file where the tails will be stored"

#### Checking the validity of the Rainbow Table chains
```
$ ./executable/rainbow_table_check <length_of_chains> <rainbow_table_path>
```
##### Where
> - **length_of_chains** is the length of the chains (head -> tail) of the Rainbow Table
> - **rainbow_table_path** is the name of the output file where the heads and the tails are stored 
>or you can enters separately each file where 
>heads is the name of the output file where the heads are stored,
>tails is the name of the output file where the tails are stored


#### Rainbow Table Attack
```
$ ./executable/rainbow_table_attack <length_of_chains> <pwd_size> <rainbow_table_path> <hash_to_crack_path>
```
##### Where
> - **length_of_chains** is the length of the chains (head -> tail) of the Rainbow Table
> - **pwd_size** the size of the heads of the given Rainbow Table (You need to have 1 rainbow table by the size of the password that you want to crack)
> - **rainbow_table_path** the path of the file of the Rainbow Table
> - **hash_to_crack_path** is the path of the file of hashes to crack
            
## Cleaning
#### clean executable data and tmp files
```
$ make clean
```