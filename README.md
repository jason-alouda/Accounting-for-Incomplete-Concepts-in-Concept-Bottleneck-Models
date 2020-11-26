# Accounting for Incomplete Concepts in Concept Bottleneck Models

Co-authored by Irena Gao

# Intro
Imagine a hospital is using a deep learning model to grade
knee osteoarthritis from x-rays. Ideally, an expert radiologist
could collaboratively interact with the model. If, at test-time,
the radiologist disagrees with the model about some prediction,
she might want to query why the model behaved the way it did
— did the model detect joint space narrowing that she missed?
Alternatively, she might want to intervene on the model —
would the model change its prediction if she declared that
there was no narrowing?
Recently, Koh et al. (2020) proposed Concept Bottleneck
Models [4], a framework for models that support this kind
of interaction. In a Concept Bottleneck Model (CBM), a
network first learns to predict meaningful high-level concepts
(e.g. joint space narrowing in knee x-rays) before predicting
the final target (e.g. osteoarthritis severity). Importantly, our
radiologist can intervene on a CBM at test-time by overriding
the predicted concepts with her own judgement.
In this project, we extend the CBM paper to account for
incomplete sets of concepts while preserving the effectiveness
of test-time interventions. Specifically, we increase the width
of the concept bottleneck layer to predict both specified concepts
c and unspecified latent concepts s. The final prediction
y is based on both c and s. We also examine the use of
regularization to limit the network’s reliance on s and preserve
the effectiveness of interventions.

Link to repo: https://github.com/jason-alouda/ConceptBottleneck


Link to full paper: https://jason-portfolio.vercel.app/images/CS221_Project_Final.pdf
