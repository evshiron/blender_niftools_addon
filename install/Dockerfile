FROM python:3.10.8

ARG cobra_commit=e1cf891f06052266e9550bfe60fb08b1d3f01672
ARG pyffi_commit=4b18387137a4e73386f020fff66d033354ab2186
ARG nifxml_commit=2331baba5468744fcd09b4760526c396dc963b5a

WORKDIR /codegen
RUN git clone https://github.com/OpenNaja/cobra-tools.git && cd cobra-tools && git reset --hard $cobra_commit && cd ..
RUN git clone https://github.com/Candoran2/new-pyffi && cd new-pyffi && git reset --hard $pyffi_commit && cd .. && \
    mv ./new-pyffi/formats/nif ./cobra-tools/source/formats && \
    mv ./new-pyffi/spells ./cobra-tools/source && \
    mv ./new-pyffi/utils ./cobra-tools/source
RUN git clone https://github.com/niftools/nifxml.git && cd nifxml && git reset --hard $nifxml_commit && cd .. && \
    mv ./nifxml/nif.xml ./cobra-tools/source/formats/nif

WORKDIR cobra-tools
RUN python3 -m pip install -i https://mirrors.ustc.edu.cn/pypi/web/simple --upgrade pip setuptools && \
    python3 -m pip install -i https://mirrors.ustc.edu.cn/pypi/web/simple -r requirements.txt

ADD generate.sh .
CMD ["./generate.sh"]
