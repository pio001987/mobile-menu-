# mobile-menu-
help how to add this html <script>

var mobileElements = {
  mobileMenu: document.querySelector('.mobile-menu'),
  mobileMenuTrigger: document.querySelector('.header__mobileMenuTrigger'),
  body: document.querySelector('body'),
  header: document.querySelector('.header'),
  items: document.querySelectorAll('.menu-item')
};
var mobileMenuTrigger = mobileElements.mobileMenuTrigger,
    mobileMenu = mobileElements.mobileMenu,
    body = mobileElements.body,
    header = mobileElements.header,
    items = mobileElements.items;

var animateItems = function animateItems() {
  var interval = 50;
  items.forEach(function (i, index) {
    i.addEventListener('click', function () {
      toggleMenu();
    });

    if (!i.classList.contains('reveal')) {
      setTimeout(function () {
        i.classList.toggle('reveal');
      }, index * interval);
    } else {
      i.classList.toggle('reveal');
    }
  });
};
