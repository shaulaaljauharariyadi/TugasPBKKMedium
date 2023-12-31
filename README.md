# Ruby on Rails sebagai Web Framework
- Shaula Aljauhara Riyadi - 5025201265
- Arfi Raushani Fikra - 5025211084
- Abyan Zhafran Trisnanto - 5025211218
## General Information and Framework Purposes
Ruby on Rails,atau disebut Rails adalah web development framework yang dibangun menggunakan bahasa pemrogramman Ruby.Rails sendiri merupakan framework *open source* yang dirilis dengan lisensi MIT. Rails dirancang untuk mempercepat dan menyederhanakan pengembangan aplikasi web dengan menyediakan tools dan konvensi yang dibutuhkan web programming developer. Framework ini bertujuan untuk meningkatkan produktivitas developer dan meminimalisir upaya yang diperlukan dalam mengatur kode dan infrastruktur dasar. Ruby on Rails adalah framework full stack, yang berarti dapat digunakan sebagai framework *back-end* untuk mengelola database dan file di server. Namun, bisa juga digunakan sebagai framework *front-end* untuk me-*render* HTML dan mengupdate halaman secara live. Framework ini menggunakan arsitektur MVC (Model View Controller) yang membuatnya menjadi fleksibel untuk membangun berbagai jenis aplikasi web, seperti *Progressive Web App* (PWA), *Single Page App* (SPA), *Rich Internet App* (RPA), bahkan Web Service dan API. Dikutip dari situs resmi Ruby on Rails, terdapat sembilan doktrin yang menjadi ciri khas dan keunggulan dari Rails, doktrin ini ditulis oleh pencipta Rails yaitu David Heinemeier Hansson. Kesembilan doktrinnya yaitu : Dioptimalkan untuk kebahagiaan programmer, Konvensi di atas Konfigurasi, Menunya adalah omakase (Pembuatan suatu fitur dan fasilitas oleh pihak lain, tetapi dapat diandalkan dan tidak perlu diragukan), Tidak ada satu paradigma pun (Gabungan dari banyak ide dan bahkan paradigma yang berbeda, namun bersatu menjadi sebuah kegunaan), Mengagungkan kode yang indah (Kode yang tidak hanya dipahami komputer, namun juga dapat dinikmati oleh penulisnya), Menyediakan pisau tajam (Berisi banyak kelengkapan tools dan disertai panduan menggunakannya agar dapat digunakan secara optimal), Menilai sistem terintegrasi (Rails menjunjung upaya untuk menciptakan keseluruhan sistem yang mengatasi keseluruhan masalah), Kemajuan melebihi stabilitas, dan Mendorong tenda yang besar (Rails mampu mendukung komunitas besar di bawah satu cakupan tenda). Dengan keunggulannya tersebut, Rails digunakan oleh banyak perusahaan dan developer untuk membangun aplikasi web yang kuat dan efisien seperti Shopify, Dribble, Hulu, AirBnB, Twitch, Soundcloud, bahkan Github.

## Framework's Comparison
Rails dapat dibandingkan dengan dua framework web populer lainnya, yaitu Django (Python) dan Laravel (PHP), dalam beberapa aspek berikut:

   - Bahasa Pemrograman: Rails menggunakan Ruby, sedangkan Django menggunakan Python dan Laravel menggunakan PHP. Rails tidak bisa berjalan di atas bahasa pemrograman lain, seperti Python atau PHP. Rails juga mengikuti semua aturan yang ditetapkan Ruby. Rails dibuat untuk meningkatkan kemampuan Ruby itu sendiri. Dengan begitu, Ruby on Rails bisa melakukan hal-hal yang tidak dapat dilakukan Ruby secara native.
   - Konvensi vs. Konfigurasi: Rails mengutamakan konvensi daripada konfigurasi, sementara Django dan Laravel cenderung lebih berorientasi pada konfigurasi. Ruby on Rails mengharuskan pengembang mengikuti konvensi yang sudah ditentukan oleh kerangka kerja. Hal ini memungkinkan pengembang untuk lebih fokus pada logika aplikasi daripada menghabiskan waktu mengatur konfigurasi.
   - ORM (Object-Relational Mapping): Rails memiliki ORM yang kuat bernama ActiveRecord, yang memungkinkan pengembang untuk berinteraksi dengan database menggunakan objek Ruby. Django memiliki Django ORM, dan Laravel menggunakan Eloquent ORM. Pola ActiveRecord merupakan pendekatan untuk mengakses data dalam database. Tabel atau tampilan database digabungkan ke dalam kelas. Jadi, sebuah *instance* objek akan terikat pada satu baris dalam tabel. Setelah pembuatan objek, baris baru ditambahkan ke tabel setelah disimpan. Setiap objek yang dimuat mendapatkan informasinya dari database. Ketika suatu objek diperbarui, baris terkait dalam tabel juga diperbarui. ActiveRecord juga tidak terhalangi oleh perbedaan jenis database yang digunakan, selama file `config/database.yml`-nya benar, ActiveRecord dapat menghubungkannya. Jika berpindah database, kita tidak perlu mengubah kode aplikasi utama, hanya perlu mengubah beberapa file konfigurasi. 
   - Komunitas dan Ekosistem: Rails memiliki komunitas besar dan ekosistem yang kaya, sementara Django dan Laravel juga memiliki komunitas yang kuat, tetapi dalam bahasa pemrograman yang berbeda.
   - Skalabilitas: Rails, Django, dan Laravel semuanya dapat digunakan untuk membangun aplikasi yang dapat diskalakan dengan baik, tetapi pendekatan dan alat yang digunakan mungkin berbeda.

