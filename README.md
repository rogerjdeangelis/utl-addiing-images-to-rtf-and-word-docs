# utl-addiing-images-to-rtf-and-word-docs
Addiing images to rtf_and word docs 
    Adding images to rtf_and word docs                                                                           
                                                                                                                 
      Five methods                                                                                               
                                                                                                                 
         1. Title statemet  http://tinyurl.com/y4qt4hop                                                          
         2. Ods rtf text http://tinyurl.com/y2uynnrn                                                             
         3. proc report 'column'  http://tinyurl.com/yy5wd725                                                    
         4. proc report define (John Hendrix) http://tinyurl.com/y6qggt4w                                        
         5. proc report side by side images (John Hendrix) http://tinyurl.com/yxzctqxc                           
                                                                                                                 
    github                                                                                                       
    http://tinyurl.com/y63sjkh4                                                                                  
    https://github.com/rogerjdeangelis/utl-adding-images-to-rtf-and-word-docs                                    
                                                                                                                 
    *_                   _                                                                                       
    (_)_ __  _ __  _   _| |_                                                                                     
    | | '_ \| '_ \| | | | __|                                                                                    
    | | | | | |_) | |_| | |_                                                                                     
    |_|_| |_| .__/ \__,_|\__|                                                                                    
            |_|                                                                                                  
    ;                                                                                                            
                                                                                                                 
    Create Two images to use with the five methods                                                               
                                                                                                                 
    * BIG IMAGE;                                                                                                 
                                                                                                                 
    http://tinyurl.com/y5ntddew                                                                                  
                                                                                                                 
    ods listing gpath="d:\rtf\png" style=analysis;                                                               
    ods graphics on / reset=index width=5in height=3.5in imagefmt=png imagename='imgBig';                        
    proc sgplot data=sashelp.class;                                                                              
        vbar sex;                                                                                                
    run;quit;                                                                                                    
                                                                                                                 
    * SMALL IMAGE;                                                                                               
                                                                                                                 
    http://tinyurl.com/y385llu9                                                                                  
                                                                                                                 
    ods listing gpath="d:\rtf\png" style=analysis;                                                               
    ods graphics on / reset=index width=.5in height=.5in imagefmt=png imagename='imgLtl';                        
    proc sgplot data=sashelp.class;                                                                              
        vbar sex;                                                                                                
    run;quit;                                                                                                    
                                                                                                                 
                                                                                                                 
    LITTLE IMAGE                                                                                                 
    ------------                                                                                                 
                                                                                                                 
    +--------------------+                                                                                       
    |                    |                                                                                       
    |   |         *****  |                                                                                       
    | 8 +  *****  *****  |                                                                                       
    |   |  *****  *****  |                                                                                       
    | 4 +  *****  *****  |                                                                                       
    |   |  *****  *****  |                                                                                       
    |   ---------------  |                                                                                       
    |       F SEX  M     |                                                                                       
    +--------------------+                                                                                       
                                                                                                                 
                                                                                                                 
    BIG IMAGE                                                                                                    
    ---------                                                                                                    
                                                                                                                 
    +-------------------------------------------+                                                                
    |                                           |                                                                
    |          Math Class Sex Histogram         |                                                                
    | 10 +-----------------------------------+  |                                                                
    |    |                         *****     |  |                                                                
    |  9 +                         *****     +  |                                                                
    |    |       *****             *****     |  |                                                                
    |  8 +       *****             *****     +  |                                                                
    |    |       *****             *****     |  |                                                                
    |  7 +       *****             *****     +  |                                                                
    |    |       *****             *****     |  |                                                                
    |  6 +       *****             *****     +  |                                                                
    |    |       *****             *****     |  |                                                                
    |  5 +       *****             *****     +  |                                                                
    |    |       *****             *****     |  |                                                                
    |  5 +       *****             *****     +  |                                                                
    |    |       *****             *****     |  |                                                                
    |  4 +       *****             *****     +  |                                                                
    |    |       *****             *****     |  |                                                                
    |  3 +-----------------------------------+  |                                                                
    |              F      SEX        M          |                                                                
    |                                           |                                                                
    +-------------------------------------------+                                                                
                                                                                                                 
                                                                                                                 
    *          _       _   _                                                                                     
     ___  ___ | |_   _| |_(_) ___  _ __  ___                                                                     
    / __|/ _ \| | | | | __| |/ _ \| '_ \/ __|                                                                    
    \__ \ (_) | | |_| | |_| | (_) | | | \__ \                                                                    
    |___/\___/|_|\__,_|\__|_|\___/|_| |_|___/                                                                    
                                                                                                                 
    ;                                                                                                            
                                                                                                                 
    *_     _____ _ _   _                                                                                         
    / |   |_   _(_) |_| | ___                                                                                    
    | |     | | | | __| |/ _ \                                                                                   
    | |_    | | | | |_| |  __/                                                                                   
    |_(_)   |_| |_|\__|_|\___|                                                                                   
                                                                                                                 
    ;                                                                                                            
                                                                                                                 
    ods escapechar='~';                                                                                          
    options center orientation=portrait;                                                                         
    ods rtf file="d:/rtf/title.rtf" style=journal;                                                               
    title j=l "~S={preimage='d:/rtf/png/imgLtl.png'}"                                                            
          j=c "~S={font_size=24pt} Math"                                                                         
          j=r "~S={preimage='d:/rtf/png/imgLtl.png'}";                                                           
    proc report nowd missing data=sashelp.class(obs=5);                                                          
    run;quit;                                                                                                    
    ods rtf close;                                                                                               
                                                                                                                 
    ------                                                                                                       
    OUTPUT                                                                                                       
    ------                                                                                                       
                                                                                                                 
    d:/rtf/title.rtf                                                                                             
                                                                                                                 
                                                                                                                 
    +--------------------+                            +--------------------+                                     
    |                    |                            |                    |                                     
    |   |         *****  |    __  __       _   _      |   |         *****  |                                     
    | 8 +  *****  *****  |   |  \/  | __ _| |_| |__   | 8 +  *****  *****  |                                     
    |   |  *****  *****  |   | |\/| |/ _` | __| '_ \  |   |  *****  *****  |                                     
    | 4 +  *****  *****  |   | |  | | (_| | |_| | | | | 4 +  *****  *****  |                                     
    |   |  *****  *****  |   |_|  |_|\__,_|\__|_| |_| |   |  *****  *****  |                                     
    |   ---------------  |                            |   ---------------  |                                     
    |       F SEX  M     |                            |       F SEX  M     |                                     
    +--------------------+                            +--------------------+                                     
                                                                                                                 
                                                                                                                 
                 NAME     SEX       AGE     HEIGHT     WEIGHT                                                    
                                                                                                                 
                 Alfred    M         14         69      112.5                                                    
                 Alice     F         13       56.5         84                                                    
                 Barbara   F         13       65.3         98                                                    
                 Carol     F         14       62.8      102.5                                                    
                 Henry     M         14       63.5      102.5                                                    
                                                                                                                 
                                                                                                                 
    *____       ___      _       _            _                                                                  
    |___ \     / _ \  __| |___  | |_ _____  _| |_                                                                
      __) |   | | | |/ _` / __| | __/ _ \ \/ / __|                                                               
     / __/ _  | |_| | (_| \__ \ | ||  __/>  <| |_                                                                
    |_____(_)  \___/ \__,_|___/  \__\___/_/\_\\__|                                                               
                                                                                                                 
    ;                                                                                                            
                                                                                                                 
    title;                                                                                                       
    ods escapechar='~';                                                                                          
    options nocenter;                                                                                            
    ods rtf file="d:/rtf/odsText.rtf" style=journal;                                                             
    ods text='~S={outputwidth=100% preimage="d:/rtf/png/imgLtl.png"}';                                           
    ods text='~{newline}  ~{newline}';                                                                           
    proc report nowd missing data=sashelp.class(obs=5) headskip;                                                 
    run;quit;                                                                                                    
    ods rtf close;                                                                                               
                                                                                                                 
    ------                                                                                                       
    OUTPUT                                                                                                       
    ------                                                                                                       
                                                                                                                 
    d:/rtf/odsText.rtf                                                                                           
                                                                                                                 
                                                                                                                 
      +--------------------+                                                                                     
      |                    |                                                                                     
      |   |         *****  |                                                                                     
      | 8 +  *****  *****  |                                                                                     
      |   |  *****  *****  |                                                                                     
      | 4 +  *****  *****  |                                                                                     
      |   |  *****  *****  |                                                                                     
      |   ---------------  |                                                                                     
      |       F SEX  M     |                                                                                     
      +--------------------+                                                                                     
                                                                                                                 
                                                                                                                 
      NAME     SEX       AGE     HEIGHT     WEIGHT                                                               
                                                                                                                 
      Alfred    M         14         69      112.5                                                               
      Alice     F         13       56.5         84                                                               
      Barbara   F         13       65.3         98                                                               
      Carol     F         14       62.8      102.5                                                               
      Henry     M         14       63.5      102.5                                                               
                                                                                                                 
                                                                                                                 
    *_____    ____                       _               _                                                       
    |___ /   |  _ \ ___ _ __   ___  _ __| |_    ___ ___ | |_   _ _ __ ___  _ __                                  
      |_ \   | |_) / _ \ '_ \ / _ \| '__| __|  / __/ _ \| | | | | '_ ` _ \| '_ \                                 
     ___) |  |  _ <  __/ |_) | (_) | |  | |_  | (_| (_) | | |_| | | | | | | | | |                                
    |____(_) |_| \_\___| .__/ \___/|_|   \__|  \___\___/|_|\__,_|_| |_| |_|_| |_|                                
                       |_|                                                                                       
    ;                                                                                                            
                                                                                                                 
    ods escapechar='~';                                                                                          
    options nocenter;                                                                                            
    ods rtf file="d:/rtf/reportColumn.rtf" style=minimal;                                                        
    proc report nowd missing data=sashelp.class(obs=5);                                                          
      cols ( '~S={just=left preimage="d:/rtf/png/imgLtl.png"}' _ALL_);                                           
    run;quit;                                                                                                    
    ods rtf close;                                                                                               
                                                                                                                 
                                                                                                                 
    d:/rtf/reportColumn.rtf                                                                                      
                                                                                                                 
      +--------------------+                                                                                     
      |                    |                                                                                     
      |   |         *****  |                                                                                     
      | 8 +  *****  *****  |                                                                                     
      |   |  *****  *****  |                                                                                     
      | 4 +  *****  *****  |                                                                                     
      |   |  *****  *****  |                                                                                     
      |   ---------------  |                                                                                     
      |       F SEX  M     |                                                                                     
      +--------------------+                                                                                     
                                                                                                                 
                                                                                                                 
      NAME     SEX       AGE     HEIGHT     WEIGHT                                                               
                                                                                                                 
      Alfred    M         14         69      112.5                                                               
      Alice     F         13       56.5         84                                                               
      Barbara   F         13       65.3         98                                                               
      Carol     F         14       62.8      102.5                                                               
      Henry     M         14       63.5      102.5                                                               
                                                                                                                 
                                                                                                                 
    *_  _      ____                       _         _       __ _                                                 
    | || |    |  _ \ ___ _ __   ___  _ __| |_    __| | ___ / _(_)_ __   ___                                      
    | || |_   | |_) / _ \ '_ \ / _ \| '__| __|  / _` |/ _ \ |_| | '_ \ / _ \                                     
    |__   _|  |  _ <  __/ |_) | (_) | |  | |_  | (_| |  __/  _| | | | |  __/                                     
       |_|(_) |_| \_\___| .__/ \___/|_|   \__|  \__,_|\___|_| |_|_| |_|\___|                                     
                        |_|                                                                                      
    ;                                                                                                            
    /*Dummy dataset with two column variables*/                                                                  
    data colx;                                                                                                   
        text='Math';                                                                                             
        c1=' ';                                                                                                  
    run;                                                                                                         
                                                                                                                 
    options orientation=landscape ps=171;                                                                        
    ods rtf file="d:/rtf/reportDefine.rtf" style=Journal;                                                        
    proc report data=colx nowindows contents=""                                                                  
        style=[                                                                                                  
            bordertopwidth=0 borderbottomwidth=0 borderleftwidth=0 BORDERRIGHTWIDTH=0                            
            bordertopcolor=white borderbottomcolor=white borderleftcolor=white borderrightcolor=white            
        ];                                                                                                       
        columns text c1;                                                                                         
        define text / display style={just=center font_size=64pt outputwidth=100pct} ' ';                         
        define c1   / display '~S={just=center outputwidth=100pct postimage="d:/rtf/png/imgBig.png"}' ' ';       
    run;quit;                                                                                                    
    ods rtf close;                                                                                               
    ods select all;                                                                                              
                                                                                                                 
                                                                                                                 
    d:/rtf/reportDefine.rtf                                                                                      
                                                                                                                 
             __  __    _  _____ _   _                                                                            
            |  \/  |  / \|_   _| | | |                                                                           
            | |\/| | / _ \ | | | |_| |                                                                           
            | |  | |/ ___ \| | |  _  |                                                                           
            |_|  |_/_/   \_\_| |_| |_|                                                                           
                                                                                                                 
                                                                                                                 
    +-------------------------------------------+                                                                
    |                                           |                                                                
    |          Math Class Sex Histogram         |                                                                
    | 10 +-----------------------------------+  |                                                                
    |    |                         *****     |  |                                                                
    |  9 +                         *****     +  |                                                                
    |    |       *****             *****     |  |                                                                
    |  8 +       *****             *****     +  |                                                                
    |    |       *****             *****     |  |                                                                
    |  7 +       *****             *****     +  |                                                                
    |    |       *****             *****     |  |                                                                
    |  6 +       *****             *****     +  |                                                                
    |    |       *****             *****     |  |                                                                
    |  5 +       *****             *****     +  |                                                                
    |    |       *****             *****     |  |                                                                
    |  5 +       *****             *****     +  |                                                                
    |    |       *****             *****     |  |                                                                
    |  4 +       *****             *****     +  |                                                                
    |    |       *****             *****     |  |                                                                
    |  3 +-----------------------------------+  |                                                                
    |              F      SEX        M          |                                                                
    |                                           |                                                                
    +-------------------------------------------+                                                                
                                                                                                                 
                                                                                                                 
                                                                                                                 
    *____     ____  _     _        _                 _     _                                                     
    | ___|   / ___|(_) __| | ___  | |__  _   _   ___(_) __| | ___                                                
    |___ \   \___ \| |/ _` |/ _ \ | '_ \| | | | / __| |/ _` |/ _ \                                               
     ___) |   ___) | | (_| |  __/ | |_) | |_| | \__ \ | (_| |  __/                                               
    |____(_) |____/|_|\__,_|\___| |_.__/ \__, | |___/_|\__,_|\___|                                               
                                         |___/                                                                   
    ;                                                                                                            
                                                                                                                 
                                                                                                                 
    data colx;                                                                                                   
        c1=' '; c2=' ';                                                                                          
    run;quit;                                                                                                    
                                                                                                                 
    options orientation=landscape;                                                                               
    ods rtf file="d:/rtf/reportSidebySide.rtf" style=Journal;                                                    
    proc report data=colx nowindows contents=""                                                                  
        style=[                                                                                                  
            bordertopwidth=0 borderbottomwidth=0 borderleftwidth=0 BORDERRIGHTWIDTH=0                            
            bordertopcolor=white borderbottomcolor=white borderleftcolor=white borderrightcolor=white            
        ];                                                                                                       
        *columns c1 c2;                                                                                          
        columns ( '~S={just=center font_size=32pt} Math' c1 c2);                                                 
        define c1   / display style={width=5in just=center postimage="d:/rtf/png/imgBig.png"} ' ';               
        define c2   / display style={width=5in just=center postimage="d:/rtf/png/imgBig.png"} ' ';               
    run;                                                                                                         
    ods rtf close;                                                                                               
    ods _all_ close;                                                                                             
                                                                                                                 
                                                                                                                 
    d:/rtf/reportSidebySide.rtf                                                                                  
                                        __  __    _  _____ _   _                                                 
                                       |  \/  |  / \|_   _| | | |                                                
                                       | |\/| | / _ \ | | | |_| |                                                
                                       | |  | |/ ___ \| | |  _  |                                                
                                       |_|  |_/_/   \_\_| |_| |_|                                                
                                                                                                                 
                                                                                                                 
                                                                                                                 
    +-------------------------------------------+  +-------------------------------------------+                 
    |                                           |  |                                           |                 
    |          Math Class Sex Histogram         |  |          Math Class Sex Histogram         |                 
    | 10 +-----------------------------------+  |  | 10 +-----------------------------------+  |                 
    |    |                         *****     |  |  |    |                         *****     |  |                 
    |  9 +                         *****     +  |  |  9 +                         *****     +  |                 
    |    |       *****             *****     |  |  |    |       *****             *****     |  |                 
    |  8 +       *****             *****     +  |  |  8 +       *****             *****     +  |                 
    |    |       *****             *****     |  |  |    |       *****             *****     |  |                 
    |  7 +       *****             *****     +  |  |  7 +       *****             *****     +  |                 
    |    |       *****             *****     |  |  |    |       *****             *****     |  |                 
    |  6 +       *****             *****     +  |  |  6 +       *****             *****     +  |                 
    |    |       *****             *****     |  |  |    |       *****             *****     |  |                 
    |  5 +       *****             *****     +  |  |  5 +       *****             *****     +  |                 
    |    |       *****             *****     |  |  |    |       *****             *****     |  |                 
    |  5 +       *****             *****     +  |  |  5 +       *****             *****     +  |                 
    |    |       *****             *****     |  |  |    |       *****             *****     |  |                 
    |  4 +       *****             *****     +  |  |  4 +       *****             *****     +  |                 
    |    |       *****             *****     |  |  |    |       *****             *****     |  |                 
    |  3 +-----------------------------------+  |  |  3 +-----------------------------------+  |                 
    |              F      SEX        M          |  |              F      SEX        M          |                 
    |                                           |  |                                           |                 
    +-------------------------------------------+  +-------------------------------------------+                 
                                                                                                                 
                                                                                                                 
                                                                                                                 
                                                                                                                 
                                                                                                                 
                                                                                                                 
                                                                                                                 
