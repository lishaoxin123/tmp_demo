<template>
  <div class="onsumer pages-learn" @click.stop="handleCloseAll">
    <header id="header">
      <div class="bg-oil show-for-medium-up">
        <nav class="secondary-bar clearfix">
          <ul class="list-inline left">
            <li>
              <a target="_blank" href="https://support.ezlicence.com.au/hc">Support</a>
            </li>
            <li><a href="/blog">Blog</a></li>
            <li>&vert;</li>
            <li><a href="/instruct">Instruct with EzLicence</a></li>
            <li>
              <a href="/become-a-driving-instructor">Become an instructor</a>
            </li>
          </ul>
          <ul class="list-inline right">
            <li><a href="/learners/login">Learner Login</a></li>
            <li><a href="/instructors/login">Instructor Login</a></li>
          </ul>
        </nav>
      </div>
      <div class="small-padding-5">
        <nav class="top-bar expanded" data-topbar="" role="navigation">
          <ul class="title-area">
            <li class="name">
              <h2 class="small-margin-0">
                <a class="inline-block" href="/">Book Driving Lessons: Find the Best Driving Instructors Near
                  You
                </a>
              </h2>
            </li>
            <li class="toggle-topbar">
              <div title="Mobile Nav Toggle" @click="isOpen = !isOpen">
                <span class="hide">Mobile Nav Toggle</span>
                <div id="control-icon" :class="isOpen ? 'open' : ''">
                  <span></span>
                  <span></span>
                  <span></span>
                  <span></span>
                  <span></span>
                  <span></span>
                </div>
              </div>
            </li>
          </ul>
          <section class="top-bar-section" @touchmove.prevent @mousewheel.prevent>
            <ul class="nav left">
              <li>
                <a title="Driving Lessons" href="/driving-lessons">Driving Lessons</a>
              </li>
              <li>
                <a title="Test Packages" href="/driving-lessons/test-package">Test Packages</a>
              </li>
              <li>
                <a title="Gift Vouchers" href="/driving-lessons/gift-voucher">Gift Vouchers</a>
              </li>
              <li class="divider"></li>
              <li><a title="Pricing" href="/pricing">Pricing</a></li>
            </ul>
            <ul class="nav right">
              <li class="cta show-for-large-up">
                <a class="button yellow" title="Book Driving Lessons Online" href="/instructors">Book online</a>
              </li>
              <li class="has-dropdown hide-for-large-up">
                <a href="#">#</a>
                <ul :class="['dropdown', isOpen ? 'small-height-100' : '']">
                  <li>
                    <a title="Driving Lessons" href="/driving-lessons">Driving Lessons</a>
                  </li>
                  <li>
                    <a title="Test Packages" href="/driving-lessons/test-package">Test Packages</a>
                  </li>
                  <li>
                    <a title="Gift Vouchers" href="/driving-lessons/gift-voucher">Gift Vouchers</a>
                  </li>
                  <li><a title="Pricing" href="/pricing">Pricing</a></li>
                  <li class="divider"></li>
                  <li class="contact-us small-padding-top-20 small-padding-bottom-10">
                    <a class="button yellow large small-fontsize-16 caps" title="Book Driving Lessons Online"
                      href="/instructors">Book Online <i class="fas fa-angle-right fa-fw"></i></a>
                  </li>
                  <li><a href="/learners/login">Learner Login</a></li>
                  <li><a href="/instructors/login">Instructor Login</a></li>
                  <li class="divider"></li>
                  <li>
                    <a target="_blank" href="https://support.ezlicence.com.au/hc">Support</a>
                  </li>
                  <li><a href="/blog">Blog</a></li>
                  <li>
                    <a href="https://support.ezlicence.com.au/hc">Contact</a>
                  </li>
                  <li>
                    <a title="NSW - Driver Knowledge Test" href="/learners-tests/nsw">NSW - Driver Knowledge Test</a>
                  </li>
                  <li>
                    <a title="QLD - Road Rules Test" href="/learners-tests/qld">QLD - Road Rules Test</a>
                  </li>
                  <li>
                    <a title="VIC - Learner Permit Knowledge Test" href="/learners-tests/vic">VIC - Learner Permit
                      Knowledge Test</a>
                  </li>
                  <li>
                    <a title="WA - Road Rules Test" href="/learners-tests/wa">WA - Road Rules Test</a>
                  </li>
                  <li class="divider"></li>
                  <li><a href="/instruct">Instruct with EzLicence</a></li>
                  <li class="small-margin-bottom-20">
                    <a href="/become-a-driving-instructor">Become an instructor</a>
                  </li>
                </ul>
              </li>
            </ul>
          </section>
        </nav>
      </div>
      <div class="container">
        <div id="lesson_price_container"></div>
      </div>
    </header>

    <main id="main">
      <section class="section hero-patterned hero-instructor">
        <div class="container">
          <h1 class="text-white text-center small-padding-20">
            Where do you need driving lessons?
          </h1>
          <div class="cta-box well small-padding-20 shadow collapsed" id="suburb-select2-search">
            <form class="form1 simple_form new_public_search_record" id="new_public_search_record"
              novalidate="novalidate" action="/search_instructor" accept-charset="UTF-8" data-remote="true" method="get"
              data-select2-id="new_public_search_record">
              <input name="utf8" type="hidden" value="✓" />
              <div class="search-form-field" data-controller-name="pages" data-test-location="" data-select2-id="13">
                <div class="relative" data-select2-id="12">
                  <div class="button-group radius small-margin-bottom-15 select-con">
                    <input checked="checked" class="transmission-auto" id="public-search-record-transmission-auto"
                      name="public_search_record[transmission]" type="radio" value="Auto" />
                    <label class="button secondary small secondary-label"
                      for="public-search-record-transmission-auto">Auto</label>
                    <input class="transmission-manual" id="public-search-record-transmission-manual"
                      name="public_search_record[transmission]" type="radio" value="Manual" />
                    <label class="button secondary small secondary-label"
                      for="public-search-record-transmission-manual">Manual</label>
                  </div>
                  <div class="row container-inputs" data-select2-id="11">
                    <div class="small-12 columns container-input-suburb" data-select2-id="10">
                      <div class="row field-wrap select required public_search_record_suburb" data-select2-id="9">
                        <div class="small-12 columns"></div>
                        <div class="input-group small-12 columns" data-select2-id="8">
                          <select id="public-search-record-suburb"
                            class="select required select2-name-field select2-hidden-accessible">
                            <option value="" data-select2-id="1">
                              Enter your suburb
                            </option>
                          </select>
                          <span class="select2 select2-container select2-container--default select2-container--below"
                            dir="ltr" data-select2-id="5" @click.stop="handleShowSelect(1)" style="width: 1px"><span
                              class="selection"><span class="select2-selection select2-selection--single"
                                role="combobox" aria-haspopup="true" aria-expanded="false" tabindex="0"
                                aria-labelledby="select2-public-search-record-suburb-container"><span
                                  class="select2-selection__rendered" id="select2-public-search-record-suburb-container"
                                  role="textbox" aria-readonly="true"><span class="select2-selection__placeholder">Enter
                                    your suburb</span></span><span class="select2-selection__arrow"
                                  role="presentation"><b role="presentation"></b></span></span></span>
                            <span v-if="isShowSelect1"
                              class="select2-container select2-container--default select2-container--open" style="
                                position: absolute;
                                bottom: 0;
                                left: 0;
                                width: 100%;
                              "><span class="select2-dropdown select2-dropdown--below" dir="ltr"
                                style="width: 100%"><span class="select2-search select2-search--dropdown"><input
                                    class="select2-search__field" @input="onSearch" type="search" tabindex="0"
                                    autocomplete="off" autocorrect="off" autocapitalize="none" spellcheck="false"
                                    role="textbox" /></span><span class="select2-results">
                                  <ul class="select2-results__options" role="tree"
                                    id="select2-public-search-record-pricing-suburb-results" aria-expanded="true"
                                    aria-hidden="false">
                                    <li v-if="searchData.length === 0"
                                      class="select2-results__option select2-results__message">
                                      Please enter a suburb or postcode
                                    </li>
                                    <li v-for="v in searchData" :key="v"
                                      class="select2-results__option select2-results__message">
                                      {{ v }}
                                    </li>
                                  </ul>
                                </span></span></span>
                          </span>
                        </div>
                      </div>
                    </div>
                    <div class="small-12 columns container-submit">
                      <input type="submit" name="commit" value="Search"
                        class="button button yellow expand medium-padding-10 small-margin-top-15"
                        id="button-search-instructor" data-disable-with="Searching ..." data-target="search-instructor"
                        data-record="" disabled="" />
                    </div>
                  </div>
                </div>
              </div>
            </form>
            <div class="text-center" id="result"></div>
          </div>

          <div class="row small-padding-top-50 small-padding-bottom-20">
            <div class="medium-6 large-7 columns large-margin-top-30 small-margin-bottom-20">
              <img alt="Get driving lessons. Choose your driving school."
                src="https://www.ezlicence.com.au/assets/banner-homepage-hero-vehicle-3465e01fa3d7e5475a9d063682f1e3dd59633afef9753679f0a9a8e47d293bf3.png" />
            </div>
            <div class="medium-6 large-5 columns">
              <ul class="list-unstyled text-white medium-fontsize-18">
                <li class="small-margin-bottom-5">
                  <svg class="svg-inline--fa fa-check fa-w-16 fa-fw text-green" aria-hidden="true" focusable="false"
                    data-prefix="fas" data-icon="check" role="img" xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 512 512" data-fa-i2svg="">
                    <path fill="currentColor"
                      d="M173.898 439.404l-166.4-166.4c-9.997-9.997-9.997-26.206 0-36.204l36.203-36.204c9.997-9.998 26.207-9.998 36.204 0L192 312.69 432.095 72.596c9.997-9.997 26.207-9.997 36.204 0l36.203 36.204c9.997 9.997 9.997 26.206 0 36.204l-294.4 294.401c-9.998 9.997-26.207 9.997-36.204-.001z">
                    </path>
                  </svg>
                  &nbsp; Choose from 900+ verified instructors
                </li>
                <li class="small-margin-bottom-5">
                  <svg class="svg-inline--fa fa-check fa-w-16 fa-fw text-green" aria-hidden="true" focusable="false"
                    data-prefix="fas" data-icon="check" role="img" xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 512 512" data-fa-i2svg="">
                    <path fill="currentColor"
                      d="M173.898 439.404l-166.4-166.4c-9.997-9.997-9.997-26.206 0-36.204l36.203-36.204c9.997-9.998 26.207-9.998 36.204 0L192 312.69 432.095 72.596c9.997-9.997 26.207-9.997 36.204 0l36.203 36.204c9.997 9.997 9.997 26.206 0 36.204l-294.4 294.401c-9.998 9.997-26.207 9.997-36.204-.001z">
                    </path>
                  </svg>
                  &nbsp; 100,000+ new learners per year
                </li>
                <li class="small-margin-bottom-5">
                  <svg class="svg-inline--fa fa-check fa-w-16 fa-fw text-green" aria-hidden="true" focusable="false"
                    data-prefix="fas" data-icon="check" role="img" xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 512 512" data-fa-i2svg="">
                    <path fill="currentColor"
                      d="M173.898 439.404l-166.4-166.4c-9.997-9.997-9.997-26.206 0-36.204l36.203-36.204c9.997-9.998 26.207-9.998 36.204 0L192 312.69 432.095 72.596c9.997-9.997 26.207-9.997 36.204 0l36.203 36.204c9.997 9.997 9.997 26.206 0 36.204l-294.4 294.401c-9.998 9.997-26.207 9.997-36.204-.001z">
                    </path>
                  </svg>
                  &nbsp; 24/7 online booking & rescheduling
                </li>
                <li>
                  <svg class="svg-inline--fa fa-check fa-w-16 fa-fw text-green" aria-hidden="true" focusable="false"
                    data-prefix="fas" data-icon="check" role="img" xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 512 512" data-fa-i2svg="">
                    <path fill="currentColor"
                      d="M173.898 439.404l-166.4-166.4c-9.997-9.997-9.997-26.206 0-36.204l36.203-36.204c9.997-9.998 26.207-9.998 36.204 0L192 312.69 432.095 72.596c9.997-9.997 26.207-9.997 36.204 0l36.203 36.204c9.997 9.997 9.997 26.206 0 36.204l-294.4 294.401c-9.998 9.997-26.207 9.997-36.204-.001z">
                    </path>
                  </svg>
                  &nbsp; Change your instructor anytime
                </li>
              </ul>
              <hr class="border-color-gray" />
              <a target="_blank" class="inline-block"
                href="https://www.google.com/search?q=ezlicence&amp;oq=ezlicence+&amp;aqs=chrome..69i57j0i512l3j69i60l4.5588j0j7&amp;sourceid=chrome&amp;ie=UTF-8#lrd=0x6ab0cf08b2b3a8d5:0x1c7668abf7d66271,1">
                <ul class="list-unstyled text-white">
                  <li>
                    <svg class="size-30 inline-block va-m small-margin-bottom-3" xmlns="http://www.w3.org/2000/svg"
                      xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="48px" height="48px"
                      viewBox="0 0 48 48">
                      <g transform="translate(0, 0)">
                        <path
                          d="M24,11a12.932,12.932,0,0,1,8.346,3.047l6.54-6.228A21.973,21.973,0,0,0,4.293,14.236l7.373,5.683A13.016,13.016,0,0,1,24,11Z"
                          fill="#d94f3d"></path>
                        <path
                          d="M11,24a12.942,12.942,0,0,1,.666-4.081L4.293,14.236a21.935,21.935,0,0,0,0,19.528l7.373-5.683A12.942,12.942,0,0,1,11,24Z"
                          fill="#f2c042"></path>
                        <path
                          d="M45.1,20h-21v9H36a10.727,10.727,0,0,1-4.555,6.162l7.316,5.64C43.436,36.606,46.183,29.783,45.1,20Z"
                          fill="#5085ed"></path>
                        <path
                          d="M31.442,35.162A13.98,13.98,0,0,1,24,37a13.016,13.016,0,0,1-12.334-8.919L4.293,33.764A22.023,22.023,0,0,0,24,46a21.865,21.865,0,0,0,14.758-5.2Z"
                          fill="#57a75c"></path>
                      </g>
                    </svg>
                    <strong class="va-m">Google Review</strong>
                    &nbsp;&nbsp;
                    <span
                      class="small-fontsize-18 font-semi-bold va-m border-white badge-oil small-width-50px small-margin-right-15">4.9</span>
                  </li>
                  <li>
                    <span class="text-yellow inline-block va-m small-fontsize-14">
                      <svg class="svg-inline--fa fa-star fa-w-18" aria-hidden="true" focusable="false" data-prefix="fas"
                        data-icon="star" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512"
                        data-fa-i2svg="">
                        <path fill="currentColor"
                          d="M259.3 17.8L194 150.2 47.9 171.5c-26.2 3.8-36.7 36.1-17.7 54.6l105.7 103-25 145.5c-4.5 26.3 23.2 46 46.4 33.7L288 439.6l130.7 68.7c23.2 12.2 50.9-7.4 46.4-33.7l-25-145.5 105.7-103c19-18.5 8.5-50.8-17.7-54.6L382 150.2 316.7 17.8c-11.7-23.6-45.6-23.9-57.4 0z">
                        </path>
                      </svg><!-- <i class="fas fa-star" aria-hidden="true"></i> Font Awesome fontawesome.com -->
                      <svg class="svg-inline--fa fa-star fa-w-18" aria-hidden="true" focusable="false" data-prefix="fas"
                        data-icon="star" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512"
                        data-fa-i2svg="">
                        <path fill="currentColor"
                          d="M259.3 17.8L194 150.2 47.9 171.5c-26.2 3.8-36.7 36.1-17.7 54.6l105.7 103-25 145.5c-4.5 26.3 23.2 46 46.4 33.7L288 439.6l130.7 68.7c23.2 12.2 50.9-7.4 46.4-33.7l-25-145.5 105.7-103c19-18.5 8.5-50.8-17.7-54.6L382 150.2 316.7 17.8c-11.7-23.6-45.6-23.9-57.4 0z">
                        </path>
                      </svg><!-- <i class="fas fa-star" aria-hidden="true"></i> Font Awesome fontawesome.com -->
                      <svg class="svg-inline--fa fa-star fa-w-18" aria-hidden="true" focusable="false" data-prefix="fas"
                        data-icon="star" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512"
                        data-fa-i2svg="">
                        <path fill="currentColor"
                          d="M259.3 17.8L194 150.2 47.9 171.5c-26.2 3.8-36.7 36.1-17.7 54.6l105.7 103-25 145.5c-4.5 26.3 23.2 46 46.4 33.7L288 439.6l130.7 68.7c23.2 12.2 50.9-7.4 46.4-33.7l-25-145.5 105.7-103c19-18.5 8.5-50.8-17.7-54.6L382 150.2 316.7 17.8c-11.7-23.6-45.6-23.9-57.4 0z">
                        </path>
                      </svg><!-- <i class="fas fa-star" aria-hidden="true"></i> Font Awesome fontawesome.com -->
                      <svg class="svg-inline--fa fa-star fa-w-18" aria-hidden="true" focusable="false" data-prefix="fas"
                        data-icon="star" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512"
                        data-fa-i2svg="">
                        <path fill="currentColor"
                          d="M259.3 17.8L194 150.2 47.9 171.5c-26.2 3.8-36.7 36.1-17.7 54.6l105.7 103-25 145.5c-4.5 26.3 23.2 46 46.4 33.7L288 439.6l130.7 68.7c23.2 12.2 50.9-7.4 46.4-33.7l-25-145.5 105.7-103c19-18.5 8.5-50.8-17.7-54.6L382 150.2 316.7 17.8c-11.7-23.6-45.6-23.9-57.4 0z">
                        </path>
                      </svg><!-- <i class="fas fa-star" aria-hidden="true"></i> Font Awesome fontawesome.com -->
                      <svg class="svg-inline--fa fa-star fa-w-18" aria-hidden="true" focusable="false" data-prefix="fas"
                        data-icon="star" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512"
                        data-fa-i2svg="">
                        <path fill="currentColor"
                          d="M259.3 17.8L194 150.2 47.9 171.5c-26.2 3.8-36.7 36.1-17.7 54.6l105.7 103-25 145.5c-4.5 26.3 23.2 46 46.4 33.7L288 439.6l130.7 68.7c23.2 12.2 50.9-7.4 46.4-33.7l-25-145.5 105.7-103c19-18.5 8.5-50.8-17.7-54.6L382 150.2 316.7 17.8c-11.7-23.6-45.6-23.9-57.4 0z">
                        </path>
                      </svg><!-- <i class="fas fa-star" aria-hidden="true"></i> Font Awesome fontawesome.com -->
                    </span>
                    <div class="inline-block va-m small-width-120px" id="justreview-summary">
                      <section class="justreview-summary">
                        <ul class="justreview-summary__row">
                          <li class="justreview-summary__card" style="border-radius: 14px; background-color: none">
                            <div class="justreview-summary__rating" style="color: rgba(255, 255, 255, 1)">
                              4.9 / 5
                            </div>
                            <div
                              class="justreview-star-rating__stars justreview-star-rating__stars--outer justreview-star-rating__stars--centered"
                              style="
                                background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAB4AAAA8CAYAAABxVAqfAAAACXBIWXMAAAsTAAALEwEAmpwYAAAG0mlUWHRYTUw6Y29tLmFkb2JlLnhtcAAAAAAAPD94cGFja2V0IGJlZ2luPSLvu78iIGlkPSJXNU0wTXBDZWhpSHpyZVN6TlRjemtjOWQiPz4gPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iQWRvYmUgWE1QIENvcmUgNS42LWMxNDIgNzkuMTYwOTI0LCAyMDE3LzA3LzEzLTAxOjA2OjM5ICAgICAgICAiPiA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPiA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIiB4bWxuczp4bXA9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC8iIHhtbG5zOnhtcE1NPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvbW0vIiB4bWxuczpzdEV2dD0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL3NUeXBlL1Jlc291cmNlRXZlbnQjIiB4bWxuczpwaG90b3Nob3A9Imh0dHA6Ly9ucy5hZG9iZS5jb20vcGhvdG9zaG9wLzEuMC8iIHhtbG5zOmRjPSJodHRwOi8vcHVybC5vcmcvZGMvZWxlbWVudHMvMS4xLyIgeG1wOkNyZWF0b3JUb29sPSJBZG9iZSBQaG90b3Nob3AgQ0MgMjAxOCAoV2luZG93cykiIHhtcDpDcmVhdGVEYXRlPSIyMDE5LTAzLTI1VDE1OjUxOjUzKzAxOjAwIiB4bXA6TWV0YWRhdGFEYXRlPSIyMDE5LTAzLTI1VDE1OjUxOjUzKzAxOjAwIiB4bXA6TW9kaWZ5RGF0ZT0iMjAxOS0wMy0yNVQxNTo1MTo1MyswMTowMCIgeG1wTU06SW5zdGFuY2VJRD0ieG1wLmlpZDplOTFmZDU3Zi0yOTllLWFkNDItYTI4ZC1lMDllZDAyYzEyMTciIHhtcE1NOkRvY3VtZW50SUQ9ImFkb2JlOmRvY2lkOnBob3Rvc2hvcDo2OThmODEyMC0yODM1LWU5NGUtYmVmMy1lMWMzM2YyYmU2M2EiIHhtcE1NOk9yaWdpbmFsRG9jdW1lbnRJRD0ieG1wLmRpZDpiMTdlYWQwMS01ZDAzLTczNGUtOWZhOS1jYjVlMTEyM2M5OTkiIHBob3Rvc2hvcDpDb2xvck1vZGU9IjMiIHBob3Rvc2hvcDpJQ0NQcm9maWxlPSJzUkdCIElFQzYxOTY2LTIuMSIgZGM6Zm9ybWF0PSJpbWFnZS9wbmciPiA8eG1wTU06SGlzdG9yeT4gPHJkZjpTZXE+IDxyZGY6bGkgc3RFdnQ6YWN0aW9uPSJjcmVhdGVkIiBzdEV2dDppbnN0YW5jZUlEPSJ4bXAuaWlkOmIxN2VhZDAxLTVkMDMtNzM0ZS05ZmE5LWNiNWUxMTIzYzk5OSIgc3RFdnQ6d2hlbj0iMjAxOS0wMy0yNVQxNTo1MTo1MyswMTowMCIgc3RFdnQ6c29mdHdhcmVBZ2VudD0iQWRvYmUgUGhvdG9zaG9wIENDIDIwMTggKFdpbmRvd3MpIi8+IDxyZGY6bGkgc3RFdnQ6YWN0aW9uPSJzYXZlZCIgc3RFdnQ6aW5zdGFuY2VJRD0ieG1wLmlpZDplOTFmZDU3Zi0yOTllLWFkNDItYTI4ZC1lMDllZDAyYzEyMTciIHN0RXZ0OndoZW49IjIwMTktMDMtMjVUMTU6NTE6NTMrMDE6MDAiIHN0RXZ0OnNvZnR3YXJlQWdlbnQ9IkFkb2JlIFBob3Rvc2hvcCBDQyAyMDE4IChXaW5kb3dzKSIgc3RFdnQ6Y2hhbmdlZD0iLyIvPiA8L3JkZjpTZXE+IDwveG1wTU06SGlzdG9yeT4gPHBob3Rvc2hvcDpEb2N1bWVudEFuY2VzdG9ycz4gPHJkZjpCYWc+IDxyZGY6bGk+YWRvYmU6ZG9jaWQ6cGhvdG9zaG9wOjY1Zjc3MWY1LTJkZDMtOTE0ZC05MTdlLWUzYWIyNmE0NWU5ZDwvcmRmOmxpPiA8cmRmOmxpPnhtcC5kaWQ6NTdCRTZDN0E0MEU2MTFFM0JGRTM5MEI1MDY4MkRCMzc8L3JkZjpsaT4gPC9yZGY6QmFnPiA8L3Bob3Rvc2hvcDpEb2N1bWVudEFuY2VzdG9ycz4gPC9yZGY6RGVzY3JpcHRpb24+IDwvcmRmOlJERj4gPC94OnhtcG1ldGE+IDw/eHBhY2tldCBlbmQ9InIiPz44G7MUAAAFO0lEQVRYhe2YS4xURRRAT9X79PQMnxn+AkYlyCfAAiEYxUgCYvwETVzrwp1LtsSEBSsiKAE36obEhJULDTGyISYqMboxxJUSNSoayCAzDENP/96r6+JW9/TnvZ6eBmTh3KQy9eZV3VP31r236rURER6E2AdCBcLWh2PHjvU7bxlwGKgB7wNT/Uw6evRosz+oxYeAR4HNwIuDKBgEvBbYBfwB/AnsAVb8F+ADQAzUgSqwCNh/v8ErUWv/8XOt7+8BRu8n+AWgiAZVQyrAEuD5+SgK5x5CAd3DtcAOYJz2BVvgBvAE8DPwNxrl9fmAR73yMWCxB46gFhWB215hp6eq6L6/CdwBpj38FjDpny8DM3ngt4DtHuC8wsTDbgGSAW1YnXhYBCwHHvJ9iwbgZeDdPPAYMIG6LsgAzCWC7n+NWetSYA0dKde5+nOA8QtIBwB3SopaXwfO9gL/CJz2/192l/AUtTIB3gOu9AID/AKc8e+WDwhP0ZxPgFNohWuTvDz+zU+oo5Hu5gF16FbdAU6i6dUlvQrI78AJoIymUr8y7KEngGt5g+aqXONoavVTaBoSoZkx2WvQXOCHgVVoWexXymj6rLkb8ArUzfPZ4xStdj2PyrnAq/2YzouZeOUjOe8i1FMDg1fQnk4O9cBadP/Hfb/TK40czpVeQROgq656pcNoURkHPgMu+nHPAXuB9WhQzfg5q9EqmHmN7QUuAOtQaxYDN4HPga9ov9xdAL4F9gFP+QUIGlwhOcdjL3DZW7UP+N4DJ3LGTgHngUt+/JPA13lQAPO/u9AvgBfAC+AF8MDSVquTT58B58AYJE2xhbh7hjHg3OPJdOlSNLa0ZhePPE2SXu2Ltv9Cs9vb4qx7hzW4cvUssMoW4vU4+aAvaKea3DfGIC5tegADWAv1dLer1fbaQgxhCCIvAVvuHdiLS1I9XZ2ACK5WP4lzmDDQBenp9s49BwOIc4iA1JNtkiT7MBZjrIJVDgGP3XOwtwpJ0lPq+sxRJ+cD7r6BGAPWgJiGRYsQ2Sq1+k5J04NYq/veLa8Bb6C3lb9o+QjvB/yIJMkrGLNDUrcGw1ZxslKQpTiZXRggIk1PtMjH/u8k8KtfwBX0c+gT9IeabrCrVC+TpqOgUaxq/UXRtPjXGEhTBc8GWKuMAbt9a8jb6EUww2LnRjV1Ojex49kYJEkVHticC2yXrGt9aAsuWxx6HSHLgg6uwSUJUk80t/uTQ7lgEwTn7EjxVTA09zSbDKnD1WoZ3smUA+idPBssWhjOByNDL2PoDbcWV65Cks4Ffxb4smt61zDnMEHwRTBSPKhplQ03gcVVqwoPM38gqqBfFt9krrtdm/E1WjBReDEYGd6FMVO9gictldQz7VZPADuB7/LmtYNFkNQhzuFqCSLygwZPjtVhiJup4Eoz/sBovkqAn/KXmwFuNgRJ0704t7TnHlpLMjUNSQJhU90q1OI+wW3mGAyyZc7UCi1Sq5NMToENWl2+uX+wzDYjIKlsz8U2vQMmCkmnS7jb0xA1a9K2/sFmtvnzaEuXkxvAIBgnCMYbzyaw1G/eQkpliCOArQNZjEiMc9vbgM6BtRUThcdtHG2wcbTBROFxrK00anrtxgRSrkIU7ujSnwcWcbPNuSXiWN8EGoMZKpy2xcImE9gjIlISkZIJ7BFbLGwyQ/FpE0WQJtSu30BmKpsIgkKrF3PBNopmWyGesHFwBmuv2zj+MBge2mgL8WEwV6WlomnfXLWF+HBQLGwMhoc/Aq4lt6dPSbladmUtMq5cbQM/sF8E/gXONPjFi8bSvQAAAABJRU5ErkJggg==);
                              ">
                              <div class="justreview-star-rating__stars justreview-star-rating__stars--inner" style="
                                  background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAB4AAAA8CAYAAABxVAqfAAAACXBIWXMAAAsTAAALEwEAmpwYAAAG0mlUWHRYTUw6Y29tLmFkb2JlLnhtcAAAAAAAPD94cGFja2V0IGJlZ2luPSLvu78iIGlkPSJXNU0wTXBDZWhpSHpyZVN6TlRjemtjOWQiPz4gPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iQWRvYmUgWE1QIENvcmUgNS42LWMxNDIgNzkuMTYwOTI0LCAyMDE3LzA3LzEzLTAxOjA2OjM5ICAgICAgICAiPiA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPiA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIiB4bWxuczp4bXA9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC8iIHhtbG5zOnhtcE1NPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvbW0vIiB4bWxuczpzdEV2dD0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL3NUeXBlL1Jlc291cmNlRXZlbnQjIiB4bWxuczpwaG90b3Nob3A9Imh0dHA6Ly9ucy5hZG9iZS5jb20vcGhvdG9zaG9wLzEuMC8iIHhtbG5zOmRjPSJodHRwOi8vcHVybC5vcmcvZGMvZWxlbWVudHMvMS4xLyIgeG1wOkNyZWF0b3JUb29sPSJBZG9iZSBQaG90b3Nob3AgQ0MgMjAxOCAoV2luZG93cykiIHhtcDpDcmVhdGVEYXRlPSIyMDE5LTAzLTI1VDE1OjUxOjUzKzAxOjAwIiB4bXA6TWV0YWRhdGFEYXRlPSIyMDE5LTAzLTI1VDE1OjUxOjUzKzAxOjAwIiB4bXA6TW9kaWZ5RGF0ZT0iMjAxOS0wMy0yNVQxNTo1MTo1MyswMTowMCIgeG1wTU06SW5zdGFuY2VJRD0ieG1wLmlpZDplOTFmZDU3Zi0yOTllLWFkNDItYTI4ZC1lMDllZDAyYzEyMTciIHhtcE1NOkRvY3VtZW50SUQ9ImFkb2JlOmRvY2lkOnBob3Rvc2hvcDo2OThmODEyMC0yODM1LWU5NGUtYmVmMy1lMWMzM2YyYmU2M2EiIHhtcE1NOk9yaWdpbmFsRG9jdW1lbnRJRD0ieG1wLmRpZDpiMTdlYWQwMS01ZDAzLTczNGUtOWZhOS1jYjVlMTEyM2M5OTkiIHBob3Rvc2hvcDpDb2xvck1vZGU9IjMiIHBob3Rvc2hvcDpJQ0NQcm9maWxlPSJzUkdCIElFQzYxOTY2LTIuMSIgZGM6Zm9ybWF0PSJpbWFnZS9wbmciPiA8eG1wTU06SGlzdG9yeT4gPHJkZjpTZXE+IDxyZGY6bGkgc3RFdnQ6YWN0aW9uPSJjcmVhdGVkIiBzdEV2dDppbnN0YW5jZUlEPSJ4bXAuaWlkOmIxN2VhZDAxLTVkMDMtNzM0ZS05ZmE5LWNiNWUxMTIzYzk5OSIgc3RFdnQ6d2hlbj0iMjAxOS0wMy0yNVQxNTo1MTo1MyswMTowMCIgc3RFdnQ6c29mdHdhcmVBZ2VudD0iQWRvYmUgUGhvdG9zaG9wIENDIDIwMTggKFdpbmRvd3MpIi8+IDxyZGY6bGkgc3RFdnQ6YWN0aW9uPSJzYXZlZCIgc3RFdnQ6aW5zdGFuY2VJRD0ieG1wLmlpZDplOTFmZDU3Zi0yOTllLWFkNDItYTI4ZC1lMDllZDAyYzEyMTciIHN0RXZ0OndoZW49IjIwMTktMDMtMjVUMTU6NTE6NTMrMDE6MDAiIHN0RXZ0OnNvZnR3YXJlQWdlbnQ9IkFkb2JlIFBob3Rvc2hvcCBDQyAyMDE4IChXaW5kb3dzKSIgc3RFdnQ6Y2hhbmdlZD0iLyIvPiA8L3JkZjpTZXE+IDwveG1wTU06SGlzdG9yeT4gPHBob3Rvc2hvcDpEb2N1bWVudEFuY2VzdG9ycz4gPHJkZjpCYWc+IDxyZGY6bGk+YWRvYmU6ZG9jaWQ6cGhvdG9zaG9wOjY1Zjc3MWY1LTJkZDMtOTE0ZC05MTdlLWUzYWIyNmE0NWU5ZDwvcmRmOmxpPiA8cmRmOmxpPnhtcC5kaWQ6NTdCRTZDN0E0MEU2MTFFM0JGRTM5MEI1MDY4MkRCMzc8L3JkZjpsaT4gPC9yZGY6QmFnPiA8L3Bob3Rvc2hvcDpEb2N1bWVudEFuY2VzdG9ycz4gPC9yZGY6RGVzY3JpcHRpb24+IDwvcmRmOlJERj4gPC94OnhtcG1ldGE+IDw/eHBhY2tldCBlbmQ9InIiPz44G7MUAAAFO0lEQVRYhe2YS4xURRRAT9X79PQMnxn+AkYlyCfAAiEYxUgCYvwETVzrwp1LtsSEBSsiKAE36obEhJULDTGyISYqMboxxJUSNSoayCAzDENP/96r6+JW9/TnvZ6eBmTh3KQy9eZV3VP31r236rURER6E2AdCBcLWh2PHjvU7bxlwGKgB7wNT/Uw6evRosz+oxYeAR4HNwIuDKBgEvBbYBfwB/AnsAVb8F+ADQAzUgSqwCNh/v8ErUWv/8XOt7+8BRu8n+AWgiAZVQyrAEuD5+SgK5x5CAd3DtcAOYJz2BVvgBvAE8DPwNxrl9fmAR73yMWCxB46gFhWB215hp6eq6L6/CdwBpj38FjDpny8DM3ngt4DtHuC8wsTDbgGSAW1YnXhYBCwHHvJ9iwbgZeDdPPAYMIG6LsgAzCWC7n+NWetSYA0dKde5+nOA8QtIBwB3SopaXwfO9gL/CJz2/192l/AUtTIB3gOu9AID/AKc8e+WDwhP0ZxPgFNohWuTvDz+zU+oo5Hu5gF16FbdAU6i6dUlvQrI78AJoIymUr8y7KEngGt5g+aqXONoavVTaBoSoZkx2WvQXOCHgVVoWexXymj6rLkb8ArUzfPZ4xStdj2PyrnAq/2YzouZeOUjOe8i1FMDg1fQnk4O9cBadP/Hfb/TK40czpVeQROgq656pcNoURkHPgMu+nHPAXuB9WhQzfg5q9EqmHmN7QUuAOtQaxYDN4HPga9ov9xdAL4F9gFP+QUIGlwhOcdjL3DZW7UP+N4DJ3LGTgHngUt+/JPA13lQAPO/u9AvgBfAC+AF8MDSVquTT58B58AYJE2xhbh7hjHg3OPJdOlSNLa0ZhePPE2SXu2Ltv9Cs9vb4qx7hzW4cvUssMoW4vU4+aAvaKea3DfGIC5tegADWAv1dLer1fbaQgxhCCIvAVvuHdiLS1I9XZ2ACK5WP4lzmDDQBenp9s49BwOIc4iA1JNtkiT7MBZjrIJVDgGP3XOwtwpJ0lPq+sxRJ+cD7r6BGAPWgJiGRYsQ2Sq1+k5J04NYq/veLa8Bb6C3lb9o+QjvB/yIJMkrGLNDUrcGw1ZxslKQpTiZXRggIk1PtMjH/u8k8KtfwBX0c+gT9IeabrCrVC+TpqOgUaxq/UXRtPjXGEhTBc8GWKuMAbt9a8jb6EUww2LnRjV1Ojex49kYJEkVHticC2yXrGt9aAsuWxx6HSHLgg6uwSUJUk80t/uTQ7lgEwTn7EjxVTA09zSbDKnD1WoZ3smUA+idPBssWhjOByNDL2PoDbcWV65Cks4Ffxb4smt61zDnMEHwRTBSPKhplQ03gcVVqwoPM38gqqBfFt9krrtdm/E1WjBReDEYGd6FMVO9gictldQz7VZPADuB7/LmtYNFkNQhzuFqCSLygwZPjtVhiJup4Eoz/sBovkqAn/KXmwFuNgRJ0704t7TnHlpLMjUNSQJhU90q1OI+wW3mGAyyZc7UCi1Sq5NMToENWl2+uX+wzDYjIKlsz8U2vQMmCkmnS7jb0xA1a9K2/sFmtvnzaEuXkxvAIBgnCMYbzyaw1G/eQkpliCOArQNZjEiMc9vbgM6BtRUThcdtHG2wcbTBROFxrK00anrtxgRSrkIU7ujSnwcWcbPNuSXiWN8EGoMZKpy2xcImE9gjIlISkZIJ7BFbLGwyQ/FpE0WQJtSu30BmKpsIgkKrF3PBNopmWyGesHFwBmuv2zj+MBge2mgL8WEwV6WlomnfXLWF+HBQLGwMhoc/Aq4lt6dPSbladmUtMq5cbQM/sF8E/gXONPjFi8bSvQAAAABJRU5ErkJggg==);
                                  width: 98.4%;
                                "></div>
                            </div>
                            <div class="justreview-summary__count" style="color: rgba(255, 255, 255, 1)">
                              Reviews: 5034
                            </div>
                            <div class="justreview-summary__icon-wrapper">
                              <svg class="justreview-icon google" data-name="Warstwa 1"
                                xmlns="http://www.w3.org/2000/svg" viewBox="0 0 414.37 138.11">
                                <title>Google</title>
                                <path fill="#4184f2"
                                  d="M78.15,48.62c7.56,0,15.12,0,22.67,0,1.31,0,1.76.36,1.91,1.68C104,62,102.64,73.38,96.39,83.6c-7.29,11.89-18.1,19-31.83,21.42-14.38,2.51-28,.31-40.2-8C7.27,85.42-1.39,69.13.49,48.41,2.36,27.88,13.51,13,32.3,4.89,52.6-3.86,71.77-1,88.8,13.61c1,.87,1.14,1.35.1,2.33-2.81,2.65-5.51,5.41-8.2,8.18-.69.71-1.07.71-1.81,0C58.68,5.84,23.31,14.51,16.74,44.91,12,66.64,26,87.61,47.74,91,60,92.86,71.06,90.14,80.17,81.2c4.84-4.75,7-10.75,8-17.27.1-.65,0-.91-.68-.87-.38,0-.77,0-1.15,0-10.32,0-20.65,0-31,0-1.27,0-1.65-.31-1.62-1.61q.14-5.62,0-11.25c0-1.26.3-1.65,1.61-1.64C62.94,48.66,70.54,48.62,78.15,48.62Z">
                                </path>
                                <path fill="#4184f2"
                                  d="M307.38,45.55c0-1.63.05-3,0-4.45-.05-.91.25-1.21,1.19-1.19,3.91,0,7.83.07,11.74,0,1.17,0,1.29.45,1.28,1.41,0,6.2,0,12.4,0,18.6,0,14.13,0,28.27,0,42.4a41.79,41.79,0,0,1-2.62,15c-4.3,11.24-12.71,17.24-24.46,18.81-7.76,1-15.17-.08-22-4.18a33.58,33.58,0,0,1-12.86-14.16c-.54-1.08-.39-1.53.78-2q5.23-2,10.36-4.32c1.07-.47,1.42-.2,1.9.76,4.4,8.71,12.82,12.57,22.19,10.13,6.84-1.78,10.51-6.55,11.94-13.26a46.19,46.19,0,0,0,.57-9.9c0-.3.11-.69-.29-.84s-.5.15-.66.34c-7.53,8.51-21.57,9.18-32.1,3.49-12-6.49-19.44-20.24-17.88-33.36,1.76-14.87,11.45-26.61,25.13-30,9.41-2.34,18-.81,25.1,6.38A3.7,3.7,0,0,0,307.38,45.55Zm-36.07,25c0,5.59.91,9.42,3.07,12.85,3.86,6.13,9.39,9.43,16.72,9.11,6.93-.3,11.92-3.9,14.9-10a22.79,22.79,0,0,0-.74-22.32,17.14,17.14,0,0,0-24-6.38A19.75,19.75,0,0,0,271.31,70.5Z">
                                </path>
                                <path fill="#f9ba05"
                                  d="M251,71.94a33.63,33.63,0,0,1-34.21,34c-19.3-.07-34.16-14.92-34.13-34.08s14.94-34,34.21-34S251,52.73,251,71.94ZM216.89,92.51a17.66,17.66,0,0,0,9.44-2.63c7.61-4.59,11.2-13.79,9.09-23.28-3.11-14-19.22-20-30.2-11.23-6.6,5.29-8.49,12.49-7.26,20.62A19.28,19.28,0,0,0,216.89,92.51Z">
                                </path>
                                <path fill="#e84235"
                                  d="M143.12,105.94c-19.25,0-34.19-14.89-34.17-34s14.86-34,34.18-34,34.17,14.79,34.17,34S162.37,105.94,143.12,105.94Zm0-13.43a18.24,18.24,0,0,0,9.73-2.77c7.47-4.63,11-14.09,8.78-23.42-3.36-13.94-19.53-19.74-30.38-10.77-6.29,5.21-8.15,12.19-7.09,20.08A19.36,19.36,0,0,0,143.17,92.51Z">
                                </path>
                                <path fill="#e84234"
                                  d="M385,105.92c-20.58,0-35.85-17.26-33.58-37.74,1.17-10.5,5.53-19.13,14.43-25.1,12.57-8.44,33.61-8.45,44.58,11.9,1.25,2.3,2.11,4.76,3.15,7.15.43,1,.24,1.38-.76,1.79q-13.54,5.55-27.07,11.19c-5.21,2.16-10.4,4.37-15.65,6.45-1.3.52-1.46.92-.76,2.16,6.34,11.22,21.37,10.9,28.62,3.9a21.32,21.32,0,0,0,3.12-3.53c.57-.89,1-.82,1.8-.28,3.05,2.1,6.11,4.16,9.23,6.14,1.08.68,1.19,1.15.41,2.21A33.84,33.84,0,0,1,385,105.92ZM385,51c-10.46-.11-19.1,8.78-18.9,18.61,0,1.47.73.93,1.44.64,9.15-3.81,18.3-7.64,27.49-11.38,1.5-.61,1.44-1.21.65-2.32C392.85,52.64,388.82,51.29,385,51Z">
                                </path>
                                <path fill="#33a652"
                                  d="M330.38,53.93c0-16,0-31.95,0-47.93,0-1.57.39-2,2-2,3.75.12,7.5.07,11.25,0,1.15,0,1.46.36,1.46,1.48q0,48.42,0,96.83c0,1.22-.35,1.57-1.56,1.54-3.81-.07-7.61-.08-11.41,0-1.37,0-1.72-.38-1.72-1.73C330.4,86.09,330.38,70,330.38,53.93Z">
                                </path>
                              </svg>
                            </div>
                          </li>
                        </ul>
                      </section>
                    </div>
                  </li>
                </ul>
              </a>
            </div>
          </div>
        </div>
      </section>
      <section class="section small bg-yellow" id="pricing">
        <div class="container">
          <div class="row">
            <div class="large-6 columns cta-text">
              <div class="media small-margin-top-5">
                <div class="media-left small-padding-right-20">
                  <svg class="dark-gray small-margin-top-5 small-width-60px medium-width-70px"
                    xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
                    width="64px" height="64px" viewBox="0 0 64 64" stroke-width="3">
                    <g stroke-width="3" transform="translate(0.5, 0.5)">
                      <circle fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square"
                        stroke-miterlimit="10" cx="32" cy="32" r="30" stroke-linejoin="miter"></circle>
                      <line data-color="color-2" fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square"
                        stroke-miterlimit="10" x1="32" y1="12" x2="32" y2="52" stroke-linejoin="miter"></line>
                      <path data-color="color-2" fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square"
                        stroke-miterlimit="10"
                        d="M42,20 c-4.545-2.361-19.148-4.145-19.148,3.983c0,9.731,18.182,6.296,18.182,14.882s-11.818,7.942-20,5.151"
                        stroke-linejoin="miter"></path>
                    </g>
                  </svg>
                </div>
                <div class="media-body">
                  <h3 class="small-fontsize-30 font-condensed small-margin-bottom-0 medium-margin-bottom-10">
                    Driving lesson<br />pricing & packages
                  </h3>
                  <h3 class="font-light large-margin-bottom-0 show-for-large-up">
                    Buy more lessons & get more discount
                  </h3>
                </div>
              </div>
            </div>
            <div class="large-6 columns" id="pricing-search-form">
              <form class="simple_form new_public_search_record" id="new_public_search_record" novalidate="novalidate"
                action="/search_instructor" accept-charset="UTF-8" data-remote="true" method="get">
                <input name="utf8" type="hidden" value="✓" /><input type="hidden" name="lesson_amount"
                  id="lesson_amount" />
                <div class="search-form-field" data-controller-name="pages" data-test-location="">
                  <input value="public-search-pricing-result" type="hidden"
                    name="public_search_record[result_field_name]" id="public_search_record_result_field_name" />
                  <input type="hidden" name="public_search_record[public_search_type]"
                    id="public_search_record_public_search_type" />
                  <input value="learn_page_pricing_search" type="hidden"
                    name="public_search_record[event_tracking_type]" id="public_search_record_event_tracking_type" />
                  <div class="relative">
                    <h4 class="small-margin-top-15 medium-margin-top-0 small-margin-bottom-15">
                      <svg class="svg-inline--fa fa-search fa-w-16 fa-fw" aria-hidden="true" focusable="false"
                        data-prefix="fas" data-icon="search" role="img" xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 512 512" data-fa-i2svg="">
                        <path fill="currentColor"
                          d="M505 442.7L405.3 343c-4.5-4.5-10.6-7-17-7H372c27.6-35.3 44-79.7 44-128C416 93.1 322.9 0 208 0S0 93.1 0 208s93.1 208 208 208c48.3 0 92.7-16.4 128-44v16.3c0 6.4 2.5 12.5 7 17l99.7 99.7c9.4 9.4 24.6 9.4 33.9 0l28.3-28.3c9.4-9.4 9.4-24.6.1-34zM208 336c-70.7 0-128-57.2-128-128 0-70.7 57.2-128 128-128 70.7 0 128 57.2 128 128 0 70.7-57.2 128-128 128z">
                        </path>
                      </svg><!-- <i class="fas fa-search fa-fw" aria-hidden="true"></i> Font Awesome fontawesome.com -->
                      Check pricing for your suburb
                    </h4>
                    <div class="button-group radius small-margin-bottom-15">
                      <input checked="checked" class="transmission-auto"
                        id="public-search-record-pricing-transmission-auto" name="public_search_record[transmission]"
                        type="radio" value="Auto" />
                      <label class="button secondary small secondary-label"
                        for="public-search-record-pricing-transmission-auto">Auto</label>
                      <input class="transmission-manual" id="public-search-record-pricing-transmission-manual"
                        name="public_search_record[transmission]" type="radio" value="Manual" />
                      <label class="button secondary small secondary-label"
                        for="public-search-record-pricing-transmission-manual">Manual</label>
                    </div>
                    <div class="media container-inputs">
                      <div class="media-body container-input-suburb">
                        <div class="row field-wrap select required public_search_record_suburb">
                          <div class="small-12 columns"></div>
                          <div class="input-group small-12 columns">
                            <select include_blank="false" id="public-search-record-pricing-suburb"
                              class="select required select2-name-field select2-hidden-accessible" required="required"
                              aria-required="true" name="public_search_record[suburb]"
                              data-select2-id="public-search-record-pricing-suburb" tabindex="-1" aria-hidden="true">
                              <option value="" data-select2-id="3">
                                Enter your suburb
                              </option>
                            </select><span class="select2 select2-container select2-container--default"
                              style="width: 1px" @click.stop="handleShowSelect(2)"><span class="selection"><span
                                  class="select2-selection select2-selection--single" role="combobox"
                                  aria-haspopup="true" aria-expanded="false" tabindex="0"
                                  aria-labelledby="select2-public-search-record-pricing-suburb-container"><span
                                    class="select2-selection__rendered"
                                    id="select2-public-search-record-pricing-suburb-container" role="textbox"
                                    aria-readonly="true"><span class="select2-selection__placeholder">Enter your
                                      suburb</span></span><span class="select2-selection__arrow" role="presentation"><b
                                      role="presentation"></b></span></span></span>
                              <span v-if="isShowSelect2"
                                class="select2-container select2-container--default select2-container--open" style="
                                  position: absolute;
                                  bottom: 0;
                                  left: 0;
                                  width: 100%;
                                "><span class="select2-dropdown select2-dropdown--below" dir="ltr"
                                  style="width: 100%"><span class="select2-search select2-search--dropdown"><input
                                      class="select2-search__field" type="search" @input="onSearch" tabindex="0"
                                      autocomplete="off" autocorrect="off" autocapitalize="none" spellcheck="false"
                                      role="textbox" /></span><span class="select2-results">
                                    <ul class="select2-results__options" role="tree"
                                      id="select2-public-search-record-pricing-suburb-results" aria-expanded="true"
                                      aria-hidden="false">
                                      <li v-if="searchData.length === 0"
                                        class="select2-results__option select2-results__message">
                                        Please enter a suburb or postcode
                                      </li>
                                      <li v-for="v in searchData" :key="v"
                                        class="select2-results__option select2-results__message">
                                        {{ v }}
                                      </li>
                                    </ul>
                                  </span></span></span>
                            </span>
                          </div>
                        </div>
                      </div>
                      <div class="media-right container-submit">
                        <input type="submit" name="commit" value="Search"
                          class="button button oil small-padding-10 last" id="button-search-pricing-instructor"
                          data-disable-with="Searching ..." data-target="search-instructor" data-record=""
                          disabled="" />
                      </div>
                    </div>
                  </div>
                </div>

                <div class="text-center" id="public-search-pricing-result"></div>
              </form>
            </div>
          </div>
        </div>
      </section>

      <div class="bg-oil small-padding-15">
        <div class="container small-margin-top-5">
          <div class="media media-middle">
            <div class="media-left">
              <svg class="size-70 white medium-margin-right-20" xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="64px" height="64px"
                viewBox="0 0 64 64" stroke-width="3">
                <g stroke-width="3" transform="translate(0.5, 0.5)">
                  <path fill="none" stroke="#444444" stroke-width="3" stroke-linecap="round" stroke-miterlimit="10"
                    d="M41.999,41.374 C38.277,40.577,33.636,40,28,40c-11.14,0-18.494,2.331-22.453,4.087C3.379,45.048,2,47.196,2,49.567V60h28"
                    stroke-linejoin="round"></path>
                  <path fill="none" stroke="#444444" stroke-width="3" stroke-linecap="round" stroke-miterlimit="10"
                    d="M14,16 c0-7.732,6.268-14,14-14s14,6.268,14,14s-6.268,16-14,16S14,23.732,14,16z"
                    stroke-linejoin="round"></path>
                  <polyline data-color="color-2" fill="none" stroke="#444444" stroke-width="3" stroke-linecap="round"
                    stroke-miterlimit="10" points=" 40,54 46,60 60,46 " stroke-linejoin="round"></polyline>
                </g>
              </svg>
            </div>
            <div class="media-body">
              <h3 class="small-fontsize-30 text-white small-margin-top-10 small-margin-bottom-5">
                Driving lesson guarantee!
              </h3>
              <h3 class="text-secondary small-fontsize-18 font-normal font-semi-condensed">
                We will fulfill your driving lesson booking or you won’t be
                charged
              </h3>
            </div>
          </div>
        </div>
      </div>

      <section class="bg-white section">
        <div class="container">
          <div class="row">
            <div class="small-12 columns text-center">
              <h3 class="small-fontsize-30 small-margin-0">
                How EzLicence works
              </h3>
              <h3 class="lead small-fontsize-22 medium-margin-bottom-20">
                Simple & flexible booking system
              </h3>
            </div>
            <div class="small-12 columns">
              <div class="media media-middle collapse-small collapse-medium">
                <div class="media-left">
                  <div class="text-center video-player large-width-400px" id="video-ezlicence">
                    <video ref="videoRef" className="video-js ytb-video" />
                  </div>
                  <div></div>
                </div>
                <div class="media-body large-padding-left-30 small-padding-top-20">
                  <div class="media">
                    <div class="media-left small-padding-right-15">
                      <span class="badge-yellow small-fontsize-24 va-b small-width-30px">1</span>
                    </div>
                    <div class="media-body">
                      <h3 class="small-margin-0">
                        Find Your Driving Instructors
                      </h3>
                      <p>
                        Choose from a wide variety of instructors in your area.
                        Check rating & reviews from real learners.
                      </p>
                    </div>
                  </div>
                  <div class="media">
                    <div class="media-left small-padding-right-15">
                      <span class="badge-yellow small-fontsize-24 va-b small-width-30px">2</span>
                    </div>
                    <div class="media-body">
                      <h3 class="small-margin-0">Book Your Driving Lessons</h3>
                      <p>
                        Book online with instant confirmation. Easily manage
                        your lesson schedule via our online dashboard.
                      </p>
                    </div>
                  </div>
                  <div class="media">
                    <div class="media-left small-padding-right-15">
                      <span class="badge-yellow small-fontsize-24 va-b small-width-30px">3</span>
                    </div>
                    <div class="media-body">
                      <h3 class="small-margin-0">Learn to Drive</h3>
                      <p>
                        Your instructor picks you up from your chosen address
                        and you're on your way 🚗
                      </p>
                    </div>
                  </div>
                </div>
              </div>
              <div class="text-center small-margin-top-30">
                <a class="button oil" href="/driving-lessons">Start learning to drive now
                  <i class="fas fa-angle-right fr"></i></a>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section class="bg-gray-lighter section">
        <div class="container">
          <div class="row">
            <div class="small-12 columns text-center">
              <h4 class="small-fontsize-30 small-margin-bottom-10">
                What our learners say
              </h4>
              <h4 class="lead small-fontsize-22 small-margin-bottom-30">
                Choose a driving instructor you can trust
              </h4>
            </div>
            <div class="small-12 columns">
              <div class="owl-carousel owl-carousel-div owl-loaded owl-drag">
                <div class="owl-stage-outer" @touchstart="onTouchStart" @touchend="onTouchEnd" @mousedown="onMousedown"
                  @mouseup="onMouseup">
                  <div class="owl-stage" :style="getOwlStyle">
                    <div v-for="(v, itemIdx) in list" :key="v" class="owl-item" style="width: auto; margin-right: 10px">
                      <!-- class="owl-item active" -->
                      <div class="item small-margin-bottom-20">
                        <div class="border-border small-width-300px small-padding-20 bg-white">
                          <div class="media media-middle small-margin-bottom-20">
                            <div class="media-left">
                              <img style="width: 50px; height: 50px; opacity: 1"
                                class="img-circle img-featured owl-lazy" loading="lazy"
                                src="https://assets.ezlicence.com.au/instructor_users/user_images/000/000/191/xs/Adriana_Image-38620ede6c913de00c27e1eb92d22afa.jpg" />
                            </div>
                            <div class="media-body">
                              <strong class="block">Adriana{{ itemIdx }}</strong>
                              <svg class="svg-inline--fa fa-star fa-w-18 text-yellow" aria-hidden="true"
                                focusable="false" data-prefix="fas" data-icon="star" role="img"
                                xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512" data-fa-i2svg="">
                                <path fill="currentColor"
                                  d="M259.3 17.8L194 150.2 47.9 171.5c-26.2 3.8-36.7 36.1-17.7 54.6l105.7 103-25 145.5c-4.5 26.3 23.2 46 46.4 33.7L288 439.6l130.7 68.7c23.2 12.2 50.9-7.4 46.4-33.7l-25-145.5 105.7-103c19-18.5 8.5-50.8-17.7-54.6L382 150.2 316.7 17.8c-11.7-23.6-45.6-23.9-57.4 0z">
                                </path>
                              </svg><!-- <i class="fas fa-star text-yellow" aria-hidden="true"></i> Font Awesome fontawesome.com -->
                              <svg class="svg-inline--fa fa-star fa-w-18 text-yellow" aria-hidden="true"
                                focusable="false" data-prefix="fas" data-icon="star" role="img"
                                xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512" data-fa-i2svg="">
                                <path fill="currentColor"
                                  d="M259.3 17.8L194 150.2 47.9 171.5c-26.2 3.8-36.7 36.1-17.7 54.6l105.7 103-25 145.5c-4.5 26.3 23.2 46 46.4 33.7L288 439.6l130.7 68.7c23.2 12.2 50.9-7.4 46.4-33.7l-25-145.5 105.7-103c19-18.5 8.5-50.8-17.7-54.6L382 150.2 316.7 17.8c-11.7-23.6-45.6-23.9-57.4 0z">
                                </path>
                              </svg><!-- <i class="fas fa-star text-yellow" aria-hidden="true"></i> Font Awesome fontawesome.com -->
                              <svg class="svg-inline--fa fa-star fa-w-18 text-yellow" aria-hidden="true"
                                focusable="false" data-prefix="fas" data-icon="star" role="img"
                                xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512" data-fa-i2svg="">
                                <path fill="currentColor"
                                  d="M259.3 17.8L194 150.2 47.9 171.5c-26.2 3.8-36.7 36.1-17.7 54.6l105.7 103-25 145.5c-4.5 26.3 23.2 46 46.4 33.7L288 439.6l130.7 68.7c23.2 12.2 50.9-7.4 46.4-33.7l-25-145.5 105.7-103c19-18.5 8.5-50.8-17.7-54.6L382 150.2 316.7 17.8c-11.7-23.6-45.6-23.9-57.4 0z">
                                </path>
                              </svg><!-- <i class="fas fa-star text-yellow" aria-hidden="true"></i> Font Awesome fontawesome.com -->
                              <svg class="svg-inline--fa fa-star fa-w-18 text-yellow" aria-hidden="true"
                                focusable="false" data-prefix="fas" data-icon="star" role="img"
                                xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512" data-fa-i2svg="">
                                <path fill="currentColor"
                                  d="M259.3 17.8L194 150.2 47.9 171.5c-26.2 3.8-36.7 36.1-17.7 54.6l105.7 103-25 145.5c-4.5 26.3 23.2 46 46.4 33.7L288 439.6l130.7 68.7c23.2 12.2 50.9-7.4 46.4-33.7l-25-145.5 105.7-103c19-18.5 8.5-50.8-17.7-54.6L382 150.2 316.7 17.8c-11.7-23.6-45.6-23.9-57.4 0z">
                                </path>
                              </svg><!-- <i class="fas fa-star text-yellow" aria-hidden="true"></i> Font Awesome fontawesome.com -->
                              <svg class="svg-inline--fa fa-star fa-w-18 text-yellow" aria-hidden="true"
                                focusable="false" data-prefix="fas" data-icon="star" role="img"
                                xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512" data-fa-i2svg="">
                                <path fill="currentColor"
                                  d="M259.3 17.8L194 150.2 47.9 171.5c-26.2 3.8-36.7 36.1-17.7 54.6l105.7 103-25 145.5c-4.5 26.3 23.2 46 46.4 33.7L288 439.6l130.7 68.7c23.2 12.2 50.9-7.4 46.4-33.7l-25-145.5 105.7-103c19-18.5 8.5-50.8-17.7-54.6L382 150.2 316.7 17.8c-11.7-23.6-45.6-23.9-57.4 0z">
                                </path>
                              </svg><!-- <i class="fas fa-star text-yellow" aria-hidden="true"></i> Font Awesome fontawesome.com -->
                            </div>
                          </div>
                          <p class="ellipsis line-11 small-fontsize-14"
                            title="Adriana is a really good instructor!She knows everything and she always make sure to correct every detail before the test.Apart from that, she is very sweet and calm. I was blessed to find her.Thanks Adriana!!!!">
                            Adriana is a really good instructor! She knows
                            everything and she always make sure to correct every
                            detail before the test. Apart from that, she is very
                            sweet and calm. I was blessed to find her. Thanks
                            Adriana!!!!
                          </p>
                          <i class="font-bold block">Livia</i>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
                <div class="owl-nav disabled">
                  <div class="owl-prev">prev</div>
                  <div class="owl-next">next</div>
                </div>
                <div class="owl-dots">
                  <div v-for="(v, dotIdx) in list" :key="v" @click="handleClickDot(dotIdx)"
                    :class="['owl-dot', setDotActClass(dotIdx)]">
                    <span></span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section class="bg-gray-lighter medium-padding-10 section">
        <div class="container text-center">
          <div class="row">
            <div class="medium-6 medium-centered large-uncentered columns text-center small-margin-top-20">
              <img alt="Driving lessons. Learning to drive. Book driving test." loading="lazy" height="500" width="400"
                style="width: 100%"
                src="https://www.ezlicence.com.au/assets/image-home-gift-cards-stack.mobile-aa61ad906178d6b3feaa5b295c3377e6a02b25c14d1020d99c2024f0da82097a.png" />
            </div>
            <div class="large-6 columns">
              <h3 class="medium-margin-top-60">The gift of life long skills</h3>
              <div class="row">
                <div class="small-6 columns">
                  <svg class="size-50 oil lp-center" xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="64px" height="64px"
                    viewBox="0 0 64 64" stroke-width="3">
                    <g stroke-width="3" transform="translate(0.5, 0.5)">
                      <line fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square" stroke-miterlimit="10"
                        x1="6" y1="47" x2="28" y2="47" stroke-linejoin="miter"></line>
                      <line fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square" stroke-miterlimit="10"
                        x1="6" y1="12" x2="46" y2="12" stroke-linejoin="miter"></line>
                      <path data-cap="butt" fill="none" stroke="#444444" stroke-width="3" stroke-miterlimit="10"
                        d="M42,62H10c-2.2,0-4-1.8-4-4V6 c0-2.2,1.8-4,4-4h32c2.2,0,4,1.8,4,4v28.101"
                        stroke-linejoin="miter" stroke-linecap="butt"></path>
                      <polyline data-cap="butt" data-color="color-2" fill="none" stroke="#444444" stroke-width="3"
                        stroke-miterlimit="10" points="28.096,36 14,36 14,24 28.391,24 " stroke-linejoin="miter"
                        stroke-linecap="butt"></polyline>
                      <path data-color="color-2" fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square"
                        stroke-miterlimit="10"
                        d="M51,59 L27.05,34.95c-2.734-2.734-2.734-7.166,0-9.899l0,0c2.734-2.734,7.166-2.734,9.899,0L61,49"
                        stroke-linejoin="miter"></path>
                      <line data-color="color-2" fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square"
                        stroke-miterlimit="10" x1="33.284" y1="33.284" x2="35.284" y2="31.284" stroke-linejoin="miter">
                      </line>
                    </g>
                  </svg>
                  <h4 class="small-margin-5">Pick a voucher</h4>
                  <p>Choose the number of lessons that you want to purchase</p>
                </div>
                <div class="small-6 columns">
                  <svg class="size-50 oil lp-center" xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="64px" height="64px"
                    viewBox="0 0 64 64" stroke-width="3">
                    <g stroke-width="3" transform="translate(0.5, 0.5)">
                      <polyline fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square"
                        stroke-miterlimit="10" points="56,24 56,60 8,60 8,24 " stroke-linejoin="miter"></polyline>
                      <rect x="2" y="14" fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square"
                        stroke-miterlimit="10" width="60" height="10" stroke-linejoin="miter"></rect>
                      <path data-color="color-2" fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square"
                        stroke-miterlimit="10"
                        d="M14,8 c0-3.314,2.686-6,6-6c8.875,0,12,12,12,12s-8.686,0-12,0S14,11.314,14,8z"
                        stroke-linejoin="miter"></path>
                      <path data-color="color-2" fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square"
                        stroke-miterlimit="10"
                        d="M50,8 c0-3.314-2.686-6-6-6c-8.875,0-12,12-12,12s8.686,0,12,0S50,11.314,50,8z"
                        stroke-linejoin="miter"></path>
                      <polyline data-color="color-2" fill="none" stroke="#444444" stroke-width="3"
                        stroke-linecap="square" stroke-miterlimit="10" points=" 38,14 38,60 26,60 26,14 "
                        stroke-linejoin="miter"></polyline>
                    </g>
                  </svg>
                  <h4 class="small-margin-5">Send your gift</h4>
                  <p>Enter the recipients info and the gift is on the way.</p>
                </div>
              </div>
              <div class="small-padding-10"></div>
              <a class="button yellow" href="/driving-lessons/gift-voucher">Buy a Gift Voucher <i
                  class="fas fa-angle-right fr"></i></a>
            </div>
          </div>
        </div>
      </section>

      <section class="bg-white section">
        <div class="container">
          <div class="row">
            <div class="small-12 columns text-center">
              <h4 class="small-fontsize-30 small-margin-0">
                Ready for driving lessons?
              </h4>
              <h4 class="lead small-fontsize-22 medium-margin-bottom-30">
                EzLicence connects learner drivers with the best driving schools
              </h4>
            </div>
          </div>
          <div class="row" data-equalizer>
            <div class="medium-6 columns">
              <div class="media" data-equalizer-watch>
                <div class="media-left small-padding-right-15">
                  <svg class="size-40 yellow" xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="64px" height="64px"
                    viewBox="0 0 64 64" stroke-width="3">
                    <g stroke-width="3" transform="translate(0.5, 0.5)">
                      <path d="M32,24c-5,0-9,4-14,4H10.363" fill="none" stroke="#444444" stroke-miterlimit="10"
                        stroke-width="3" data-cap="butt" data-color="color-2" stroke-linecap="butt"
                        stroke-linejoin="miter"></path>
                      <path d="M32,40c-5,0-9-4-14-4H10.363" fill="none" stroke="#444444" stroke-miterlimit="10"
                        stroke-width="3" data-cap="butt" data-color="color-2" stroke-linecap="butt"
                        stroke-linejoin="miter"></path>
                      <path d="M24,32c0,5,4,9,4,14v7.637" fill="none" stroke="#444444" stroke-miterlimit="10"
                        stroke-width="3" data-cap="butt" data-color="color-2" stroke-linecap="butt"
                        stroke-linejoin="miter"></path>
                      <path d="M40,32c0,5-4,9-4,14v7.637" fill="none" stroke="#444444" stroke-miterlimit="10"
                        stroke-width="3" data-cap="butt" data-color="color-2" stroke-linecap="butt"
                        stroke-linejoin="miter"></path>
                      <path d="M32,24c5,0,9,4,14,4h7.637" fill="none" stroke="#444444" stroke-miterlimit="10"
                        stroke-width="3" data-cap="butt" data-color="color-2" stroke-linecap="butt"
                        stroke-linejoin="miter"></path>
                      <path d="M32,40c5,0,9-4,14-4h7.637" fill="none" stroke="#444444" stroke-miterlimit="10"
                        stroke-width="3" data-cap="butt" data-color="color-2" stroke-linecap="butt"
                        stroke-linejoin="miter"></path>
                      <circle cx="32" cy="32" r="30" fill="none" stroke="#444444" stroke-linecap="square"
                        stroke-miterlimit="10" stroke-width="3" stroke-linejoin="miter"></circle>
                      <circle cx="32" cy="32" r="22" fill="none" stroke="#444444" stroke-linecap="square"
                        stroke-miterlimit="10" stroke-width="3" stroke-linejoin="miter"></circle>
                      <circle cx="32" cy="32" r="8" fill="none" stroke="#444444" stroke-linecap="square"
                        stroke-miterlimit="10" stroke-width="3" stroke-linejoin="miter"></circle>
                    </g>
                  </svg>
                </div>
                <div class="media-body">
                  <h4 class="small-margin-0">Learner drivers</h4>
                  <p>
                    Gain experience, prepare for your driving test and complete
                    log book hours.
                  </p>
                </div>
              </div>
              <div class="media" data-equalizer-watch>
                <div class="media-left small-padding-right-15">
                  <svg class="size-40 yellow" xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="64px" height="64px"
                    viewBox="0 0 64 64" stroke-width="3">
                    <g stroke-width="3" transform="translate(0.5, 0.5)">
                      <path data-color="color-2" fill="none" stroke="#444444" stroke-width="3" stroke-miterlimit="10"
                        d="M14.804,7.414 c1.892,1.399,3.345,4.956,3.345,4.956s1.634,1.135,2.146,2.584c0.511,1.449,0.028,3.417,0.028,3.417s1.449,4.253,0.767,5.447 c-0.682,1.193-3.58,1.96-3.58,1.96s-1.193,2.216-3.665,2.642c-1.619,0.17-3.239,1.278-3.239,3.58s2.301,6.051,2.301,6.051 s2.386,1.167,2.727,2.02s0.457,2.838,0.457,2.838s2.27,4.006,0.992,6.307c-0.408,0.734-2.301,1.278-2.301,1.278l-2.654,3.982"
                        stroke-linejoin="miter" stroke-linecap="square"></path>
                      <path data-color="color-2" fill="none" stroke="#444444" stroke-width="3" stroke-miterlimit="10"
                        d="M55.676,13.574 c-2.895,1.388-7.959,2.546-7.959,2.546s-3.7,4.119-6.129,3.778c-2.429-0.341-4.901-3.068-4.901-3.068s0.17-5.028-0.597-5.284 c-0.767-0.256-2.812,1.108-4.091,0.085c-1.278-1.023-0.541-3.905-0.541-3.905s-2.783-0.867-3.124-1.805 c-0.341-0.938,1.013-3.025,1.271-3.826"
                        stroke-linejoin="miter" stroke-linecap="square"></path>
                      <path data-color="color-2" fill="none" stroke="#444444" stroke-width="3" stroke-miterlimit="10"
                        d="M53.989,33.96 c0.682,1.619-1.28,5.755-2.898,6.562c-2.142,1.069-3.603,2.411-4.199,3.349c-0.597,0.938-1.381,4.806-3.342,5.573 c-1.96,0.767-6.607,5.141-9.078,4.459C32,53.222,32,47.341,33.705,44.699c1.018-1.577-0.17-5.028-0.256-6.222 c-0.085-1.193-3.665-3.409-3.665-4.602c0-1.875,4.091-6.818,4.091-6.818s3.352-1.108,4.375-0.852s2.955,1.449,2.955,1.449 s3.835,0.341,5.284,1.108l1.96,1.79C48.449,30.551,53.307,32.341,53.989,33.96z"
                        stroke-linejoin="miter" stroke-linecap="square"></path>
                      <circle fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square"
                        stroke-miterlimit="10" cx="32" cy="32" r="30" stroke-linejoin="miter"></circle>
                    </g>
                  </svg>
                </div>
                <div class="media-body">
                  <h4 class="small-margin-0">International conversions</h4>
                  <p>
                    Convert your licence or simply build your confidence on
                    Australian roads.
                  </p>
                </div>
              </div>
            </div>
            <div class="medium-6 columns">
              <div class="media" data-equalizer-watch>
                <div class="media-left small-padding-right-15">
                  <svg class="size-40 yellow" xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="64px" height="64px"
                    viewBox="0 0 64 64" stroke-width="3">
                    <g stroke-width="3" transform="translate(0.5, 0.5)">
                      <line data-cap="butt" fill="none" stroke="#444444" stroke-width="3" stroke-miterlimit="10" x1="32"
                        y1="28" x2="41" y2="19" stroke-linecap="butt" stroke-linejoin="miter"></line>
                      <path data-cap="butt" fill="none" stroke="#444444" stroke-width="3" stroke-miterlimit="10"
                        d="M57,28L52.531,8.335 C52.22,6.969,51.006,6,49.605,6H14.395c-1.401,0-2.615,0.969-2.925,2.335L7,28"
                        stroke-linecap="butt" stroke-linejoin="miter"></path>
                      <polyline data-color="color-2" fill="none" stroke="#444444" stroke-width="3"
                        stroke-linecap="square" stroke-miterlimit="10" points=" 18,50 18,57 6,57 6,50 "
                        stroke-linejoin="miter"></polyline>
                      <polyline data-color="color-2" fill="none" stroke="#444444" stroke-width="3"
                        stroke-linecap="square" stroke-miterlimit="10" points=" 58,50 58,57 46,57 46,50 "
                        stroke-linejoin="miter"></polyline>
                      <path fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square" stroke-miterlimit="10"
                        d="M62,50H2V35.448 c0-0.936,0.328-1.842,0.927-2.561L7,28h50l4.073,4.887C61.672,33.606,62,34.512,62,35.448V50z"
                        stroke-linejoin="miter"></path>
                      <circle data-color="color-2" fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square"
                        stroke-miterlimit="10" cx="12" cy="39" r="4" stroke-linejoin="miter"></circle>
                      <circle data-color="color-2" fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square"
                        stroke-miterlimit="10" cx="52" cy="39" r="4" stroke-linejoin="miter"></circle>
                      <line data-color="color-2" fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square"
                        stroke-miterlimit="10" x1="26" y1="39" x2="38" y2="39" stroke-linejoin="miter"></line>
                    </g>
                  </svg>
                </div>
                <div class="media-body">
                  <h4 class="small-margin-0">Learn in your car</h4>
                  <p>
                    Use your instructors car or learn in the comfort of your own
                    vehicle.
                  </p>
                </div>
              </div>
              <div class="media" data-equalizer-watch>
                <div class="media-left small-padding-right-15">
                  <svg class="size-40 yellow" xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="64px" height="64px"
                    viewBox="0 0 64 64" stroke-width="3">
                    <g stroke-width="3" transform="translate(0.5, 0.5)">
                      <polyline data-color="color-2" fill="none" stroke="#444444" stroke-width="3"
                        stroke-linecap="square" stroke-miterlimit="10" points=" 25,35 30,40 40,30 "
                        stroke-linejoin="miter"></polyline>
                      <polyline fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square"
                        stroke-miterlimit="10" points="49,11 57,11 57,62 7,62 7,11 15,11 " stroke-linejoin="miter">
                      </polyline>
                      <path fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square" stroke-miterlimit="10"
                        d="M39,9c0-3.866-3.134-7-7-7 s-7,3.134-7,7h-5v8h24V9H39z" stroke-linejoin="miter"></path>
                      <circle data-stroke="none" fill="#444444" cx="32" cy="9" r="2" stroke-linejoin="miter"
                        stroke-linecap="square"></circle>
                      <polyline data-color="color-2" fill="none" stroke="#444444" stroke-width="3"
                        stroke-linecap="square" stroke-miterlimit="10" points=" 51,17 51,56 13,56 13,17 "
                        stroke-linejoin="miter"></polyline>
                    </g>
                  </svg>
                </div>
                <div class="media-body">
                  <h4 class="small-margin-0">Driving tests</h4>
                  <p>
                    Book a test package which includes pick-up, a pre-test
                    lesson, use of a car & drop off.
                  </p>
                </div>
              </div>
            </div>
            <div class="small-12 columns small-margin-top-30 text-center">
              <a class="button yellow anchor" href="/driving-lessons">Book driving lessons now <i
                  class="fas fa-angle-right fr"></i></a>
            </div>
          </div>
        </div>
      </section>

      <section class="bg-gray-lighter section">
        <div class="container">
          <div class="row">
            <div class="large-8 columns">
              <h3>Top Frequently Asked Questions</h3>
              <el-collapse accordion small-margin-top-30 small-margin-bottom-30>
                <el-collapse-item name="1" class="accordion-navigation">
                  <template #title>
                    <router-link class="small-padding-top-20 small-padding-bottom-20" to="#accordion-faq-12">
                      <h4 class="small-margin-0 font-normal small-fontsize-16">
                        Do I Need to Provide My Own Car For Driving Lessons or
                        Do You Provide a Vehicle?
                      </h4>
                    </router-link>
                  </template>

                  <div class="bg-gray-lighter content" id="accordion-faq-12">
                    <article class="html-content small-margin-0">
                      <p>
                        <meta charset="utf-8" />
                      </p>

                      <p dir="ltr">
                        If you would prefer to learn in your own vehicle, you
                        can choose to do so, provided that you are a competent
                        driver and your vehicle is roadworthy, clean, and
                        registered. You may also opt to use the<a
                          href="https://www.ezlicence.com.au/blog/reasons-why-you-should-book-a-driving-instructors-car-for-your-test">
                          driving instructor&rsquo;s vehicle</a>, an instructional vehicle with dual controls for added
                        safety, at no extra cost.
                      </p>

                      <p>
                        <br />
                        &nbsp;
                      </p>
                    </article>
                  </div>
                </el-collapse-item>
                <el-collapse-item name="2" class="accordion-navigation">
                  <template #title>
                    <router-link class="small-padding-top-20 small-padding-bottom-20" to="#accordion-faq-6">
                      <h4 class="small-margin-0 font-normal small-fontsize-16">
                        How Much Do Driving Lessons Cost?
                      </h4>
                    </router-link>
                  </template>
                  <div class="bg-gray-lighter content" id="accordion-faq-6">
                    <article class="html-content small-margin-0">
                      <p>
                        <meta charset="utf-8" />
                      </p>

                      <p>
                        At EzLicence, we have set<a href="https://www.ezlicence.com.au/pricing">
                          driving lesson prices</a>
                        based on our extensive research of driving schools
                        across Australia. Prices can&nbsp;vary depending on the
                        suburb where you will be picked up and your preferred
                        transmission type (automatic or manual).&nbsp; Enter the
                        information into our search tool&nbsp;to compare driving
                        lesson prices.
                      </p>

                      <p>
                        <meta charset="utf-8" />
                      </p>

                      <p dir="ltr">
                        Note that we offer discounts for learner drivers who
                        purchase driving lesson packages.&nbsp;
                      </p>

                      <p></p>
                    </article>
                  </div>
                </el-collapse-item>
                <el-collapse-item name="3" class="accordion-navigation">
                  <template #title>
                    <router-link class="small-padding-top-20 small-padding-bottom-20" to="#accordion-faq-8">
                      <h4 class="small-margin-0 font-normal small-fontsize-16">
                        Do You Offer Any Special Lessons to Prepare for the
                        Driving Test?
                      </h4>
                    </router-link>
                  </template>
                  <div class="bg-gray-lighter content" id="accordion-faq-8">
                    <article class="html-content small-margin-0">
                      <p>
                        EzLicence offers a driving test package for $199, which
                        includes:
                      </p>

                      <p>
                        <meta charset="utf-8" />
                      </p>

                      <p dir="ltr">
                        &bull;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Pick-up from
                        your chosen location
                      </p>

                      <p dir="ltr">
                        &bull;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 45-minute
                        pre-test driving lesson
                      </p>

                      <p dir="ltr">
                        &bull;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Use of your
                        instructor&rsquo;s vehicle for the driving test
                      </p>

                      <p dir="ltr">
                        &bull;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Drop off to
                        your chosen location
                      </p>

                      <p dir="ltr">
                        The EzLicence Test Package is available to all customers
                        except those in ACT, SA or TAS. Some EzLicence
                        instructors require you book a lesson with them prior to
                        booking a Test Package. Others will offer this as a
                        standalone item. Find an instructor for a Test Package<a
                          href="https://www.ezlicence.com.au/driving-lessons/test-package">
                          here</a>.&nbsp;
                      </p>

                      <p></p>

                      <p>&nbsp;</p>

                      <p>&nbsp;</p>
                    </article>
                  </div>
                </el-collapse-item>
                <el-collapse-item name="4" class="accordion-navigation">
                  <template #title>
                    <router-link class="small-padding-top-20 small-padding-bottom-20" to="#accordion-faq-15">
                      <h4 class="small-margin-0 font-normal small-fontsize-16">
                        How Many Driving Lessons Do I Need?
                      </h4>
                    </router-link>
                  </template>

                  <div class="bg-gray-lighter content" id="accordion-faq-15">
                    <article class="html-content small-margin-0">
                      <p>
                        After your first lesson, your driving instructor will be
                        in the best position to assess how many driving lessons
                        you should take, based on factors such as:
                      </p>

                      <p>
                        <meta charset="utf-8" />
                      </p>

                      <p dir="ltr">
                        &bull;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Previous
                        driving experience, if any
                      </p>

                      <p dir="ltr">
                        &bull;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Confidence
                        level
                      </p>

                      <p dir="ltr">
                        &bull;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; How quickly you
                        appear to learn and master driving techniques
                      </p>

                      <p dir="ltr"><strong>A New Driver</strong></p>

                      <p dir="ltr">
                        If you have no driving experience at all, we recommend
                        at least 7 to 10 hours of driving lessons with an
                        accredited driving instructor. For less confident
                        learners, it&rsquo;s not unusual to book up to 20 hours
                        of instruction. We all learn at different speeds, and it
                        is important to make sure you have a handle on what
                        you&rsquo;ve been taught in your driving lessons, not
                        just for your driver&rsquo;s test, but to be a safe and
                        competent driver.
                      </p>

                      <p dir="ltr">
                        If you are a new driver but have had some driving
                        experience &ndash; say, with a family member or friend
                        &ndash; we recommend at least 5 to 7 hours of driving
                        instruction to fine-tune your skills and prepare for
                        your driving test.
                      </p>

                      <p dir="ltr">
                        <strong>International Driver&rsquo;s Licence Holders</strong>
                      </p>

                      <p dir="ltr">
                        Most<a
                          href="https://www.ezlicence.com.au/blog/transferring-an-international-driver-s-licence-to-an-australian-licence">
                          international driver&rsquo;s licence holders</a>
                        book about 2 to 3 hours of driving instruction to
                        prepare for the driver&rsquo;s test here. Notably, there
                        has been a high failure rate in this category, so we
                        recommend starting with at least 3 to 5 hours of driving
                        lessons before attempting the driving test.
                      </p>

                      <p>
                        <strong>Licenced wanting to learn how to drive a manual
                          car</strong>
                      </p>

                      <p>
                        Most learners who already hold an Australian
                        Driver&#39;s Licence, but wish to learn on a manual
                        vehicle, will require 3 to 5 hours of driving lessons.
                      </p>

                      <p>
                        <em>Please note that these ranges are a guide only and
                          will vary from learner to learner.</em>
                      </p>

                      <p></p>
                    </article>
                  </div>
                </el-collapse-item>
                <el-collapse-item name="5" class="accordion-navigation">
                  <template #title>
                    <router-link class="small-padding-top-20 small-padding-bottom-20" to="#accordion-faq-11">
                      <h4 class="small-margin-0 font-normal small-fontsize-16">
                        Can I get the bonus logbook hours if I take lessons from
                        an EzLicence Driving Instructor?
                      </h4>
                    </router-link>
                  </template>

                  <div class="bg-gray-lighter content" id="accordion-faq-11">
                    <article class="html-content small-margin-0">
                      <p>Definitely.</p>

                      <p>
                        <meta charset="utf-8" />
                      </p>

                      <p dir="ltr">
                        Taking structured driving lessons with an EzLicence
                        instructor in
                        <a
                          href="https://www.ezlicence.com.au/blog/hr-3-hrs-how-to-get-bonus-log-book-hours-nsw">NSW</a>,
                        <a href="https://www.ezlicence.com.au/blog/hr-3-hrs-how-to-get-bonus-log-book-hours-qld">QLD</a>
                        &amp; ACT lets you record 3 hours of driving experience
                        in your logbook for every 1 hour of driving instruction,
                        up to a maximum of 30 hours recorded for 10 hours of
                        lessons. You can, of course, continue to take driving
                        lessons with EzLicence instructors after you have
                        recorded the maximum allowable bonus, but each 1 hour
                        will equal 1 hour in your logbook.
                      </p>

                      <p dir="ltr">
                        Note that if you take a driving lesson at night (i.e.
                        between sunset and sunrise), you can only record 1 hour
                        of night driving. The remaining 2 hours are added to
                        your log of day driving experience hours.
                      </p>

                      <p dir="ltr">
                        In Tasmania, you&rsquo;ll get 1 extra hour of credit for
                        every hour of driving instruction, up to a maximum of 20
                        hours recorded for 10 hours of lessons.
                      </p>

                      <p></p>
                    </article>
                  </div>
                </el-collapse-item>
                <el-collapse-item name="6" class="accordion-navigation">
                  <template #title>
                    <router-link class="small-padding-top-20 small-padding-bottom-20" to="#accordion-faq-21">
                      <h4 class="small-margin-0 font-normal small-fontsize-16">
                        What if There Are No Available Driving Instructors in My
                        Area?
                      </h4>
                    </router-link>
                  </template>

                  <div class="bg-gray-lighter content" id="accordion-faq-21">
                    <article class="html-content small-margin-0">
                      <p>
                        If your search comes up with no results, it is because
                        there are no driving instructors who are currently
                        willing or able to service the area of your chosen
                        pick-up location. Simply enter an alternate location
                        that is convenient for you and search again.
                      </p>

                      <p>
                        <meta charset="utf-8" />
                      </p>

                      <p></p>
                    </article>
                  </div>
                </el-collapse-item>
                <el-collapse-item name="7" class="accordion-navigation">
                  <template #title>
                    <router-link class="small-padding-top-20 small-padding-bottom-20" to="#accordion-faq-31">
                      <h4 class="small-margin-0 font-normal small-fontsize-16">
                        Can I Take Refresher Driving Lessons?
                      </h4>
                    </router-link>
                  </template>

                  <div class="bg-gray-lighter content" id="accordion-faq-31">
                    <article class="html-content small-margin-0">
                      <p>
                        Of course! Many existing driver&rsquo;s licence holders
                        book driving lessons to<a
                          href="https://www.ezlicence.com.au/blog/stay-at-your-best-with-refresher-driving-lessons">
                          refresh their skills</a>
                        or build up some more confidence, especially if they
                        have spent some time not driving. We recommend about 3
                        to 5 hours of driving instruction in cases like this.
                      </p>

                      <p>
                        <meta charset="utf-8" />
                      </p>
                    </article>
                  </div>
                </el-collapse-item>
                <el-collapse-item name="8" class="accordion-navigation">
                  <template #title>
                    <router-link class="small-padding-top-20 small-padding-bottom-20" to="#accordion-faq-32">
                      <h4 class="small-margin-0 font-normal small-fontsize-16">
                        Can I Change Instructors?
                      </h4>
                    </router-link>
                  </template>
                  <div class="bg-gray-lighter content" id="accordion-faq-32">
                    <article class="html-content small-margin-0">
                      <p>
                        Absolutely. At EzLicence, we know that having a rapport
                        with your driving instructor makes for a more
                        comfortable &ndash; and therefore effective &ndash;
                        learning experience. If you want to book a lesson with
                        another driving instructor, just follow the same steps.
                        From your dashboard select &#39;find another
                        instructor&#39; and then choose the instructor you&#39;d
                        like. Check their availability and book online. Take
                        your driving lesson. It&#39;s that simple.
                      </p>

                      <p>
                        <meta charset="utf-8" />
                      </p>
                    </article>
                  </div>
                </el-collapse-item>
                <el-collapse-item name="9" class="accordion-navigation">
                  <template #title>
                    <router-link class="small-padding-top-20 small-padding-bottom-20" to="#accordion-faq-33">
                      <h4 class="small-margin-0 font-normal small-fontsize-16">
                        Is EzLicence a Driving School?
                      </h4>
                    </router-link>
                  </template>
                  <div class="bg-gray-lighter content" id="accordion-faq-33">
                    <article class="html-content small-margin-0">
                      <p>
                        <meta charset="utf-8" /><b
                          id="docs-internal-guid-6e493859-7fff-cad3-d81a-de0abba757eb">EzLicence is like a driving
                          school only better,
                          allowing&nbsp;you to access the services of a driving
                          school with market leading convenience, choice and
                          flexibility.</b>
                      </p>

                      <p dir="ltr">
                        <b id="docs-internal-guid-6e493859-7fff-cad3-d81a-de0abba757eb">EzLicence has partnered with
                          over 350 driving schools
                          across Sydney, Melbourne, Brisbane and Perth to create
                          a single destination for learner drivers to view,
                          compare and book driving instructors online 24/7.</b>
                      </p>

                      <p dir="ltr">
                        <b id="docs-internal-guid-6e493859-7fff-cad3-d81a-de0abba757eb">Unlike a traditional driving
                          school, EzLicence allows
                          you to:</b>
                      </p>

                      <ul>
                        <li dir="ltr">
                          <p dir="ltr" role="presentation">
                            <b id="docs-internal-guid-6e493859-7fff-cad3-d81a-de0abba757eb">Find and compare a large
                              range of driving
                              instructors in your area.</b>
                          </p>
                        </li>
                        <li dir="ltr">
                          <p dir="ltr" role="presentation">
                            <b id="docs-internal-guid-6e493859-7fff-cad3-d81a-de0abba757eb">Choose your own instructor
                              based on comprehensive
                              profile information, including ratings and
                              reviews.</b>
                          </p>
                        </li>
                        <li dir="ltr">
                          <p dir="ltr" role="presentation">
                            <b id="docs-internal-guid-6e493859-7fff-cad3-d81a-de0abba757eb">View each driving
                              instructor&rsquo;s real-time
                              availability and make online bookings straight
                              into their calendar.</b>
                          </p>
                        </li>
                        <li dir="ltr">
                          <p dir="ltr" role="presentation">
                            <b id="docs-internal-guid-6e493859-7fff-cad3-d81a-de0abba757eb">Change your driving
                              instructor selection online
                              anytime.</b>
                          </p>
                        </li>
                        <li dir="ltr">
                          <p dir="ltr" role="presentation">
                            <b id="docs-internal-guid-6e493859-7fff-cad3-d81a-de0abba757eb">Manage existing bookings
                              (reschedule/cancel) and
                              make new bookings online</b>
                          </p>
                        </li>
                      </ul>

                      <p dir="ltr">
                        <b id="docs-internal-guid-6e493859-7fff-cad3-d81a-de0abba757eb">Each of our driving instructors
                          are independent and
                          operating their own driving school.</b>
                      </p>

                      <p>&nbsp;</p>
                    </article>
                  </div>
                </el-collapse-item>
                <el-collapse-item name="10" class="accordion-navigation">
                  <template #title>
                    <router-link class="small-padding-top-20 small-padding-bottom-20" to="#accordion-faq-2">
                      <h4 class="small-margin-0 font-normal small-fontsize-16">
                        Can I Book Driving Lessons to Learn How to Drive Manual?
                      </h4>
                    </router-link>
                  </template>
                  <div class="bg-gray-lighter content" id="accordion-faq-2">
                    <article class="html-content small-margin-0">
                      <p>
                        Absolutely.&nbsp; Driving a<a href="https://www.ezlicence.com.au/blog/manual-driving-lessons">
                          manual transmission</a>
                        vehicle is becoming less and less common, but it&rsquo;s
                        not yet a &ldquo;lost art&rdquo;. Whether you are
                        learning manual to be more versatile or because
                        it&rsquo;s a more engaging (and fun) drive, we recommend
                        booking 3 to 5 hours of driving instruction to start.
                      </p>

                      <p>
                        <meta charset="utf-8" />
                      </p>

                      <p>&nbsp;</p>
                    </article>
                  </div>
                </el-collapse-item>
              </el-collapse>
              <a class="button small oil" href="/support">Read More FAQs</a>
            </div>
            <div class="large-4 columns">
              <h3>Featured Blogs</h3>
              <a class="block panel small-padding-0 text-oil hover-yellow"
                href="/blog/reasons-why-you-might-not-pass-your-driving-test">
                <div class="panel-body">
                  <img loading="lazy" alt="28 Reasons Why You Might NOT Pass Your Driving Test" class="img-expand"
                    height="300" width="150"
                    src="//s3-ap-southeast-2.amazonaws.com/ezlicence-uploads/blog_posts/featured_images/000/000/013/sm/Main_Image--.png?1562648831" />
                  <div class="media media-middle small-margin-0">
                    <div class="media-body">
                      <h5 class="font-normal small-margin-15 small-fontsize-16">
                        28 Reasons Why You Might NOT Pass Your Driving Test
                      </h5>
                    </div>
                    <div class="media-right small-padding-right-10">
                      <i class="fas fa-chevron-right fa-sm fa-fw"></i>
                    </div>
                  </div>
                </div>
              </a><a class="block panel small-padding-0 text-oil hover-yellow"
                href="/blog/tips-for-choosing-a-good-driving-instructor">
                <div class="panel-body">
                  <img loading="lazy" alt="11 Tips for Choosing a Good Driving Instructor" class="img-expand"
                    height="300" width="150"
                    src="//s3-ap-southeast-2.amazonaws.com/ezlicence-uploads/blog_posts/featured_images/000/000/012/sm/11_Tips_for_Choosing_a_Good_Driving_Instructor-.png?1562648830" />
                  <div class="media media-middle small-margin-0">
                    <div class="media-body">
                      <h5 class="font-normal small-margin-15 small-fontsize-16">
                        11 Tips for Choosing a Good Driving Instructor
                      </h5>
                    </div>
                    <div class="media-right small-padding-right-10">
                      <i class="fas fa-chevron-right fa-sm fa-fw"></i>
                    </div>
                  </div>
                </div>
              </a>
              <div class="small-padding-top-10">
                <a class="button small oil" href="/blog">Read More Blogs</a>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section class="bg-white section">
        <div class="container text-center">
          <div class="row">
            <div class="small-12 columns">
              <h5 class="small-fontsize-30 small-margin-bottom-10">
                Why choose EzLicence?
              </h5>
              <p class="lead">
                Unlike a typical driving school, EzLicence is an Australian
                first platform that allows learner drivers & parents to
                <u class="font-semi-bold">find, compare and book verified driving instructors
                  online.</u>
                The platform brings transparency, choice and efficiency to the
                selection of a driving instructor and the ongoing management of
                driving lessons.
              </p>
            </div>
          </div>
          <div class="row caps" data-equalizer="">
            <div class="medium-4 columns medium-margin-top-30" data-equalizer-watch="">
              <div class="panel bg-yellow">
                <h3 class="small-fontsize-18 text-oil">
                  <span class="block small-fontsize-70">900+</span>
                  Driving Instructors
                </h3>
              </div>
            </div>
            <div class="medium-4 columns medium-margin-top-30" data-equalizer-watch="">
              <div class="panel bg-yellow">
                <h3 class="small-fontsize-18 text-oil">
                  <span class="block small-fontsize-70">2500+</span>
                  Suburbs Serviced
                </h3>
              </div>
            </div>
            <div class="medium-4 columns medium-margin-top-30" data-equalizer-watch="">
              <div class="panel bg-yellow">
                <h3 class="small-fontsize-18 text-oil">
                  <span class="block small-fontsize-70">#1</span>
                  Online Bookings
                </h3>
              </div>
            </div>
          </div>
          <div class="row">
            <div class="small-12 columns">
              <ul class="text-left medium-block-grid-2 large-block-grid-4 small-margin-top-20 font-semi-condensed">
                <li>
                  <div class="media">
                    <div class="media-left medium-fontsize-30 text-yellow">
                      ✓
                    </div>
                    <div class="media-body">
                      Choose your own private driving instructor
                    </div>
                  </div>
                </li>
                <li>
                  <div class="media">
                    <div class="media-left medium-fontsize-30 text-yellow">
                      ✓
                    </div>
                    <div class="media-body">
                      Largest choice of driving instructors in Australia
                    </div>
                  </div>
                </li>
                <li>
                  <div class="media">
                    <div class="media-left medium-fontsize-30 text-yellow">
                      ✓
                    </div>
                    <div class="media-body">
                      Book driving lessons online in real-time
                    </div>
                  </div>
                </li>
                <li>
                  <div class="media">
                    <div class="media-left medium-fontsize-30 text-yellow">
                      ✓
                    </div>
                    <div class="media-body">
                      Driving instructor profiles, ratings & reviews
                    </div>
                  </div>
                </li>
                <li>
                  <div class="media">
                    <div class="media-left medium-fontsize-30 text-yellow">
                      ✓
                    </div>
                    <div class="media-body">
                      Manage your driving lesson bookings online
                    </div>
                  </div>
                </li>
                <li>
                  <div class="media">
                    <div class="media-left medium-fontsize-30 text-yellow">
                      ✓
                    </div>
                    <div class="media-body">
                      Change your driving instructor online
                    </div>
                  </div>
                </li>
                <li>
                  <div class="media">
                    <div class="media-left medium-fontsize-30 text-yellow">
                      ✓
                    </div>
                    <div class="media-body">
                      International driver’s licence conversions
                    </div>
                  </div>
                </li>
                <li>
                  <div class="media">
                    <div class="media-left medium-fontsize-30 text-yellow">
                      ✓
                    </div>
                    <div class="media-body">
                      Book driving lessons with flexibility
                    </div>
                  </div>
                </li>
                <li>
                  <div class="media">
                    <div class="media-left medium-fontsize-30 text-yellow">
                      ✓
                    </div>
                    <div class="media-body">
                      Licenced and accredited driving instructors
                    </div>
                  </div>
                </li>
                <li>
                  <div class="media">
                    <div class="media-left medium-fontsize-30 text-yellow">
                      ✓
                    </div>
                    <div class="media-body">
                      Get one free lesson with keys2drive
                    </div>
                  </div>
                </li>
                <li>
                  <div class="media">
                    <div class="media-left medium-fontsize-30 text-yellow">
                      ✓
                    </div>
                    <div class="media-body">
                      Eligible for bonus log book hours (1 hr = 3 hrs)
                    </div>
                  </div>
                </li>
                <li>
                  <div class="media">
                    <div class="media-left medium-fontsize-30 text-yellow">
                      ✓
                    </div>
                    <div class="media-body">
                      Driving school instructor cars dual controlled
                    </div>
                  </div>
                </li>
                <li>
                  <div class="media">
                    <div class="media-left medium-fontsize-30 text-yellow">
                      ✓
                    </div>
                    <div class="media-body">
                      Auto & manual cars available - or use your own!
                    </div>
                  </div>
                </li>
                <li>
                  <div class="media">
                    <div class="media-left medium-fontsize-30 text-yellow">
                      ✓
                    </div>
                    <div class="media-body">
                      Your very own private driving instructor
                    </div>
                  </div>
                </li>
                <li>
                  <div class="media">
                    <div class="media-left medium-fontsize-30 text-yellow">
                      ✓
                    </div>
                    <div class="media-body">
                      Review all of the driving schools in your area
                    </div>
                  </div>
                </li>
                <li>
                  <div class="media">
                    <div class="media-left medium-fontsize-30 text-yellow">
                      ✓
                    </div>
                    <div class="media-body">
                      Patient & friendly male & female driving instructors
                    </div>
                  </div>
                </li>
              </ul>
            </div>
            <div class="small-12 columns small-margin-top-30 text-center">
              <a class="button yellow last" href="/driving-lessons">Book a driving school today
                <i class="fas fa-angle-right fr"></i></a>
            </div>
          </div>
        </div>
      </section>
      <hr class="small-margin-0" />
      <section class="bg-white section">
        <div class="container medium-margin-bottom-20">
          <div class="row">
            <div class="small-12 large-10 columns small-centered">
              <h5 class="small-fontsize-30 text-center small-margin-bottom-30">
                The EzLicence advantage
              </h5>
              <el-collapse>
                <el-collapse-item name="1" class="accordion-navigation-other">
                  <template #title>
                    <router-link class="small-padding-10" to="#accordion-advantage-1">
                      <div class="media media-middle">
                        <div class="media-left medium-padding-right-20">
                          <svg class="size-40 yellow" xmlns="http://www.w3.org/2000/svg"
                            xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="64px" height="64px"
                            viewBox="0 0 64 64" stroke-width="3">
                            <g stroke-width="3" transform="translate(0.5, 0.5)">
                              <line x1="24" y1="2" x2="40" y2="2" fill="none" stroke="#444444" stroke-linecap="square"
                                stroke-miterlimit="10" stroke-width="3" stroke-linejoin="miter"></line>
                              <line x1="32" y1="2" x2="32" y2="5" fill="none" stroke="#444444" stroke-linecap="square"
                                stroke-miterlimit="10" stroke-width="3" stroke-linejoin="miter"></line>
                              <circle cx="32" cy="36" r="26" fill="none" stroke="#444444" stroke-linecap="square"
                                stroke-miterlimit="10" stroke-width="3" stroke-linejoin="miter"></circle>
                              <path data-color="color-2"
                                d="M28.716,38.284c-1.261-1.814-5.281-14.6-5.281-14.6S34.022,31.9,35.283,33.717a4,4,0,1,1-6.567,4.567Z"
                                fill="none" stroke="#444444" stroke-linecap="square" stroke-miterlimit="10"
                                stroke-width="3" stroke-linejoin="miter"></path>
                              <line data-color="color-2" x1="32" y1="16" x2="32" y2="20" fill="none" stroke="#444444"
                                stroke-linecap="square" stroke-miterlimit="10" stroke-width="3" stroke-linejoin="miter">
                              </line>
                              <line data-color="color-2" x1="52" y1="36" x2="48" y2="36" fill="none" stroke="#444444"
                                stroke-linecap="square" stroke-miterlimit="10" stroke-width="3" stroke-linejoin="miter">
                              </line>
                              <line data-color="color-2" x1="32" y1="56" x2="32" y2="52" fill="none" stroke="#444444"
                                stroke-linecap="square" stroke-miterlimit="10" stroke-width="3" stroke-linejoin="miter">
                              </line>
                              <line data-color="color-2" x1="12" y1="36" x2="16" y2="36" fill="none" stroke="#444444"
                                stroke-linecap="square" stroke-miterlimit="10" stroke-width="3" stroke-linejoin="miter">
                              </line>
                              <line x1="50" y1="9" x2="59" y2="18" fill="none" stroke="#444444" stroke-linecap="square"
                                stroke-miterlimit="10" stroke-width="3" stroke-linejoin="miter"></line>
                            </g>
                          </svg>
                        </div>
                        <div class="media-body">
                          <h4 class="small-margin-0 small-fontsize-18 text-oil hover-yellow">
                            Book driving lessons online in under 60 seconds
                          </h4>
                        </div>
                      </div>
                    </router-link>
                  </template>
                  <div class="content bg-white" id="accordion-advantage-1">
                    <p>
                      Booking
                      <a href="/driving-lessons">driving lessons</a> through
                      EzLicence is a quick and hassle free process that gives
                      you all the choice and control. Why deal with traditional
                      Driving Schools over the phone or by email when you can
                      manage your driving instructor choice & book driving
                      lessons yourself anywhere, and at any time through our
                      secure online platform?
                    </p>
                  </div>
                </el-collapse-item>
                <el-collapse-item name="2">
                  <template #title>
                    <router-link class="small-padding-10" to="#accordion-advantage-2">
                      <div class="media media-middle">
                        <div class="media-left medium-padding-right-20">
                          <svg class="size-40 yellow" xmlns="http://www.w3.org/2000/svg"
                            xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="64px" height="64px"
                            viewBox="0 0 64 64" stroke-width="3">
                            <g stroke-width="3" transform="translate(0.5, 0.5)">
                              <polyline data-color="color-2" fill="none" stroke="#444444" stroke-width="3"
                                stroke-linecap="square" stroke-miterlimit="10" points=" 18,2 8,2 8,12 "
                                stroke-linejoin="miter"></polyline>
                              <polyline data-color="color-2" fill="none" stroke="#444444" stroke-width="3"
                                stroke-linecap="square" stroke-miterlimit="10" points=" 43,12 43,2 33,2 "
                                stroke-linejoin="miter"></polyline>
                              <line fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square"
                                stroke-miterlimit="10" x1="21" y1="34" x2="21" y2="42" stroke-linejoin="miter"></line>
                              <path fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square"
                                stroke-miterlimit="10"
                                d="M30,35v-3.5 c0-2.485,2.015-4.5,4.5-4.5h0c2.485,0,4.5,2.015,4.5,4.5V35"
                                stroke-linejoin="miter"></path>
                              <path fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square"
                                stroke-miterlimit="10"
                                d="M39,33.5 c0-2.485,2.015-4.5,4.5-4.5h0c2.485,0,4.5,2.015,4.5,4.5V36"
                                stroke-linejoin="miter"></path>
                              <path fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square"
                                stroke-miterlimit="10"
                                d="M18.197,61 C16.123,57.661,13,54.23,13,50V38c0-2.209,1.791-4,4-4h4V11.5C21,9.015,23.015,7,25.5,7h0c2.485,0,4.5,2.015,4.5,4.5V34"
                                stroke-linejoin="miter"></path>
                              <path fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square"
                                stroke-miterlimit="10"
                                d="M48,36c0,0,0.125-4,4-4 c2.312,0,4,1.375,4,4c0,10.047-2.441,19.483-4.21,25"
                                stroke-linejoin="miter"></path>
                            </g>
                          </svg>
                        </div>
                        <div class="media-body">
                          <h4 class="small-margin-0 small-fontsize-18 text-oil hover-yellow">
                            More control over your bookings
                          </h4>
                        </div>
                      </div>
                    </router-link>
                  </template>
                  <div class="content bg-white" id="accordion-advantage-2">
                    <p>
                      From the moment you enter your pickup suburb you have more
                      control over your driving lesson compared to traditional
                      driving schools. Choose, compare, and book your driving
                      instructor and preferred vehicle transmission based on
                      in-depth driving instructor profiles, including ratings
                      and reviews from learners just like you. The best part?
                      Bookings are made in real-time, so you can book your
                      driving lesson instantly and at a convenient time.
                    </p>
                  </div>
                </el-collapse-item>
                <el-collapse-item name="3">
                  <template #title>
                    <router-link class="small-padding-10" to="#accordion-advantage-3">
                      <div class="media media-middle">
                        <div class="media-left medium-padding-right-20">
                          <svg class="size-40 yellow" xmlns="http://www.w3.org/2000/svg"
                            xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="64px" height="64px"
                            viewBox="0 0 64 64" stroke-width="3">
                            <g stroke-width="3" transform="translate(0.5, 0.5)">
                              <line data-color="color-2" x1="32" y1="29" x2="32" y2="45" fill="none" stroke="#444444"
                                stroke-linecap="square" stroke-miterlimit="10" stroke-width="3" stroke-linejoin="miter">
                              </line>
                              <line data-color="color-2" x1="40" y1="37" x2="24" y2="37" fill="none" stroke="#444444"
                                stroke-linecap="square" stroke-miterlimit="10" stroke-width="3" stroke-linejoin="miter">
                              </line>
                              <line data-cap="butt" x1="3" y1="20" x2="61" y2="20" fill="none" stroke="#444444"
                                stroke-miterlimit="10" stroke-width="3" stroke-linecap="butt" stroke-linejoin="miter">
                              </line>
                              <rect x="3" y="8" width="58" height="48" fill="none" stroke="#444444"
                                stroke-linecap="square" stroke-miterlimit="10" stroke-width="3" stroke-linejoin="miter">
                              </rect>
                              <circle data-color="color-2" data-stroke="none" cx="10" cy="14" r="2" fill="#444444">
                              </circle>
                              <circle data-color="color-2" data-stroke="none" cx="18" cy="14" r="2" fill="#444444">
                              </circle>
                            </g>
                          </svg>
                        </div>
                        <div class="media-body">
                          <h4 class="small-margin-0 small-fontsize-18 text-oil hover-yellow">
                            Your online dashboard
                          </h4>
                        </div>
                      </div>
                    </router-link>
                  </template>
                  <div class="content bg-white" id="accordion-advantage-3">
                    <p>
                      Manage your preferences, existing bookings & future
                      driving lesson bookings from your secure online account.
                      Reschedule bookings up to 24 hrs prior to the lesson start
                      time - perfect for those with an unpredictable schedule!
                      Want to try a different driving instructor? You can change
                      your driving instructor at the push of a button, no
                      questions asked.
                    </p>
                  </div>
                </el-collapse-item>
                <el-collapse-item name="4">
                  <template #title>
                    <router-link class="small-padding-10" to="#accordion-advantage-4">
                      <div class="media media-middle">
                        <div class="media-left medium-padding-right-20">
                          <svg class="size-40 yellow" xmlns="http://www.w3.org/2000/svg"
                            xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="64px" height="64px"
                            viewBox="0 0 64 64" stroke-width="3">
                            <g stroke-width="3" transform="translate(0.5, 0.5)">
                              <path data-color="color-2" fill="none" stroke="#444444" stroke-width="3"
                                stroke-linecap="square" stroke-miterlimit="10"
                                d="M39,19H25v0 c0-3.314,2.686-6,6-6h2C36.314,13,39,15.686,39,19L39,19z"
                                stroke-linejoin="miter"></path>
                              <circle data-color="color-2" fill="none" stroke="#444444" stroke-width="3"
                                stroke-linecap="square" stroke-miterlimit="10" cx="32" cy="6" r="4"
                                stroke-linejoin="miter"></circle>
                              <path data-color="color-2" fill="none" stroke="#444444" stroke-width="3"
                                stroke-linecap="square" stroke-miterlimit="10"
                                d="M16,28H2v0 c0-3.314,2.686-6,6-6h2C13.314,22,16,24.686,16,28L16,28z"
                                stroke-linejoin="miter"></path>
                              <circle data-color="color-2" fill="none" stroke="#444444" stroke-width="3"
                                stroke-linecap="square" stroke-miterlimit="10" cx="9" cy="15" r="4"
                                stroke-linejoin="miter"></circle>
                              <path data-color="color-2" fill="none" stroke="#444444" stroke-width="3"
                                stroke-linecap="square" stroke-miterlimit="10"
                                d="M63,28H49v0 c0-3.314,2.686-6,6-6h2C60.314,22,63,24.686,63,28L63,28z"
                                stroke-linejoin="miter"></path>
                              <circle data-color="color-2" fill="none" stroke="#444444" stroke-width="3"
                                stroke-linecap="square" stroke-miterlimit="10" cx="56" cy="15" r="4"
                                stroke-linejoin="miter"></circle>
                              <circle fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square"
                                stroke-miterlimit="10" cx="32" cy="36" r="9" stroke-linejoin="miter"></circle>
                              <path fill="none" stroke="#444444" stroke-width="3" stroke-linecap="square"
                                stroke-miterlimit="10"
                                d="M35,50h-6 c-6.627,0-12,5.373-12,12v0h30v0C47,55.373,41.627,50,35,50z"
                                stroke-linejoin="miter"></path>
                            </g>
                          </svg>
                        </div>
                        <div class="media-body">
                          <h4 class="small-margin-0 small-fontsize-18 text-oil hover-yellow">
                            The widest range of driving instructors
                          </h4>
                        </div>
                      </div>
                    </router-link>
                  </template>
                  <div class="content bg-white" id="accordion-advantage-4">
                    <p>
                      EzLicence provides access to more than 900+
                      <a href="/instructors">fully qualified driving instructors</a>
                      across Sydney, Melbourne, Brisbane, Perth, Adelaide,
                      Hobart, Gold Coast, Sunshine Coast, Newcastle, Central
                      Coast, Geelong, Toowoomba, Wollongong, Cairns, Coffs
                      Harbour, Bendigo, Canberra. All driving instructors
                      available through EzLicence are required to have a
                      current, valid clearance for working with children, as
                      well as having their vehicles equipped with dual control
                      pedals for added safety. With an EzLicence driving
                      instructor, you can be sure you’re in good hands.
                    </p>
                  </div>
                </el-collapse-item>
                <el-collapse-item name="5">
                  <template #title>
                    <router-link class="small-padding-10" to="#accordion-advantage-5">
                      <div class="media media-middle">
                        <div class="media-left medium-padding-right-20">
                          <svg style="margin: 5px 0 -5px" class="size-40 yellow" xmlns="http://www.w3.org/2000/svg"
                            xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="64px" height="64px"
                            viewBox="0 0 64 64" stroke-width="3">
                            <g stroke-width="3" transform="translate(0.5, 0.5)">
                              <circle cx="46" cy="34" r="6" fill="none" stroke="#444444" stroke-linecap="square"
                                stroke-miterlimit="10" stroke-width="3" stroke-linejoin="miter"></circle>
                              <path d="M62,35c0,8.837-16,24-16,24S30,43.837,30,35a16,16,0,0,1,32,0Z" fill="none"
                                stroke="#444444" stroke-linecap="square" stroke-miterlimit="10" stroke-width="3"
                                stroke-linejoin="miter"></path>
                              <path d="M24,13c0,6.075-11,16-11,16S2,19.075,2,13a11,11,0,0,1,22,0Z" fill="none"
                                stroke="#444444" stroke-linecap="square" stroke-miterlimit="10" stroke-width="3"
                                stroke-linejoin="miter"></path>
                              <circle cx="13" cy="13" r="3" fill="none" stroke="#444444" stroke-linecap="square"
                                stroke-miterlimit="10" stroke-width="3" stroke-linejoin="miter"></circle>
                              <path d="M29,53A16,16,0,0,1,13,37" fill="none" stroke="#444444" stroke-linecap="square"
                                stroke-miterlimit="10" stroke-width="3" data-color="color-2" stroke-linejoin="miter">
                              </path>
                            </g>
                          </svg>
                        </div>
                        <div class="media-body">
                          <h4 class="small-margin-0 small-fontsize-18 text-oil hover-yellow">
                            Servicing YOUR area
                          </h4>
                        </div>
                      </div>
                    </router-link>
                  </template>
                  <div class="content bg-white" id="accordion-advantage-5">
                    <p>
                      Thanks to our comprehensive driving instructor service
                      area coverage, you can choose your pickup location from
                      anywhere in Sydney, Melbourne, Brisbane, Adelaide, Perth,
                      Hobart, Gold Coast, Sunshine Coast, Newcastle, Central
                      Coast, Geelong, Toowoomba, Wollongong, Cairns, Coffs
                      Harbour, Bendigo, Canberra or the surrounding areas..
                      EzLicence now proudly services over 2500+ suburbs across
                      NSW, VIC, QLD, SA, TAS, WA and ACT, and will continue to
                      grow.
                    </p>
                  </div>
                </el-collapse-item>
              </el-collapse>

              <div class="small-padding-30"></div>
              <div class="bg-gray-lighter small-padding-20 medium-padding-30">
                <p>
                  Finding the right driving school and instructor can be
                  difficult. And time-consuming.
                </p>
                <p>
                  There’s a lot to navigate when booking driving lessons and it
                  can be difficult to find instructors that are close by.
                </p>
                <p>
                  EzLicence removes the stress and time required to find a
                  driving school by giving you access to the largest number of
                  verified driving instructors in Australia.
                </p>
                <p>
                  With EzLicence, you’re able to browse instructor profiles
                  before you book your driving lessons, meaning you can make a
                  more informed decision.
                </p>

                <el-collapse v-model="activeNames" @change="handleChange">
                  <el-collapse-item v-for="(v, i) in Array(4).fill('1')" :key="i" :name="i"
                    class="accordion-navigation border-none">
                    <template #title>
                      <router-link class="font-semi-bold shadow-none text-oil hover-yellow" to="#accordion-ezlicence-h0"
                        tag="a">How do I find private driving instructors near
                        me?</router-link>
                    </template>
                    <div class="content bg-gray-lighter small-padding-5" id="accordion-ezlicence-h0">
                      <p>
                        We know what it’s like when you first start learning to
                        drive - we were all there once too. Some of us were
                        nervous, some were excited, but all of us were ready to
                        succeed. Where do you start when you are ready to choose
                        a driving school? Our driving instructors are ready to
                        help you achieve your goals, and at a pace you are
                        comfortable with.
                      </p>
                      <p>
                        Regardless of whether you’re learning to drive for the
                        first time and looking to log your first few hours, or
                        an experienced driver looking to ease yourself back into
                        the driver’s seat with
                        <a href="/driving-lessons/refresher-driving-lessons">refresher driving lessons</a>, our wide
                        variety of driving instructors can cater to
                        your individual needs. Any transmission, any suburb, any
                        day; we’re here to help you become the safe and
                        confident driver you need to be on the road.
                      </p>
                      <p>
                        Learn from a true professional and book your
                        <a href="/driving-lessons">driving lessons</a> with a
                        private driving instructor at EzLicence, so you can get
                        your driving experience started the right way. Choose a
                        driving school in your area and begin learning to drive
                        today.
                      </p>
                      <p class="font-bold">
                        Learn smart. Learn safe. Learn easy with EzLicence.
                      </p>
                    </div>
                  </el-collapse-item>
                </el-collapse>
                <!-- todo...修改折叠菜单 -->
              </div>
            </div>
          </div>
        </div>
      </section>
    </main>

    <div class="bg-white">
      <footer id="footer">
        <div class="container small-text-center medium-text-left">
          <div class="media collapse-small">
            <div class="media-left">
              <div class="hide-for-small-only">
                <div class="medium-width-250px medium-padding-right-20">
                  <h6>Who is EzLicence?</h6>
                  <p class="small-fontsize-13">
                    EzLicence takes the hassle out of choosing a driving school
                    by helping learner drivers find, compare and book verified
                    driving instructors online.
                  </p>
                  <p class="small-fontsize-13">
                    The EzLicence online platform brings transparency, choice
                    and efficiency to booking and managing driving instructors
                    and driving lessons in Sydney, Melbourne, Brisbane, Perth,
                    Adelaide, Hobart, Gold Coast, Sunshine Coast, Newcastle,
                    Central Coast, Geelong, Toowoomba, Wollongong, Cairns, Coffs
                    Harbour, Bendigo, Canberra.
                  </p>
                </div>
              </div>
            </div>
            <div class="media-body">
              <div class="row">
                <div class="large-7 columns small-margin-bottom-20 seo-links">
                  <h6>Learners Tests Online</h6>
                  <ul class="list-unstyled">
                    <li>
                      <a href="/learners-tests">FREE Practice Learners Test</a>
                    </li>
                    <li>
                      <a href="/learners-tests/nsw">NSW Driver Knowledge Test</a>
                    </li>
                    <li>
                      <a href="/learners-tests/vic">VIC Learner Permit Knowledge Test</a>
                    </li>
                    <li>
                      <a href="/learners-tests/qld">QLD Road Rules Test</a>
                    </li>
                    <li>
                      <a href="/learners-tests/wa">WA Road Rules Theory Test</a>
                    </li>
                    <li>
                      <a href="/learners-tests/sa">SA Learner Theory Test</a>
                    </li>
                    <li>
                      <a href="/learners-tests/tas">TAS Driver Knowledge Test</a>
                    </li>
                    <li>
                      <a href="/learners-tests/act">ACT Road Rules Knowledge Test</a>
                    </li>
                  </ul>
                  <br />
                </div>
                <div class="large-5 columns small-margin-bottom-20">
                  <h6>Resources</h6>
                  <ul class="list-unstyled">
                    <li>
                      <a target="_blank" href="https://support.ezlicence.com.au/hc">Support</a>
                    </li>
                    <li><a href="/blog">Blog</a></li>
                    <li>
                      <a href="https://support.ezlicence.com.au/hc">Contact</a>
                    </li>
                    <li><a href="/about">About</a></li>
                    <li><a href="/instruct">Instruct with EzLicence</a></li>
                    <li>
                      <a href="/become-a-driving-instructor">Become an instructor</a>
                    </li>
                  </ul>
                  <br />
                </div>
              </div>
              <div class="row">
                <div class="large-7 columns small-margin-bottom-20 seo-links">
                  <h6>Driving Instructors by State</h6>
                  <ul class="list-unstyled">
                    <li>
                      <a title="NSW Driving instructors" href="/driving-instructors/nsw">NSW Driving instructors</a>
                    </li>
                    <li>
                      <a title="VIC Driving instructors" href="/driving-instructors/vic">VIC Driving instructors</a>
                    </li>
                    <li>
                      <a title="QLD Driving instructors" href="/driving-instructors/qld">QLD Driving instructors</a>
                    </li>
                    <li>
                      <a title="WA Driving instructors" href="/driving-instructors/wa">WA Driving instructors</a>
                    </li>
                    <li>
                      <a title="SA Driving instructors" href="/driving-instructors/sa">SA Driving instructors</a>
                    </li>
                    <li>
                      <a title="TAS Driving instructors" href="/driving-instructors/tas">TAS Driving instructors</a>
                    </li>
                    <li>
                      <a title="ACT Driving instructors" href="/driving-instructors/act">ACT Driving instructors</a>
                    </li>
                  </ul>
                </div>
                <div class="large-5 columns small-margin-bottom-20">
                  <h6>Driving Instructors by City</h6>
                  <ul class="list-unstyled">
                    <li>
                      <a title="Sydney Driving instructors" href="/driving-instructors/nsw/sydney">Sydney Driving
                        instructors</a>
                    </li>
                    <li>
                      <a title="Melbourne Driving instructors" href="/driving-instructors/vic/melbourne">Melbourne
                        Driving instructors</a>
                    </li>
                    <li>
                      <a title="Brisbane Driving instructors" href="/driving-instructors/qld/brisbane-city">Brisbane
                        Driving instructors</a>
                    </li>
                    <li>
                      <a title="Perth Driving instructors" href="/driving-instructors/wa/perth">Perth Driving
                        instructors</a>
                    </li>
                    <li>
                      <a title="Adelaide Driving instructors" href="/driving-instructors/sa/adelaide">Adelaide Driving
                        instructors</a>
                    </li>
                    <li>
                      <a title="Hobart Driving instructors" href="/driving-instructors/tas/hobart-region">Hobart Driving
                        instructors</a>
                    </li>
                    <li>
                      <a title="Canberra Driving instructors" href="/driving-instructors/act/canberra-region">Canberra
                        Driving instructors</a>
                    </li>
                    <!-- %li= link_to 'Darwin Driving instructors', seo_instructors_path(location_params: 'nt'), title: 'Darwin Driving instructors' -->
                  </ul>
                </div>
              </div>
            </div>
            <div class="media-right">
              <div class="medium-width-180px">
                <h6>Learn to Drive</h6>
                <ul class="list-unstyled">
                  <li>
                    <a class="button yellow small" title="Book online" href="/instructors">Book online</a>
                  </li>
                  <li>
                    <a title="Driving Lessons" href="/driving-lessons">Driving Lessons</a>
                  </li>
                  <li>
                    <a title="Test Packages" href="/driving-lessons/test-package">Test Packages</a>
                  </li>
                  <li>
                    <a title="Gift Vouchers" href="/driving-lessons/gift-voucher">Gift Vouchers</a>
                  </li>
                  <li>
                    <a title="Refresher Driving Lessons" href="/driving-lessons/refresher-driving-lessons">Refresher
                      Driving Lessons</a>
                  </li>
                  <li>
                    <a title="International Driver’s Licence Conversions"
                      href="/driving-lessons/international-drivers-licence-conversions">International Driver’s Licence
                      Conversions</a>
                  </li>
                </ul>
              </div>
            </div>
          </div>
          <hr />
          <div class="row small-fontsize-13">
            <div class="medium-8 columns small-margin-top-8">
              <ul class="list-inline legal-links">
                <li>Ez Licence Pty Ltd &copy; 2023</li>
                <li><a href="/privacy-policy">Privacy Policy</a></li>
                <li>
                  <a href="/terms-and-conditions-learners">Terms and Conditions</a>
                </li>
              </ul>
            </div>
            <div class="medium-4 columns small-margin-top-10 medium-margin-top-0">
              <ul class="list-inline medium-text-right">
                <li>
                  <a href="https://www.facebook.com/ezlicence/" rel="noopener" target="_blank"
                    title="EzLicence Facebook"><svg class="svg-inline--fa fa-facebook fa-w-16 fa-2x" aria-hidden="true"
                      focusable="false" data-prefix="fab" data-icon="facebook" role="img"
                      xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" data-fa-i2svg="">
                      <path fill="currentColor"
                        d="M504 256C504 119 393 8 256 8S8 119 8 256c0 123.78 90.69 226.38 209.25 245V327.69h-63V256h63v-54.64c0-62.15 37-96.48 93.67-96.48 27.14 0 55.52 4.84 55.52 4.84v61h-31.28c-30.8 0-40.41 19.12-40.41 38.73V256h68.78l-11 71.69h-57.78V501C413.31 482.38 504 379.78 504 256z">
                      </path>
                    </svg><!-- <i class="fab fa-facebook fa-2x" aria-hidden="true"></i> Font Awesome fontawesome.com --></a>
                </li>
                <li>
                  <a href="https://www.instagram.com/ezlicence/" rel="noopener" target="_blank"
                    title="EzLicence Instagram"><svg class="svg-inline--fa fa-instagram fa-w-14 fa-2x"
                      aria-hidden="true" focusable="false" data-prefix="fab" data-icon="instagram" role="img"
                      xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512" data-fa-i2svg="">
                      <path fill="currentColor"
                        d="M224.1 141c-63.6 0-114.9 51.3-114.9 114.9s51.3 114.9 114.9 114.9S339 319.5 339 255.9 287.7 141 224.1 141zm0 189.6c-41.1 0-74.7-33.5-74.7-74.7s33.5-74.7 74.7-74.7 74.7 33.5 74.7 74.7-33.6 74.7-74.7 74.7zm146.4-194.3c0 14.9-12 26.8-26.8 26.8-14.9 0-26.8-12-26.8-26.8s12-26.8 26.8-26.8 26.8 12 26.8 26.8zm76.1 27.2c-1.7-35.9-9.9-67.7-36.2-93.9-26.2-26.2-58-34.4-93.9-36.2-37-2.1-147.9-2.1-184.9 0-35.8 1.7-67.6 9.9-93.9 36.1s-34.4 58-36.2 93.9c-2.1 37-2.1 147.9 0 184.9 1.7 35.9 9.9 67.7 36.2 93.9s58 34.4 93.9 36.2c37 2.1 147.9 2.1 184.9 0 35.9-1.7 67.7-9.9 93.9-36.2 26.2-26.2 34.4-58 36.2-93.9 2.1-37 2.1-147.8 0-184.8zM398.8 388c-7.8 19.6-22.9 34.7-42.6 42.6-29.5 11.7-99.5 9-132.1 9s-102.7 2.6-132.1-9c-19.6-7.8-34.7-22.9-42.6-42.6-11.7-29.5-9-99.5-9-132.1s-2.6-102.7 9-132.1c7.8-19.6 22.9-34.7 42.6-42.6 29.5-11.7 99.5-9 132.1-9s102.7-2.6 132.1 9c19.6 7.8 34.7 22.9 42.6 42.6 11.7 29.5 9 99.5 9 132.1s2.7 102.7-9 132.1z">
                      </path>
                    </svg><!-- <i class="fab fa-instagram fa-2x" aria-hidden="true"></i> Font Awesome fontawesome.com --></a>
                </li>
                <li>
                  <a href="https://twitter.com/ezlicence" rel="noopener" target="_blank" title="EzLicence Twitter"><svg
                      class="svg-inline--fa fa-twitter fa-w-16 fa-2x" aria-hidden="true" focusable="false"
                      data-prefix="fab" data-icon="twitter" role="img" xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 512 512" data-fa-i2svg="">
                      <path fill="currentColor"
                        d="M459.37 151.716c.325 4.548.325 9.097.325 13.645 0 138.72-105.583 298.558-298.558 298.558-59.452 0-114.68-17.219-161.137-47.106 8.447.974 16.568 1.299 25.34 1.299 49.055 0 94.213-16.568 130.274-44.832-46.132-.975-84.792-31.188-98.112-72.772 6.498.974 12.995 1.624 19.818 1.624 9.421 0 18.843-1.3 27.614-3.573-48.081-9.747-84.143-51.98-84.143-102.985v-1.299c13.969 7.797 30.214 12.67 47.431 13.319-28.264-18.843-46.781-51.005-46.781-87.391 0-19.492 5.197-37.36 14.294-52.954 51.655 63.675 129.3 105.258 216.365 109.807-1.624-7.797-2.599-15.918-2.599-24.04 0-57.828 46.782-104.934 104.934-104.934 30.213 0 57.502 12.67 76.67 33.137 23.715-4.548 46.456-13.32 66.599-25.34-7.798 24.366-24.366 44.833-46.132 57.827 21.117-2.273 41.584-8.122 60.426-16.243-14.292 20.791-32.161 39.308-52.628 54.253z">
                      </path>
                    </svg><!-- <i class="fab fa-twitter fa-2x" aria-hidden="true"></i> Font Awesome fontawesome.com --></a>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </footer>
    </div>


    <div class="help-wrap" @click="isShowHelp = true">
      <div>
        <button data-testid="launcher" aria-label="帮助" class="help-btn">
          <span data-testid="Icon"
            class="container-2zrgf u-userColor icon-3CF6U Icon-1QudM Arrange-sizeFit u-textInheritColor u-inlineBlock Icon mobile-22a4Y is-mobile"
            type="Icon"><svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px"
              y="0px" width="20px" height="20px" viewBox="0 0 20 20" xml:space="preserve" aria-hidden="true">
              <g></g>
              <g></g>
              <g></g>
              <g>
                <g>
                  <g>
                    <path
                      d="M11,12.3V13c0,0-1.8,0-2,0v-0.6c0-0.6,0.1-1.4,0.8-2.1c0.7-0.7,1.6-1.2,1.6-2.1c0-0.9-0.7-1.4-1.4-1.4 c-1.3,0-1.4,1.4-1.5,1.7H6.6C6.6,7.1,7.2,5,10,5c2.4,0,3.4,1.6,3.4,3C13.4,10.4,11,10.8,11,12.3z">
                    </path>
                    <circle cx="10" cy="15" r="1"></circle>
                  </g>
                  <path
                    d="M10,2c4.4,0,8,3.6,8,8s-3.6,8-8,8s-8-3.6-8-8S5.6,2,10,2 M10,0C4.5,0,0,4.5,0,10s4.5,10,10,10s10-4.5,10-10S15.5,0,10,0 L10,0z">
                  </path>
                </g>
              </g>
            </svg></span><span class="help-label" v-if="!isPhone" data-testid="launcher-label">帮助</span>
        </button>
      </div>
    </div>
    <div v-if="isShowHelp" class="help-from" :class="isPhone ? 'help-from-mobile' : 'help-from-pc'">
      <div class="from-wrap">
        <div class="from-wrap-header">
          <button v-if="isShowForm" @click="isShowForm = false" type="button"
            class="sc-htpNat gtoymc sc-EHOje hssBvG"><svg xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="13px" height="10px" viewBox="0 0 13 9"
              xml:space="preserve" data-garden-id="buttons.icon" data-garden-version="8.13.0" theme="[object Object]"
              class="sc-bwzfXH hDrfMZ styles__StyledBackIcon-sc-zoeqtl-0 iWmNMo">
              <g></g>
              <g></g>
              <g></g>
              <g>
                <path
                  d="M12,4H3.4l2.3-2.3c0.4-0.4,0.4-1,0-1.4s-1-0.4-1.4,0l-4,4C0.2,4.4,0.1,4.5,0.1,4.6C0,4.9,0,5.1,0.1,5.4 c0.1,0.1,0.1,0.2,0.2,0.3l4,4C4.5,9.9,4.7,10,5,10s0.5-0.1,0.7-0.3c0.4-0.4,0.4-1,0-1.4L3.4,6H12c0.6,0,1-0.4,1-1S12.6,4,12,4z">
                </path>
              </g>
            </svg></button>
          <h1 class="lEoZF">给我们留言</h1>
          <button @click="isShowHelp = false" type="button" class="sc-htpNat gtoymc sc-EHOje hssBvG"><svg
              xmlns="http://www.w3.org/2000/svg" width="16" height="16" focusable="false" viewBox="0 0 16 16"
              data-testid="Icon--dash" data-garden-id="buttons.icon" data-garden-version="8.13.0"
              theme="[object Object]" class="sc-bwzfXH hDrfMZ">
              <path stroke="currentColor" stroke-linecap="round" stroke-width="2" d="M3 8h10"></path>
            </svg></button>
        </div>
        <template v-if="!isShowForm">
          <div class="from-wrap-main">
            <h2 class="iNnKBF">请选择问题</h2>
            <ul>
              <li v-for="(val, idx) in [
                  'I am a Learner Driver',
                  'I am a Driving Instructor',
                  'I am a Driving Instructor interested in joining EzLicence',
                  'I am interested in becoming a Driving EzLicence',
                  'I have a Media / PR enquiry'
                ]" :key="idx" @click="getCurHeloStr(val)"><button
                  class="styles__Button-sc-1hxfrny-0 dynvPd">{{val}}</button></li>
            </ul>
          </div>
          <div class="from-wrap-footer">
            <a href="https://www.zendesk.com/embeddables/?utm_source=webwidget&amp;utm_medium=poweredbyzendesk&amp;utm_campaign=image"
              target="_blank" class="ZendeskLogo__Link-sc-151i2mf-0 hSqSwo">zendesk</a>
          </div>
        </template>
        <div class="ctpnMq" v-else>
          <div class="fMlLlM">{{curHeloStr}}</div>

          <div class="styles__Fields-sc-cb953b-1 gJkjOz">
            <div>
              <div data-garden-id="forms.field" data-garden-version="8.49.4" class="StyledField-sc-12gzfsu-0 bJlzcx">
                <label data-garden-id="forms.input_label" data-garden-version="8.49.4" id="31val-field_1.3.10--label"
                  for="31val-field_1.3.10--input" data-garden-container-id="containers.field"
                  data-garden-container-version="1.3.10" data-fieldid="name"
                  class="styles__FormLabel-sc-1hkyxd5-0 kskvjZ StyledLabel-sc-2utmsz-0 bYrRLL">
                  <div>
                    <strong>姓名</strong>
                  </div>
                </label>
                <input data-garden-id="forms.input" data-garden-version="8.49.4" aria-invalid="false"
                  id="31val-field_1.3.10--input" aria-labelledby="31val-field_1.3.10--label"
                  aria-describedby="31val-field_1.3.10--hint" name="name" required="" type="text"
                  class="StyledTextInput-sc-k12n8x-0 jsIKFI" value="" />
              </div>
            </div>
            <div>
              <div data-garden-id="forms.field" data-garden-version="8.49.4" class="StyledField-sc-12gzfsu-0 bJlzcx">
                <label data-garden-id="forms.input_label" data-garden-version="8.49.4" id="32val-field_1.3.10--label"
                  for="32val-field_1.3.10--input" data-garden-container-id="containers.field"
                  data-garden-container-version="1.3.10" data-fieldid="email"
                  class="styles__FormLabel-sc-1hkyxd5-0 kskvjZ StyledLabel-sc-2utmsz-0 bYrRLL">
                  <div>
                    <strong>电邮地址</strong>
                  </div>
                </label>
                <input data-garden-id="forms.input" data-garden-version="8.49.4" aria-invalid="false"
                  id="32val-field_1.3.10--input" aria-labelledby="32val-field_1.3.10--label"
                  aria-describedby="32val-field_1.3.10--hint" name="email" required="" type="email"
                  class="StyledTextInput-sc-k12n8x-0 jsIKFI" value="" />
              </div>
            </div>
            <div>
              <div role="presentation" tabindex="-1">
                <div data-garden-id="forms.field" data-garden-version="8.49.4" class="StyledField-sc-12gzfsu-0 bJlzcx">
                  <label data-garden-id="forms.input_label" data-garden-version="8.49.4" id="downshift-1-label"
                    for="downshift-1-input" data-garden-container-id="containers.field"
                    data-garden-container-version="1.3.10" data-fieldid="key:9991869759641"
                    class="styles__FormLabel-sc-1hkyxd5-0 kskvjZ StyledLabel-sc-2utmsz-0 bYrRLL">
                    <div>
                      <strong>Choose your type of enquiry below</strong>
                    </div>
                  </label>
                  <el-select style="width: 100%; margin-bottom:20px;" v-model="helpForm.type"
                    placeholder="please select your zone">
                    <el-option label="Zone one" value="shanghai" />
                    <el-option label="Zone two" value="beijing" />
                  </el-select>
                </div>
              </div>
            </div>
            <div>
              <div data-garden-id="forms.field" data-garden-version="8.49.4" class="StyledField-sc-12gzfsu-0 bJlzcx">
                <label data-garden-id="forms.input_label" data-garden-version="8.49.4" id="34val-field_1.3.10--label"
                  for="34val-field_1.3.10--input" data-garden-container-id="containers.field"
                  data-garden-container-version="1.3.10" data-fieldid="subject"
                  class="styles__FormLabel-sc-1hkyxd5-0 kskvjZ StyledLabel-sc-2utmsz-0 bYrRLL">
                  <div>
                    <strong>Subject or topic</strong>
                  </div>
                </label>
                <input data-garden-id="forms.input" data-garden-version="8.49.4" aria-invalid="false"
                  id="34val-field_1.3.10--input" aria-labelledby="34val-field_1.3.10--label"
                  aria-describedby="34val-field_1.3.10--hint" name="subject" required="" type="text"
                  class="StyledTextInput-sc-k12n8x-0 jsIKFI" value="" />
              </div>
            </div>
            <div>
              <div role="presentation" tabindex="-1">
                <div data-garden-id="forms.field" data-garden-version="8.49.4" class="StyledField-sc-12gzfsu-0 bJlzcx">
                  <label data-garden-id="forms.input_label" data-garden-version="8.49.4" id="downshift-4-label"
                    for="downshift-4-input" data-garden-container-id="containers.field"
                    data-garden-container-version="1.3.10" data-fieldid="key:10074955827737"
                    class="styles__FormLabel-sc-1hkyxd5-0 kskvjZ StyledLabel-sc-2utmsz-0 bYrRLL">
                    <div>
                      <strong>Please categorise the reason for getting in touch</strong>
                    </div>
                  </label>
                  <div data-garden-id="dropdowns.faux_input" data-garden-version="8.49.4" aria-invalid="false"
                    tabindex="0" role="button" aria-haspopup="true" data-toggle="true" data-testid="dropdown-field"
                    name="key:10074955827737"
                    class="StyledTextInput-sc-k12n8x-0 styles__DropdownSelect-sc-tgua31-0 ctBQaH StyledFauxInput-sc-1l592ed-0 kaEIfG StyledTextFauxInput-sc-yqw7j9-0 eFJONy">
                    <div data-garden-id="dropdowns.select" data-garden-version="8.49.4"
                      class="StyledSelect-sc-xifmwj-0 eSliJF">
                      -
                    </div>
                    <input data-garden-id="dropdowns.input" data-garden-version="8.49.4" aria-invalid="false"
                      id="downshift-4-input" aria-labelledby="downshift-4-label"
                      aria-describedby="232val-field_1.3.10--hint" aria-autocomplete="list" autocomplete="off"
                      readonly="" tabindex="-1"
                      class="StyledInput-sc-hzhvmp-0 dcmoVt StyledTextInput-sc-k12n8x-0 kFSjuy" value="" />
                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" focusable="false" viewbox="0 0 16 16"
                      aria-hidden="true" data-garden-id="forms.media_figure" data-garden-version="8.49.4"
                      class="StyledTextMediaFigure-sc-1qepknj-0 lnDzQq">
                      <path fill="currentColor"
                        d="M12.688 5.61a.5.5 0 01.69.718l-.066.062-5 4a.5.5 0 01-.542.054l-.082-.054-5-4a.5.5 0 01.55-.83l.074.05L8 9.359l4.688-3.75z">
                      </path>
                    </svg>
                  </div>
                </div>
                <div data-garden-id="dropdowns.menu_wrapper" data-garden-version="8.49.4"
                  class="StyledMenuWrapper-sc-tiwdxz-0 hPndRc"
                  style="position: absolute; top: 0px; left: 0px; opacity: 0; pointer-events: none;">
                  <ul data-garden-id="dropdowns.menu" data-garden-version="8.49.4"
                    class="StyledMenu-sc-1vpttfd-0 deFHct" role="listbox" aria-labelledby="downshift-4-label"
                    id="downshift-4-menu" data-testid="dropdown-options"></ul>
                </div>
              </div>
            </div>

            <div>
              <div data-garden-id="forms.field" data-garden-version="8.49.4" class="StyledField-sc-12gzfsu-0 bJlzcx">
                <label data-garden-id="forms.input_label" data-garden-version="8.49.4" id="35val-field_1.3.10--label"
                  for="35val-field_1.3.10--input" data-garden-container-id="containers.field"
                  data-garden-container-version="1.3.10" data-fieldid="description"
                  class="styles__FormLabel-sc-1hkyxd5-0 kskvjZ StyledLabel-sc-2utmsz-0 bYrRLL">
                  <div>
                    <strong>Tell us more, providing as much detail as you can will allow us to help you as quickly as
                      possible. *</strong>
                  </div>
                </label>
                <div data-garden-id="forms.input_hint" data-garden-version="8.49.4" id="35val-field_1.3.10--hint"
                  class="Hint-sc-15a6xtc-0 kKpfjY StyledHint-sc-17c2wu8-0 hTKgDl">
                  Some information you include in your message may be considered sensitive by some privacy laws. By
                  submitting your request, you give us consent to process any sensitive information included in your
                  enquiry. For more information, please refer to our Privacy Policy.
                </div>
                <textarea data-garden-id="forms.textarea" data-garden-version="8.49.4" aria-invalid="false"
                  id="35val-field_1.3.10--input" aria-labelledby="35val-field_1.3.10--label"
                  aria-describedby="35val-field_1.3.10--hint" rows="5" name="description" required=""
                  class="StyledTextInput-sc-k12n8x-0 StyledTextarea-sc-wxschl-0 jywVgl"></textarea>
              </div>
            </div>

            <div>
              <div data-garden-id="forms.field" data-garden-version="8.49.4" data-testid="attachment-list-container"
                class="styles__Container-sc-1af6jqh-0 iMpSSB StyledField-sc-12gzfsu-0 bJlzcx">
                <label id="36val-field_1.3.10--label" for="file-input"
                  class="styles__StyledLabel-sc-1af6jqh-1 gfCpVw StyledLabel-sc-2utmsz-0 bYrRLL">附件</label>
                <button type="button" id="dropzone-input" @click="handleClickFile"
                  class="styles__AttachmentButton-sc-o76a7f-0 kEOBdL">
                  <div class="styles__Description-sc-o76a7f-1 eiBYcC">
                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" focusable="false" viewbox="0 0 16 16"
                      class="styles__Icon-sc-o76a7f-3 jdAgtb">
                      <path fill="none" stroke="currentColor" stroke-linecap="round"
                        d="M9.5 4v7.7c0 .8-.7 1.5-1.5 1.5s-1.5-.7-1.5-1.5V3C6.5 1.6 7.6.5 9 .5s2.5 1.1 2.5 2.5v9c0 1.9-1.6 3.5-3.5 3.5S4.5 13.9 4.5 12V4">
                      </path>
                    </svg>
                    <div id="attachmentButtonDescription" class="styles__Label-sc-o76a7f-2 blfOQk">
                      最多可添加 5 个文件
                    </div>
                  </div>
                </button>
                <input id="file-input" type="file" multiple="" data-testid="dropzone-input"
                  class="styles__HiddenInput-sc-ty3c29-0 iquIjP" />
              </div>
            </div>
          </div>
          <footer class="FooterView-sc-101yy6s-0 yKsqd">
            <div class="styles__Container-sc-1ifgvkh-0 itjVyT">
              <a data-testid="Icon--zendesk"
                href="https://www.zendesk.com/embeddables/?utm_source=webwidget&amp;utm_medium=poweredbyzendesk&amp;utm_campaign=image"
                target="_blank" class="ZendeskLogo__Link-sc-151i2mf-0 hSqSwo">
                zendesk
              </a>
              <button data-garden-id="buttons.button" data-garden-version="8.13.0" type="submit" data-testid="button-ok"
                class="sc-htpNat hzziHz">发送</button>
            </div>
          </footer>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import {
    computed,
    ref,
    reactive,
    onMounted
  } from "vue";
  import videojs from "video.js";
  import "videojs-youtube";
  import "video.js/dist/video-js.css";
  export default {
    setup() {
      const isShowForm = ref(false)
      const isShowHelp = ref(false)
      const curHeloStr = ref('I am a Learner Driver')
      const helpForm = reactive({
        name: '',
        address: '',
        type: '',
        topic: '',
        des: '',
        file: ''
      })
      let startX = 0;
      let startY = 0;
      const videoRef = ref(null);
      const isInitVideo = ref(false);
      const curIdx = ref(0);
      const isOpen = ref(false);
      const isShowSelect1 = ref(false);
      const isShowSelect2 = ref(false);
      const list = ref(Array(10).fill("1"));
      const searchData = ref([]);
      const selectMode = ref(1);
      const videoJSOptions = {
        autoplay: "muted",
        controls: true,
        userActions: {
          hotkeys: true
        },
        playbackRates: [0.5, 1, 1.5, 2],
        poster: "https://www.ezlicence.com.au/assets/image-how-ezlicence-works-415d08b55319a406f603278be7ad21087314f9cfeeb03ce7d455798611ec9b27.png",
        controlBar: {
          children: [
            "playToggle",
            "progressControl",
            "volumePanel",
            "qualitySelector",
            "fullscreenToggle"
          ]
        },
        width: "100%",
        height: "350px",
        sources: [{
          type: "video/youtube",
          src: "https://www.youtube.com/watch?v=evUfG3lrk5U&ab_channel=Veritasium"
        }],
        techOrder: ["youtube", "vimeo", "flash"]
      };

      const initVideo = () => {
        if (videoRef.value) {
          const player = videojs(videoRef.value, videoJSOptions, () => {
            // player.play();
          });
        }
      };

      const getCurHeloStr = str => {
        curHeloStr.value = str
        isShowForm.value = true
      }

      const handleClickFile = () => {
        document.getElementById('file-input').click()
      }

      const handleShowSelect = id => {
        if (id === 1) {
          isShowSelect1.value = true;
          isShowSelect2.value = false;
        } else {
          isShowSelect2.value = true;
          isShowSelect1.value = false;
        }
      };

      const handleCloseAll = () => {
        isShowSelect1.value && (isShowSelect1.value = false);
        isShowSelect2.value && (isShowSelect2.value = false);
      };

      const handleClickDot = idx => {
        curIdx.value = idx;
      };

      const setDotActClass = idx => {
        return idx === curIdx.value ? "active" : "";
      };

      const isPhone = computed(() => {
        return /Mobi|Android|iPhone/i.test(navigator.userAgent);
      });

      const getOwlStyle = computed(() => {
        return {
          transform: `translate3d(-${curIdx.value * 310}px, 0px, 0px)`,
          transition: "all 0.25s ease 0s",
          width: list.value.length * 310 + "px"
        };
      });

      const getSlideAngle = (dx, dy) => {
        return (Math.atan2(dy, dx) * 180) / Math.PI;
      };

      const getSlideDirection = (startX, startY, endX, endY) => {
        let dy = endY - startY;
        let dx = endX - startX;
        let result = 0;
        if (Math.abs(dx) < 2 && Math.abs(dy) < 2) {
          return result;
        }
        const angle = getSlideAngle(dx, dy);
        if (angle >= -45 && angle < 45) {
          result = 4;
        } else if (angle >= 45 && angle < 135) {
          result = 1;
        } else if (angle >= -135 && angle < -45) {
          result = 2;
        } else if (
          (angle >= 135 && angle <= 180) ||
          (angle >= -180 && angle < -135)
        ) {
          result = 3;
        }
        return result;
      };

      const changeSlide = (startX, startY, endX, endY) => {
        const direction = getSlideDirection(startX, startY, endX, endY);

        switch (direction) {
          case 0:
            console.log("没滑动");
            break;
          case 3:
            console.log("向左", list.value.length - 1, curIdx.value);
            if (list.value.length - 1 <= curIdx.value) return;
            curIdx.value += 1;
            break;
          case 4:
            console.log("向右");
            if (curIdx.value === 0) return;
            curIdx.value -= 1;
            break;
          default:
        }
      };

      const onTouchStart = e => {
        e.preventDefault();
        startX = e.changedTouches[0].pageX;
        startY = e.changedTouches[0].pageY;
      };
      const onTouchEnd = e => {
        const endX = e.changedTouches[0].pageX;
        const endY = e.changedTouches[0].pageY;
        changeSlide(startX, startY, endX, endY);
      };

      const onMousedown = e => {
        e.preventDefault();
        startX = e.pageX;
        startY = e.pageY;
      };
      const onMouseup = e => {
        const endX = e.pageX;
        const endY = e.pageY;
        changeSlide(startX, startY, endX, endY);
      };

      const onSearch = val => {
        const data = val.srcElement.value;
        // tood..搜索内容赋值
        searchData.value = [];
        console.log("val", data);
      };

      onMounted(() => {
        initVideo();
        // console.log("list->", list.value);
      });

      return {
        onTouchStart,
        onTouchEnd,
        onMousedown,
        onMouseup,
        onSearch,
        handleClickDot,
        handleShowSelect,
        handleCloseAll,
        handleClickFile,
        setDotActClass,
        getOwlStyle,
        list,
        searchData,
        videoRef,
        isInitVideo,
        isOpen,
        isShowSelect1,
        isShowSelect2,
        isPhone,
        helpForm,
        curHeloStr,
        isShowForm,
        isShowHelp,
        getCurHeloStr
      };
    }
  };
