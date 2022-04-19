A) Frontend vuejs
  1) get file
    this.Images = this.$refs.name_ref.files[0];
  2) create formData
    let formData = new FormData()
  3) add file on formData
    formData.append("file", this.Images);
  4) call api with parameter is formData

B) Backend laravel use medialibrary
  1) get file
      $file = $request->file("file");
  2) delete all file old
      $user->clearMediaCollection('user_avt');
  3) add file
     $user->addMedia($file)->toMediaCollection('user_avt');
