FROM karalabe/xgo-latest

ADD "http://downloads.sourceforge.net/project/mingw-w64/mingw-w64/mingw-w64-release/mingw-w64-v5.0-rc2.zip" mingw-w64-v5.0-rc2.zip

RUN unzip -q mingw-w64-v5.0-rc2.zip && cd mingw-w64-v5.0-rc2 && \
	\
	cd mingw-w64-headers && \
	./configure --prefix=/usr && \
	make && make install && \
	\
	cd ../mingw-w64-crt && \
	./configure --prefix=/usr --host=i686-w64-mingw32 --disable-lib64 --enable-lib32 && \
	make && make install
