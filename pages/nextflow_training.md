---
title: Nextflow training
type: Collection
---

Nextflow is a powerful tool for scalable and reproducible bioinformatics workflows, and nf-core provides a rich ecosystem of curated pipelines built on Nextflow’s latest framework. Australian BioCommons and the [National Bioinformatics Training Cooperative](https://www.biocommons.org.au/training-cooperative) have collaboratively developed high-quality Nextflow training resources, supporting life science researchers across Australia to build practical workflow skills. This collection brings these materials together in one place for self-paced learning and for trainers who want to reuse and rerun workshops in their local context.

### Browse the collection

<div class="navigation-tiles row row-cols-1 row-cols-md-2 g-4 my-4">
	<div class="col">
		<a class="card h-100 text-decoration-none text-body" href="#self-paced-learning">
			<div class="card-body">
				<p class="card-title h2 border-0 pt-0">Self-paced learning</p>
				<p class="card-text">Build your Nextflow skills through tutorials and practical learning resources.</p>
			</div>
		</a>
	</div>
	<div class="col">
		<a class="card h-100 text-decoration-none text-body" href="#training-materials">
			<div class="card-body">
				<p class="card-title h2 border-0 pt-0">Training materials</p>
				<p class="card-text">Find reusable workshop materials and guidance for delivering Nextflow training.</p>
			</div>
		</a>
	</div>
</div>

{% assign nextflow_resources = site.data.all_content_list | add_collection | where: "collection", "nextflow_training" %}

## Self-paced learning

<div class="row row-cols-1 row-cols-md-2 g-4 mb-5" id="self-paced-learning">
	{% for resource in nextflow_resources %}
		{% if resource.topics == "self-paced learning" %}
			<div class="col">
				<div class="card border h-100">
					<div class="card-body d-flex flex-column">
						<h3 class="card-title h5">{{ resource.name }}</h3>
						<p class="card-text">{{ resource.description }}</p>
						<dl class="mb-0 mt-auto small">
							<dt>Provider</dt>
							<dd>{{ resource.provider }}</dd>
							<dt>Format</dt>
							<dd>{{ resource.type }}</dd>
						</dl>
					</div>
					<div class="card-footer bg-transparent">
						<a href="{{ resource.url }}">Open resource</a>
					</div>
				</div>
			</div>
		{% endif %}
	{% endfor %}
</div>

## Training materials

<div class="row row-cols-1 row-cols-md-2 g-4 mb-5" id="training-materials">
	{% for resource in nextflow_resources %}
		{% if resource.topics == "workshop materials" %}
			<div class="col">
				<div class="card border h-100">
					<div class="card-body d-flex flex-column">
						<h3 class="card-title h5">{{ resource.name }}</h3>
						<p class="card-text">{{ resource.description }}</p>
						<dl class="mb-0 mt-auto small">
							<dt>Provider</dt>
							<dd>{{ resource.provider }}</dd>
							<dt>Format</dt>
							<dd>{{ resource.type }}</dd>
						</dl>
					</div>
					<div class="card-footer bg-transparent">
						<a href="{{ resource.url }}">Open resource</a>
					</div>
				</div>
			</div>
		{% endif %}
	{% endfor %}
</div>
