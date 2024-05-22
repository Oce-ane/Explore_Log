<h1>My Rails Application</h1>

<h3>Table of Contents</h3>

- Introduction
- Features
- Setup and Installation
- Usage
- Controllers and Actions
- Customization
- Contributing
- License

<h3>Introduction</h3>

This Rails application allows users to create, edit, and manage journeys and pins. Users can add text and photos to their journeys. They can follow their journey on a map by following the route. Users could potentially create a video summary of their journey when it's completed. The application also includes functionality for undoing actions and dynamically placing and resizing elements.

<h3>Features</h3>

- Create and manage journeys and pins.
- Add text and photo inputs to journeys.
- Undo the last action.
- Dynamic resizing and positioning of text and photo elements.
- SweetAlert integration for confirmation dialogs.

<h3>Setup and Installation</h3>

1.**Clone the Repository:**

```bash
git clone https://github.com/yourusername/your-repo.git
cd your-repo
```

2.**Install Dependencies:**

```bash
bundle install
yarn install
```
3.**Set Up the Database:**

```bash
rails db:create
rails db:migrate
```

Environment Variables:
Create a .env file in the root directory and add your Cloudinary credentials:

makefile
Copier le code
CLOUDINARY_URL=your_cloudinary_url
Start the Server:

bash
Copier le code
rails server
Visit the Application:
Open your browser and go to http://localhost:3000.

Usage

Adding a Journey
Navigate to the "New Journey" page.
Fill in the required details and submit the form.
You will be redirected to the journey's show page, where you can add pins.
Adding Pins
On the journey's show page, click on "Add Pin."
Choose between adding text or photo inputs.
For text, enter your text and click outside the input to save it.
For photos, upload an image file from your device.
Resize and reposition the elements as needed.
Embedding Videos
Use the video_tag helper to embed videos from Cloudinary.
ruby
Copier le code
<%= video_tag "https://res.cloudinary.com/your_account/video/upload/v123456789/video_name.mp4", controls: true, type: "video/mp4" %>
Undoing Actions
If you want to undo the last action, use the undo functionality provided in the application.
Controllers and Actions

BlankController
connect: Initializes the canvas and gesturable elements.
toggleSideBar: Toggles the sidebar visibility.
onChangeColor: Changes the background color of the canvas.
addTextInput: Adds a new text input to the canvas.
addPhotoInput: Adds a new photo input to the canvas.
handleTextChange: Handles changes to text inputs.
handlePhotoChange: Handles changes to photo inputs.
initializeInteract: Initializes draggable and resizable functionality for elements.
initializeGesturable: Initializes gesturable functionality for elements.
undoLastAction: Undoes the last action.
JourneysController
index: Lists all journeys.
show: Displays a specific journey.
new: Shows the form for creating a new journey.
create: Creates a new journey.
edit: Shows the form for editing a journey.
update: Updates a specific journey.
destroy: Deletes a specific journey.
PinsController
create: Creates a new pin within a journey.
edit: Shows the form for editing a pin.
update: Updates a specific pin.
destroy: Deletes a specific pin.
Customization

To customize the application's appearance and functionality, you can modify the corresponding controllers, views, and stylesheets.

Adding Custom Styles
Add your custom styles to app/assets/stylesheets/application.css or create new stylesheets and include them in the application.

Modifying Views
Edit the views located in app/views to change the HTML structure and content displayed to users.

Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.

Fork the repository.
Create a new branch: git checkout -b my-feature-branch
Make your changes and commit them: git commit -am 'Add new feature'
Push to the branch: git push origin my-feature-branch
Create a pull request.
License

This project is licensed under the MIT License. See the LICENSE file for details.

