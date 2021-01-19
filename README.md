<!--
*** Thanks for checking out. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request.
*** Thanks again!
-->


<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/slohani-ai/LG-OAM-simulations-with-Tensors/">
    <img src="images/Image_1.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">LG-OAM with Tensors (GPU/CPU)</h3>

  <p align="center">
    Let's leverage the power of tensor operations in simulating LG-OAM intensity patterns and phase patterns for a Spatial Light Modulator (SLM). Being tensors, the generated patterns can be directly fed into any machine learning frameworks.
    <br />
    <a href="https://github.com/slohani-ai/LG-OAM-simulations-with-Tensors/"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/slohani-ai/LG-OAM-simulations-with-Tensors/blob/main/Superposition_OAM_Tensors_GPU.ipynb">Superposition OAM Tensors</a>
    .
    <a href="https://github.com/slohani-ai/LG-OAM-simulations-with-Tensors/blob/main/NonSuperposition_OAM_Tensors-GPU.ipynb">Non-Superposition OAM Tensors</a>
    ·
    <a href="https://github.com/slohani-ai/LG-OAM-simulations-with-Tensors/issues">Report Bug</a>
    ·
    <a href="https://github.com/slohani-ai/LG-OAM-simulations-with-Tensors/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

Optical communication relies on the generation, transmission, and detection of states of light to encode and send information. In order to increase the transfer rate one of the most promising methods is making use of orbital angular momentum (OAM) states of light. However, a primary technical difficulty is the accurate classification of OAM value  detected at the receiver. This project explores the various ways to simulate LG-OAM states (with GPU) that can be easily applied to train/test any machine learning setups at the receiver in prior. Additionally, the code generates phase patterns that can be uploaded to a SLM in order to have the correspoinding spatial distribution at the receiver. Overall this provides the robust way to simulate Laguerre-Gauss OAM modes to be used in the real-world communication setups.


### Built With

* [Tensorflow 2.4](https://www.tensorflow.org/)
* [Tensorflow Probability](https://www.tensorflow.org/probability)



<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running follow these simple steps.

### Prerequisites

Please install libraries from the requirements.txt file
  ```sh
  pip install requirements.txt
  ```

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/slohani-ai/LG-OAM-simulations-with-Tensors.git
   ```
<!-- 
2. Install NPM packages
   ```sh
   npm install
   ```
-->


<!-- USAGE EXAMPLES -->
## Usage

```sh
from utils.Imaging import Save
from utils.Noise import Noise_Dist
from source.OAM_Intensity_Phase import LG_Lights_Tensorflow

lg = LG_Ligths_Tensorflow(xpixel,ypixel,dT,verbose)
```
where xpixel = width, ypixel = height, dT = SLM resolution (typically 8e-6 m), and versbose is False as default.

It only requires a single line of code to simulate everything.

* [Superpostion Modes](https://github.com/slohani-ai/LG-OAM-simulations-with-Tensors/blob/main/Superposition_OAM_Tensors_GPU.ipynb)
  * A single batch of superpostion of various modes
  $`\psi = \alpha_1 |LG_{0,1}^{\ell_1}\rangle + \alpha_2|LG_{0,1}^{\ell_2}\rangle+ \alpha_2|LG_{0,1}^{\ell_2}\rangle + ... ...`$
  
```sh
Intensity, Phase = lg.Superposition(p_l_array,alpha_array,w,grating_period,save_image)
```
# Simultaneous simulation for multple batches of superpostion modes

where p_l_array


_For more examples, please refer to the [Documentation](https://example.com)_



<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/github_username/repo_name/issues) for a list of proposed features (and known issues).



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.



<!-- CONTACT -->
## Contact

Your Name - [@twitter_handle](https://twitter.com/twitter_handle) - email

Project Link: [https://github.com/github_username/repo_name](https://github.com/github_username/repo_name)



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements

* []()
* []()
* []()





<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/github_username/repo.svg?style=for-the-badge
[contributors-url]: https://github.com/github_username/repo/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/github_username/repo.svg?style=for-the-badge
[forks-url]: https://github.com/github_username/repo/network/members
[stars-shield]: https://img.shields.io/github/stars/github_username/repo.svg?style=for-the-badge
[stars-url]: https://github.com/github_username/repo/stargazers
[issues-shield]: https://img.shields.io/github/issues/github_username/repo.svg?style=for-the-badge
[issues-url]: https://github.com/github_username/repo/issues
[license-shield]: https://img.shields.io/github/license/github_username/repo.svg?style=for-the-badge
[license-url]: https://github.com/github_username/repo/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/github_username
