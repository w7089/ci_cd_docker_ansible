FROM python:2.7

# Create virtual environment
RUN virtualenv /appenv && \
    . /appenv/bin/activate && \
    pip install pip --upgrade
    
# Add entrypoint script
ADD scripts/entrypoint.sh /usr/local/bin/entrypoint.sh
RUN chmod +x /usr/local/bin/entrypoint.sh
ENTRYPOINT ["entrypoint.sh"]

LABEL application=todobackend