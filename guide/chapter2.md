# Chapter 2: Update the Block Page Container
### Overview
Our `Block Page` container code has a link in the block web page that takes the user to the `Request Unblock` page if they want to submit an unblock request. That link is currently unconfigured. In this chapter we will update the URL for that link in the `Block Page` container code, rebuild our container image, and deploy the new image to Kubernetes.

### Edit the Code

 - [ ] In VS Code, on the `main` branch, browse to `services/block-page`.
 - [ ] Open `index.html`.
 - [ ] On line 131 there is a link that looks like this: `<a href="">here</a>`
 - [ ] Inside the quotes, put `https://request.edl.###.deep608lab.com/` where `###` is your lab id (ex: 021).
 - [ ] Save the file.

### Commit, Push, & Build
Let's commit our change and build a new container image!

 - [ ] Commit your local changes to Git.
 - [ ] Push your commit to GitHub.
 - [ ] Browse to your repository on GitHub and go to the `Actions` tab.
 - [ ] Select the `Block Page` Workflow on the left.
 - [ ] Monitor the Workflow run that kicked off from your push and make sure it completes successfully (green check).

### Verify
Let's verify that we have a new container image in our Container Registry!

 - [ ] Log into the GCP Portal.
 - [ ] Use the hamburger menu or the search bar up top to browse to the Google Container Registry (GCR) page.
 - [ ] On the `Images` tab, click on the `block-page` image.
 - [ ] You should see at least two images listed. One should have a recent `Created` timestamp (column on the right) and have the `Latest` tag assigned to it.
 - [ ] If you don't see the new container image, we will need to troubleshoot.

If your container image is ready to go, continue to Chapter 3 to configure Ambassador!

## Continue to [Chapter 3](chapter3.md) (Ambassador Configuration)