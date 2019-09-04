# How-To-Create-WordPress-Percent-Bar-Shortcode



////////// PERCENTAGE BAR
    function percentbar ($atts, $content = null) {
            extract(shortcode_atts(array(
                'percentage' => ''
                ), $atts));
                 
        return '<div class="progressbar"><span class="percentage" style="width:' . ($percentage) . '%">'.do_shortcode($content).'</span></div>';
        }
        add_shortcode ("percentbar", "percentbar");
        
        
        
        
        
        style:
        
        /********** SHORTCODE STYLES **********/
.progressbar {width: 100%;background:#CCC;margin-bottom:15px;}
.progressbar span.percentage {background-color:#2fcefc; padding:10px 0; text-indent:15px; display:block; color:#fff; min-height:35px;}

Usages:

[percentbar percentage="50"]50% Shortcode[/percentbar]
