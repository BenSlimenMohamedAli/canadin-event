<template>
  <section id="previous-event-sec">
        <div class="previous-event-heading-bg white-heading">
          <div class="container">
            <div class="row text-center">
              <div class="col-lg-12 col-md-12 col-sm-12 heading-col">
                <h2>Galleries</h2>
                <hr />
              </div>
            </div>
          </div>
        </div>
        <div class="previous-event-gallery">
          <div class="gallery">
            <div class="gallery-img">
              <img src="images/gallery1/1.jpg" />
            </div>
            <div class="gallery-img">
              <img src="images/gallery1/2.jpg" />
            </div>
            <div class="gallery-img">
              <img src="images/gallery1/3.jpg" />
            </div>

            <div class="gallery-img">
              <img src="images/gallery1/4.jpg" />
            </div>
          </div>

          <div class="gallery">
            <div class="gallery-img">
              <img src="images/gallery1/5.jpg" />
            </div>
            <div class="gallery-img">
              <img src="images/gallery1/6.jpg" />
            </div>
            <div class="gallery-img">
              <img src="images/gallery1/7.jpg" />
            </div>
            <div class="gallery-img">
              <img src="images/gallery1/8.jpg" />
            </div>
          </div>

          <div class="gallery">
            <div class="gallery-img">
              <img src="images/gallery1/9.jpg" />
            </div>
            <div class="gallery-img">
              <img src="images/gallery1/10.jpg" />
            </div>
            <div class="gallery-img">
              <img src="images/gallery1/11.jpg" />
            </div>
            <div class="gallery-img">
              <img src="images/gallery1/12.jpg" />
            </div>
          </div>
        </div>

        <div id="myModal" class="modalModal">
          <span class="close cursor" onclick="closeModalModal()">&times</span>
          <div class="modalModal-content fadeInDown">
            <div class="mySlides">
              <img src="images/gallery1/1.jpg" class="zoomIn" />
            </div>

            <div class="mySlides">
              <img src="images/gallery1/2.jpg" class="zoomIn" />
            </div>

            <div class="mySlides">
              <img src="images/gallery1/3.jpg" class="zoomIn" />
            </div>

            <div class="mySlides">
              <img src="images/gallery1/4.jpg" class="zoomIn" />
            </div>
            <div class="mySlides">
              <img src="images/gallery1/5.jpg" class="zoomIn" />
            </div>

            <div class="mySlides">
              <img src="images/gallery1/6.jpg" class="zoomIn" />
            </div>

            <div class="mySlides">
              <img src="images/gallery1/7.jpg" class="zoomIn" />
            </div>

            <div class="mySlides">
              <img src="images/gallery1/8.jpg" class="zoomIn" />
            </div>
            <div class="mySlides">
              <img src="images/gallery1/9.jpg" class="zoomIn" />
            </div>
            <div class="mySlides">
              <img src="images/gallery1/10.jpg" class="zoomIn" />
            </div>
            <div class="mySlides">
              <img src="images/gallery1/11.jpg" class="zoomIn" />
            </div>
            <div class="mySlides">
              <img src="images/gallery1/12.jpg" class="zoomIn" />
            </div>
            <a class="prev" onclick="plusSlides(-1)">&#10094</a>
            <a class="next" onclick="plusSlides(1)">&#10095</a>
          </div>
        </div>
      </section>
</template>
