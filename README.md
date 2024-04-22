# Advance Programming Tutorial 8
Tutorial for Advanced Programming 2024 Module 8 - Faculty of Computer Science, Universitas Indonesia

---

## Reflection

1. How many data your publlsher program will send to the message broker in one run?

    Data yang akan dikirimkan oleh publisher ada 5, karena terdapat pemanggilan `publish_event` yang melakukan `UserCreatedEventMessage` sejumlah 5 pesan.

2. The url of `ampq://guest:guest@localhost:5672`, is the same as in the subscriber program, what does it mean?

    Artinya bahwa Subscriber dan Publisher terkoneksi ke sebuah _message broker_ dengan protokol AMPQ yang sama. _Broker_ dijalankan pada mesin yang sama dengan Subscriber, yaitu pada `localhost` dengan nomor port `5672`.

## RabbitMQ

1. RabbitMQ as message broker

    ![RabbitMQ as message broker](/publisher/image/RabbitMQ-1.png)

2. Sending and processing event

    ![Publisher Terminal](/publisher/image/Publisher.png)
    ![Subscriber Terminal](/publisher/image/Subscriber.png)
    ![RabbitMQ Process](/publisher/image/RabbitMQ-2.png)

3. Monitoring chart based on publisher

    ![RabbitMQ Chart Spike](/publisher/image/RabbitMQ-3.png)