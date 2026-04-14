class Node:
    def __init__(self, name, age, gender):
        self.name = name
        self.age = age
        self.gender = gender
        self.next = None


def add_front(self, new):
    if self.head is None:
        self.head = new
    else:
        new.next = self.head
        self.head = new

def add_between(self, target_name, new_node):
    if self.head is None:
        self.head = new_node
    else:
        tmp = self.head

        while tmp is not None:
            if tmp.name == target_name:
                new_node.next = tmp.next
                tmp.next = new_node
                return
            else:
                tmp = tmp.next

    print(f"{target_name} not found")


def add_end(self, new_node):
    if self.head is None:
        self.head = new_node
    else:
        tmp = self.head
        while tmp.next is not None:
            tmp = tmp.next
        tmp.next = new_node


def print_list(self):
    tmp = self.head
    while tmp is not None:
        print(tmp.name, tmp.age, tmp.gender)
        tmp = tmp.next
