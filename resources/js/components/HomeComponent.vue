<template>
  <div>
    <!-- SLIDER SECTION START -->
    <div class="slider-2 bg-3">
      <div class="wow fadeInUp" data-wow-duration="1s" data-wow-delay="0.5s">
        <div class="row search-boxes">
          <div class="col-md-6">
            <div class="find-home-box box-left1">
              <div class="section-title text-white">
                <h2 class="h1">SEARCH MLS</h2>
              </div>
              <div class="find-homes">
                <div class="row">
                  <div class="col-md-12 col-sm-12 col-xs-12">
                    <div class="find-home-item">
                      <input
                        type="text"
                        name="mls"
                        placeholder="ADDRESS, ZIP, NEIGHBORHOOD, PROPERTY TYPE"
                      />
                      <a href="#" class="prevent-default search-standard">
                        <i class="icon-search2"></i>
                      </a>
                    </div>
                  </div>
                  <div class="col-sm-12 col-xs-12">
                    <div class="find-home-item">
                      <a class="button-1 btn-block btn-hover-1" href="#">VIEW ALL MLS</a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <div class="col-md-6">
            <div class="find-home-box box-right1">
              <div class="section-title text-white">
                <h2 class="h1">SEARCH DEVELOPMENTS</h2>
              </div>
              <div class="find-homes">
                <div class="row">
                  <div class="col-md-12 col-sm-12 col-xs-12">
                    <div class="find-home-item">
                      <input
                        type="text"
                        name="developments"
                        placeholder="DEVELOPMENT, BUILDER, ADDRESS, ZIP, NEIGHBORHOOD, STYLE"
                      />
                      <a href="#" class="prevent-default search-standard">
                        <i class="icon-search2"></i>
                      </a>
                    </div>
                  </div>
                  <div class="col-sm-12 col-xs-12">
                    <div class="find-home-item">
                      <a class="button-1 btn-block btn-hover-1" href="#">VIEW ALL DEVELOPMENTS</a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- SLIDER SECTION END -->
    <div class="vc_row-full-width vc_clearfix"></div>
      <div
        data-vc-full-width="true"
        data-vc-full-width-init="false"
        class="vc_row wpb_row vc_row-fluid vc_custom_1485139818778 vc_row-has-fill"
      >
        <div class="container">
          <div class="wpb_column vc_column_container vc_col-sm-12">
            <div class="vc_column-inner">
              <div class="wpb_wrapper">
                <div
                  class="vc_row wpb_row vc_inner vc_row-fluid vc_row-o-equal-height vc_row-o-content-middle vc_row-flex"
                >
                  <div class="wpb_column vc_column_container vc_col-sm-3">
                    <div class="vc_column-inner">
                      <div class="wpb_wrapper">
                        <div
                          class="g5plus-space space"
                          data-id="5ed1ab7fd11ff"
                          data-tablet="70"
                          data-tablet-portrait="60"
                          data-mobile="40"
                          data-mobile-landscape="50"
                          style="clear: both; display: block; height: 90px;"
                        ></div>
                        <div class="wpb_text_column wpb_content_element">
                          <div class="wpb_wrapper">
                            <p class="hd-subtitle-spec">DISCOVER YOUR</p>
                            <h2 class="hd-title-spec">
                              <span class="fl-accent">DREAM</span>
                              <span class="fl-accent">HOUSE</span>
                            </h2>
                          </div>
                        </div>
                        <div
                          class="g5plus-space space"
                          data-id="5ed1ab7fd1652"
                          data-tablet="70"
                          data-tablet-portrait="60"
                          data-mobile="40"
                          data-mobile-landscape="50"
                          style="clear: both; display: block; height: 90px;"
                        ></div>
                      </div>
                    </div>
                  </div>
                  <div
                    class="bg-dark-left wpb_column vc_column_container vc_col-sm-9 vc_col-has-fill"
                  >
                    <div class="column-inner vc_custom_1485091686429">
                      <div class="wpb_wrapper">
                        <div
                          class="search-properties clearfix show-status-tab style-default-small color-light"
                        >
                          <div class="form-search-wrap">
                            <div class="form-search-inner">
                              <div class="search-content">
                                <div data-href="#" class="search-properties-form">
                                  <div class="search-status-tab">
                                    <input
                                      class="search-field"
                                      type="hidden"
                                      name="status"
                                      value="for-rent"
                                      data-default-value
                                    />
                                    <button
                                      type="button"
                                      data-value="for-rent"
                                      class="btn-status-filter active"
                                    >For Rent</button>
                                    <button
                                      type="button"
                                      data-value="for-sale"
                                      class="btn-status-filter"
                                    >For Sale</button>
                                  </div>
                                  <form @submit.prevent="HomeFilter" @keydown="form.onKeydown($event)">
                                  <div class="row">
                                    <div class="col-md-4 col-sm-6 col-xs-12 form-group">
                                      <select
                                        name="type"
                                        title="Property Types"
                                        class="search-field form-control"
                                        data-default-value
                                         v-model="form.type"
                                        :class="{ 'is-invalid': form.errors.has('type') }"
                                      >
                                        <option value>Any Type</option>
                                        <option  value="single" >Single House</option>
                                        <option  value="mid" >Mid Town</option>
                                        <option  value="town" >Town Condo</option>
                                      </select>
                                    </div>
                                    <div class="col-md-4 col-sm-6 col-xs-12 form-group">
                                      <input
                                        type="text"
                                        class="form-control search-field"
                                        data-default-value
                                        value
                                        name="title"
                                        placeholder="Title"
                                        v-model="form.title"
                                        :class="{ 'is-invalid': form.errors.has('title') }"
                                      />
                                    </div>
                                    <div class="col-md-4 col-sm-6 col-xs-12 form-group">
                                      <input
                                        type="text"
                                        class="ere-location form-control search-field"
                                        data-default-value
                                        value
                                        name="address"
                                        placeholder="Address"
                                        v-model="form.address"
                                        :class="{ 'is-invalid': form.errors.has('address') }"
                                      />
                                    </div>
                                    <div class="col-md-4 col-sm-6 col-xs-12 form-group">
                                      <select
                                        name="bedroom"
                                        title="Property Bedrooms"
                                        class="search-field form-control"
                                        data-default-value
                                        v-model="form.bedroom"
                                        :class="{ 'is-invalid': form.errors.has('bedroom') }"
                                      >
                                        <option value>Any Bedrooms</option>
                                        <option  v-for="index in home.maxbedroom" :key="index" :value="index">{{index}}</option>
                                      </select>
                                    </div>
                                    <div class="col-md-4 col-sm-6 col-xs-12 form-group">
                                      <select
                                        name="bathroom"
                                        title="Property Bathrooms"
                                        class="search-field form-control"
                                        data-default-value
                                        v-model="form.bathroom"
                                        :class="{ 'is-invalid': form.errors.has('bthroom') }"
                                      >
                                        <option value>Any Bathroom</option>
                                        <option  v-for="index in home.maxbathroom" :key="index" :value="index">{{index}}</option>
                                      </select>
                                    </div>
                                      <div class="col-md-4 col-sm-6 col-xs-12 form-group">
                                      <input
                                        type="text"
                                        class="ere-property-identity form-control search-field"
                                        data-default-value
                                        value
                                        name="property_identity"
                                        placeholder="Property ID"
                                      />
                                    </div>
                                    <div class="col-md-4 col-sm-6 col-xs-12 form-group">
                                      
                                    </div>
                                    <div class="col-md-4 col-sm-6 col-xs-12 form-group">
                                    </div>
                                  
                                    <div
                                      class="col-md-12 col-sm-6 col-xs-12 form-group submit-search-form pull-right"
                                    >
                                      <button type="submit" class="ere-advanced-search-btn">
                                        <i class="fa fa-search"></i> Search
                                      </button>
                                    </div>
                                  </div>
                                  </form>
                                </div>
                              </div>
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    <div class="vc_row-full-width vc_clearfix"></div>
    <!-- FEATURED FLAT AREA START -->
    <div class="featured-flat-area pt-115 pb-80">
      <div class="container">
        <div class="featured-flat">
          <div class="row">
            <!-- flat-item -->
            <div class="col-lg-4 col-md-6 col-12">
              <div class="flat-item">
                <div class="flat-item-image">
                  <span class="for-sale">For Sale</span>
                  <a href="#">
                    <img src="vue/images/flat/1.jpg" alt />
                  </a>
                  <div class="flat-link">
                    <a href="#">More Details</a>
                  </div>
                  <ul class="flat-desc">
                    <li>
                      <img src="vue/images/icons/4.png" alt />
                      <span>450 sqft</span>
                    </li>
                    <li>
                      <img src="vue/images/icons/5.png" alt />
                      <span>5</span>
                    </li>
                    <li>
                      <img src="vue/images/icons/6.png" alt />
                      <span>3</span>
                    </li>
                  </ul>
                </div>
                <div class="flat-item-info">
                  <div class="flat-title-price">
                    <h5>
                      <a href="#">Masons de Villa</a>
                    </h5>
                    <span class="price">$52,350</span>
                  </div>
                  <p>
                    <img src="vue/images/icons/location.png" alt />568 E 1st Ave, Ney Jersey
                  </p>
                </div>
              </div>
            </div>
            <!-- flat-item -->
            <div class="col-lg-4 col-md-6 col-12">
              <div class="flat-item">
                <div class="flat-item-image">
                  <a href="#">
                    <img src="vue/images/flat/2.jpg" alt />
                  </a>
                  <div class="flat-link">
                    <a href="#">More Details</a>
                  </div>
                  <ul class="flat-desc">
                    <li>
                      <img src="vue/images/icons/4.png" alt />
                      <span>450 sqft</span>
                    </li>
                    <li>
                      <img src="vue/images/icons/5.png" alt />
                      <span>5</span>
                    </li>
                    <li>
                      <img src="vue/images/icons/6.png" alt />
                      <span>3</span>
                    </li>
                  </ul>
                </div>
                <div class="flat-item-info">
                  <div class="flat-title-price">
                    <h5>
                      <a href="#">Masons de Villa</a>
                    </h5>
                    <span class="price">$52,350</span>
                  </div>
                  <p>
                    <img src="vue/images/icons/location.png" alt />568 E 1st Ave, Ney Jersey
                  </p>
                </div>
              </div>
            </div>
            <!-- flat-item -->
            <div class="col-lg-4 col-md-6 col-12">
              <div class="flat-item">
                <div class="flat-item-image">
                  <span class="for-sale rent">For rent</span>
                  <a href="#">
                    <img src="vue/images/flat/3.jpg" alt />
                  </a>
                  <div class="flat-link">
                    <a href="#">More Details</a>
                  </div>
                  <ul class="flat-desc">
                    <li>
                      <img src="vue/images/icons/4.png" alt />
                      <span>450 sqft</span>
                    </li>
                    <li>
                      <img src="vue/images/icons/5.png" alt />
                      <span>5</span>
                    </li>
                    <li>
                      <img src="vue/images/icons/6.png" alt />
                      <span>3</span>
                    </li>
                  </ul>
                </div>
                <div class="flat-item-info">
                  <div class="flat-title-price">
                    <h5>
                      <a href="#">Masons de Villa</a>
                    </h5>
                    <span class="price">$52,350</span>
                  </div>
                  <p>
                    <img src="vue/images/icons/location.png" alt />568 E 1st Ave, Ney Jersey
                  </p>
                </div>
              </div>
            </div>
            <!-- flat-item -->
            <div class="col-lg-4 col-md-6 col-12">
              <div class="flat-item">
                <div class="flat-item-image">
                  <a href="#">
                    <img src="vue/images/flat/4.jpg" alt />
                  </a>
                  <div class="flat-link">
                    <a href="#">More Details</a>
                  </div>
                  <ul class="flat-desc">
                    <li>
                      <img src="vue/images/icons/4.png" alt />
                      <span>450 sqft</span>
                    </li>
                    <li>
                      <img src="vue/images/icons/5.png" alt />
                      <span>5</span>
                    </li>
                    <li>
                      <img src="vue/images/icons/6.png" alt />
                      <span>3</span>
                    </li>
                  </ul>
                </div>
                <div class="flat-item-info">
                  <div class="flat-title-price">
                    <h5>
                      <a href="#">Masons de Villa</a>
                    </h5>
                    <span class="price">$52,350</span>
                  </div>
                  <p>
                    <img src="vue/images/icons/location.png" alt />568 E 1st Ave, Ney Jersey
                  </p>
                </div>
              </div>
            </div>
            <!-- flat-item -->
            <div class="col-lg-4 col-md-6 col-12">
              <div class="flat-item">
                <div class="flat-item-image">
                  <span class="for-sale">For Sale</span>
                  <a href="properties-details.html">
                    <img src="vue/images/flat/5.jpg" alt />
                  </a>
                  <div class="flat-link">
                    <a href="#">More Details</a>
                  </div>
                  <ul class="flat-desc">
                    <li>
                      <img src="vue/images/icons/4.png" alt />
                      <span>450 sqft</span>
                    </li>
                    <li>
                      <img src="vue/images/icons/5.png" alt />
                      <span>5</span>
                    </li>
                    <li>
                      <img src="vue/images/icons/6.png" alt />
                      <span>3</span>
                    </li>
                  </ul>
                </div>
                <div class="flat-item-info">
                  <div class="flat-title-price">
                    <h5>
                      <a href="#">Masons de Villa</a>
                    </h5>
                    <span class="price">$52,350</span>
                  </div>
                  <p>
                    <img src="vue/images/icons/location.png" alt />568 E 1st Ave, Ney Jersey
                  </p>
                </div>
              </div>
            </div>
            <!-- flat-item -->
            <div class="col-lg-4 col-md-6 col-12">
              <div class="flat-item">
                <div class="flat-item-image">
                  <a href="#">
                    <img src="vue/images/flat/6.jpg" alt />
                  </a>
                  <div class="flat-link">
                    <a href="#">More Details</a>
                  </div>
                  <ul class="flat-desc">
                    <li>
                      <img src="vue/images/icons/4.png" alt />
                      <span>450 sqft</span>
                    </li>
                    <li>
                      <img src="vue/images/icons/5.png" alt />
                      <span>5</span>
                    </li>
                    <li>
                      <img src="vue/images/icons/6.png" alt />
                      <span>3</span>
                    </li>
                  </ul>
                </div>
                <div class="flat-item-info">
                  <div class="flat-title-price">
                    <h5>
                      <a href="#">Masons de Villa</a>
                    </h5>
                    <span class="price">$52,350</span>
                  </div>
                  <p>
                    <img src="vue/images/icons/location.png" alt />568 E 1st Ave, Ney Jersey
                  </p>
                </div>
              </div>
            </div>
            <!-- flat-item -->
            <div class="col-lg-4 col-md-6 col-12">
              <div class="flat-item">
                <div class="flat-item-image">
                  <span class="for-sale rent">For rent</span>
                  <a href="#">
                    <img src="vue/images/flat/7.jpg" alt />
                  </a>
                  <div class="flat-link">
                    <a href="#">More Details</a>
                  </div>
                  <ul class="flat-desc">
                    <li>
                      <img src="vue/images/icons/4.png" alt />
                      <span>450 sqft</span>
                    </li>
                    <li>
                      <img src="vue/images/icons/5.png" alt />
                      <span>5</span>
                    </li>
                    <li>
                      <img src="vue/images/icons/6.png" alt />
                      <span>3</span>
                    </li>
                  </ul>
                </div>
                <div class="flat-item-info">
                  <div class="flat-title-price">
                    <h5>
                      <a href="#">Masons de Villa</a>
                    </h5>
                    <span class="price">$52,350</span>
                  </div>
                  <p>
                    <img src="vue/images/icons/location.png" alt />568 E 1st Ave, Ney Jersey
                  </p>
                </div>
              </div>
            </div>
            <!-- flat-item -->
            <div class="col-lg-4 col-md-6 col-12">
              <div class="flat-item">
                <div class="flat-item-image">
                  <a href="#">
                    <img src="vue/images/flat/8.jpg" alt />
                  </a>
                  <div class="flat-link">
                    <a href="#">More Details</a>
                  </div>
                  <ul class="flat-desc">
                    <li>
                      <img src="vue/images/icons/4.png" alt />
                      <span>450 sqft</span>
                    </li>
                    <li>
                      <img src="vue/images/icons/5.png" alt />
                      <span>5</span>
                    </li>
                    <li>
                      <img src="vue/images/icons/6.png" alt />
                      <span>3</span>
                    </li>
                  </ul>
                </div>
                <div class="flat-item-info">
                  <div class="flat-title-price">
                    <h5>
                      <a href="#">Masons de Villa</a>
                    </h5>
                    <span class="price">$52,350</span>
                  </div>
                  <p>
                    <img src="vue/images/icons/location.png" alt />568 E 1st Ave, Ney Jersey
                  </p>
                </div>
              </div>
            </div>
            <!-- flat-item -->
            <div class="col-lg-4 col-12 d-none d-lg-block">
              <div class="flat-item">
                <div class="flat-item-image">
                  <span class="for-sale">For Sale</span>
                  <a href="#">
                    <img src="vue/images/flat/9.jpg" alt />
                  </a>
                  <div class="flat-link">
                    <a href="#">More Details</a>
                  </div>
                  <ul class="flat-desc">
                    <li>
                      <img src="vue/images/icons/4.png" alt />
                      <span>450 sqft</span>
                    </li>
                    <li>
                      <img src="vue/images/icons/5.png" alt />
                      <span>5</span>
                    </li>
                    <li>
                      <img src="vue/images/icons/6.png" alt />
                      <span>3</span>
                    </li>
                  </ul>
                </div>
                <div class="flat-item-info">
                  <div class="flat-title-price">
                    <h5>
                      <a href="#">Masons de Villa</a>
                    </h5>
                    <span class="price">$52,350</span>
                  </div>
                  <p>
                    <img src="vue/images/icons/location.png" alt />568 E 1st Ave, Ney Jersey
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- FEATURED FLAT AREA END -->
    <!-- MAPSEARCH AREA START -->
    <mapfilter-component/>
    <!-- NEIGHBORHOOD AREA START -->
     <neighbour-component></neighbour-component>
    <!-- NEIGHBORHOOD AREA END -->
    <!-- BRAND AREA START -->
    <div class="brand-area pb-115">
      <div class="container">
        <div class="row">
          <div class="col-12">
            <div class="section-title-2 text-center">
              <h2>AUSTIN'S DEVELOPERS</h2>
            </div>
          </div>
          <div class="col-12">
            <div class="brand-carousel">
              <!-- brand-item -->
              <div class="col">
                <div class="brand-item">
                  <img src="vue/images/1.png" alt />
                </div>
              </div>
              <!-- brand-item -->
              <div class="col">
                <div class="brand-item">
                  <img src="vue/images/2.png" alt />
                </div>
              </div>
              <!-- brand-item -->
              <div class="col">
                <div class="brand-item">
                  <img src="vue/images/3.png" alt />
                </div>
              </div>
              <!-- brand-item -->
              <div class="col">
                <div class="brand-item">
                  <img src="vue/images/4.png" alt />
                </div>
              </div>
              <!-- brand-item -->
              <div class="col">
                <div class="brand-item">
                  <img src="vue/images/5.png" alt />
                </div>
              </div>
              <!-- brand-item -->
              <div class="col">
                <div class="brand-item">
                  <img src="vue/images/1.png" alt />
                </div>
              </div>
              <!-- brand-item -->
              <div class="col">
                <div class="brand-item">
                  <img src="vue/images/4.png" alt />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- BRAND AREA END -->
    <!-- SUBSCRIBE AREA START -->
     <subscribe-component></subscribe-component>
    <!-- SUBSCRIBE AREA END -->
  </div>
</template>

<script>
    export default {
  data(){
    return{
      home:{},
      form: new Form({
        address: "",
        bedroom: "",
        bathroom: "",
        type: "",
        title: "",
        minarea: "",
        maxarea: "",
        minprice: "",
        maxprice: "",

      })
    }
  },
  methods:  {
   loadHome()
    {
      axios.get("api/home-filter-data").then(({data})=>(this.home = data)); 
    },
    HomeFilter() {
      // Submit the form via a POST request
      this.form
        .post("/api/home-house-list-filter")
        .then(({ data }) => {
          console.log(data);})
    }
  },

  
  mounted() {
    this.loadHome();
  }
};
</script>