</script>

<style lang="scss" scoped>
  .lp-center {
    margin: 0 auto;
  }

  ::v-deep .accordion-navigation-other.el-collapse-item__header {
    background: #f6f6f6;
    height: 100%;
  }

  ::v-deep .accordion-navigation-other.el-collapse-item__header>a {
    font-family: "Roboto", sans-serif;
    font-size: 1rem;
    padding: 0.625rem 1.25rem 0.625rem 0.3125rem;
  }

  ::v-deep .accordion-navigation .el-collapse-item__header {
    background: #f6f6f6;
    height: 100%;
  }

  ::v-deep .accordion-navigation .el-collapse-item__wrap {
    background: #f6f6f6;
  }

  ::v-deep .accordion-navigation .el-collapse-item__header>a {
    font-family: "Roboto", sans-serif;
    font-size: 1rem;
    padding: 0.625rem 1.25rem 0.625rem 0.3125rem;
  }

  ::v-deep .accordion-navigation .el-collapse-item__content {
    background-color: #f6f6f6;
    /* 设置背景色 */
  }

  ::v-deep .el-input__wrapper {
    margin-top: 1.14286rem;
  }

  ::v-deep .el-input__wrapper {
    height: 43px;
  }

  .help-wrap {
    position: fixed;
    right: 20px;
    bottom: 20px;
    z-index: 199;

    .help-btn {
      display: flex;
      background-color: #ffc20e !important;
      color: #675110 !important;
      fill: #675110 !important;
      padding: 0.92857rem 1.57143rem;
      border-radius: 999rem;
      bottom: 0;
      letter-spacing: 0.6;
      font-size: 1.07143rem;
      align-items: center;

      .help-label {
        vertical-align: middle;
        font-size: 1.07143rem;
        padding-left: 10px;
      }
    }
  }

  .help-from {
    height: 100%;
    width: 100%;
    padding: 1.14286rem;

    .from-wrap {
      display: flex;
      flex-direction: column;
      box-sizing: border-box;
      color: rgb(47, 57, 65);
      height: 100%;
      width: 100%;
      max-width: 100vw;
      position: relative;
      overflow: hidden;
      background-color: rgb(255, 255, 255);
      box-shadow: rgba(0, 0, 0, 0.2) 0px 0px 0.428571rem 0px;
      border-radius: 0.571429rem;

      .from-wrap-header {
        display: flex;
        align-items: center;
        padding: 0.571429rem 1rem;
        background: rgb(255, 194, 14) !important;
        color: rgb(103, 81, 16) !important;

        .gtoymc {
          width: 2rem;
          height: 2rem;
          flex-shrink: 0;
        }

        [type=button],
        [type=reset],
        [type=submit],
        button {
          -webkit-appearance: button;
        }

        .hssBvG {
          display: inline-flex;
          -webkit-box-align: center;
          align-items: center;
          -webkit-box-pack: center;
          justify-content: center;
          transition: border-color 0.25s ease-in-out 0s, box-shadow 0.1s ease-in-out 0s, background-color 0.25s ease-in-out 0s, color 0.25s ease-in-out 0s;
          margin: 0px;
          border-radius: 4px;
          cursor: pointer;
          overflow: hidden;
          text-decoration: none;
          text-overflow: ellipsis;
          white-space: nowrap;
          font-family: inherit;
          font-weight: 400;
          -webkit-font-smoothing: subpixel-antialiased;
          box-sizing: border-box;
          user-select: none;
          height: 32px;
          line-height: 30px;
          font-size: 12px;
          background-color: transparent;
          border: none;
          padding: 0px;
          width: 32px;
          color: rgb(104, 115, 125);
        }

        // .goJWmE .Title-sc-10f4djx-0:nth-last-child(2) {
        //   margin-right: 2rem;
        // }
        .lEoZF {
          font-weight: 700;
          text-align: center;
          letter-spacing: 0.0214286rem;
          line-height: 1.5;
          font-size: 1.07143rem;
          -webkit-box-flex: 1;
          flex-grow: 1;
          margin-bottom: 2px;
        }
      }

      .from-wrap-main {
        -webkit-box-flex: 2;
        flex-grow: 2;
        padding-top: 1.07143rem;
        padding-left: 0.714286rem;
        padding-right: 1.07143rem;
        margin-left: 0.714286rem;
        margin-right: 0.357143rem;
        overflow: hidden auto;
        height: 100%;

        &:first-child {
          padding-bottom: 2.14rem
        }

        .fMlLlM {
          margin-bottom: 0.714286rem !important;
        }

        .iNnKBF {
          border-bottom: 0.0785714rem solid rgb(233, 235, 237);
          padding-bottom: 1.14286rem;
          color: rgb(47, 57, 65);
          font-size: 1rem;
          font-weight: 700;
          padding-left: 0.857143rem !important;
          padding-right: 0.857143rem !important;
        }

        ol,
        ul {
          margin: 0;
          list-style: none;
          padding: 0;
        }

        li {
          display: list-item;
          text-align: -webkit-match-parent;
        }

        .jEmvsT {
          display: flex;
          flex-direction: column;
          box-sizing: border-box;
          color: rgb(47, 57, 65);
          height: 100%;
          width: 100%;
          max-width: 100vw;
          position: relative;
          overflow: hidden;
          background-color: rgb(255, 255, 255);
          box-shadow: rgba(0, 0, 0, 0.2) 0px 0px 0.428571rem 0px;
          border-radius: 0.571429rem;
        }

        .dynvPd {
          border-width: 0px 0px 0.0785714rem;
          border-top-style: initial;
          border-right-style: initial;
          border-left-style: initial;
          border-top-color: initial;
          border-right-color: initial;
          border-left-color: initial;
          border-image: initial;
          border-bottom-style: solid;
          border-bottom-color: rgb(233, 235, 237);
          line-height: 1.28571;
          list-style: none;
          display: block;
          width: 100%;
          text-align: start;
          background-color: transparent;
          text-decoration-color: rgb(255, 194, 14) !important;
          padding: 1.28571rem 0.857143rem !important;
        }

        button,
        html input[type="button"],
        input[type="reset"],
        input[type="submit"] {
          -webkit-appearance: button;
          cursor: pointer;
          color: #333;
        }

        button:hover {
          background-color: #fafafa;
          text-decoration: yellow
        }
      }

      .from-wrap-footer {
        padding: 0.714286rem 1.42857rem;
        border-top: 0.0785714rem solid rgb(233, 235, 237);
        box-shadow: rgba(0, 0, 0, 0.08) 0px -0.0714286rem 0.857143rem;

        .hSqSwo {
          display: inline-block;
          color: #333;
          text-decoration: none;
          text-align: center;
          display: flex;
          align-items: center;
          justify-content: center;
        }
      }

      .iNnKBF {
        margin-bottom: 0.714286rem !important;
      }

      .ctpnMq {
        webkit-box-flex: 2;
        flex-grow: 2;
        padding-top: 1.07143rem;
        padding-left: 0.714286rem;
        padding-right: 1.07143rem;
        margin-left: 0.714286rem;
        margin-right: 0.357143rem;
        overflow: hidden auto;
        height: 100%;
      }

      .jEmvsT {
        display: flex;
        flex-direction: column;
        box-sizing: border-box;
        color: rgb(47, 57, 65);
        height: 100%;
        width: 100%;
        max-width: 100vw;
        position: relative;
        overflow: hidden;
        background-color: rgb(255, 255, 255);
        box-shadow: rgba(0, 0, 0, 0.2) 0px 0px 0.428571rem 0px;
        border-radius: 0.571429rem;
      }

      .bJlzcx {
        position: relative;
        margin: 0px;
        border: 0px;
        padding: 0px;
        font-size: 0px;
      }

      .bYrRLL {
        vertical-align: middle;
        line-height: 1.42857;
        color: rgb(47, 57, 65);
        font-size: 14px;
        font-weight: 600;
      }

      .kskvjZ {
        display: block;
        margin-bottom: 0.428571rem;
        word-break: break-word;
        line-height: 1.42857 !important;
      }

      .bYrRLL {
        vertical-align: middle;
        line-height: 1.42857;
        color: rgb(47, 57, 65);
        font-size: 14px;
        font-weight: 600;
      }

      .hTKgDl {
        display: block;
        vertical-align: middle;
        line-height: 1.42857;
        color: rgb(104, 115, 125);
        font-size: 14px;
      }

      .kKpfjY {
        word-break: break-word;
      }

      .jywVgl {
        margin-top: 10px;
        appearance: none;
        transition: border-color 0.25s ease-in-out 0s, box-shadow 0.1s ease-in-out 0s, background-color 0.25s ease-in-out 0s, color 0.25s ease-in-out 0s, z-index 0.25s ease-in-out 0s;
        border: 1px solid rgb(216, 220, 222);
        border-radius: 4px;
        width: 100%;
        box-sizing: border-box;
        vertical-align: middle;
        font-family: inherit;
        padding: 0.714286em 0.857143em;
        min-height: 40px;
        line-height: 1.28571;
        font-size: 14px;
        background-color: rgb(255, 255, 255);
        color: rgb(47, 57, 65);
        resize: none;
        overflow: auto;
        cursor: auto;
      }

      .kEOBdL:hover {
        background-color: rgb(248, 249, 249) !important;
      }

      [type=button],
      [type=reset],
      [type=submit],
      button {
        -webkit-appearance: button;
      }

      .gfCpVw {
        display: block;
        font-weight: bold !important;
      }

      .bYrRLL {
        vertical-align: middle;
        line-height: 1.42857;
        color: rgb(47, 57, 65);
        font-size: 14px;
        font-weight: 600;
      }

      .kEOBdL {
        border-width: 0.142857rem;
        border-color: rgb(216, 220, 222);
        border-style: dashed;
        border-radius: 0.357143rem;
        background-color: rgb(255, 255, 255);
        opacity: 0.9;
        display: block;
        width: 100%;
        // padding: 1rem 0.714286rem;
        color: rgb(47, 57, 65);
        cursor: pointer !important;
      }

      .eiBYcC {
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center !important;
      }

      .jdAgtb {
        max-width: 100%;
        margin-right: 0.357143rem;
        color: rgb(135, 146, 157);
        min-width: 1.28571rem;
        min-height: 1.28571rem;
        height: 1.28571rem;
        width: 1.28571rem;
      }

      .blfOQk {
        max-width: 100%;
        color: rgb(104, 115, 125);
        display: inline-block !important;
        vertical-align: top !important;
      }

      .iquIjP {
        display: none;
      }

      svg {
        max-height: 100%;
      }

      .yKsqd {
        padding: 1.07143rem 1.42857rem;
        border-top: 0.0785714rem solid rgb(233, 235, 237);
        box-shadow: rgba(0, 0, 0, 0.08) 0px -0.0714286rem 0.857143rem;
      }

      .itjVyT {
        display: flex;
        -webkit-box-pack: justify;
        justify-content: space-between;
        align-items: flex-end;
      }

      .hSqSwo {
        position: relative;
        display: inline-block;
        color: #333;
        text-decoration: none;
      }

      .hzziHz:not([disabled]) {
        background-color: rgb(47, 57, 65) !important;
        color: rgb(255, 255, 255) !important;
        border-color: rgb(47, 57, 65) !important;
      }

      [type=button],
      [type=reset],
      [type=submit],
      button {
        -webkit-appearance: button;
      }

      .hzziHz {
        display: inline-flex;
        -webkit-box-align: center;
        align-items: center;
        -webkit-box-pack: center;
        justify-content: center;
        transition: border-color 0.25s ease-in-out 0s, box-shadow 0.1s ease-in-out 0s, background-color 0.25s ease-in-out 0s, color 0.25s ease-in-out 0s;
        margin: 0px;
        border: 1px solid transparent;
        border-radius: 4px;
        cursor: pointer;
        text-decoration: none;
        font-family: inherit;
        font-weight: 400;
        -webkit-font-smoothing: subpixel-antialiased;
        box-sizing: border-box;
        user-select: none;
        padding: 0px 1.07143em;
        font-size: 14px;
        background-color: rgb(104, 115, 125);
        color: rgb(255, 255, 255);
        height: 2.71429rem !important;
        white-space: nowrap !important;
        overflow: hidden !important;
        text-overflow: ellipsis !important;
        line-height: 2.57143rem !important;
      }
    }
  }

  .help-from-pc {
    width: 374px;
    max-height: calc(100vh - 32px);
    height: 572px;
    position: fixed;
    opacity: 1;
    border: 0px;
    transition-duration: 250ms;
    transition-timing-function: cubic-bezier(0.645, 0.045, 0.355, 1);
    transition-property: opacity, top, bottom;
    z-index: 1999;
    right: 0px;
    bottom: 0px;
  }

  .help-from-mobile {
    width: 100%;
    height: 100%;
    position: fixed;
    opacity: 1;
    border: 0px;
    transition-duration: 250ms;
    transition-timing-function: cubic-bezier(0.645, 0.045, 0.355, 1);
    transition-property: opacity, top, bottom;
    z-index: 1999;
    top: 0px;
    left: 0px;
    padding: 0
  }

  @import url("./font.css");
  @import url("./svg.css");
  @import url("./justreview.css");
  @import url("./common.css");
</style>