# Ineuron-mock25-june
Implement a queue using an array in JavaScript. Include the necessary methods such as enqueue, dequeue, and isEmpty.

ans

class Queue {
  constructor() {
    this.items = []; // Array to store queue elements
  }

  // Add an element to the queue
  enqueue(element) {
    this.items.push(element);
  }

  // Remove the front element from the queue
  dequeue() {
    if (this.isEmpty()) {
      return null;
    }
    return this.items.shift();
  }

  // Check if the queue is empty
  isEmpty() {
    return this.items.length === 0;
  }

  // Get the front element of the queue without removing it
  peek() {
    if (this.isEmpty()) {
      return null;
    }
    return this.items[0];
  }

  // Get the size of the queue
  size() {
    return this.items.length;
  }

  // Clear the queue
  clear() {
    this.items = [];
  }
}

// Usage example:
const queue = new Queue();

queue.enqueue("A");
queue.enqueue("B");
queue.enqueue("C");

console.log(queue.size()); // Output: 3

console.log(queue.dequeue()); // Output: "A"

console.log(queue.peek()); // Output: "B"

console.log(queue.isEmpty()); // Output: false

queue.clear();

console.log(queue.isEmpty()); // Output: true


