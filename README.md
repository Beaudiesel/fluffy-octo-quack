<?php
/**
 * Template Name: Dropcap
 * @package  WordPress Landing Pages
 * @author   David Wells
 */
//gets template directory name to use as identifier - do not edit - include in all template files
$key = lp_get_parent_directory(dirname(__FILE__));
do_action('lp_global_config');
$lp_data[$key]['info'] =
array(
	'data_type' => 'template', // Template Data Type
	'version' => "2.0.0", // Version Number
	'label' => "Dropcap", // Nice Name
	'category' => 'v1, 1 column layout', // Template Category
	'demo' => 'http://demo.inboundnow.com/go/dropcap-lander-preview/', // Demo Link
	'description'  => 'Create a great looking quote styled landing page' // template description
);
// Define Meta Options for template
// These values are returned in the template's index.php file with lp_get_value($post, $key, 'field-id') function
$lp_data[$key]['settings'] =
array(
	array(
		'label' => 'turn-off-editor', /* Turns off main content */
		'description' => 'Turn off editor',
		'id'	=> 'turn-off-editor',
		'type'	=> 'custom-css',
		'default'	=> '#postdivrich, #lp_2_form_content {display:none !important;}'
		),
     array(
           'label' => __( 'Main Content' , 'landing-pages' ) ,
           'description' => __( 'This is the default content from template.' , 'landing-pages' ),
           'id' => "main-content",
           'type' => "wysiwyg",
           'default' => '<p>This is the first paragraph of your landing page. You want to grab the visitors attention and describe a commonly felt problem that they might be experiencing. Try and relate to your target audience and draw them in.</p>
<strong>In this guide you will learn:</strong>
[list icon="ok-sign" font_size="16" icon_color="#00a319" text_color="" bottom_margin="10"]
<ul>
	<li>This list was created with the list icon shortcode.</li>
	<li>Click on the power icon in your editor to customize your own</li>
	<li>Explain why users will want to fill out the form</li>
	<li>Keep it short and sweet.</li>
	<li>This list should be easily scannable</li>
</ul>
[/list]
<p>This is the final sentence or paragraph reassuring the visitor of the benefits of filling out the form and how their data will be safe.</p>'
         ),
	array(
           'label' => __( 'Conversion Area' , 'landing-pages' ),
           'description' => __( 'Place your call to action here.' , 'landing-page' ),
           'id' => "conversion-area-content",
           'type' => "wysiwyg",
           'default' => ''
         ),
    array(
        'label' => 'Text color', // Label of field
        'description' => "Use this setting to change the Text Color", // field description
        'id' => 'text-color', // metakey.
        'type'  => 'colorpicker', // text metafield type
        'default'  => 'ffffff', // default content
        'context'  => 'normal' // Context in screen for organizing options
        ),
    array(
        'label' => 'Content Background Color',
        'description' => "Use this setting to change the Content Area Background Color",
        'id'  => 'content-background',
        'type'  => 'colorpicker',
        'default'  => '000000',
        'context'  => 'normal'
        ),
    array(
        'label' => 'Conversion Area Text Color',
        'description' => "Use this setting to change the Conversion Area text Color",
        'id'  => 'form-text-color',
        'type'  => 'colorpicker',
        'default'  => 'ffffff',
        'context'  => 'normal'
        ),
    /* Background Settings */
    array(
        'label' => 'Background Settings',
        'description' => "Set the template's background",
        'id'  => 'background-style',
        'type'  => 'dropdown',
        'default'  => 'fullscreen',
        'options' => array('fullscreen'=>'Fullscreen Image', 'tile'=>'Tile Background Image', 'color' => 'Solid Color', 'repeat-x' => 'Repeat Image Horizontally', 'repeat-y' => 'Repeat Image Vertically', 'custom' => 'Custom CSS'),
        'context'  => 'normal'
        ),
    array(
        'label' => 'Background Image',
        'description' => "Enter an URL or upload an image for the banner.",
        'id'  => 'background-image',
        'type'  => 'media',
        'default'  => '/wp-content/plugins/landing-pages/templates/dropcap/assets/images/beach-1.jpg',
        'context'  => 'normal'
        ),
    array(
        'label' => 'Background Color',
        'description' => "Use this setting to change the templates background color",
        'id'  => 'background-color',
        'type'  => 'colorpicker',
        'default'  => '186d6d',
        'context'  => 'normal'
        )
    );





