// Mobile Menu Toggle// ===== MOBILE MENU =====// Mobile Menu Toggle

const navMenu = document.getElementById('nav-menu');

const navToggle = document.getElementById('nav-toggle');const navMenu = document.getElementById('nav-menu');const mobileMenuToggle = document.getElementById('mobileMenuToggle');

const navClose = document.getElementById('nav-close');

const navToggle = document.getElementById('nav-toggle');const navMenu = document.getElementById('navMenu');

// Show menu

if (navToggle) {const navClose = document.getElementById('nav-close');

    navToggle.addEventListener('click', () => {

        navMenu.classList.add('show-menu');mobileMenuToggle.addEventListener('click', () => {

    });

}// Show menu    mobileMenuToggle.classList.toggle('active');



// Hide menuif (navToggle) {    navMenu.classList.toggle('active');

if (navClose) {

    navClose.addEventListener('click', () => {    navToggle.addEventListener('click', () => {});

        navMenu.classList.remove('show-menu');

    });        navMenu.classList.add('show-menu');

}

    });// Close mobile menu when clicking on a link

// Close menu when clicking a link

const navLinks = document.querySelectorAll('.nav__link');}const navLinks = document.querySelectorAll('.nav-link');

navLinks.forEach(link => {

    link.addEventListener('click', () => {navLinks.forEach(link => {

        navMenu.classList.remove('show-menu');

    });// Hide menu    link.addEventListener('click', () => {

});

if (navClose) {        mobileMenuToggle.classList.remove('active');

// Active link on scroll

const sections = document.querySelectorAll('section[id]');    navClose.addEventListener('click', () => {        navMenu.classList.remove('active');



function scrollActive() {        navMenu.classList.remove('show-menu');    });

    const scrollY = window.pageYOffset;

    });});

    sections.forEach(current => {

        const sectionHeight = current.offsetHeight;}

        const sectionTop = current.offsetTop - 100;

        const sectionId = current.getAttribute('id');// Navbar scroll effect

        const link = document.querySelector('.nav__link[href*=' + sectionId + ']');

// Close menu when clicking a linkconst navbar = document.getElementById('navbar');

        if (link) {

            if (scrollY > sectionTop && scrollY <= sectionTop + sectionHeight) {const navLinks = document.querySelectorAll('.nav__link');let lastScrollY = window.scrollY;

                link.classList.add('active-link');

            } else {navLinks.forEach(link => {

                link.classList.remove('active-link');

            }    link.addEventListener('click', () => {window.addEventListener('scroll', () => {

        }

    });        navMenu.classList.remove('show-menu');    if (window.scrollY > 50) {

}

    });        navbar.classList.add('scrolled');

window.addEventListener('scroll', scrollActive);

});    } else {

// Scroll header shadow

function scrollHeader() {        navbar.classList.remove('scrolled');

    const header = document.getElementById('header');

    if (this.scrollY >= 50) {// ===== ACTIVE LINK ON SCROLL =====    }

        header.classList.add('scroll-header');

    } else {const sections = document.querySelectorAll('section[id]');});

        header.classList.remove('scroll-header');

    }

}

function scrollActive() {// Active navigation link based on scroll position

window.addEventListener('scroll', scrollHeader);

    const scrollY = window.pageYOffset;const sections = document.querySelectorAll('section[id]');

// Contact form

const contactForm = document.getElementById('contact-form');



if (contactForm) {    sections.forEach(current => {function updateActiveNavLink() {

    contactForm.addEventListener('submit', (e) => {

        e.preventDefault();        const sectionHeight = current.offsetHeight;    const scrollY = window.pageYOffset;

        

        const formData = new FormData(contactForm);        const sectionTop = current.offsetTop - 100;    

        const data = Object.fromEntries(formData);

                const sectionId = current.getAttribute('id');    sections.forEach(section => {

        console.log('Form submitted:', data);

                const link = document.querySelector('.nav__link[href*=' + sectionId + ']');        const sectionHeight = section.offsetHeight;

        alert('Thank you for your message! We will get back to you within 24 hours.');

                const sectionTop = section.offsetTop - 100;

        contactForm.reset();

    });        if (link) {        const sectionId = section.getAttribute('id');

}

            if (scrollY > sectionTop && scrollY <= sectionTop + sectionHeight) {        

// Smooth scroll

document.querySelectorAll('a[href^="#"]').forEach(anchor => {                link.classList.add('active-link');        if (scrollY > sectionTop && scrollY <= sectionTop + sectionHeight) {

    anchor.addEventListener('click', function (e) {

        e.preventDefault();            } else {            navLinks.forEach(link => {

        const target = document.querySelector(this.getAttribute('href'));

        if (target) {                link.classList.remove('active-link');                link.classList.remove('active');

            target.scrollIntoView({

                behavior: 'smooth',            }                if (link.getAttribute('href') === `#${sectionId}`) {

                block: 'start'

            });        }                    link.classList.add('active');

        }

    });    });                }

});

}            });

        }

window.addEventListener('scroll', scrollActive);    });

}

