const toggle = document.querySelector(".nav-toggle");
const links = document.querySelector(".nav-links");

toggle?.addEventListener("click", () => {
  const open = links.classList.toggle("open");
  toggle.setAttribute("aria-expanded", open ? "true" : "false");
});

const dropdown = document.querySelector(".dropdown");
const dropBtn = document.querySelector(".dropdown-btn");

dropBtn?.addEventListener("click", (e) => {
  e.stopPropagation();
  const open = dropdown.classList.toggle("open");
  dropBtn.setAttribute("aria-expanded", open ? "true" : "false");
});

document.addEventListener("click", () => {
  dropdown?.classList.remove("open");
  dropBtn?.setAttribute("aria-expanded", "false");
});