<?php
/**
* WordPress Landing Page Config File
* Template Name:	Youtube Lander
* @package	WordPress Landing Pages
* @author 	Naples Wine Aficionados, Corp
*
* This is a demo template for developers and designers to use as a reference for building landing page templates
* for Wordpress Landing Pages Plugin http://wordpress.org/plugins/landing-pages/
*
*/
 
do_action('lp_global_config'); // The lp_global_config function is for global code added by 3rd party extensions
 
//gets template directory name to use as identifier - do not edit - include in all template files
$key = lp_get_parent_directory(dirname(__FILE__));
$path = (preg_match("/uploads/", dirname(__FILE__))) ? LANDINGPAGES_UPLOADS_URLPATH . $key .'/' : LANDINGPAGES_URLPATH.'templates/'.$key.'/'; // This defines the path to your template folder. /wp-content/uploads/landing-pages/templates by default
 
/**
 * Landing Page Main Setup Params
 *
	$lp_data[$key]['info'] Parameters
 
	'version' => (string) (required)
	- Version Number. default = "1.0"
 
	'label' => (string) (required)
	- Custom Nice Name for templates. default = template file folder name
 
	'description' => (string) (required)
	- Landing page description.
 
	'category' => (string) (required)
	- Category for template. default = "all"
 
	'demo' => (string) (required)
	- Link to demo url.
*/
 
