FROM bcgovimages/von-image:next-1

ADD requirements.txt .
RUN pip3 install --upgrade pip
RUN pip install --no-cache-dir -r ./fetch-validator-status/requirements.txt

ADD ./fetch-validator-status/networks.json .
ADD ./fetch-validator-status/*.py ./

ENTRYPOINT ["bash", "-c", "python main.py $@", "--"]