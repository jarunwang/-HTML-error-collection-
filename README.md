# -HTML-error-collection-

1.window.onerror
//捕获全局错误demo

window.onerror = function(errorMessage, scriptURI, lineNumber,columnNumber,errorObj) { 
				var data  = {
						errorMsg : errorMessage,//出错的信息
						errorBrowser : navigator.userAgent,//浏览器信息
						errorUrl : window.location.href,//出错的位置
             					errorFile : scriptURI,//出错的文件
						errorLine : lineNumber,//出错代码的行号
						errorCol : columnNumber//出错代码的列号
					}
				  console.log(data); 
				  //repore.send()
		    return true;// 阻止在控制台中打印错误信息
};
