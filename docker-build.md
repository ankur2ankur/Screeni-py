
docker kill ank-screeni-py

# Build Image
docker build -t ank-screeni-py:2.23 -f ./Dockerfile .

# Run Image (Auto Start Mode)
docker run --name ank-screeni-py -p 8501:8501 -d --restart unless-stopped ank-screeni-py:2.23

# Run Image (And Auto Start Mode apply)
docker run --name ank-screeni-py -p 8501:8501 -d ank-screeni-py:dev
docker update --restart unless-stopped ank-screeni-py


# docker run --name screeni-py -p 8502:8501 -d --restart unless-stopped joshipranjal/screeni-py:2.22
# docker update --restart unless-stopped screeni-py
