# Elixir Enum.each and Process Termination

This repository demonstrates a subtle bug related to the use of `Enum.each` in Elixir and how unhandled exceptions within the enumeration function can lead to premature process termination.

The `bug.exs` file shows the problematic code, where a process exit is triggered if a specific element is encountered. This interrupts the `Enum.each` operation before it can fully iterate over the list.

The `bugSolution.exs` file provides a corrected version, employing `Enum.try_each` to handle potential exceptions gracefully and complete the iteration even when an error occurs.

This example highlights the importance of cautious error handling when using functions like `Enum.each` to avoid unexpected behavior and ensure clean termination of processes.