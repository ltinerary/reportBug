const prviewImage = (key) => {
    // let allKey = needPic('all');
    let index = imageKey.value.indexOf(key);
    if (index != -1) {
        let resultArr = []
        imageKey.value.forEach(key => {
            resultArr.push(resultAllFileList[key])
        })
        console.log('当前预览的Key',key,index)
        console.log('能够预览的图片key==>',imageKey.value)
        console.log('能够预览的图片',resultArr)
        ImagePreview({
            images: resultArr,
            startPosition: index,
            closeable: true,
        })
    } else {
        Toast(`没有找到您要预览的大图${key}`)
    }
}
