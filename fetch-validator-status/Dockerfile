FROM bcgovimages/von-image:next-1

ADD ./fetch-validator-status/requirements.txt .
RUN pip3 install --upgrade pip
RUN pip install --no-cache-dir -r requirements.txt

ADD ./fetch-validator-status/networks.json .
ADD ./fetch-validator-status/*.py ./

ENTRYPOINT ["bash", "-c", "python main.py $@", "--"]