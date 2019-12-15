# Training the RollerBall

Clone repo and open project, build it for Linux platform and save it in tf/envs folder.

Start training.

```bash
cd tf

# Change run-id every run to compare the effect of different configurations
mlagents-learn config.yaml --env=envs/RollerBall --run-id=RollerBall-1 --train

tensorboard --logdir=summaries --port 6006

cp models/RollerBallBrain.nn ../Assets/TFModels
```

Open project again and, on agent prefab, assign to Behavior Preferences model the `RollerBallBrain`.

Play project.