# My Projects

## Signal Quality Assessment for Reliable Fetal Heart Rate Detection Using Deep Learning

The present work is concerned with assessing the signal quality of a four-channel non-invasive fetal ECG recording. The fetal ECG recordings contain multiple fetal and maternalnoise sources and are destined to be used to estimate the Fetal Heart Rate (FHR). Highsignal quality is associated with reliable FHR estimation and low quality with unreliable.We approached the topic from the perspective of anomaly detection, in which low qualitysignals are considered anomalies. For this purpose, two deep learning-based approachesfor anomaly detection were explored. The first approach consisted of autoencoders trainedon data considered non-anomalous. Then, the reconstruction error serves as an anomalymetric.  To encapsulate the temporal interdependence of the data, we used an LSTMclassifier that labelled a segment as an anomaly based on its reconstruction error as wellas the reconstruction errors of the segments that preceded it.  Two autoencoders weredeveloped, one operating on the time domain and one on the frequency domain.  Theresulting final pipeline has relatively adequate performance. The second approach was theGAN based anomaly detection. In this technique, a GAN is trained to generate data thatare considered non-anomalous using a random vector input sampled from a latent space.Afterwards, a query sample is mapped to this latent space, something that can be donewith a few techniques that we discuss, and the mapped latent vector is used to re-generatethe segment. The fidelity of the re-generated sample serves as an anomaly score. GAN-based anomaly detection can be conducted locally; so we can train GANs to generate longsignals and assess the quality in their segments. In order to generate signals, we proposed anew GAN architecture aimed to generate signals based on their frequency representation.Unfortunately, the GAN based anomaly detection did not work on the target dataset.However, it did work successfully on a simpler dataset, showcasing its efficacy.
