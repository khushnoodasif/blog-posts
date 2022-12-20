# Exporting Your Instagram Followers List with Python

Are you looking to learn how to export a list of followers from Instagram using Python? If so, you're in luck! In this tutorial, we'll be using a Python library called Instaloader to access our Instagram account and retrieve the details of our followers.

Instaloader is a powerful tool that allows us to interact with Instagram in a number of ways. We can post pictures, videos, add stories, and access many other features of the platform. For this tutorial, we'll be using it to get a list of our followers.

To get started, we'll need to install the library and log into our Instagram account. Here's the source code for the required program:

```python
# Get instance
import instaloader

L = instaloader.Instaloader()

# Login or load session
username = "<username>"
password = "<password>"
L.login(username, password)  # (login)

# Obtain profile metadata
profile = instaloader.Profile.from_username(L.context, username)

# Print list of followers
follow_list = []
count = 0
for follower in profile.get_followers():
    follow_list.append(follower.username)
    count = count + 1

#Print Number of followers
print("No of followers", count)
```

To use this program, simply replace `<username>` and `<password>` with your own Instagram login credentials. When you run the program, it will print out a list of your followers, as well as the total number of followers you have.

If you want to save the list of followers to a text file, you can simply open the file in write mode and append each follower's username to the file. With this simple program, you'll be able to easily export a list of followers from Instagram using Python.

To export the list of followers to a text file, you can simply add the following code to the end of the program:

```python

# Open a text file in write mode
with open("followers.txt", "w") as f:
    # Iterate through the list of followers and write each one to the file
    for follower in follow_list:
        f.write(follower + "\n")
```

This will open a new text file called "followers.txt" in write mode and write each follower's username to a new line in the file. When the program finishes running, you should have a text file containing a list of all your Instagram followers.

Here's the complete code with the text file export added:

```python
# Get instance
import instaloader

L = instaloader.Instaloader()

# Login or load session
username = "<username>"
password = "<password>"
L.login(username, password)  # (login)

# Obtain profile metadata
profile = instaloader.Profile.from_username(L.context, username)

# Print list of followers
follow_list = []
count = 0
for follower in profile.get_followers():
    follow_list.append(follower.username)
    count = count + 1

# Print number of followers
print("No of followers", count)

# Open a text file in write mode
with open("followers.txt", "w") as f:
    # Iterate through the list of followers and write each one to the file
    for follower in follow_list:
        f.write(follower + "\n")
```

I hope this helps! Let me know if you have any questions or need further assistance.