FROM python-dev

# COPY APP
COPY . /repo

# Install python packages
RUN \
  pip install -r /repo/.pythonrc

# Run setting
CMD ["python", "/repo/setup.py"]
