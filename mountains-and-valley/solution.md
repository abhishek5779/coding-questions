```cpp
#include <iostream>
#include <vector>

struct Node {
    int data;
    Node *next;
};

class LinkedList {
public:
    Node *head, *tail;
    LinkedList() : head(nullptr), tail(nullptr) {}
    void push(int data) {
        Node *new_node = new Node{data, nullptr};
        if (head == nullptr) {
            head = new_node;
            tail = new_node;
        } else {
            tail->next = new_node;
            tail = new_node;
        }
    }
};

int user_logic(LinkedList &list) {
    // Implement your logic here
    Node *current = list.head;
    if(current->next==NULL)
        return 1;
    int top;
    
    if(current->data > current->next->data)
        top=1;    // starting value is high i.e. starts from mountain
    else if(current->data < current->next->data)
        top=0;    // starting value is low i.e. starts from valley
    else
        return 0;  // both values are same i.e. criteria doesn't satisfy

    while(current!=NULL && current->next!=NULL)
    {
        if(top==1)
        {
            if(current->data > current->next->data)
                top=0;
            else
                return 0;
        }
        else
        {
            if(current->data < current->next->data)
                top=1;
            else
                return 0;
        }
        current=current->next;
    }
    return 1;
}

int main() {
    int n;
    std::cin >> n;
    LinkedList ll;
    for (int i = 0; i < n; ++i) {
        int value;
        std::cin >> value;
        ll.push(value);
    }
    int result = user_logic(ll);
    std::cout << result << std::endl;
    return 0;
}
```