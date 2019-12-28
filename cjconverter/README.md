# CJConverter 

**Version 1.0.0**

This is a two-way JSON and CSV file converter. 
Its features are as follows :

* Convert a simple json file to a simple csv file.
* Convert a simple csv file to a simple json file.
* Convert a nested json file to a logical csv file
* Convert a csv file from a nested json conversion to a nested json file.
* Do the 4 types of previous conversions using a configuration file allowing the manipulation of data in one or other of the extensions.
* Read CSV, Json and configuration files.
* Parse CSV, Json and configuration files.
* Write CSV Json and configuration files.
* Print the Syntaxic trees from Json file and configuration files.
* Print Headers, Keys, Subkeys etc... from CSV and Json files.



## User manual

As described above, the application allows you to do several actions on `CSV` and `Json` files. In the following we will describe the user manual in order to perform the various manipulations. two shell scripts are used `convert_json.sh` and `convert_csv.sh` to launch the program and therefore contain the following command :

```
clear
mvn clean
mvn install
java -jar CJConverter-jar-with-dependencies.jar ./CSV_Files/FILE.csv or /FILE.json
```

***From `Json` to `CSV` File :***

*Simple & Classical conversion*

1.Open `convert_json.sh` :

```
nano convert_json.sh
```
2.Put the absolute path of your `Json` File :
```
/you/path/here
ctrl+x
o
enter
```
3.Then type the following command lines :

```
cd /your_path/CJConverter
./convert_json.sh
```

*Conversion with configuration*

1.Open youre `Configuration file` File :
```
nano convert_json.sh
```
2.Then add Configs

```
Sum = SUM( x ) ;
```

3.Put the absolute path of your `Json` File :

```
nano convert_json.sh
```
4.Put the absolute path of your `Json` File :
```
/you/path/here
ctrl+x
o
enter
```
5.Then type the following command lines :

```
cd /your_path/CJConverter
./convert_json.sh
```
***From `Json` to `CSV` File :***

*Simple & Classical conversion*

1.Open `convert_csv.sh` :
```
nano convert_csv.sh
```
2.Put the absolute path of your `CSV` File :
```
/you/path/here
ctrl+x
o
enter
```
3.Then type the following command lines :

```
cd /your_path/CJConverter
./convert_csv.sh
```
*Conversion with configuration*

1.Open youre `Configuration file` File :
```
nano convert_csv.sh
```
2.Then add Configs

```
Sum = SUM( x ) ;
```

3.Put the absolute path of your `CSV` File :

```
nano convert_csv.sh
```
4.Put the absolute path of your `CSV` File :
```
/you/path/here
ctrl+x
o
enter
```
5.Then type the following command lines :

```
cd /your_path/CJConverter
./convert_csv.sh
```

## Technical manual 

The application is based on syntax trees for the three types of files. Indeed is original, and all methods / functions and added artisanally. The algorithm start by maturing a maximum of information on the contents of the files (Header, Lingnes etc ...) using its information a k-array tree is constructed and is traversed in postfix notation. The configuration file is based on the Parse of the language `Tiger` and allows adding constraints on the conversion. We can therefore do :

* SUM 
> calculates the sum of an entire column
* MAX
> Find the maximum value of the column
* MIN
> Find the minimal value of the column
* SORT
> Sort the values of a column
* X + Y * Z + L ... *-+/


The implementation is also based on cryptographical algorithms as MD5 to hash files. The use of scripts is also engaged.
The output files are distributed either in Json Outputs or in CSV outputs depending on the type of file desired. Two folders also exist under the names of `CSV` Files and `Json` Files containing some good files to test.

## Upgrading

A graphical window was created but was not placed in the project sources, because the teacher responsible for this project, **Mr. Stéphane Lopez** requested that the compilation be done in command lines.

## License & copyright

© **Chahi Rabie Ala Eddine**, **Keskes Yasmine** ***Versailles Saint Quentin en Yvelines college***.

