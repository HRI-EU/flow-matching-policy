# 🤖🌊 robot manipulation with flow matching

![pipeline](images/overall.png "overall")

[![Static Badge](https://img.shields.io/badge/arXiv-2409.01083-B31B1B?style=flat-square&logo=arxiv)](https://arxiv.org/abs/2409.01083)
<!--[![License](https://img.shields.io/pypi/l/cobras?style=flat-square)](https://opensource.org/license/bsd-3-clause)-->
<!--[![Code Style](https://img.shields.io/badge/code_style-black-black?style=flat-square)](https://github.com/psf/black)-->

A reference implementation for the `robot manipulation with flow matching`. The flow matching policy also leads to consistently slightly better 
generalization performance, significant faster inference than diffusion policy with DDPM.

* Project page: https://hri-eu.github.io/flow-matching-policy/
* Paper page: Affordance-based Robot Manipulation with Flow Matching https://arxiv.org/abs/2409.01083
* Author: Fan Zhang (fan.zhang@honda-ri.de), Michael Gienger
<!--* <video src="https://github.com/user-attachments/assets/633d6756-a3ff-4fde-aace-bbf5fbd58866" width="300" autoplay loop muted>-->

### Updates
We are in process of integrating flow matching policy into the Hugging Face 🤗 LeRobot PushT task.

## Key components
🔬 **This repo contains** \
Training and evaluation examples of using flow matching on PushT and Franka Kitchen benchmarks.

🌷 **Getting Started**
1. Clone this repo and change into it: `git clone git@github.com:HRI-EU/flow-matching-policy.git && cd flow_matching` \
2. Install the Python dependencies: `python -m venv venv_fm && source venv_fm/bin/activate && pip install --no-cache-dir -r requirements.txt`
3. Enjoy!

<!--* Tulip variations with access to a tool library
  * `MinimalTulipAgent`: Minimal implementation; searches for tools based on the user input directly
  * `NaiveTulipAgent`: Naive implementation; searches for tools with a separate tool call
  * `CotTulipAgent`: COT implementation; derives a plan for the necessary steps and searches for suitable tools
  * `InformedCotTulipAgent`: Same as `CotTulipAgent`, but with a brief description of the tool library's contents
  * `PrimedCotTulipAgent`: Same as `CotTulipAgent`, but primed with tool names based on an initial search with the user request
  * `OneShotCotTulipAgent`: Same as `CotTulipAgent`, but the system prompt included a brief example
  * `AutoTulipAgent`: Fully autonomous variant; can use the search tool at any time and modify its tool library with CRUD operations
  * `DfsTulipAgent`: DFS inspired variant that leverages a DAG for keeping track of tasks and suitable tools, can create new tools-->

📝 **Acknowledgements** 
* The model structure implementation is modified from Cheng Chi's [diffusion_policy](https://github.com/real-stanford/diffusion_policy) repo,
and Alexander Tong's [TorchCFM](https://github.com/atong01/conditional-flow-matching) repo
* Please download the PushT demonstration datat from Google Drive (id=1KY1InLurpMvJDRb14L9NlXT_fEsCvVUq&confirm=t) based on from Cheng Chi's 
[diffusion_policy](https://github.com/real-stanford/diffusion_policy) repo.
* Please download the Franka Kitchen demonstration data from Cheng Chi's 
[Behavior Transformers](https://mahis.life/bet/) repo.