## Framework's architecture  illustration
![Rails Illustration](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*KK61kGXrkaFBDfY7uWukyQ.png)

Arsitektur Rails menggunakan pola Model-View-Controller(MVC) dimana Setelah browser melakukan web request pada artikel di suatu web, kemudian *request* tersebut akan diteruskan menuju router yang lalu akan diteruskan menuju controller. Controller akan meminta model untuk mengambil data dan render tampilan yang berada di database sesuai *request* yang diberikan. Lalu model akan memberikan data dan render tampilan artikel tersebut ke controller. Kemudian controller memberikan view data dan render tampilan(UI) yang di-*request* tersebut, selanjutnya view akan meneruskan langsung ke web server dan lalu user dapat melihat dan mengakses artikel tersebut dari browser setelah web server menerima data yang di-*request* dari view. Rails mengikuti konsep konvensi diatas konfigurasi dimana pada ilustrasi ini kita hanya perlu melakukan konfigurasi pada bagian router dan komponen lain menggunakan komponen default dari framework rails itu sendiri.
Umumnya,rails berisi struktur folder default sebagai berikut :
| File/folder   |Tujuan  |
|--------|------|
| app/  | berisi inti dari aplikasi Rails Anda dan terbagi menjadi beberapa subfolder seperti assests,channel,controller,helpers jobs, mailers,models, dan views | 
| bin/  |  Berisi file-file skrip yang digunakan untuk menjalankan berbagai tugas pengembangan, seperti server pengembangan dan konsol | 
| config/  | Direktori yang berisi konfigurasi aplikasi, termasuk file-file seperti routes.rb (mengatur rute), application.rb (konfigurasi aplikasi), dan database.yml (konfigurasi basis data) | 
| config.ru | berkas konfigurasi yang digunakan dalam proyek Ruby on Rails dan umumnya terkait dengan server web Ruby yang berbasis Rack, seperti server pengembangan WEBrick atau Puma |
| db/ | Berisi file-file migrasi basis data, yang digunakan untuk mengelola skema basis data aplikasi Anda. termasuk database dari migrasi |
| Gemfile & Gemfile.lock | File-file ini berisi daftar dependensi (gems) yang digunakan dalam proyek Rails |
| log/ | File-file log aplikasi akan disimpan di sini, termasuk log produksi, pengembangan, dan pengujian |
| public/ | Berisi file-file statis yang dapat diakses secara langsung oleh klien, seperti gambar dan favicon |
| Rakefile |  File yang berisi tugas-tugas (tasks) Rake yang dapat Anda jalankan dari baris perintah |
| README.md |  Dokumentasi proyek Rails yang dikembangkan |
| storage/ |  Direktori ini (biasanya) digunakan untuk menyimpan file-file yang diunggah oleh pengguna jika aplikasi Anda memerlukan fitur unggahan file |
| test/ | Direktori untuk pengujian aplikasi. Ini berisi file-file tes unit, fungsional, dan integrasi |
| tmp/ | Tempat untuk menyimpan file sementara dan cache |
| vendor/ | Berisi kode dari pihak ketiga yang digunakan dalam proyek |
| .gitattributes | digunakan untuk mengatur aksi khusus yang akan diambil oleh Git saat berinteraksi dengan berkas atau direktori tertentu dalam repositori. Ini sering digunakan untuk mengatur cara Git memperlakukan berkas teks dan biner |
| .gitignore | digunakan untuk memberi tahu Git tentang berkas atau direktori yang harus diabaikan (ignored) saat melakukan operasi seperti git status, git add, atau git commit. Ini sangat berguna untuk menghindari melacak file-file sementara, berkas konfigurasi lokal, atau file log dalam repositori |
|  .ruby-version | versi default ruby yang digunakan,biasanya menggunakan versi terkini |

