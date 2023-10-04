# queue_implementation
# CLI queue

A simple command line interface (CLI) for interacting with a queue using Rust. This CLI uses the `dummy-queue` box for queue operations.

## Code
https://crates.io/crates/actividadSemana20

## Example
fn main() {
    let mut queue = Queue::new();

    loop {
        clear_screen();
        println!("Queue CLI Menu:");
        println!("1. Queue a value");
        println!("2. Dequeue a value");
        println!("3. Show top value");
        println!("4. Show queue len");
        println!("5. Show all values");
        println!("6. Exit");
        println!("Enter your choice:");

        let mut choice = String::new();
        io::stdin()
            .read_line(&mut choice)
            .expect("Failed to read line");
        let choice: u32 = match choice.trim().parse() {
            Ok(num) => num,
            Err(_) => {
                println!("Invalid input. Please enter a number.");
                continue;
            }
        };

This project is licensed under the MIT License - see the LICENSE file for details.
This CLI project makes use of the dummy-queue crate for implementing queue operations.
