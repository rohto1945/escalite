# escalite
SQLite forensic tool

## Usage

```
./escalite.py <database>
```

### Interactive

| cmd           | Description                                           |
|---------------|-------------------------------------------------------|
| ```help```    | Show available commands                               |
| ```h```       | Show DB header information                            |
| ```o```       | Show overview of all pages                            |
| ```b <n>```   | Show a graph of the BTree of Page n (Default: n = 2)  |
| ```p <n>```   | Show information about the n-th page                  |
| ```pc <n>```  | Show all cells on page n                              |
| ```pr <n>```  | Try to retrieve deleted data on page n                |
| ```pd <n>```  | Print hexdump of page n                               |
| ```f <n>```   | Show information about freelist trunk page n          |
| ```fcl <n>``` | Check if freelist-leaf page n is empty                |
| ```fl```      | Show freelistgraph                                    |
| ```exit, q``` | Close program                                         |

### Examples graphs

#### Freelist graph: Large empty database
![Large empty database](freelist_example.png "Freelist graph: Large empty database")

#### BTree graph: Large database (test_fl.db)
![BTree graph: test_fl.db](btree_example.png "BTree graph: test_fl.db")


## Features planned

* BTree-graph generation *In progress*

	* Interpret first pages to get overview of btree starts

* Print hexdump of bytes proofing a interpretation of bytes (cmdline-argument)


