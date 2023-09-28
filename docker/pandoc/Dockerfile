FROM 3w36zj6/latex:latest
WORKDIR /pandoc
RUN wget https://github.com/jgm/pandoc/releases/download/3.1.8/pandoc-3.1.8-1-amd64.deb && \
    dpkg -i pandoc-3.1.8-1-amd64.deb
RUN wget https://github.com/lierdakil/pandoc-crossref/releases/download/v0.3.17.0/pandoc-crossref-Linux.tar.xz && \
    tar -Jxvf pandoc-crossref-Linux.tar.xz && \
    mkdir -p ~/.local/share/pandoc/filter && \
    cp pandoc-crossref /usr/local/bin
ENTRYPOINT [ "/usr/bin/pandoc" ]
WORKDIR /workdir
