---

# HTA-Gallery

HTA-Gallery is an HTML Application that enables secure, anonymous sharing of images, GIFs, and video files directly from the HTA interface to your computer. Designed to make file sharing easy and private, HTA-Gallery sources its media files from GitHub, but the file links remain hidden, ensuring an extra layer of security and privacy for users. With HTA-Gallery, you can transfer media files without navigating through a browser, creating a seamless and secure experience for sharing content with friends and collaborators.

One of the unique features of HTA-Gallery is its support for embedding hidden files within media files. Using a simple CMD command, users can insert additional files—such as .zip or .rar folders—into images, GIFs, or video files. This allows for secure, anonymous sharing of files or programs concealed within regular media formats. Whether you want to share an image or securely deliver a program, HTA-Gallery offers a flexible solution that combines ease of use with powerful privacy options.

## Features

- **Drag-and-Drop Functionality**: Easily drag images, GIFs, or video files from the HTA-Gallery interface to your computer for quick access and sharing.
- **Anonymous Sharing**: File links are hidden, ensuring privacy while allowing secure downloads from GitHub.
- **File Concealment in Media**: Support for embedding hidden files inside images, GIFs, or videos using CMD commands. This feature allows you to combine media files with additional hidden content for secure sharing.
- **Browser-Free Experience**: Share and receive files without using a browser, making the process more streamlined and private.

## How It Works

HTA-Gallery is powered by HTML Application (HTA) technology, which provides a user-friendly interface for displaying and interacting with media files. The application:

1. **Sources Files from GitHub**: All media files displayed in HTA-Gallery are hosted on GitHub, but their direct links are hidden, maintaining user anonymity.
2. **Supports Concealment with CMD**: By using the `copy /b` command in CMD (e.g., `copy /b image.extension+folder.zip+folder.rar image.extension`), users can hide additional files within media files. This command appends a compressed folder (.zip or .rar) to the end of the media file, allowing for file storage within images, GIFs, or videos.
3. **Drag-and-Drop Sharing**: Users can simply drag media files from the HTA interface to their computer, enabling a quick and private way to transfer files without direct file links.

## Installation

To use HTA-Gallery, follow these steps:

1. **Clone or Download the Repository**:
   ```bash
   git clone https://github.com/yourusername/HTA-Gallery.git
   ```
2. **Open the HTA Application**:
   - Run the HTA file to launch HTA-Gallery.
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
- **Compatibility**: While media files with embedded content still function as normal, extraction of hidden files may require specific tools (e.g., WinRAR, 7-Zip).
- **No Browser Needed**: Enjoy a fully standalone experience—HTA-Gallery operates outside the browser, providing a streamlined and private sharing platform.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
