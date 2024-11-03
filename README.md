---

# HTA-Gallery

HTA-Gallery is a Windows-only HTML Application that enables secure, anonymous sharing of images, GIFs, and video files directly from the HTA interface to your computer. Designed to make file sharing easy and private, HTA-Gallery sources its media files from GitHub while keeping the file links hidden for added security. With HTA-Gallery, you can transfer media files without navigating through a browser, creating a streamlined and private sharing experience for content with friends and collaborators.

One unique feature of HTA-Gallery is its support for embedding hidden files within media files. Using a simple CMD command, users can insert additional files—such as .zip or .rar folders—into images, GIFs, or video files, enabling secure, anonymous sharing of files or programs within regular media formats. Whether sharing an image or securely delivering a program, HTA-Gallery offers a flexible solution that combines ease of use with powerful privacy options.

## Features

- **Drag-and-Drop Functionality**: Easily drag images, GIFs, or video files from the HTA-Gallery interface to your computer for quick access and sharing.
- **Anonymous Sharing**: File links are hidden, ensuring privacy while allowing secure downloads from GitHub.
- **File Concealment in Media**: Support for embedding hidden files inside images, GIFs, or videos using CMD commands, allowing you to combine media files with additional hidden content.
- **Browser-Free Experience**: Share and receive files without using a browser, making the process more streamlined and private.

> **Note**: HTA-Gallery is designed to work on Windows only, as it relies on the Windows HTA (HTML Application) platform.

## How It Works

HTA-Gallery leverages HTML Application (HTA) technology, which provides a user-friendly Windows-based interface for displaying and interacting with media files. The application:

1. **Sources Files from GitHub**: All media files displayed in HTA-Gallery are hosted on GitHub, but their direct links are hidden, maintaining user anonymity.
2. **Supports Concealment with CMD**: By using the `copy /b` command in CMD (e.g., `copy /b image.extension+folder.zip+folder.rar image.extension`), users can hide additional files within media files.
3. **Drag-and-Drop Sharing**: Users can drag media files from the HTA interface to their computer, providing a quick and private way to transfer files without direct file links.

## Installation

1. **Clone or Download the Repository**:
   ```bash
   git clone https://github.com/yourusername/HTA-Gallery.git
   ```
2. **Open the HTA Application**:
   - Run the HTA file on Windows to launch HTA-Gallery.
3. **Drag-and-Drop Usage**:
   - Select and drag images, GIFs, or video files from the application to your computer.

## Embedding Hidden Files

To conceal files within media files, follow these instructions:

1. Place the media file (e.g., `image.jpg`) in the same directory as the files you want to hide (e.g., `folder.zip`).
2. Run the following command in CMD:
   ```cmd
   copy /b image.jpg+folder.zip image.jpg
   ```
3. This will embed `folder.zip` inside `image.jpg`. The resulting file appears as a standard image but can be extracted with file archiving tools to reveal the hidden content.

## Usage Tips

- **Privacy**: HTA-Gallery hides file links, making it ideal for users who want to share files discreetly.
- **Compatibility**: Media files with embedded content still function normally, but hidden files may require specific extraction tools (e.g., WinRAR, 7-Zip).
- **Windows-Only**: HTA-Gallery is designed exclusively for Windows, as HTA applications are not compatible with other operating systems.

---

## Project Structure and Features

### 1. **Dual Interface: Public and Private Files**

   - **Public Interface**:
     - Files in the public interface are openly viewable by all users who access the HTA-Gallery application.
     - Users can see, interact with, and download public images, GIFs, and videos.
     - Includes a timer showing days remaining before deletion.
     - Media files in this section are stored temporarily, subject to the 30-day deletion policy.

   - **Private Interface**:
     - Accessible only through UUID v5 ID authentication.
     - Files are only viewable or downloadable by entering the unique ID.
     - This setup ensures an extra layer of security for sharing sensitive files, limiting access to those who have the unique ID.

### 2. **File Expiration and Deletion Management**

   - **30-Day Deletion Limit with Customizable Deletion Date**:
     - Users can set a custom deletion date within the 30-day maximum limit.
     - The system will allow users to select a specific date (e.g., 10, 15, or 25 days from the upload date).
     - Once set, users cannot change the deletion date to prevent unintended file retention.

   - **Potential Subscription Option (Future Consideration)**:
     - Optional feature to extend file storage time beyond the 30-day limit for subscribers.
     - Subscribers could have options for file retention up to 60 days or longer, based on chosen plans.
     - This feature is only conceptual for now but could be implemented if long-term file storage becomes a demand.

### 3. **Integrated File Concealment with CMD**

   - **Embed Files within Media**:
     - The HTA-Gallery interface includes a “Choose a File” button that automates the CMD command (`copy /b image.jpg+folder.zip image.jpg`) to embed files within media files.
     - This button allows users to generate hidden-content media files without needing external commands.
      - **Diagram**
        - Choose a File (Image, Video, Gif) -> Choose a File (Zip, Rar, Txt, etc...) -Optional-> (Choose another File) -Result-> input(Image-Name.extension)

   - **User Flow**:
     - Users select a media file and any additional file(s) to be embedded.
     - HTA-Gallery runs the CMD command to create a new file that combines the files, concealing the added files.

## Technical Components and Implementation

### 1. **Interface Development (HTML/CSS/JavaScript)**

   - **Deletion Date Selector**:
     - Add a date picker allowing users to set their desired deletion date within the 30-day range.
     - The selected date will be stored alongside each file’s metadata and used by the auto-deletion script.

   - **HTA Interface Layout**:
     - Add tabs or buttons for Public and Private sections, with input for UUID v5 in the Private section.
     - Include the "Choose a File" button and drag-and-drop features.

### 2. **File Storage and Deletion Management**

   - **Automated Expiration Script**:
     - Regularly check files against their custom deletion dates and delete them once they expire.
     - The system will display the remaining time before deletion for each file, whether set to the 30-day limit or an earlier custom date.

### 3. **Embedded Content Generator**

   - The “Choose a File” option automates the embedding command directly in HTA-Gallery, providing users with an intuitive way to hide files within media.

## Other Plans

   - API to get files and load them in other websites
   - The API For the private files needs to have the uuid v5 as a key to gain access

--- 

## With these additions, HTA-Gallery now includes flexible file management features that offer users greater control over file retention and deletion settings.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
