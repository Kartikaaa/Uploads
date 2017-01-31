# uploads
library upload file or multi files in codeigniter 


#import library
copy file uploads.php in path application/libraries


#load library
$this->load->library('uploads');


# example single file
```
/*
* in controller
**/

$paths = FCROOT . 'upload';
$index = 'file';

$result = $this->uploads->upload($paths, $index);

echo '<pre>';
print_r($result);




/*
* in view
**/

<form action="URL_UPLOAD" method="post" enctype="multipart/form-data">
    <input type="file" name="file" />
    <input type="submit" />
</form>

```



# example multi file
```
/*
* in controller
**/

$paths = FCROOT . 'upload';
$index = 'file';

$result = $this->uploads->multi_upload($paths, $index);

echo '<pre>';
print_r($result);




/*
* in view
**/

<form action="URL_UPLOAD" method="post" enctype="multipart/form-data">
    <input type="file" name="file[]" multiple />
    <input type="submit" />
</form>

```


# RESULT
```
Array
(
    [total] => 2
    [uploaded] => 2
    [faild] => 0
    [file_uploaded] => Array
        (
            [0] => cb0290554de4fc8d214aeae5e0054a83.png
            [1] => 32c8e939b8f86fe35dc5026ae22ea461.png
        )

    [file_faild] => Array
        (
        )

)
```
