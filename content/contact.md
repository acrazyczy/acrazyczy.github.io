---
title: "Contact"
date: 2025-11-02
hidemeta: true
description: "Contact"
---

<div class="contact-email-row">
  <span class="contact-email-label">Email</span>
  <span class="contact-email-value">zc417 [at] cs [dot] rutgers [dot] edu</span>
  <button
    id="copy-email-button"
    class="contact-copy-button"
    type="button"
    data-email="zc417@cs.rutgers.edu"
  >
    Copy
  </button>
</div>

<script>
  (function () {
    const button = document.getElementById("copy-email-button");
    if (!button) return;

    button.addEventListener("click", async function () {
      const email = button.getAttribute("data-email");
      if (!email) return;

      try {
        await navigator.clipboard.writeText(email);
        button.textContent = "Copied";
      } catch (error) {
        const helper = document.createElement("textarea");
        helper.value = email;
        helper.setAttribute("readonly", "");
        helper.style.position = "absolute";
        helper.style.left = "-9999px";
        document.body.appendChild(helper);
        helper.select();
        document.execCommand("copy");
        document.body.removeChild(helper);
        button.textContent = "Copied";
      }
    });
  })();
</script>
