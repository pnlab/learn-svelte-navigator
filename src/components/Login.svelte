<script>
  import { useNavigate } from "svelte-navigator"
  let user = ""; // var, let
  let password = ""; 
  const navigate = useNavigate();

  const handleLogin =(e)=>{
    e.preventDefault()
    // gọi api đăng nhập
    // kết quả lưu vào bộ nhớ trình duyệt
    
    navigate('/') // chuyển hướng vể trang chủ 
    console.log("User Login: ", user)    
    
  }


</script>

<div>
  <h1>Hello {user}</h1>
 <form class='form' on:submit={handleLogin} >
    <input type="text" placeholder="Name" bind:value={user} />
    <input type="password" bind:value={password} />
    <button type="submit">Login</button>
 </form>
</div>

<style>
  .form{
    display: flex;
    flex-direction: column;
  }
  h1{
    color: red;
  }
</style>
