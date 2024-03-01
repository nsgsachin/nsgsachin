import tkinter as tk
from tkinter import messagebox

# Create the main window
root = tk.Tk()
root.title("Login Form")
root.geometry("300x200")

# Username and password labels and entries
username_label = tk.Label(root, text="Username:")
username_label.pack()
username_entry = tk.Entry(root)
username_entry.pack()

password_label = tk.Label(root, text="Password:")
password_label.pack()
password_entry = tk.Entry(root, show="*")  # Hide password characters
password_entry.pack()

# Login button
def login():
    username = username_entry.get()
    password = password_entry.get()

    # Replace with your actual authentication logic
    if username == "user1" and password == "password1":
        messagebox.showinfo("Login Successful", "Welcome!")
    else:
        messagebox.showerror("Login Failed", "Invalid username or password.")

login_button = tk.Button(root, text="Login", command=login)
login_button.pack()

# Run the main loop
root.mainloop()