## Source Code Sample
Berikut contoh source code Ruby on Rails :

### Model ('User' model):
Buat file 'user.rb' dalam direktori '/app/models'
```ruby
# /app/models/user.rb
class User < ApplicationRecord
  validates :name, presence: true
  validates :email, presence: true, uniqueness: true
end
```
### Controller ('UsersController'):
Buat controller untuk mengelola pengguna dengan perintah berikut
```bash
rails generate controller Users
```
Ini akan menghasilkan file 'users_controller.rb' dalam direktori '/app/controllers'. Berikut adalah contoh kode dalam controller
```ruby
# /app/controllers/users_controller.rb
class UsersController < ApplicationController
  def index
    @users = User.all
  end

  def show
    @user = User.find(params[:id])
  end

  def new
    @user = User.new
  end

  def create
    @user = User.new(user_params)
    if @user.save
      redirect_to users_path, notice: 'User successfully created.'
    else
      render 'new'
    end
  end

  private

  def user_params
    params.require(:user).permit(:name, :email)
  end
end
```
### View
Buat file tampilan dalam direktori '/app/views/users'. Berikut adalah contoh tampilan untuk halaman indeks ('index.html.erb'):
```ruby
<!-- /app/views/users/index.html.erb -->
<h1>Users</h1>

<ul>
  <% @users.each do |user| %>
    <li><%= user.name %> (<%= user.email %>)</li>
  <% end %>
</ul>

<%= link_to 'New User', new_user_path %>
```
### Routes
Konfigurasi rute Anda dalam file 'routes.rb' di dalam direktori '/config'
```ruby
# /config/routes.rb
Rails.application.routes.draw do
  resources :users
  root 'users#index'
end
```
### Migrasi Database
untuk melakukan migrasi untuk membuat tabel pengguna menggunakan perintah berikut
```bash
rails generate migration CreateUsers
```
Ini akan menghasilkan file migrasi dalam direktori '/db/migrate'. Ubah file migrasi tersebut sesuai kebutuhan Anda, lalu jalankan migrasi dengan perintah 'rails db:migrate'.

Ruby on Rails memiliki ekosistem yang kaya dengan berbagai pustaka (gems) dan plugin yang dapat digunakan untuk memperluas fungsionalitas aplikasi. Ada banyak gems yang tersedia untuk berbagai keperluan, seperti otentikasi pengguna, pengelolaan gambar, pemrosesan pembayaran, dan masih banyak lagi. Adapun, dengan fitur-fitur seperti migrasi database, pembuatan kode yang cepat dengan metode bawaan, dan pustaka yang kaya, Ruby on Rails memungkinkan development aplikasi web yang cepat dan efisien. Rails juga mendukung prinsip-prinsip Agile dan metode pengembangan cepat lainnya. Untuk bacaan lebih lanjut dan tutorial tentang Ruby on Rails, dapat mengunjungi situs web resmi Rails (https://rubyonrails.org/) dan sumber daya online seperti Ruby on Rails Guides (https://guides.rubyonrails.org/) dan Ruby on Rails Tutorial by Michael Hartl (https://www.railstutorial.org/).

## Reference
- Rails official website (https://rubyonrails.org/)
- Ruby on Rails Guides (https://guides.rubyonrails.org/)
- Rails architecture illustration (https://medium.com/the-renaissance-developer/ruby-on-rails-http-mvc-and-routes-f02215a46a84)
- Get to know Rails [Bahasa Indonesia] (https://www.niagahoster.co.id/blog/ruby-on-rails-adalah/)
- Ruby Programming Language [Bahasa Indonesia] (https://codingstudio.id/blog/bahasa-pemrograman-ruby/)
- Object Relational Mapping (ORM) in Rails (https://ygok17.medium.com/what-is-object-relational-mapping-orm-in-ruby-on-rails-68d6b89fc75a)