/* DEMO TEMPLATE INFO SETUP */
$lp_data[$key]['info'] =
array(
	'data_type' => "template", // Youtube Lander
	'version' => "2.0.0", // Second Version
	'label' => "Demo", // Naples Wine Aficionados
	'category' => 'Demo', // Travel and Entertainment
	'demo' => 'http://napleswineaficionados.com/youtubelander
	'description'	=> 'Naples Wine Aficionados, Corporation is a journalistic series of syndicated Content Management Platforms that focus on wine, food, cigars and live musical entertainment in the South West Florida Area. Our services include wine, food, cigar and live musical entertainment reviews via our wesite http://napleswineaficionados.com and Google + Page: http://GooGle.com/+napleswineaficianadosmagazine.   Essentially Naples Wine Aficionados Corporation is an epicurean journalistic endeavor which utilizes Social Media Network Engineering as a vehicle to communicate with the people and community of Naples, FL. and beyond.' // template description
);
 
 
/**
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<link rel='stylesheet' href='http://napleswineaficianados.com/wp-admin/load-styles.php?c=1&amp;dir=ltr&amp;load=dashicons,admin-bar,buttons,media-views,wp-admin,wp-auth-check&amp;ver=4.0' type='text/css' media='all' />
<link rel='stylesheet' id='open-sans-css'  href='//fonts.googleapis.com/css?family=Open+Sans%3A300italic%2C400italic%2C600italic%2C300%2C400%2C600&#038;subset=latin%2Clatin-ext&#038;ver=4.0' type='text/css' media='all' />
<link rel='stylesheet' id='thickbox-css'  href='http://napleswineaficianados.com/wp-includes/js/thickbox/thickbox.css?ver=4.0' type='text/css' media='all' />
<link rel='stylesheet' id='mediaelement-css'  href='http://napleswineaficianados.com/wp-includes/js/mediaelement/mediaelementplayer.min.css?ver=2.15.0' type='text/css' media='all' />
<link rel='stylesheet' id='wp-mediaelement-css'  href='http://napleswineaficianados.com/wp-includes/js/mediaelement/wp-mediaelement.css?ver=4.0' type='text/css' media='all' />
<link rel='stylesheet' id='imgareaselect-css'  href='http://napleswineaficianados.com/wp-includes/js/imgareaselect/imgareaselect.css?ver=0.9.8' type='text/css' media='all' />
<link rel='stylesheet' id='colors-css'  href='http://napleswineaficianados.com/wp-admin/css/colors/light/colors.min.css?frontend=false&#038;ver=4.0' type='text/css' media='all' />
<!--[if lte IE 7]>
<link rel='stylesheet' id='ie-css'  href='http://napleswineaficianados.com/wp-admin/css/ie.min.css?ver=4.0' type='text/css' media='all' />
<![endif]-->
<link rel='stylesheet' id='wp-cta-admin-css-css'  href='http://napleswineaficianados.com/wp-content/plugins/cta/css/admin-style.css?ver=4.0' type='text/css' media='all' />
<link rel='stylesheet' id='lp-admin-css-css'  href='http://napleswineaficianados.com/wp-content/plugins/landing-pages/css/admin-style.css?ver=4.0' type='text/css' media='all' />
<link rel='stylesheet' id='jpicker-css-css'  href='http://napleswineaficianados.com/wp-content/plugins/landing-pages/js/libraries/jpicker/css/jPicker-1.1.6.min.css?ver=4.0' type='text/css' media='all' />
<link rel='stylesheet' id='qtip-css-css'  href='http://napleswineaficianados.com/wp-content/plugins/landing-pages/css/jquery.qtip.min.css?ver=4.0' type='text/css' media='all' />
<link rel='stylesheet' id='lp-only-cpt-admin-css-css'  href='http://napleswineaficianados.com/wp-content/plugins/landing-pages/css/admin-lp-cpt-only-style.css?ver=4.0' type='text/css' media='all' />
<link rel='stylesheet' id='inbound-metaboxes-css'  href='http://napleswineaficianados.com/wp-content/plugins/landing-pages/shared/metaboxes/inbound-metaboxes.css?ver=4.0' type='text/css' media='all' />
<link rel='stylesheet' id='lp-css-post-new-css'  href='http://napleswineaficianados.com/wp-content/plugins/landing-pages/css/admin-post-new.css?ver=4.0' type='text/css' media='all' />
<link rel='stylesheet' id='inbound-shortcodes-css'  href='http://napleswineaficianados.com/wp-content/plugins/cta/shared/shortcodes/css/shortcodes.css?ver=4.0' type='text/css' media='all' />
<link rel='stylesheet' id='selectjs-css'  href='http://napleswineaficianados.com/wp-content/plugins/cta/shared/shortcodes/css/select2.css?ver=4.0' type='text/css' media='all' />
<link rel='stylesheet' id='inbound-admin-css'  href='http://napleswineaficianados.com/wp-content/plugins/cta/shared/assets/admin/css/global-inbound-admin.css?ver=4.0' type='text/css' media='all' />
 * $lp_data[$key]['settings']
 * Landing Page Main Setting Params
 * - Creates template metaboxes
	$lp_data[$key]['settings'] Parameters
 
	'label' => (string) (required)
	- Label for Meta Fields.
 
	'description' => (string) (required)
	- Description for meta Field
 
	'id' => (string) (required)
	- unprefixed-meta-key. The $key (template file path name) is appended in the loop this array is used in.
 
	'type' => (string) (required)
	- Meta box type. default = 'text'
 
	'default' => (string) (optional)
	- Default Field Value.	default = ''
 
	'options' => (array) (required for metaboxes with multiple options)
	- example: 'options' => array('value' => 'label','value_2'=>'label 2')
	- For dropdowns, checkboxes, etc.
 
	'context' => (string) (optional)
	- where this box will go, will be used for advanced placement/styling.	default = normal
 
*/
 
