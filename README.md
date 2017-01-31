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
