Overview
============

As highlighted in the ratio combination paper, the calculation of a polyclonal titer becomes
complicated and difficult to interpret depending on the interaction model.

The formula for the additive model is the sum titers unless the Hill slope is not 1 (which it may not be)

The formula for the bliss-hill model is a polynomial root, there's a proto-package that does this calculation in R:
https://github.com/mayerbry/combination_titer

Specifically for the BH: BH is an neutralization interaction. The titer represents a distance factor on the individual titers that reduces neutralization to a desired level. The ratio combination paper shows that the BH titer does not uniquely map to a neutralization. That is, a BH titer of 300 may correspond to a wide range of underlying neutralization, all higher than the neutralization of a monoclonal at a titer of 300. The downside of this is that if the actual correlate is neutralization (rather than titer by proxy), a monoclonal titer threshold or dose-response could under-estimate the equivalent BH titer dose-response effect. This could suggest that for combination bnabs and maybe even for a vaccine(!), the bar may be lower than the AMP correlate threshold.

The goal of this project was to better spell out polyclonal titer at a technical level. 

- How does the assay logistic curve convolute across multiple antibodies? 
- Is IIP a better outcome as it combines the ID80 and ID50 to incorporate a slope? 
- Could IIP always be calculated as an extrapolation to titration = 1:1 in a vaccine context?


