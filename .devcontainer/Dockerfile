FROM  --platform=linux/arm64 gcr.io/google.com/cloudsdktool/google-cloud-cli:506.0.0
RUN apt install python3.11-venv -y
RUN python3 -m venv venv
RUN source venv/bin/activate && pip3 install --upgrade pip google-adk

# Map python command to python3
# RUN ln -s /usr/bin/python3 /usr/bin/python

# ENV GOOGLE_CLOUD_PROJECT=nintest1




ENTRYPOINT [ "/bin/bash" ]
