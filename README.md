# Control AI robots with phospho

**phospho** (or **phosphobot**) is a software that lets you control robots, record data, train and use VLA (vision language action models).

<div align="center">

<a href="https://pypi.org/project/phosphobot/"><img src="https://img.shields.io/pypi/v/phosphobot?style=flat-square&label=pypi+phospho" alt="phosphobot Python package on PyPi"></a>
<a href="https://www.ycombinator.com/companies/phospho"><img src="https://img.shields.io/badge/Y%20Combinator-W24-orange?style=flat-square" alt="Y Combinator W24"></a>
<a href="https://discord.gg/cbkggY6NSK"><img src="https://img.shields.io/discord/1106594252043071509" alt="phospho discord"></a>

</div>

## Overview of phospho

- 🧑‍💻 Features a simple and clean UI to get you started in no time
- 🕹️ Control your robots to record datasets in minutes with a headset, a keyboard, a gamepad, a leader arm, and more
- 💿 Fully accessible simulation environment for your robot
- 🔢 Easy and quick calibration to get your started in no time
- ⚡ Train Action models such as ACT, smolVLA, π0.5 or gr00t-n1.5 in one click
- 🦾 Compatible with the SO-100, SO-101, Unitree Go2, Agilex Piper...
- 🚪 Dev-friendly API that let's you interact through code
- 🤗 Fully compatible with LeRobot and HuggingFace
- 🖥️ Runs on macOS, Linux and Windows
- 🥽 Meta Quest app for teleoperation
- 📸 Supports most cameras (classic, depth, stereo)
- 🔌 Open Source: [Extend it with your own robots and cameras](https://github.com/phospho-app/phosphobot/tree/main/phosphobot)

## Getting started with phosphobot

### 1. Get a robot

Purchase your phospho starter pack at [robots.phospho.ai](https://robots.phospho.ai/starter-pack), or use one of the supported robots:

- [SO-101](https://docs.phospho.ai/so-101/quickstart)
- [SO-100](https://docs.phospho.ai/so-100/quickstart)
- [Koch v1.1](https://github.com/jess-moss/koch-v1-1) (beta)
- WX-250 by Trossen Robotics (beta)
- [LeCabot](https://github.com/phospho-app/lecabot) (beta)
- [Unitree Go2 Air, Pro, Edu](https://shop.unitree.com/en-fr/products/unitree-go2) (beta)
- [AgileX Piper](https://global.agilex.ai/products/piper) (Linux-only, beta. Make sure you install the required packages: `sudo apt ethtool can-utils`)

See this [README](phosphobot/README.md) for more details on how to add support for a new robot.

### 2. Install the phosphobot server

Install phosphobot for your OS [using the one liners available here](https://docs.phospho.ai/installation).

### 3. Make your robot move for the first time!

Go to the webapp at `YOUR_SERVER_ADDRESS:YOUR_SERVER_PORT` (default is `localhost:80`) and click control.

You'll be able to control your robot with:

- a keyboard
- a gamepad
- a leader arm
- a Meta Quest

> _Note: port 80 might already be in use, if that's the case, the server will spin up on localhost:8020_

### 4. Record a dataset

Record a 50 episodes dataset of the task you want the robot to learn.

Check out the [docs](https://docs.phospho.ai/basic-usage/dataset-recording) for more details.

### 5. Train an action model

To train an action model on the dataset you recorded, you can:

- train a model directly from the phosphobot webapp (see [this tutorial](https://docs.phospho.ai/basic-usage/training))
- use your own machine (see [this tutorial](tutorials/00_finetune_gr00t_vla.md) to finetune gr00t n1)

In both cases, you will have a trained model exported to Huggingface.

To learn more about training action models for robotics, check out the [docs](https://docs.phospho.ai/basic-usage/training).

### 6. Use the model to control your robot

Now that you have a trained model hosted on huggingface, you can use it to control your robot either:

- directly from the webapp
- from your own code using the phosphobot python package (see [this script](scripts/quickstart_ai_gr00t.py) for an example)

Learn more [in the docs](https://docs.phospho.ai/basic-usage/inference).

Congrats! You just trained and used your first action model on a real robot.

## Advanced Usage

You can directly call the phosphobot server from your own code, using the API.

Go to the interactive docs of the API to use it interactively and learn more.

It is available at `YOUR_SERVER_ADDRESS:YOUR_SERVER_PORT/docs` (default: `localhost:80/docs`)

We release new versions very often, so make sure to check the API docs for the latest features and changes.

## Join the Community

Connect with other developers and share your experience in our [Discord community](https://discord.gg/cbkggY6NSK)

## Install from source

1. Download and install [uv](https://docs.astral.sh/uv/getting-started/installation/) and [npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm). Best compatibility is with `python>=3.10` and `node>=20`.

2. Clone github

```bash
git clone https://github.com/phospho-app/phosphobot.git
```

3. On MacOS and Linux, to build the frontend and start the backend, run:

```bash
make
```

On Windows, the Makefile don't work. You can run the commands directly.

```
cd ./dashboard && (npm i && npm run build && mkdir -p ../phosphobot/resources/dist/ && cp -r ./dist/* ../phosphobot/resources/dist/)
cd phosphobot && uv run --python 3.10 phosphobot run --simulation=headless
```

4. Go to `localhost:80` or `localhost:8020` in your browser to see the dashboard. Go to `localhost:80/docs` to see API docs.

## Contributing

We welcome contributions! Read our [contribution guide](./CONTRIBUTING.md). Also checkout our [bounty program](https://docs.google.com/spreadsheets/d/1NKyKoYbNcCMQpTzxbNJeoKWucPzJ5ULJkuiop4Av8ZQ/edit?gid=0#gid=0).

Here are some of the ways you can contribute:

- Add support for new AI models
- Add support for new teleoperation controllers
- Add support for new robots and sensors
- Add something you built to the examples
- Improve the dataset collection and manipulation
- Improve the [documentation and tutorials](https://github.com/phospho-app/docs)
- Improve code quality and refacto
- Improve the performance of the app
- Fix issues you faced

## Support

- **Documentation**: Read the [documentation](https://docs.phospho.ai)
- **Community Support**: Join our [Discord server](https://discord.gg/cbkggY6NSK)
- **Issues**: Submit problems or suggestions through [GitHub Issues](https://github.com/phospho-app/phosphobot/issues)

## License

MIT License

---

Made with 💚 by the Phospho community

Check out other free projects related to this as well. They will be helpful.

luckyAl_google-research.rar
https://drive.google.com/file/d/1y4eci0VTEVJOH-oIM9auF7l0y7Ob0e8h/view?usp=sharing

luckyAl_notebooks.rar
https://drive.google.com/file/d/1470iAKAqavHbzMrbZjJgljh4gwEnixjx/view?usp=sharing

luckyAl_punct_cap_seg_47_language.rar
https://drive.google.com/file/d/1hbNQx8xzYZSsVbwIdaRYD5zkKNOJBs9d/view?usp=sharing

luckyAl_ros.rar
https://drive.google.com/file/d/1mvO23xX3iZndCZImUN6lMhSaMxKea8Lk/view?usp=sharing

luckyAl_sentence_boundary_detection_multilang.rar
https://drive.google.com/file/d/1aSeWi5OAqjsAVkbewf3pV5Ib_uBfg4co/view?usp=sharing

Gru_coqui_pth.rar
https://drive.google.com/file/d/1ReaWzQO0N7leMEjn_JMgVKNzmFy3xwbR/view?usp=sharing

Gru_phosphobot.rar
https://drive.google.com/file/d/1veoORXzygzJjus0HUU24UhICRfo5E7MQ/view?usp=sharing

Gru_Qengineering_1.part1.rar
https://drive.google.com/file/d/18jJxKg7i_T7LKo6rShLoSJhTsjkHHR6P/view?usp=sharing

Gru_Qengineering_1.part2.rar
https://drive.google.com/file/d/1A1qKm78bBT_0R6eUlnN9jiwyRlkOyjFD/view?usp=sharing

Gru_Qengineering_1.part3.rar
https://drive.google.com/file/d/10t88kK4gugBuFt9gkQSGb9Zoh8H6zWiu/view?usp=sharing

Gru_Qengineering_2.rar
https://drive.google.com/file/d/1KVCM3gEt7QUx1T2FcmVF-d7DChV9atUP/view?usp=sharing

Gru_Qengineering_3.rar
https://drive.google.com/file/d/1dBnCPVDNX6TbzouqzqEfutBEM8I4WIWe/view?usp=sharing

Gru_Qengineering_4.rar
https://drive.google.com/file/d/1hQk_N6JIqnE3ndh4eOWug8FY0yVKDJco/view?usp=sharing

Gru_Qengineering_5.rar
https://drive.google.com/file/d/1hQk_N6JIqnE3ndh4eOWug8FY0yVKDJco/view?usp=sharing

Gru_Qengineering_6.rar
https://drive.google.com/file/d/10sOikO1h6Vmd02h5TkMEEUt_CMoZy8f5/view?usp=sharing

Gru_Qengineering_7.rar
https://drive.google.com/file/d/1FMyLApQ2KexY_A1IqY4vmJ2waOf9d9xX/view?usp=sharing

Gru_Qengineering_8.rar
https://drive.google.com/file/d/1mTWFmhVrsBJqLJx_0_UCEueLrwsy_PmC/view?usp=sharing

Gru_Qengineering_9.rar
https://drive.google.com/file/d/1QWz_RyhwKVMus8S-fTWjhK_GMK9_QSVd/view?usp=sharing

Gru_Qengineering_10.rar
https://drive.google.com/file/d/1f41xCFT2BfnLzqyHs5AdB7WMGU2UsI_t/view?usp=sharing

Gru_Qengineering_11.rar
https://drive.google.com/file/d/1GummpMtB2ek9pb2MLE4SQ2o0rjuXQFa8/view?usp=sharing

Gru_Qengineering_12.rar
https://drive.google.com/file/d/1nPIgjrQ7__M3WQJtrmx-CsCgmz2EkxCH/view?usp=sharing

Gru_Qengineering_13.rar
https://drive.google.com/file/d/1Ka245wvELPmutxkPQqkkt_AtrZkyoPj7/view?usp=sharing

Gru_Qengineering_14.rar
https://drive.google.com/file/d/1n_3ucB_ctHllNEGDWTgP49I5MFonuTuf/view?usp=sharing

Gru_Qengineering_15.rar
https://drive.google.com/file/d/1mi3iuxOEiVauQNUgwQTigP4Mr9dLq-8T/view?usp=sharing
