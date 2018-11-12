# data-table-simple-bundle


Insert into AppKernel.php
~~~~
new Aldaflux\DataTableSimpleBundle\AldafluxDataTableSimpleBundle(),
~~~~

in your config file
~~~~
aldaflux_data_table_simple:
    classes_to_table:
        - { class_name: table}
~~~~
all the `<table class='table'>` will be triable, filterable, and expotable in Excel and PDF


or this : 
~~~~
aldaflux_data_table_simple:
    labels:
        noresult: "<i class='glyphicon glyphicon-remove'></i>Aucun résultat"
        search: "<i class='glyphicon glyphicon-search'></i>Rechercher"
    classes_to_table:
        - { class_name: table-triable}
        - { class_name: table-triable_desc, excel: true,pdf: true, order: desc, filter: false}
        - { class_name: table-triable_simple, excel: false,pdf: false, order: asc, filter: false}
~~~~


In your template : 

~~~~
 {% block stylesheets %}
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css" integrity="sha384-1q8mTJOASx8j1Au+a5WDVnPi2lkFfwwEAa8hDDdjZlpLegxhjVME1fgjWPGmkzs7" crossorigin="anonymous">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/jqueryui/1.12.1/jquery-ui.min.css" type="text/css" rel="stylesheet" />
    <link href="{{ asset('bundles/aldafluxdatatablesimple/css/buttons.bootstrap.css')}}" type="text/css" rel="stylesheet" />
    <link href="{{ asset('bundles/aldafluxdatatablesimple/css/dataTables.bootstrap.css')}}" type="text/css" rel="stylesheet" />
 {% endblock %}


{% block javascripts %}
  <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jqueryui/1.12.1/jquery-ui.min.js"></script>

  {% include("AldafluxDataTableSimpleBundle::inc_js.html.twig") %}
{% endblock %} 

          
 
{% block body %} 
        	
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
         
{% endblock %}

~~~~
 
 
 
 
 The filters :    
 
        {{1002 | TdCurrency | raw }}
        {{150540502 | TdBytes | raw }} 
        
        
                
 
 
 
 
