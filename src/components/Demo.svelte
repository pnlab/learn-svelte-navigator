<script>
  import { Router, Link, Route } from "svelte-navigator";
  import Home from "./components/Home.svelte";
  import Login from "./components/Login.svelte";
</script>

<div>
  <Router>
    <nav>
      <Link to="/">Home</Link> 
      <Link to="login">Login</Link>
    </nav>
    <div>
      <Route path="/">
        <Home/>
        <Login />        
      </Route>
      <Route path="login">
        <Login />
      </Route>
    </div>
  </Router>
</div>
