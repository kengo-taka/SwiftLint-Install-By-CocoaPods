# How to install SwiftLint by CocoaPods

## 1, Go to your project's root directory and add the following line
```
pod init
```

## 2, Open Podfile and add the following line 
```
pod 'SwiftLint'
```
<img width="500" alt="Screen Shot 2021-06-07 at 5 49 29 PM" src="https://user-images.githubusercontent.com/60034714/121105902-d0bf3080-c7b9-11eb-9e98-0478ebb1dacd.png">
<br />
<img width="563" alt="Screen Shot 2021-06-07 at 6 01 41 PM" src="https://user-images.githubusercontent.com/60034714/121106209-6d81ce00-c7ba-11eb-923e-224d30d3a30c.png">

## 3, Add the following line 
```
pod install
```
<img width="553" alt="Screen Shot 2021-06-07 at 6 05 37 PM" src="https://user-images.githubusercontent.com/60034714/121106497-f993f580-c7ba-11eb-9bbc-8da49a5cb221.png">

## 4, Open the project and add the following line in the run Script
```
"${PODS_ROOT}/SwiftLint/swiftlint"

```

<img width="945" alt="Screen Shot 2021-06-07 at 6 09 17 PM" src="https://user-images.githubusercontent.com/60034714/121107493-dff3ad80-c7bc-11eb-8e83-f127665dcfe8.png">
</br>
</br>
<img width="668" alt="Screen Shot 2021-06-07 at 6 09 52 PM" src="https://user-images.githubusercontent.com/60034714/121107523-f0a42380-c7bc-11eb-9163-916476a3c40b.png">

## 5, Run the project

## Usage

### Command
By adding the following line, you can see subcommand.
```
Pods/SwiftLint/swiftlint help
```

<img width="559" alt="Screen Shot 2021-06-07 at 6 40 51 PM" src="https://user-images.githubusercontent.com/60034714/121109171-e59ec280-c7bf-11eb-96a6-a55b78eebf38.png">



### Change the rules
1, Create .swiftlint.yml and open it

<img width="512" alt="Screen Shot 2021-06-07 at 6 46 18 PM" src="https://user-images.githubusercontent.com/60034714/121109556-a8870000-c7c0-11eb-89f2-5d052a586618.png">

2, Write new rule which you want to change in .swiftlint.yml

Example 

Force cast is Error by default.

<img width="257" alt="Screen Shot 2021-06-07 at 6 48 34 PM" src="https://user-images.githubusercontent.com/60034714/121109889-3bc03580-c7c1-11eb-8a20-7d8ce68e3a53.png">
</br>
<img width="570" alt="Screen Shot 2021-06-07 at 6 48 43 PM" src="https://user-images.githubusercontent.com/60034714/121109927-4e3a6f00-c7c1-11eb-8233-fabca2193df9.png">

But if you add the following lines in .swiftlint.yml, the error will be just warning

```
force_cast: warning
force_try: warning
```

<img width="488" alt="Screen Shot 2021-06-07 at 6 53 56 PM" src="https://user-images.githubusercontent.com/60034714/121110186-b9844100-c7c1-11eb-975a-b1e46ab453fe.png">

</br>
<img width="237" alt="Screen Shot 2021-06-07 at 6 55 00 PM" src="https://user-images.githubusercontent.com/60034714/121110271-dde01d80-c7c1-11eb-8d3e-a5cfcc43f2bd.png">

### Auto Formatting
By assign the following lines in Run Script, the code will be autoformatted when built.
```
if which ./Pods/SwiftLint/swiftlint > /dev/null; then
    ./Pods/SwiftLint/swiftlint autocorrect --format
    ./Pods/SwiftLint/swiftlint
else
    echo "warning: SwiftLint not installed, download from https://github.com/realm/SwiftLint"
fi
```
<img width="679" alt="Screen Shot 2021-06-07 at 6 58 54 PM" src="https://user-images.githubusercontent.com/60034714/121111423-b0946f00-c7c3-11eb-9a69-e407a5f47d0c.png">



### #Memo 
If you got the error which is related with framework, delete that.

<img width="721" alt="image" src="https://user-images.githubusercontent.com/60034714/121107990-d0289900-c7bd-11eb-8628-684eefc6852e.png">



