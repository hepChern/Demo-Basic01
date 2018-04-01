##
## A container where CernVM-FS is up and running
##
FROM rootproject/root-ubuntu16

USER root
ENV USER root
ENV HOME /root
WORKDIR /root

ADD entrypoint.sh $HOME/entrypoint.sh
RUN chmod +x entrypoint.sh
ENTRYPOINT ["./entrypoint.sh"]
# ===================================================================
# !! Please only modify the contents between the two seperation line

# Add all the code you use to docker image
ADD lhcbStyle.h $HOME/lhcbStyle.h
ADD efficiency.C $HOME/efficiency.C

CMD ["root -b -q efficiency.C"]
# other examples:
# ENTRYPOINT ["python", "-b", "-q", "test2.C"]

# ===================================================================

