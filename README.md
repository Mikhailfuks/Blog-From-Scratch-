<!DOCTYPE html>
<html>
<head>
  <title>My Blog</title>
  <style>
    /* Basic styling (feel free to customize) */
    body {
      font-family: sans-serif;
      margin: 0;
      padding: 20px;
    }

    .post {
      border: 1px solid #ccc;
      padding: 20px;
      margin-bottom: 20px;
    }

    .post-title {
      font-size: 24px;
      font-weight: bold;
      margin-bottom: 10px;
    }

    .post-content {
      margin-bottom: 10px;
    }

    .post-date {
      color: #888;
      font-size: 14px;
    }
  </style>
</head>
<body>
  <h1>My Blog</h1>

  <div id="blog-posts">
    <!-- Blog posts will be displayed here -->
  </div>

  <script>
    // Sample blog post data (replace with your actual data)
    const blogPosts = [
      {
        title: "My First Blog Post",
        content: "This is the content of my very first blog post. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla facilisi.",
        date: "2023-10-26"
      },
      {
        title: "Another Interesting Post",
        content: "Here's another post with some interesting information. Maecenas sed diam eget risus varius blandit sit amet non magna.",
        date: "2023-10-28"
      },
      // Add more blog posts here
    ];

    const blogPostsContainer = document.getElementById('blog-posts');

    // Function to display blog posts
    function displayBlogPosts() {
      blogPostsContainer.innerHTML = ''; // Clear previous posts

      blogPosts.forEach(post => {
        const postElement = document.createElement('div');
        postElement.classList.add('post');
        postElement.innerHTML = 
          <h2 class="post-title">${post.title}</h2>
          <p class="post-content">${post.content}</p>
          <p class="post-date">Published: ${post.date}</p>
        ;
        blogPostsContainer.appendChild(postElement);
      });
    }

    // Initial display of blog posts
    displayBlogPosts();
  </script>
</body>
</html>
