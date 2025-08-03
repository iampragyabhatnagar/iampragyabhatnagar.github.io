// --- NAVBAR SCRIPT ---
// This script handles the mobile hamburger menu functionality.
const hamburger = document.querySelector(".hamburger");
const navMenu = document.querySelector(".nav-menu");

hamburger.addEventListener("click", mobileMenu);

function mobileMenu() {
    hamburger.classList.toggle("active");
    navMenu.classList.toggle("active");
}

const navLinks = document.querySelectorAll(".nav-link");

navLinks.forEach(n => n.addEventListener("click", closeMenu));

function closeMenu() {
    hamburger.classList.remove("active");
    navMenu.classList.remove("active");
}


// --- SCROLL ANIMATION SCRIPT ---
// This script adds a class to sections when they come into view,
// triggering CSS animations for a smoother user experience.
document.addEventListener("DOMContentLoaded", () => {
    const sections = document.querySelectorAll("section");

    const observerOptions = {
        root: null, // relative to the viewport
        rootMargin: "0px",
        threshold: 0.2 // trigger when 20% of the section is visible
    };

    const observer = new IntersectionObserver((entries, observer) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.classList.add("visible");
                observer.unobserve(entry.target);
            }
        });
    }, observerOptions);

    sections.forEach(section => {
        observer.observe(section);
    });
});

// --- 3D TILT EFFECT SCRIPT ---
// This script initializes the tilt.js library on the card elements.
// It uses a try-catch block to gracefully handle cases where the library might not load.
// The tilt.js library is loaded via a CDN in the HTML file.
document.addEventListener('DOMContentLoaded', () => {
    try {
        $('.card').tilt({
            maxTilt: 10,
            perspective: 1000,
            easing: "cubic-bezier(.03,.98,.52,.99)",
            speed: 1000,
            glare: true,
            maxGlare: 0.2
        });
    } catch (e) {
        console.warn("Tilt.js library not loaded or error occurred.", e);
    }
});
