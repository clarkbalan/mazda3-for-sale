# 2010 Mazda 3 For Sale

This is a simple, static website built with Jekyll and hosted on GitHub Pages to showcase a 2010 Mazda 3 for sale. The site provides detailed photos and information about the car's condition and features.

## Live Website

You can view the live website here: [2010 Mazda 3 For Sale](https://clarkbalan.github.io/mazda3-for-sale/)

## Features

- High-quality images of the car
- Detailed car features and description
- Responsive design (works on mobile and desktop)
- Simple and clean layout

## Getting Started for Local Development

If you'd like to clone this repository and run the site locally for development, follow the steps below.

### Prerequisites

- Ruby installed (via [Homebrew](https://brew.sh/) or another package manager)
- Bundler installed

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/clarkbalan/mazda3-for-sale.git
   cd mazda3-for-sale
   ```

2. Install the necessary dependencies:

   ```bash
   bundle install
   ```

### Running the Site Locally

Once the dependencies are installed, you can serve the site locally using Jekyll. Run the following command:

```bash
bundle exec jekyll serve
```

This will start the server at `http://localhost:4000`. You can open this link in your browser to view the site.

### Building the Site

To build the site without running the local development server, you can use the following command:

```bash
bundle exec jekyll build
```

This will generate the static files in the `_site` directory, which can be deployed to any static hosting platform.

## Deployment

This project is automatically deployed via GitHub Pages. Any changes pushed to the `main` branch will trigger a rebuild and redeploy of the site.

## Contributing

Feel free to fork this project, submit pull requests, or use it as a base for your own static websites. Please ensure your changes maintain the responsive design and clean layout.

---

Thank you for checking out the project! If you have any questions or suggestions, feel free to open an issue.