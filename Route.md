# Route

## work

    输出每一个tile的位置，按照布局结构图；    
    输出每一个tile中的muxb（开关盒）及其中的内容；  
    输出conns。     
    输出 seal 100k 器件 （SA5T-100-D0-8T999） 的 tile 和 mux 到文本文件中


    输出tile，可以直接利用dumpTileMatrix()函数修改后dumpTileSiteMatrix()函数输出按照布局结构表示的文本    
    输出mux，通过阅读代码，一个mux的信息用于将对应的tiledef中的pindef的src或dst进行初始化   
    
```c++
map<string, hash_map<RT_PIN, rtPinDef*> > _pinsInAllmuxBlocks   
muxb_name - pin_id - pin_def

for ([muxb_name, pin_map] : _pinsInAllmuxBlocks) {
    cout << muxb_name;
    for ([pin_id, pin_def] : pin_map) {
        cout << pinIdStrNameMap[pin_id];
        for ([src, dst] : pin_def) {
            
        }
    }
}
```

## Wiring Structure


