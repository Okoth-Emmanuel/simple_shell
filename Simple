#!/usr/bin/env ruby

# Method to display prompt
def display_prompt
  print "$ "
end

# Main loop for shell
loop do
  display_prompt
  # Read input from user
  input = gets
  break if input.nil? # Exit loop if Ctrl+D is pressed

  # Remove trailing newline character
  input.chomp!

  # Check if input is empty
  next if input.empty?

  # Try to execute the command
  begin
    system(input)
  rescue Errno::ENOENT => e
    puts "Error: #{e.message}"
  end
end
