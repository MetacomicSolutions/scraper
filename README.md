# Importing the required libraries
import instaloader

# Initialize the Instaloader object
loader = instaloader.Instaloader()

# Set the profile name for the Instagram account you want to scrape the content from
profile_name = "profile_name"

# Get the profile object for the specified profile name
profile = instaloader.Profile.from_username(loader.context, profile_name)

# Iterate through the posts in the profile and download the content
for post in profile.get_posts():
    # Download the image or video content for the post
    loader.download_post(post, target=profile_name)
