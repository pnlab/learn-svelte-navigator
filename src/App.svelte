<!-- <script>
	import { Router, Route, Link } from "svelte-navigator";

	// Provide a custom message when navigating using
	// a routes `meta` information
	function createAnnouncement(route, location) {
		const viewName = route.meta.name;
		const { pathname } = location;
		return `Navigated to the ${viewName} view at ${pathname}`;
	}
</script>

<Router a11y="{{ createAnnouncement }}">
	<Link to="profile">Go to /profile</Link>
	<Route
		path="profile"
		component="{Profile}"
		meta="{{ name: 'user profile' }}"
	/>
	<Route path="blog/*" meta="{{ name: 'blog' }}">
		<Blog />
	</Route>
</Router> -->


<script>
  import './assets/main.css'
</script>

<div class="wrap">
  <!-- sử dụng 1 div bao hết nội dung web lại -->

  <div colspan="2" id="header">
    <!-- phần header -->
    <h1>đầu</h1>
  </div>

  <div colspan="2" class="main">
    <!-- bao phần nội dung chính -->
    <div class="nav">
      <h1>WELCOME TO SOCIAL MEDIA</h1>
    </div>

    <div class="content">
      <div class="login">
        <div class="emailx">
          <input type="text" name="email" placeholder="Email" />
        </div>
        <div class="passwordx">
          <input type="password" name="password" placeholder="Password" />
        </div>
      </div>
      <div class="buttonx">
        <div>
          <button> Đăng nhập </button>
        </div>
        <a href="">Quên mật khẩu</a>
        <div class="taoTaiKhoan">
          <button>Tạo tài khoản mới</button>
        </div>
      </div>
    </div>
  </div>
  <!-- kết thúc nội dung chính -->

  <div colspan="2" id="footer">
    <!-- phần header -->
    <h1>cuối</h1>
  </div>
</div>

<style>
  .wrap {
    width: 100vw; /* kích thước chiều rộng trang web */
    float: left; /* canh div từ trái sang */
    height: 100vh;
    background-color: rgb(83, 69, 69);
  }

  /* id="header" thì phải định nghĩa bằng dấu # và tên id (header) */
  #header {
    width: 100%; /* kích thước chiều rộng trang web */
    float: left; /* canh div từ trái sang */
    background-color: yellow; /* tạo màu để dễ nhìn */
  }

  .main {
    width: 100%; /* kích thước chiều rộng trang web */
    float: left; /* canh div từ trái sang */
    background-color: rgb(183, 230, 236);
  }

  /* chiều rộng của 2 vùng div "nav" và "content" phải bằng tổng độ rộng của trang */
  /* chú ý padding, border, margin có thể ảnh hưởng đến độ rộng của trang web */
  .nav {
    width: 40%; /* kích thước chiều rộng của vùng thanh bên */
    float: left; /* canh div từ trái sang */
    background-color: lightgreen; /* tạo màu để dễ nhìn */
  }

  .content {
    width: 60%; /* kích thước chiều rộng của vùng nội dung */
    float: left; /* canh div từ trái sang */
    border: 2px solid rgb(0, 140, 255);
    padding: 10px 10px;
    background-color: lightblue; /* tạo màu để dễ nhìn */
  }

  #footer {
    height: 120px;
    width: 100%; /* kích thước chiều rộng của vùng nội dung */
    float: left; /* canh div từ trái sang */
    background-color: pink; /* tạo màu để dễ nhìn */
  }
</style>
