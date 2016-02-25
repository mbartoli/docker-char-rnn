# docker-char-nn
Docker container for use with Multi-layer Recurrent Neural Networks (LSTM, GRU, RNN) for character-level language models in Torch

## Usage
Run `docker run -it mbartoli/char-rnn`

### Persistent checkpoint
1. Create a folder `cv` to persist training data with `mkdir cv`.
2. Mount the folder into the container and run it:   
```docker run -v $(pwd)/cv:/home/char-rnn/cv -it mbartoli/char-rnn```
3. Train your char-rnn


### Custom training data
1. Create a folder containing some training data.   
```mkdir -p data/my-training-data```
2. Run the container with the new training data and `cv` folder mounted   
```docker run -v $(pwd)/cv:/home/char-rnn/cv -v $(pwd)/data/my-training-data:/home/char-rnn/data/my-training-data -it mbartoli/char-rnn```
3. Train your char-rnn

## Training and sampling
See the [documentation](https://github.com/karpathy/char-rnn) on how to train and sample your char-rnn.

## More Information
Docker Hub: [mbartoli/char-nn](https://hub.docker.com/r/mbartoli/char-rnn/)  
[https://github.com/karpathy/char-rnn](https://github.com/karpathy/char-rnn)   
[http://karpathy.github.io/2015/05/21/rnn-effectiveness/](http://karpathy.github.io/2015/05/21/rnn-effectiveness/)
