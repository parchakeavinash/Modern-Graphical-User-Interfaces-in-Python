# Modern-Graphical-User-Interfaces-in-Python

import customtkinter
from CTkMessagebox import CTkMessagebox

customtkinter.set_default_color_theme("green")
customtkinter.set_appearance_mode("Dark")

root_ct = customtkinter.CTk()  
root_ct.geometry("500x350")  
root_ct.title("login to your account")  


def signup():
  CTkMessagebox(title="signup", message="you are now signed up",icon = "check")

frame = customtkinter.CTkFrame(master=root_ct)
frame.pack(pady = 20, padx = 60, fill = "both", expand = True)

label = customtkinter.CTkLabel(master=frame, text="Login System",)

label.pack(pady = 12, padx = 10)

entry1 = customtkinter.CTkEntry(master=frame, placeholder_text="Username")
entry1.pack(pady = 12, padx = 10)
entry1.focus()

entry2 = customtkinter.CTkEntry(master=frame, placeholder_text="Password", show="*")
entry2.pack(pady = 12, padx = 10)

Checkbox = customtkinter.CTkCheckBox(master=frame, text="Remember me")
Checkbox.pack(pady = 12, padx = 10)

button = customtkinter.CTkButton(master=frame, text="Login", command=signup)
button.pack(pady = 12, padx = 10)




root_ct.mainloop()  
