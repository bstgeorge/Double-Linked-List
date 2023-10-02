class Node {
  constructor(value) {
    this.value = value,
    this.next = {},
    this.prev = {}
  }
}

class DLL {
  constructor(value) {
    this.head = new Node(value);
    // always points to node
    this.tail = this.head;
    this.length = 1;
  }
  prepend = (value) => {
    let newNode = new Node(value);
    newNode.next = this.head;
    this.head.prev = newNode;
    this.head = this.head.prev
    this.length++
  }

  insertAt = (index, value) => {
    let newNode = new Node(value)
    let currentNode = this.head
    for (let i = 1; i < index; i++) {
      currentNode = currentNode.next;
    }
    newNode.prev = currentNode;
    newNode.next = currentNode.next;
    currentNode.next = newNode;
    this.length++
  }

  append = (value) => {
    let newNode = new Node(value);
    newNode.prev = this.tail;
    this.tail.next = newNode;
    this.tail = newNode;
    this.length++;
  }

  remove = (value) => {
  }

  get = (index) => {
    let currentNode = this.head
    for (let i = 1; i <= index; i++) {
      currentNode = currentNode.next;
    }
    return currentNode.value;
  }

  removeAt = (index) => {
    let currentNode = this.head;
    for (let i = 1; i < index; i++) {
      currentNode = currentNode.next;
    }
    currentNode.next = currentNode.next.next;
  }

  find = (value) => {
    let currentNode = this.head;
    let idx = 0;
    while (currentNode) {
      if (currentNode.value === value) {
        return idx;
      } else {
        idx++;
        currentNode = currentNode.next;
      }
    }
  }
}

let name = 'rettst.george';
let arr = name.split('');

let dll = new DLL(null);

for (let letter of arr) {
  if (!dll.head.value) {
    dll.head.value = letter;
  } else {
    dll.append(letter)
  }
}

dll.prepend('b');
dll.insertAt(5, 'a');
dll.removeAt(dll.find('.'));
console.log('length: ', dll.length);

let currentNode = dll.head;
while (currentNode.next) {
  console.log(currentNode.value)
  currentNode = currentNode.next;
}

