<script lang="ts">
	import employeeImage from '$lib/images/employee.jpeg';
	import { Col, Row } from '@sveltestrap/sveltestrap';
</script>

<Row class="d-flex p-4 m-0">
	<Col xl={6}>
		<h2 class="text display-5 fw-bold">Hiring</h2>
		<p class="text">
			Here at ψέματα technologies, we strive for the greatest employees possible. You must have no
			mental disorders, no kids, and most importantly be kind! We are currently looking for people
			to work here. We are a good suit for you because we are well paying, good benefits, and <span
				class="test"
				contenteditable
			>
				trustworthy
			</span>.
		</p>
	</Col>
	<Col xl={6} class="text-center p-0">
		<img src={employeeImage} class="rounded border border-3" alt="employee" />
		<p id="image-text" class="text">Our number 1 employee</p>
	</Col>
</Row>

<svg>
	<defs>
		<filter id="squiggly-0">
			<feTurbulence id="turbulence" baseFrequency="0.04" numOctaves="3" result="noise" seed="0" />
			<feDisplacementMap id="displacement" in="SourceGraphic" in2="noise" scale="6" />
		</filter>
		<filter id="squiggly-1">
			<feTurbulence id="turbulence" baseFrequency="0.04" numOctaves="3" result="noise" seed="1" />
			<feDisplacementMap in="SourceGraphic" in2="noise" scale="8" />
		</filter>

		<filter id="squiggly-2">
			<feTurbulence id="turbulence" baseFrequency="0.04" numOctaves="3" result="noise" seed="2" />
			<feDisplacementMap in="SourceGraphic" in2="noise" scale="6" />
		</filter>
		<filter id="squiggly-3">
			<feTurbulence id="turbulence" baseFrequency="0.04" numOctaves="3" result="noise" seed="3" />
			<feDisplacementMap in="SourceGraphic" in2="noise" scale="8" />
		</filter>

		<filter id="squiggly-4">
			<feTurbulence id="turbulence" baseFrequency="0.04" numOctaves="3" result="noise" seed="4" />
			<feDisplacementMap in="SourceGraphic" in2="noise" scale="6" />
		</filter>
	</defs>
</svg>

<style>
	#image-text {
		font-size: 1.5em;
	}

	@media (min-width: 768px) {
		img {
			width: 400px;
			height: 400px;
		}
	}

	@media (max-width: 767px) {
		img {
			width: 200px;
			height: 200px;
		}
	}

	/* Taken from https://speckyboy.com/text-distortion-effects/ */
	@keyframes squiggly-anim {
		0% {
			filter: url('#squiggly-0');
		}

		25% {
			filter: url('#squiggly-1');
		}

		50% {
			filter: url('#squiggly-2');
		}

		75% {
			filter: url('#squiggly-3');
		}

		100% {
			filter: url('#squiggly-4');
		}
	}

	.test {
		animation: squiggly-anim 0.34s linear infinite;
	}
</style>
