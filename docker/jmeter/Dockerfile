FROM ubuntu:latest
RUN  useradd -ms /bin/bash jmeter
RUN apt-get update && apt-get install -y curl
RUN curl https://dlcdn.apache.org//jmeter/binaries/apache-jmeter-5.6.tgz --output apache-jmeter-5.6.tgz && tar -xf apache-jmeter-5.6.tgz && rm apache-jmeter-5.6.tgz && chown jmeter -R /apache-jmeter-5.6 && ln -s apache-jmeter-5.6 apache-jmeter
RUN apt-get install -y openjdk-19-jre
RUN curl https://dlcdn.apache.org/jena/binaries/apache-jena-4.8.0.tar.gz --output  apache-jena-4.8.0.tar.gz && tar -xf apache-jena-4.8.0.tar.gz && rm apache-jena-4.8.0.tar.gz && chown jmeter -R apache-jena-4.8.0 && ln -s apache-jena-4.8.0 apache-jena
USER jmeter
WORKDIR /home/jmeter
ENTRYPOINT ["/apache-jmeter/bin/jmeter"]
