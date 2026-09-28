---
title: Nextflow training
type: Collection
---

Nextflow is a powerful tool for scalable and reproducible bioinformatics workflows, and nf-core provides a rich ecosystem of curated pipelines built on Nextflow’s latest framework. Australian BioCommons and the [National Bioinformatics Training Cooperative](https://www.biocommons.org.au/training-cooperative) have collaboratively developed high-quality Nextflow training resources, supporting life science researchers across Australia to build practical workflow skills. This collection brings these materials together in one place for self-paced learning and for trainers who want to reuse and rerun workshops in their local context.

### Browse the collection

{% assign nextflow_resources = site.data.all_content_list | add_collection | where: "collection", "nextflow_training" %}

#### Self-paced learning
##### Build your Nextflow skills through tutorials and practical learning resources

<div class="row row-cols-1 row-cols-md-2 g-4 mb-5">
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
						 <a href="{{ resource.url }}" aria-label="Open {{ resource.name }}">Open resource</a>
					</div>
				</div>
			</div>
		{% endif %}
	{% endfor %}
</div>

#### Resources for trainers
##### Find reusable workshop materials and guidance for delivering Nextflow training

<div class="row row-cols-1 row-cols-md-2 g-4 mb-5">
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
						 <a href="{{ resource.url }}" aria-label="Open {{ resource.name }}">Open resource</a>
					</div>
				</div>
			</div>
		{% endif %}
	{% endfor %}
</div>
