from tkinter import *
import smtplib
def submit():
    sender = entry.get()
    receiver = entry2.get()
    password = entry3.get()
    subject = entry4.get()
    body = entry5.get()


    message = f"""From: {sender}
    To: {receiver}
    Subject: {subject}\n
    {body}
    """

    server = smtplib.SMTP("smtp.gmail.com", 587)
    server.starttls()

    try:
        server.login(sender, password)
        print("Logged in...")
        server.sendmail(sender, receiver, message)
        print("Email has been sent!")

    except smtplib.SMTPAuthenticationError:
        print("unable to sign in")


window = Tk()

entry = Entry(window,
            font=("Arial",50),
            fg="#00FF00",
            bg="black")
entry2 = Entry(window,
            font=("Arial",50),
            fg="#00FF00",
            bg="black")
entry3 = Entry(window,
            font=("Arial",50),
            fg="#00FF00",
            bg="black")
entry4 = Entry(window,
            font=("Arial",50),
            fg="#00FF00",
            bg="black")
entry5 = Entry(window,
            font=("Arial",50),
            fg="#00FF00",
            bg="black")

#entry.insert(0,'Spongebob')
entry3.config(show="*")
#entry.config(state=DISABLED)

entry.pack()
entry2.pack()
entry3.pack()
entry4.pack()
entry5.pack()


submit_button = Button(window,text="submit",command=submit)
submit_button.pack()

window.mainloop()
