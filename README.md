Performs the nonparametric decomposition described in:

Norman-Haignere SV, Kanwisher NG, McDermott JH (2015). Distinct cortical pathways for music and
speech revealed by hypothesis-free voxel decomposition. Neuron.

The algorithm iteratively rotates the top K principal components of the data matrix, X, to
maximize a measure of non-Gaussianity ('negentropy'). This procedure is closely related to
standard algorithms for independent component analysis, but unlike standard algorithms does not
depend on assumptions about the type of non-Gaussian distribution being identified. Because
negentropy is estimated with a histogram, the algorithm tends to work well with a large number of
data points (~10,000). The run-time of the algorithm increases substantially as the number of
components is increased because the optimization is performed via a brute-force search over all
pairs of components (run-time is thus proportional nchoosek(K,2) where K is the number of
components).

see nonparametric_ica.m for details on use. 