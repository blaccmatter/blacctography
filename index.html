/* ═══════════════════════════════════════════════════════════════════
   BLACCTOGRAPHY — Global JavaScript
   ═══════════════════════════════════════════════════════════════════ */

document.addEventListener('DOMContentLoaded', () => {

  // ── FLASH SHUTTER EFFECT ────────────────────────────────────────
  // Fires only on explicit user actions: form submit, polaroid click.
  // Auto-scheduling removed — was firing a full-screen white flash
  // every 7–16s uninvited, disrupting reading and form interaction.
  const flashEl = document.getElementById('flash-overlay');
  function triggerFlash() {
    if (!flashEl) return;
    flashEl.style.opacity = '0.6';
    setTimeout(() => { flashEl.style.opacity = '0'; }, 90);
  }

  // Expose globally for inline onclick use
  window.triggerFlash = triggerFlash;

  // ── SCROLL REVEAL ───────────────────────────────────────────────
  const srEls = document.querySelectorAll('.sr');
  if (srEls.length) {
    const observer = new IntersectionObserver((entries) => {
      entries.forEach((entry, i) => {
        if (entry.isIntersecting) {
          // Stagger children if parent is a group
          const delay = entry.target.dataset.srDelay || 0;
          setTimeout(() => entry.target.classList.add('in'), parseInt(delay));
          observer.unobserve(entry.target);
        }
      });
    }, { threshold: 0.08, rootMargin: '0px 0px -40px 0px' });
    srEls.forEach(el => observer.observe(el));
  }

  // ── NAVIGATION ──────────────────────────────────────────────────
  // Mobile toggle
  const navToggle = document.querySelector('.nav-toggle');
  const navLinks  = document.querySelector('.nav-links');
  if (navToggle && navLinks) {
    navToggle.addEventListener('click', () => {
      navToggle.classList.toggle('open');
      navLinks.classList.toggle('open');
    });
    // Close on link click
    navLinks.querySelectorAll('a').forEach(a => {
      a.addEventListener('click', () => {
        navToggle.classList.remove('open');
        navLinks.classList.remove('open');
      });
    });
  }

  // Active page highlight
  const currentPage = window.location.pathname.split('/').pop() || 'index.html';
  document.querySelectorAll('.nav-links a').forEach(a => {
    const href = a.getAttribute('href');
    if (href === currentPage || (currentPage === '' && href === 'index.html')) {
      a.classList.add('active');
    }
  });

  // Shrink nav on scroll
  const navEl = document.querySelector('nav');
  if (navEl) {
    window.addEventListener('scroll', () => {
      navEl.style.boxShadow = window.scrollY > 60
        ? '0 4px 40px rgba(12,11,9,0.12)'
        : 'none';
    }, { passive: true });
  }

  // ── TOAST ────────────────────────────────────────────────────────
  window.showToast = function(msg, accentColor) {
    let t = document.getElementById('toast');
    if (!t) {
      t = document.createElement('div');
      t.id = 'toast';
      t.className = 'toast';
      document.body.appendChild(t);
    }
    t.textContent = msg;
    t.style.borderLeftColor = accentColor || 'var(--red)';
    t.classList.add('show');
    setTimeout(() => t.classList.remove('show'), 4500);
  };

  // ── BOOKING FORM ─────────────────────────────────────────────────
  window.submitBookingForm = function() {
    const eventName = document.getElementById('f-event')?.value.trim();
    const ig        = document.getElementById('f-ig')?.value.trim();
    const date      = document.getElementById('f-date')?.value;
    const service   = document.getElementById('f-service')?.value;

    if (!eventName || !ig || !date || !service) {
      showToast('⚠  Fill in event name, IG handle, date & service type.', '#d63c2a');
      return;
    }

    triggerFlash();
    showToast("📸  Booking request sent! I'll hit your DM within 24 hrs.", '#e8a020');

    ['f-event','f-ig','f-date','f-time','f-loc','f-service','f-size','f-notes'].forEach(id => {
      const el = document.getElementById(id);
      if (el) el.value = '';
    });
  };

  // ── CONTACT FORM ─────────────────────────────────────────────────
  window.submitContactForm = function() {
    const name    = document.getElementById('c-name')?.value.trim();
    const ig      = document.getElementById('c-ig')?.value.trim();
    const message = document.getElementById('c-message')?.value.trim();

    if (!name || !message) {
      showToast('⚠  Name and message are required.', '#d63c2a');
      return;
    }

    triggerFlash();
    showToast("📩  Message sent! I'll respond within 24 hrs.", '#e8a020');

    ['c-name','c-ig','c-email','c-subject','c-message'].forEach(id => {
      const el = document.getElementById(id);
      if (el) el.value = '';
    });
  };

  // ── POLAROID HOVER FLASH ────────────────────────────────────────
  document.querySelectorAll('.polaroid').forEach(p => {
    p.addEventListener('click', () => triggerFlash());
  });

  // ── PORTFOLIO FILTER ────────────────────────────────────────────
  const filterBtns = document.querySelectorAll('.filter-btn');
  const portfolioGrid = document.getElementById('portfolio-grid');

  if (filterBtns.length && portfolioGrid) {
    filterBtns.forEach(btn => {
      btn.addEventListener('click', () => {
        filterBtns.forEach(b => b.classList.remove('active'));
        btn.classList.add('active');
        const filter = btn.dataset.filter;
        const items  = portfolioGrid.querySelectorAll('.port-item');
        items.forEach(item => {
          const cat = item.dataset.cat;
          const show = filter === 'all' || cat === filter;
          item.style.opacity    = show ? '1' : '0.2';
          item.style.transform  = show ? 'scale(1)' : 'scale(0.97)';
          item.style.pointerEvents = show ? 'auto' : 'none';
        });
      });
    });
  }

  // ── LIGHTBOX ────────────────────────────────────────────────────
  const lightbox = document.getElementById('lightbox');
  if (lightbox) {
    const lbImg   = document.getElementById('lb-img');
    const lbCap   = document.getElementById('lb-caption');
    const lbClose = document.getElementById('lb-close');

    document.querySelectorAll('.port-item[data-src]').forEach(item => {
      item.addEventListener('click', () => {
        lbImg.src = item.dataset.src;
        lbImg.alt = item.dataset.caption || '';
        if (lbCap) lbCap.textContent = item.dataset.caption || '';
        lightbox.classList.add('open');
        triggerFlash();
      });
    });

    lbClose?.addEventListener('click', () => lightbox.classList.remove('open'));
    lightbox.addEventListener('click', (e) => {
      if (e.target === lightbox) lightbox.classList.remove('open');
    });
    document.addEventListener('keydown', (e) => {
      if (e.key === 'Escape') lightbox.classList.remove('open');
    });
  }

  // ── SMOOTH SCROLL for same-page anchor links ─────────────────────
  document.querySelectorAll('a[href^="#"]').forEach(a => {
    a.addEventListener('click', e => {
      const target = document.querySelector(a.getAttribute('href'));
      if (target) {
        e.preventDefault();
        const top = target.getBoundingClientRect().top + window.scrollY - 72;
        window.scrollTo({ top, behavior: 'smooth' });
      }
    });
  });

});
