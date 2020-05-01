<template>
  <div id="contact">
    <div class="contact-image">
      <div class="empty m-4"></div>
      <div id="form-container" class="col-md-6 p-2 mx-auto">
        <h2 class="my-2" data-aos="fade-bottom">Contact Me</h2>
        <form id="my-form" action="https://formspree.io/xyyngqpb" method="POST">
          <label data-aos="fade-left">
            Your name:
            <input class="form-control" type="text" name="name" />
          </label>
          <br />
          <label data-aos="fade-right">
            Your email:
            <input class="form-control" type="text" name="_replyto" />
          </label>
          <br />
          <label data-aos="fade-left">
            Your subject:
            <input class="form-control" type="text" name="subject" />
          </label>
          <br />
          <label id="message" data-aos="fade-right">
            Your message:
            <textarea
              id="messageBox"
              class="form-control mx-auto"
              name="message"
            ></textarea>
          </label>
          <br />
          <button
            id="my-form-button"
            class="btn btn-light px-5 py-1 mt-2"
            type="submit"
            data-aos="fade-left"
          >
            Send
          </button>
          <p id="my-form-status"></p>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
window.addEventListener("DOMContentLoaded", function() {
  // get the form elements defined in your form HTML above

  var form = document.getElementById("my-form");
  var button = document.getElementById("my-form-button");
  var status = document.getElementById("my-form-status");

  // Success and Error functions for after the form is submitted

  function success() {
    form.reset();
    button.style = "display: none ";
    status.innerHTML = "Thanks!";
  }

  function error() {
    status.innerHTML = "Oops! There was a problem.";
  }

  // handle the form submission event

  form.addEventListener("submit", function(ev) {
    ev.preventDefault();
    var data = new FormData(form);
    ajax(form.method, form.action, data, success, error);
  });
});

// helper function for sending an AJAX request

function ajax(method, url, data, success, error) {
  var xhr = new XMLHttpRequest();
  xhr.open(method, url);
  xhr.setRequestHeader("Accept", "application/json");
  xhr.onreadystatechange = function() {
    if (xhr.readyState !== XMLHttpRequest.DONE) return;
    if (xhr.status === 200) {
      success(xhr.response, xhr.responseType);
    } else {
      error(xhr.status, xhr.response, xhr.responseType);
    }
  };
  xhr.send(data);
}
</script>

<style>
#contact {
  min-height: 100vh;
  font-size: 1.5rem;
  font-weight: bold;
  color: rgb(206, 206, 206);
}
#message {
  width: 100%;
}
#messageBox {
  width: 60%;
  height: 120px;
}

.contact-image {
  height: 100vh;
  background-attachment: fixed;
  background-image: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.85)),
    url("../../assets/contact-bg.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
}
h2 {
  font-size: 2.5rem;
  font-weight: bold;
}

.btn-light {
  font-size: 2rem;
  background-color: rgba(0, 0, 0, 0.6);
  color: rgb(238, 196, 92);
  font-weight: bold;
  border: none;
}
.btn-light:hover {
  background-color: rgb(192, 156, 66);
}
</style>
