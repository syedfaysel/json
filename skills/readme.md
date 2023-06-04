TOC  

<link rel="stylesheet" href="../style.css">

[/Parent Directory](../)
* [UI/UX](./1.json)



<div class="skills">
  <h3>HeHe!Box within a box</h3>
  <div id="items">
  </div>

  <script>
        // fetch data here
      fetch("./1.json")
        .then(response => response.json())
        .then(data => {
          console.log(data);
          displayData(data);
        });



        // display data
        function displayData(data) {
          let items = document.getElementById("items");

          for(const skill of data) {
            console.log(skill);
            

            let item = document.createElement("div");
            item.classList = "item";
            item.innerHTML = `<p>${skill.title}</p>
            <p>${skill.id}</p>
            <a href="${skill.links[0]}" target="_blank">Watch now</a>`;
            items.appendChild(item);
          }
        }


        
  </script>

</div>




