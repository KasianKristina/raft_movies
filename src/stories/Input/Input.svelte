<script lang="ts">
	import './input.css';

	export let type: string = 'text';
	export let value: string = '';
	export let placeholder: string = '';
	export let label: string = '';
	export let name: string = '';
	export let id: string = name;
	export let required: boolean = false;
	export let disabled: boolean = false;
	export let errorMessage: string = '';

	let isFocused: boolean = false;
	let hasValue: boolean = false;

	$: hasValue = Boolean(value);

	const handleFocus = () => (isFocused = true);
	const handleBlur = () => (isFocused = false);
</script>

<div class="input-wrapper">
	<div class="input-container" class:error={errorMessage}>
		{#if label}
			<label for={id} class="floating-label" class:active={isFocused || hasValue}>
				{label}
			</label>
		{/if}

		<input
			{type}
			{name}
			{id}
			{required}
			{disabled}
			bind:value
			on:focus={handleFocus}
			on:blur={handleBlur}
			class="input"
            class:input-with-label={Boolean(label)}
			placeholder={!label ? placeholder : null}
			{...$$restProps}
		/>
	</div>

	{#if errorMessage}
		<div class="error-message">{errorMessage}</div>
	{/if}
</div>
