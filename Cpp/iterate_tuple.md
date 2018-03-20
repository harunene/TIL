# Parameter pack
- c에서 va_start() ~ va_end() 류로 사용하던 가변인자를 c++에서는 언어적으로 지원하는데 이를 Parameter pack 이라고 한다.
- 함수 인자에 사용 가능하므로 람다 인자에도 사용 가능하다.
- `std::tuple`은 인자로 Parameter pack을 받는다.
  아래처럼 사용 가능하다.
  ```
    auto generic_lambda = [](auto&&... args)
    {  
        auto argtuple = std::make_tuple(args...);  
        print_tuple(argtuple);
    };
  ```
  
