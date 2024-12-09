#!/bin/bash
aaa="$1"
bbb="$2"
che(){
usage=$(df -h "$aaa" | awk 'NR==2 {print $5}' | sed 's/%//')
	if [ ! -d "$aaa" ]; 
        then 
        echo "не то,беспокойте когда что-то дельное будет 0_0" 
    exit 1 
    fi 
}
proverkanamatematika(){
	 if [ "$usage" -gt "$bbb" ];
	 then 
        echo "Вот те на те, $aaa превышает $bbb%" 
    fi 
}

provero4ka "$aaa" "$bbb"
proverkanamatematika "$aaa" "$bbb"
