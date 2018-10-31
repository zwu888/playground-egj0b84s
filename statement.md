# description: 
 There is a sequence point after the initalization of each base and member, thus the code is well-formed and defined


```C++ runnable
#include <iostream>

struct Foo
{
  Foo(int n) : x(n++), y(n++), z(n++) {}
  int x;
  int y;
  int z;
};

int main(int argc, char** argv)
{
  Foo f(3);

  std::cout << "x: " << f.x << std::endl;
  std::cout << "y: " << f.y << std::endl;
  std::cout << "z: " << f.z << std::endl;

  return 0;
}
```