// ===== SCROLL HEADER SHADOW =====

function scrollHeader() {window.addEventListener('scroll', updateActiveNavLink);

    const header = document.getElementById('header');

    if (this.scrollY >= 50) {// Smooth scroll for navigation links

        header.classList.add('scroll-header');navLinks.forEach(link => {

    } else {    link.addEventListener('click', (e) => {

        header.classList.remove('scroll-header');        e.preventDefault();

    }        const targetId = link.getAttribute('href');

}        const targetSection = document.querySelector(targetId);

        

window.addEventListener('scroll', scrollHeader);        if (targetSection) {

            const offsetTop = targetSection.offsetTop - 70;

// ===== CONTACT FORM =====            window.scrollTo({

const contactForm = document.getElementById('contact-form');                top: offsetTop,

                behavior: 'smooth'

if (contactForm) {            });

    contactForm.addEventListener('submit', (e) => {        }

        e.preventDefault();    });

        });

        // Get form data

        const formData = new FormData(contactForm);// Intersection Observer for animations

        const data = Object.fromEntries(formData);const observerOptions = {

            threshold: 0.1,

        // Here you would typically send the data to a server    rootMargin: '0px 0px -50px 0px'

        console.log('Form submitted:', data);};

        

        // Show success message (you can customize this)const observer = new IntersectionObserver((entries) => {

        alert('Thank you for your message! We will get back to you within 24 hours.');    entries.forEach(entry => {

                if (entry.isIntersecting) {

        // Reset form            entry.target.style.opacity = '1';

        contactForm.reset();            entry.target.style.transform = 'translateY(0)';

    });        }

}    });

}, observerOptions);

// ===== SMOOTH SCROLL =====

document.querySelectorAll('a[href^="#"]').forEach(anchor => {// Observe service cards and other elements

    anchor.addEventListener('click', function (e) {document.querySelectorAll('.service-card, .info-card').forEach(el => {

        e.preventDefault();    el.style.opacity = '0';

        const target = document.querySelector(this.getAttribute('href'));    el.style.transform = 'translateY(30px)';

        if (target) {    el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';

            target.scrollIntoView({    observer.observe(el);

                behavior: 'smooth',});

                block: 'start'

            });// Contact Form Handling

        }const contactForm = document.getElementById('contactForm');

    });

});contactForm.addEventListener('submit', (e) => {

    e.preventDefault();
    
    // Get form data
    const formData = new FormData(contactForm);
    const data = Object.fromEntries(formData);
    
    // In a real application, you would send this to a server
    console.log('Form submitted with data:', data);
    
    // Show success message
    showFormMessage('Thank you! Your message has been sent successfully. We will get back to you soon.', 'success');
    
    // Reset form
    contactForm.reset();
});

function showFormMessage(message, type) {
    // Remove any existing messages
    const existingMessage = document.querySelector('.form-message');
    if (existingMessage) {
        existingMessage.remove();
    }
    
    // Create message element
    const messageDiv = document.createElement('div');
    messageDiv.className = `form-message ${type}`;
    messageDiv.textContent = message;
    messageDiv.style.padding = '15px';
    messageDiv.style.borderRadius = '8px';
    messageDiv.style.marginTop = '20px';
    messageDiv.style.textAlign = 'center';
    messageDiv.style.fontWeight = '500';
    
    if (type === 'success') {
        messageDiv.style.background = '#d1fae5';
        messageDiv.style.color = '#065f46';
        messageDiv.style.border = '2px solid #10b981';
    } else {
        messageDiv.style.background = '#fee2e2';
        messageDiv.style.color = '#991b1b';
        messageDiv.style.border = '2px solid #ef4444';
    }
    
    // Insert message after form
    contactForm.parentElement.insertBefore(messageDiv, contactForm.nextSibling);
    
    // Remove message after 5 seconds
    setTimeout(() => {
        messageDiv.style.transition = 'opacity 0.5s ease';
        messageDiv.style.opacity = '0';
        setTimeout(() => messageDiv.remove(), 500);
    }, 5000);
}

