<template>
    <header class="header-global">
        <base-nav class="navbar-main" transparent type="" effect="light" expand>
            <nuxt-link slot="brand" class="navbar-brand mr-lg-5" to="/">
                <img style="width:100%; max-width: 160px; padding-top: 0 !important;" src="/Asset_3.png">
            </nuxt-link>

            <div class="row" slot="content-header" slot-scope="{closeMenu}">
                <div class="col-6 collapse-brand">
                    <nuxt-link to="/">
                        <h3 class="nav-modal-name-plate">Arielle Cerini</h3>
                    </nuxt-link>
                </div>
                <div class="col-6 collapse-close">
                    <close-button @click="closeMenu"></close-button>
                </div>
            </div>

            <ul class="navbar-nav navbar-nav-hover align-items-lg-center">
                <base-dropdown class="nav-item" menu-classes="dropdown-menu-xl">
                    <a slot="title" href="#" class="nav-link" data-toggle="dropdown" role="button">
                        <i class="ni ni-ui-04 d-lg-none"></i>
                        <span class="nav-link-inner--text font-weight-800">Portfolio</span>
                    </a>
                    <div class="dropdown-menu-inner">
                        <nuxt-link to="/design-research"
                           class="media d-flex align-items-center">
                            <!-- <div class="icon icon-shape bg-gradient-primary rounded-circle text-white">
                                <i class="ni ni-laptop"></i>
                            </div> -->
                            <div class="media-body ml-2">
                                <h6 class="heading text-primary mb-md-1">Design Research </h6>
                                <p class="description d-none d-md-inline-block mb-0">View most recent Design Research Projects</p>
                            </div>
                        </nuxt-link>
                        <nuxt-link to="/web-design"
                           class="media d-flex align-items-center">
                            <!-- <div class="icon icon-shape bg-gradient-warning rounded-circle text-white">
                                <i class="ni ni-circle-08"></i>
                            </div> -->
                            <div class="media-body ml-2">
                                <h5 class="heading text-warning mb-md-1">Website Design</h5>
                                <p class="description d-none d-md-inline-block mb-0">Archive of some of the websites that I have worked on.</p>
                            </div>
                        </nuxt-link>
                        
                    </div>
                </base-dropdown>
                <base-dropdown>
                <a slot="title" href="#" class="nav-link" data-toggle="dropdown" role="button">
                        <i class="ni ni-ui-04 d-lg-none"></i>
                        <span class="nav-link-inner--text font-weight-800">Design Blog</span>
                    </a>
                <nuxt-link to="/blog"
                           class="media d-flex align-items-center">
                            <!-- <div class="icon icon-shape bg-gradient-success rounded-circle text-white">
                                <i class="ni ni-book-bookmark"></i>
                            </div> -->
                            <div class="media-body ml-2">
                                <h5 class="heading text-success mb-md-1">Blog</h5>
                                <p class="description d-none d-md-inline-block mb-0">Read my latest posts</p>
                            </div>
                        </nuxt-link>
                </base-dropdown>
                
                
                <base-dropdown class="nav-item" menu-classes="dropdown-menu-xl">
                    <a slot="title" href="#" class="nav-link" data-toggle="dropdown3" role="button">
                        <i class="ni ni-ui-04 d-lg-none"></i>
                        <span class="nav-link-inner--text font-weight-800">Contact Details</span>
                    </a>
                    <div class="dropdown-menu-inner" style="padding: 0;">
                        <a href="mailto:arielle@acerinidesigns.com"
                           class="media d-flex align-items-center nav-link">
                            <!-- <div class="icon icon-shape bg-gradient-success rounded-circle text-white">
                                <i class="ni ni-book-bookmark"></i>
                            </div> -->
                        
                                <h5 class="heading text-success mb-md-1">arielle@acerinidesigns.com</h5>
                           
                        </a>
                    </div>

                    <div class="dropdown-menu-inner" style="padding: 0;">
                        <a href="http://acerinidesigns.com/assets/Arielle_Cerini.pdf"
                           class="media d-flex align-items-center nav-link"
                           target="_blank">
                            <!-- <div class="icon icon-shape bg-gradient-success rounded-circle text-white">
                                <i class="ni ni-book-bookmark"></i>
                            </div> -->
                            
                                <h5 class="heading text-success mb-md-1">Resume</h5>
                        </a>
                    </div>
                    <div class="dropdown-menu-inner" style="padding: 0;">
                        <a href="http://acerinidesigns.com/assets/Arielle_Cerini_cv.pdf"
                           class="media d-flex align-items-center nav-link"
                           target="_blank">
                            <!-- <div class="icon icon-shape bg-gradient-success rounded-circle text-white">
                                <i class="ni ni-book-bookmark"></i>
                            </div> -->
                         
                                <h5 class="heading text-success mb-md-1">CV</h5>
                          
                        </a>
                    </div>
                </base-dropdown>
            </ul>
            <ul class="navbar-nav align-items-lg-center ml-lg-auto">
                <li class="nav-item">
                    <a class="nav-link nav-link-icon" href="https://www.instagram.com/ariellecerini"
                       target="_blank" rel="noopener" data-toggle="tooltip" title="View my artwork">
                        <i class="fab fa-instagram"></i>
                        <span class="nav-link-inner--text d-lg-none">Instagram</span>
                    </a>
                </li>
            </ul>
        </base-nav>
    </header>
</template>
<script>
import BaseNav from "~/components/argon/BaseNav";
import BaseDropdown from "~/components/argon/BaseDropdown";
import CloseButton from "~/components/argon/CloseButton";

export default {
  components: {
    BaseNav,
    CloseButton,
    BaseDropdown
  }
};
</script>