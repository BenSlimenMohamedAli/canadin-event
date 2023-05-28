<template>
  <section id="previous-event-sec">
        <div class="previous-event-heading-bg white-heading">
          <div class="container">
            <div class="row text-center">
              <div class="col-lg-12 col-md-12 col-sm-12 heading-col">
                <span>Lieu de l’évènement</span>
                <h2>Explorez l’île Maurice et joignez l’utile à l’agréable!</h2>
                <hr />
              </div>
            </div>
          </div>
        </div>
        <div class="previous-event-gallery">
          <div class="gallery">
            <div class="gallery-img">
              <img src="maurice/gallery/1.png" />
            </div>
            <div class="gallery-img">
              <img src="maurice/gallery/2.png" />
            </div>


            <div class="gallery-img">
              <img src="maurice/gallery/4.png" />
            </div>

            <div class="gallery-img">
              <img src="maurice/gallery/7.png" />
            </div>



          </div>

          <div class="gallery">


            <div class="gallery-img">
              <img src="maurice/gallery/8.png" />
            </div>
             <div class="gallery-img">
              <img src="maurice/gallery/11.png" />
            </div>

            <div class="gallery-img">
              <img style="height:100%" src="maurice/gallery/6.png" />
            </div>




          </div>

          <div class="gallery">
            <div class="gallery-img">
              <img style="height:100%"  src="maurice/gallery/9.png" />
            </div>
            <div class="gallery-img">
              <img style="height:100%"  src="maurice/gallery/10.png" />
            </div>

            <div class="gallery-img">
              <img src="maurice/gallery/12.png" />
            </div>


          </div>
        </div>

        <div id="myModal" class="modalModal">
          <span class="close cursor" onclick="closeModalModal()">&times</span>
          <div class="modalModal-content fadeInDown">
            <div class="mySlides">
              <img src="maurice/gallery/1.png" class="zoomIn" />
            </div>

            <div class="mySlides">
              <img src="maurice/gallery/2.png" class="zoomIn" />
            </div>

            <div class="mySlides">
              <img src="maurice/gallery/3.png" class="zoomIn" />
            </div>

            <div class="mySlides">
              <img src="maurice/gallery/4.png" class="zoomIn" />
            </div>
            <div class="mySlides">
              <img src="maurice/gallery/5.png" class="zoomIn" />
            </div>

            <div class="mySlides">
              <img src="maurice/gallery/6.png" class="zoomIn" />
            </div>

            <div class="mySlides">
              <img src="maurice/gallery/7.png" class="zoomIn" />
            </div>

            <div class="mySlides">
              <img src="maurice/gallery/8.png" class="zoomIn" />
            </div>
            <div class="mySlides">
              <img src="maurice/gallery/9.png" class="zoomIn" />
            </div>
            <div class="mySlides">
              <img src="maurice/gallery/10.png" class="zoomIn" />
            </div>
            <div class="mySlides">
              <img src="maurice/gallery/11.png" class="zoomIn" />
            </div>
            <div class="mySlides">
              <img src="maurice/gallery/12.png" class="zoomIn" />
            </div>
            <a class="prev" onclick="plusSlides(-1)">&#10094</a>
            <a class="next" onclick="plusSlides(1)">&#10095</a>
          </div>
        </div>
      </section>
</template>
