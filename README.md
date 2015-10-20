======== : https://github.com/csquared/IMGKit : =========

1 ) Download(wkhtmltox-0.12.1_linux-precise-i386.deb) : http://download.gna.org/wkhtmltopdf/0.12/0.12.1/

2 ) cd Downloads
3 ) sudo dpkg -i wkhtmltox-0.12.1_linux-precise-i386.deb
4 ) cd /usr/local/bin
5 ) sudo cp wkhtmltoimage /usr/bin/wkhtmltoimage
    sudo cp wkhtmltopdf /usr/bin/wkhtmltopdf
    
def methode
  @users = User.create(params[:user])
  filename = @users.name + "_" + '.jpg'
  kit = IMGKit.new("http://shahid-resume.herokuapp.com/")
  img = kit.to_img
  file = kit.to_file(Rails.root + "public/screenshots" + filename)
end    
