# Sidebar Toggle for SB Admin 2

Sidebar with toggle option for sb admin 2. The required dependent startbootstrap libraries are not part of the download. All the required libraries are added using `bower` package manager under the folder `startbootstrap-sb-admin-2-sidebar-toggle\assets\bower'. 

## Getting Started

To run this demo application

+ Download the latest release the project on [startbootstrap-sb-admin-2-sidebar-toggle](https://github.com/pramod-rathod-avalara/startbootstrap-sb-admin-2-sidebar-toggle).

+ Unzip the archive.

+  You will need to issue the below commands form the root folder of the project i.e. 'startbootstrap-sb-admin-2-sidebar-toggle' in order to run the demo.
		
	1. This step is must and should run successfully.

			$ bower install  		

	2. This step is optional. Check the step 3.

			$ python -m SimpleHTTPServer

	3. If you do not have `python` installed, simply open `index.html` into a browser.

## Usage

#### Add references to required CSS and JS files 

1. startbootstrap SB Admin specific CSS and JS files. Please check here [SB Admin 2](https://github.com/IronSummitMedia/startbootstrap-sb-admin-2)

2. sbadmin2-sidebar-toggle.css 

```html
<link href="./sbadmin2-sidebar-toggle.css" rel="stylesheet" type="text/css">
```

#### Add required HTML Markup

```html

<div id="wrapper" class="toggled">
	<nav class="navbar navbar-default navbar-static-top" role="navigation" style="margin-bottom: 0">

		 <ul class="nav navbar-top-links navbar-right">
            <li>
            	<!--menu toggle button -->
                <button id="menu-toggle" type="button" data-toggle="button" class="btn btn-default btn-xs">
                    <i class="fa fa-exchange fa-fw"></i>
                </button>
            </li>
        </ul>
            

		<!-- Sidebar wrapper over SB Admin 2 sidebar -->
	 	<div id="sidebar-wrapper">

            <div class="navbar-default sidebar" role="navigation">

            	 <div class="sidebar-nav navbar-collapse">

                     <ul class="nav in" id="side-menu">
                     	
                     	 <li class="sidebar-search">

                            <a href="index.html" class="active"><i class="fa fa-dashboard fa-fw"></i> 

                            	<!-- Things to be hidden on toggled are encolsed with masked -->
                                <span class="masked">
                                    Dashboard
                                </span>    
                            </a>

	                    </li>

            		</ul>	
            </div>

        </div>

    </nav>

    <div id="page-wrapper" style="min-height: 158px;">
    </div>	
</div>    

```

#### Add some JavaScript to enable the toggle button


```javascript

 <script type="text/javascript">
    $(document).ready(function() {
        $("#menu-toggle").click(function(e) {
            e.preventDefault();
            
            $("#wrapper").toggleClass("toggled");

            $('#wrapper.toggled').find("#sidebar-wrapper").find(".collapse").collapse('hide');
            
        });
    });
</script>

```