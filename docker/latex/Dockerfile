FROM debian:12.1-slim@sha256:24c92a69df28b21676d721fe18c0bf64138bfc69b486746ad935b49cc31b0b91 AS installer
ENV PATH /usr/local/bin/texlive:$PATH
WORKDIR /install-tl-unx
RUN apt-get update
RUN apt-get install -y \
    perl \
    wget \
    xz-utils \
    fontconfig \
    libfontconfig1
COPY ./texlive.profile ./
RUN wget -nv https://mirror.ctan.org/systems/texlive/tlnet/install-tl-unx.tar.gz
RUN tar -xzf ./install-tl-unx.tar.gz --strip-components=1
RUN ./install-tl --profile=texlive.profile
RUN ln -sf /usr/local/texlive/*/bin/* /usr/local/bin/texlive
RUN tlmgr update --self --all
RUN tlmgr install \
    collection-fontsrecommended \
    collection-langjapanese \
    collection-latexextra \
    collection-luatex \
    latexmk \
    latex \
    luatexja \
    bxjscls \
    babel-japanese \
    bxwareki \
    everyhook \
    svn-prov \
    type1cm \
    ipaex \
    haranoaji \
    svn-prov \
    ctex \
    biblatex \
    biber
RUN cp -r /usr/local/texlive/2023/texmf-dist/fonts/truetype/public/ipaex/ /usr/share/fonts/truetype/ && \
    cp -r /usr/local/texlive/2023/texmf-dist/fonts/opentype/public/haranoaji/ /usr/share/fonts/opentype/ && \
    cp -r /usr/local/texlive/2023/texmf-dist/fonts/opentype/public/haranoaji-extra/ /usr/share/fonts/opentype/
CMD ["bash"]
