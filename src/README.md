## Binding HTML in Svelte

You can save html in const/let and can display it in html using:

```
{@html VARIABLENAME}
```

eg:

```
<script>
	const htmlBinding = '<strong>Hello World!</strong>';
</script>

<main>
	<h1>{@html htmlBinding}</h1>
</main>
```

## Caution

Please use HTML Binding with caution as its allows XSS attacks.
