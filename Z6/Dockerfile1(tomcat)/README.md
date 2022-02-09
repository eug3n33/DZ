version: '3.3'
services:
  mvn:
    build: mvn_dock_f
    volumes:
      - tupe: volume
          source: webapps
          target: /tmp/webapps
volumes:
  webapps:./webapps
