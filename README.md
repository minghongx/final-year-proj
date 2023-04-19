## Activity Diary

```mermaid
gantt
    dateFormat  YYYY-MM-DD

    Literature Review: literature_review, 2022-10-17, 2022-10-31

    section Preparation
    Implement a SOTA algo: 2022-10-24, 7d
    Test the algo on popular environments: test_algo, 2022-10-30, 2d
    Algorithm is ready : milestone, 2022-11-01, 0d

    section Sanity Test
    Load the robot into the simulator: load_robot, after test_algo, 3d
    Set a randomly generated target: generate_target, after load_robot, 5d
    Define the reward function: after generate_target, 7d
    Match the interface between algo and simulation: 2022-11-12, 2022-11-20
    Training: traning_in_empty_world, 2022-11-16, 2022-11-20
    Trained a policy in an empty world: milestone, 2022-11-20, 
    
    section Training
    Set up an indoor environment filled with obstacles for training: setup_indoor_env, after traning_in_empty_world, 7d
    Training in the indoor environment: training_in_indoor_env, after setup_indoor_env, 2022-12-16
    Trained a policy for mapless navi: milestone, after training_in_indoor_env

    section Training-Evaluation Loop
    Set up another environment for evaluating the performance of trained policy: setup_devel_env, after training_in_indoor_env, 7d
    Repeat Training & Evaluating loop: training_evaluating_loop, after setup_devel_env, 28d
    Select a policy which has the best performance on evaluating env: milestone, after training_evaluating_loop
```