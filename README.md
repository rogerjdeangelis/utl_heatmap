# utl_heatmap
SAS/WPS/R Heat map of overnite room rates around Austin Texas

    ```    ```
    ```    ```
    ```  T1006830 StackOverflow R: Heatmap - Overnite room rates around Austin Texas (fake data?) IML/R  ```
    ```    ```
    ```  Fake room rates around Austin Texas  ```
    ```    ```
    ```  for output see (or run the code)  ```
    ```  https://www.dropbox.com/s/hrve86qsudvg3rh/heatmap.pdf?dl=0  ```
    ```    ```
    ```         WORKING CODE  ```
    ```         ============  ```
    ```           SAS/R  ```
    ```    ```
    ```            map <- get_map(location = "austin", zoom = 11);  ```
    ```            ggmap(map, extent = "device") +  ```
    ```            stat_summary_2d(data = data, aes(x = LON, y = LAT,  ```
    ```            z = ROOM_RATE), fun = mean, alpha = 0.6, bins = 20) +  ```
    ```                scale_fill_gradient(name = "Price", low = "yellow", high = "red");  ```
    ```    ```
    ```  see  ```
    ```  https://goo.gl/e7U8fB  ```
    ```  https://stackoverflow.com/questions/45319970/generating-spatial-heat-map-via-ggmap-in-r-based-on-a-value  ```
    ```    ```
    ```  gconstantinos profile  ```
    ```  https://stackoverflow.com/users/1430542/gconstantinos  ```
    ```    ```
    ```    ```
    ```  HAVE  ```
    ```  ===  ```
    ```    ```
    ```  Up to 40 obs from sd1.have total obs=1,478  ```
    ```    ```
    ```          ROOM_  ```
    ```   Obs     RATE      LAT       LON  ```
    ```    ```
    ```     1       82    30.310    -97.732  ```
    ```     2      110    30.244    -97.775  ```
    ```     3      119    30.300    -97.779  ```
    ```     4      105    30.278    -97.719  ```
    ```     5       50    30.233    -97.589  ```
    ```   ...  ```
    ```    ```
    ```    ```
    ```  WANT   (ASCII representation see link or run program to get high resolution plot)  ```
    ```  =================================================================================  ```
    ```    ```
    ```                      Contour plot of LAT*LON.  ```
    ```    ```
    ```     LAT |                     ---  ```
    ```    30.5 +                   ... ....  ```
    ```         |                   .. ...  ```
    ```         |       ..........................................  ```
    ```         |     ...............................................  ```
    ```    30.4 +    .................................... ++++++......  ```
    ```         |          ................==.............+++.........  ```
    ```         |       .................====.=............+.......;;...  ```
    ```         |   ...W................=Austin===........--..  ```
    ```    30.3 +    ..**......-........=========........---..................  ```
    ```         | ....W*W-..........X...........++..........  ```
    ```         |       ......................  --....-.....  ```
    ```         |         .........................###.............;..  ```
    ```    30.2 +            .......................#.........................  ```
    ```         ---+-----------------------+-----------------------+--  ```
    ```          -97.6                   -97.8                   -98.0  ```
    ```    ```
    ```                                   LON  ```
    ```    ```
    ```            Symbol    ROOM_RATE     Symbol    ROOM_RATE  ```
    ```    ```
    ```            .....      0 -  450     OOOOO   2250 - 2700  ```
    ```            '''''    450 -  900     XXXXX   2700 - 3150  ```
    ```            -----    900 - 1350     WWWWW   3150 - 3600  ```
    ```            =====   1350 - 1800     *****   3600 - 4050  ```
    ```            +++++   1800 - 2250     #####   4050 - 4500  ```
    ```    ```
    ```    ```
