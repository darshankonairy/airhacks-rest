# Build
mvn clean package && docker build -t com.metlife.ins/eReportingServiceNew .

# RUN

docker rm -f eReportingServiceNew || true && docker run -d -p 8080:8080 -p 4848:4848 --name eReportingServiceNew com.metlife.ins/eReportingServiceNew 