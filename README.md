# json-cpp

https://linux.tips/programming/how-to-install-and-use-json-cpp-library-on-ubuntu-linux-os
# install guid
```
// install: sudo apt-get install libjsoncpp-dev
// Compile: g++ -o json_write json_write.cpp -ljsoncpp
// run: ./json_write
```
Example
```
#include <iostream>
#include <fstream>
#include <jsoncpp/json/json.h>

using namespace std;

int main() {
    ifstream ifs("profile.json");
    Json::Reader reader;
    Json::Value obj;
    reader.parse(ifs, obj);     // Reader can also read strings
    cout << "Last name: " << obj["lastname"].asString() << endl;
    cout << "First name: " << obj["firstname"].asString() << endl;
    return 1;
}
```
