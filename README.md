# prodigy
html
<header id="nav-menu">
  <div class="container">
    <div class="nav-start">
      <a class="logo" href="/">
        <img src="logo.png" width="35" height="35" alt="Inc Logo">
      </a>
      <nav class="menu"></nav>
    </div>
    <div class="nav-end">
      <button class="btn btn-primary">Create</button>
    </div>
  </div>
</header>



css
#nav-menu {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: white;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  transition: background-color 0.3s ease;
}

#nav-menu.scrolled {
  background-color: #f2f2f2;
}

#nav-menu .container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
}

#nav-menu .menu {
  display: flex;
  align-items: center;
}

#nav-menu .menu a {
  color: #333;
  text-decoration: none;
  margin-right: 1rem;
  transition: color 0.3s ease;
}

#nav-menu .menu a:hover {
  color: #555;
}




java script
const navMenu = document.getElementById("nav-menu");

window.addEventListener("scroll", function() {
  if (window.pageYOffset > 0) {
    navMenu.classList.add("scrolled");
  } else {
    navMenu.classList.remove("scrolled");
  }
});

const menuItems = document.querySelectorAll("#nav-menu .menu a");

menuItems.forEach(function(item) {
  item.addEventListener("mouseover", function() {
    item.style.color = "#555";
  });
  item.addEventListener("mouseout", function() {
    item.style.color = "#333";
  });
});
