# assignment 4
#task 2

str1= input("enter a string")
f1= open("output.txt","w")
writing_file= f1.write(str1)
print("data successfully written to output.txt")
f1.close()


f1= open("output.txt","a")
str2= input("enter additional text to append")
appending_file= f1.write(str2)
print("data successfully appended")
f1.close()

f1= open("output.txt","r")
reading_file= f1.read()
print(reading_file)
f1.close()

#task 1

try:
    f1= open("sample.txt","r")
    for line in f1:
        print(line.strip())
except FileNotFoundError:
    print("error")
finally:
    print("the file sample.txt was not found")
