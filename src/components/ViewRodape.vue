<template lang="">
<div class="footer">
    <ul class="social-icons">
        <li><a href="https://www.facebook.com/pedro.ponte2" target="_blank"><img src="../assets/facebook.png" alt="Facebook"></a></li>
        <li><a href="https://twitter.com/pedroponte1989"  target="_blank"><img src="../assets/x.png" alt="twitter"></a></li>
        <li><a href="https://www.instagram.com/pedro.ponte2/" target="_blank"><img src="../assets/instagram.png" alt="Instagram"></a></li>
        <li><a href="https://www.linkedin.com/in/pedroponte1989" target="_blank"><img src="../assets/LinkedIn.png" alt="LinkedIn"></a></li>
    </ul>
</div>
</template>
<script>
export default {
    name:"ViewRodape"
}
</script>
<style >
      .footer {
            background-color: #000000;
            padding: 20px;
            text-align: center;
        }
        .footer a{
            color: #fff;
        }
        .social-icons {
            list-style: none;
            padding: 0;
        }
        .social-icons li {
            display: inline;
            margin-right: 10px;
        }
        .social-icons li:last-child {
            margin-right: 0;
        }
        .social-icons a {
            text-decoration: none;
        }
        .social-icons img{
            width: 50px;
        }
</style>