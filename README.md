<h1>Explore Log</h1>

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

4.**Environment Variables:**

Create a .env file in the root directory and add your Cloudinary credentials:

```makefile
MAPBOX_API_KEY=your_apikey
CLOUDINARY_URL=your_cloudinary_url
```

5.**Start the Server:**

```bash
rails server
```

6.**Visit the Application:**

Open your browser and go to **http://localhost:3000**.

<h3>Usage</h3>

<h4>Adding a Journey</h4>

1. Navigate to the "New Journey" page.
2. Fill in the required details and submit the form.
3. You will be redirected to the journey's show page, where you can add pins.

<h4>Adding Pins</h4>

1. On the journey's show page, click on "Add Pin."
2. Choose between one of our beautiful templates or a blank canvas.
3. Choose between adding text or photo inputs.
4. For text, enter your text and click outside the input to save it.
5. For photos, upload an image file from your device.
6. Resize and reposition the elements as needed.

<h4>Undoing Actions</h4>

1. If you want to undo the last action, use the undo functionality provided in the application.

<h3>Controllers and Actions</h4>

<h4>BlankController</h4>

- **connect:** Initializes the canvas and gesturable elements.
- **toggleSideBar:** Toggles the sidebar visibility.
- **onChangeColor:** Changes the background color of the canvas.
- **addTextInput:** Adds a new text input to the canvas.
- **addPhotoInput:** Adds a new photo input to the canvas.
- **handleTextChange:** Handles changes to text inputs.
- **handlePhotoChange:** Handles changes to photo inputs.
- **initializeInteract:** Initializes draggable and resizable functionality for elements.
- **initializeGesturable:** Initializes gesturable functionality for elements.
- **undoLastAction:** Undoes the last action.

<h4>JourneysController</h4>

- **index:** Lists all journeys.
- **show:** Displays a specific journey.
- **new:** Shows the form for creating a new journey.
- **create:** Creates a new journey.
- **edit:** Shows the form for editing a journey.
- **update:** Updates a specific journey.
- **destroy:** Deletes a specific journey.
  
<h4>PinsController</h4>

- **create:** Creates a new pin within a journey.
- **edit:** Shows the form for editing a pin.
- **update:** Updates a specific pin.
- **destroy:** Deletes a specific pin.

<h3>Customization</h3>

To customize the application's appearance and functionality, you can modify the corresponding controllers, views, and stylesheets.

<h4>Adding Custom Styles</h4>
Add your custom styles to <strong>'app/assets/stylesheets/application.css'</strong> or create new stylesheets and include them in the application.

<h4>Modifying Views</h4>
Edit the views located in <strong>'app/views'</strong> to change the HTML structure and content displayed to users.

<h3>Contributing</h3>

Contributions are welcome! Please fork the repository and create a pull request with your changes.

1. Fork the repository.
2. Create a new branch: **git checkout -b my-feature-branch**
3. Make your changes and commit them: **git commit -am 'Add new feature'**
4. Push to the branch: **git push origin my-feature-branch**
5. Create a pull request.
   
<h3>License</h3>

This project is licensed under the MIT License. See the LICENSE file for details.

