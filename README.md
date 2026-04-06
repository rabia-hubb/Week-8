class Node:
    def __init__(self, name, age, gender):
        self.name = name
        self.age = age
        self.gender = gender
        self.next = None


class LinkedList:
    def __init__(self):
        self.head = None 

    #addFront
    def add_front(self, name, age, gender):
        new = Node(name, age, gender)

        if self.head is None:
            self.head = new
        else:
            new.next = self.head
            self.head = new

    #addEnd
    def add_end(self, name, age, gender):
        new = Node(name, age, gender)

        if self.head is None:
            self.head = new
        else:
            temp = self.head

            while temp.next is not None:
                temp = temp.next

            temp.next = new

    #addBetween
    def add_between(self, name, age, gender, index):
        new = Node(name, age, gender)

        if index == 0:
            new.next = self.head
            self.head = new
            return

        temp = self.head
        count = 0

        while temp is not None and count < index - 1:
            temp = temp.next
            count += 1

        if temp is None:
            print("Index out of range")
        else:
            new.next = temp.next
            temp.next = new
