# OOPs-notes

Dynamic Binding (Late Binding)
   Dynamic binding means the function call is decided at runtime (during execution), not at compile time.
     class A {
        public:
        virtual void show() {
          cout << "A";
        }
    };

  class B : public A {
      public:
    void show() override {
        cout << "B";
    }
    };

  int main() {
    A* obj = new B();
    obj->show();   // Output: B
}



With virtual, the function is called based on the object type, NOT the pointer type.
