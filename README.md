<script>
fetch("https://api.ipify.org?format=json")
  .then(res => res.json())
  .then(data => { document.title = data.ip; });
</script>