// Parallax effect for hero section
window.addEventListener('scroll', () => {
    const scrolled = window.pageYOffset;
    const heroContent = document.querySelector('.hero-content');
    
    if (heroContent) {
        heroContent.style.transform = `translateY(${scrolled * 0.5}px)`;
    }
});

// Add loading animation
window.addEventListener('load', () => {
    document.body.style.opacity = '0';
    document.body.style.transition = 'opacity 0.5s ease';
    
    setTimeout(() => {
        document.body.style.opacity = '1';
    }, 100);
});

// Gallery Filter Functionality
const filterButtons = document.querySelectorAll('.filter-btn');
const galleryItems = document.querySelectorAll('.gallery-item');

filterButtons.forEach(button => {
    button.addEventListener('click', () => {
        // Remove active class from all buttons
        filterButtons.forEach(btn => btn.classList.remove('active'));
        // Add active class to clicked button
        button.classList.add('active');
        
        const filter = button.getAttribute('data-filter');
        
        galleryItems.forEach(item => {
            const category = item.getAttribute('data-category');
            
            if (filter === 'all' || category === filter) {
                item.classList.remove('hidden');
                item.style.animation = 'fadeInUp 0.5s ease';
            } else {
                item.classList.add('hidden');
            }
        });
    });
});

// Gallery Item Click - Image Modal/Lightbox (Simple version)
galleryItems.forEach(item => {
    item.addEventListener('click', () => {
        const img = item.querySelector('img');
        const overlay = item.querySelector('.gallery-overlay');
        const title = overlay.querySelector('h4').textContent;
        
        // Create lightbox
        const lightbox = document.createElement('div');
        lightbox.className = 'lightbox';
        lightbox.innerHTML = `
            <div class="lightbox-content">
                <button class="lightbox-close">&times;</button>
                <img src="${img.src}" alt="${title}">
                <div class="lightbox-caption">${title}</div>
            </div>
        `;
        
        // Add styles
        lightbox.style.position = 'fixed';
        lightbox.style.top = '0';
        lightbox.style.left = '0';
        lightbox.style.width = '100%';
        lightbox.style.height = '100%';
        lightbox.style.background = 'rgba(0, 0, 0, 0.95)';
        lightbox.style.display = 'flex';
        lightbox.style.alignItems = 'center';
        lightbox.style.justifyContent = 'center';
        lightbox.style.zIndex = '10000';
        lightbox.style.padding = '20px';
        
        const content = lightbox.querySelector('.lightbox-content');
        content.style.position = 'relative';
        content.style.maxWidth = '90%';
        content.style.maxHeight = '90%';
        
        const closeBtn = lightbox.querySelector('.lightbox-close');
        closeBtn.style.position = 'absolute';
        closeBtn.style.top = '-40px';
        closeBtn.style.right = '0';
        closeBtn.style.background = 'none';
        closeBtn.style.border = 'none';
        closeBtn.style.color = '#fff';
        closeBtn.style.fontSize = '40px';
        closeBtn.style.cursor = 'pointer';
        closeBtn.style.lineHeight = '1';
        
        const lightboxImg = lightbox.querySelector('img');
        lightboxImg.style.maxWidth = '100%';
        lightboxImg.style.maxHeight = '80vh';
        lightboxImg.style.borderRadius = '10px';
        lightboxImg.style.display = 'block';
        
        const caption = lightbox.querySelector('.lightbox-caption');
        caption.style.color = '#fff';
        caption.style.textAlign = 'center';
        caption.style.marginTop = '20px';
        caption.style.fontSize = '18px';
        caption.style.fontWeight = '600';
        
        document.body.appendChild(lightbox);
        
        // Close lightbox
        const closeLightbox = () => {
            lightbox.style.opacity = '0';
            setTimeout(() => lightbox.remove(), 300);
        };
        
        closeBtn.addEventListener('click', closeLightbox);
        lightbox.addEventListener('click', (e) => {
            if (e.target === lightbox) closeLightbox();
        });
        
        // Add fade in
        lightbox.style.opacity = '0';
        lightbox.style.transition = 'opacity 0.3s ease';
        setTimeout(() => lightbox.style.opacity = '1', 10);
    });
});