/* DEMO TEMPLATE Metabox SETUP */
// These values are returned in the template's index.php file with the lp_get_value($post, $key, 'text-box-id')
$lp_data[$key]['settings'] =
array(
	array(
		'label' => 'turn-off-editor', /* Turns off main content */
		'description' => 'Turn off editor',
		'id'	=> 'turn-off-editor',
		'type'	=> 'custom-css',
		'default'	=> '#postdivrich, #lp_2_form_content {display:none !important;}'
		),
	array(
			'label' => __( 'Main Content' , 'landing-pages' ) ,
			'description' => __( 'This is the default content from template.' , 'landing-pages' ),
			'id' => "main-content",
			'type' => "wysiwyg",
			'default' => '<p>This is the first paragraph of your landing page. You want to grab the visitors attention and describe a commonly felt problem that they might be experiencing. Try and relate to your target audience and draw them in.</p>
 
<strong>In this guide you will learn:</strong>
 
[list icon="ok-sign" font_size="16" icon_color="#00a319" text_color="" bottom_margin="10"]
<ul>
	<li>This list was created with the list icon shortcode.</li>
	<li>Click on the power icon in your editor to customize your own</li>
	<li>Explain why users will want to fill out the form</li>
	<li>Keep it short and sweet.</li>
	<li>This list should be easily scannable</li>
</ul>
[/list]
 
<p>This is the final sentence or paragraph reassuring the visitor of the benefits of filling out the form and how their data will be safe.</p>'
		),
 
	array(
			'label' => __( 'Conversion Area' , 'landing-pages' ),
			'description' => __( 'Place your call to action here.' , 'landing-page' ),
			'id' => "conversion-area-content",
			'type' => "wysiwyg",
			'default' => ''
		),
	/* Text field Example */
	array(
		'label' => 'Text Field Label', // Label of field
		'description' => "Text field Description", // field description
		'id' => 'text-box-id', // metakey. The $key Prefix is appended making the meta value demo-text-box-id
		'type'	=> 'text', // text metafield type
		'default'	=> '2013-1-31 13:00', // default content
		'context'	=> 'normal' // Context in screen for organizing options
		),
	/* Textarea Example */
	array(
		'label' => 'Textarea Label',
		'description' => "Textarea description to the user",
		'id'	=> 'textarea-id', // called in template's index.php file with lp_get_value($post, $key, 'textarea-id');
		'type'	=> 'textarea',
		'default'	=> 'Default text in textarea',
		'context'	=> 'normal'
		),
	/* Colorpicker Example */
	array(
		'label' => 'ColorPicker Label',
		'description' => "Colorpicker field description",
		'id'	=> 'color-picker-id', // called in template's index.php file with lp_get_value($post, $key, 'color-picker-id');
		'type'	=> 'colorpicker',
		'default'	=> 'ffffff',
		'context'	=> 'normal'
		),
	/* Radio Button Example */
	array(
		'label' => 'Radio Label',
		'description' => "Radio field description",
		'id'	=> 'radio-id-here', // called in template's index.php file with lp_get_value($post, $key, 'radio-id-here');
		'type'	=> 'radio',
		'default'	=> '1',
		'options' => array('1' => 'on','0'=>'off'),
		'context'	=> 'normal'
		),
	/* Checkbox Example */
	array(
		'label' => 'Checkbox Label',
		'description' => "Example Checkbox Description",
		'id'	=> 'checkbox-id-here', // called in template's index.php file with lp_get_value($post, $key, 'checkbox-id-here');
		'type'	=> 'checkbox',
		'default'	=> 'on',
		'options' => array('option_on' => 'on','option_off'=>'off'),
		'context'	=> 'normal'
		),
	/* Dropdown Example */
	array(
		'label' => 'Dropdown Label',
		'description' => "Dropdown option description",
		'id'	=> 'dropdown-id-here', // called in template's index.php file with lp_get_value($post, $key, 'dropdown-id-here');
		'type'	=> 'dropdown',
		'default'	=> 'default',
		'options' => array('right'=>'Float right','left'=>'Float left', 'default'=>'Default option'),
		'context'	=> 'normal'
		),
	/* Date Picker Example */
	array(
		'label' => 'Date Picker Label',
		'description' => "Date Picker Description",
		'id'	=> 'date-picker', // called in template's index.php file with lp_get_value($post, $key, 'date-picker');
		'type'	=> 'datepicker',
		'default'	=> '2013-12-27',
		'context'	=> 'normal'
		),
	/* WYSIWYG Example */
	array(
		'label' => 'Main Content Box 2',
		'description' => "wysiwyg description",
		'id'	=> 'wysiwyg-id', // called in template's index.php file with lp_get_value($post, $key, 'wysiwyg-id');
		'type'	=> 'wysiwyg',
		'default'	=> 'Default WYSIWYG content',
		'context'	=> 'normal'
		),
	/* Media Uploaded Example */
	array(
		'label' => 'File/Image Upload Label',
		'description' => "File/Image Upload Description",
		'id'	=> 'media-id', // called in template's index.php file with lp_get_value($post, $key, 'media-id');
		'type'	=> 'media',
		'default'	=> '/wp-content/plugins/landing-pages/templates/path-to-image-place-holder.png',
		'context'	=> 'normal'
		)
	);
