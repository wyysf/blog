        function getParam(name){
                var reg = new RegExp(name,"ig");
                var arr = window.location.search.substring(1).split("&");
                var obj = {};
                for (var i = 0; i < arr.length; i++) {
                    if(reg.test(arr[i])){
                        obj[name] = arr[i].replace(reg,"").substring(1);
                    }
                }
                return obj[name] ? obj[name] : "";
        }
