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

    ![RabbitMQ as message broker](image/RabbitMQ-1.png)

2. Sending and processing event

    ![Publisher Terminal](image/Publisher.png)
    ![Subscriber Terminal](image/Subscriber.png)
    ![RabbitMQ Process](image/RabbitMQ-2.png)

3. Monitoring chart based on publisher

    ![RabbitMQ Chart Spike](image/RabbitMQ-3.png)

    Spike pada RabbitMQ dipengaruhi oleh jalannya Publisher. Ketika program Publisher dijalankan berulang, bisa terjadi lonjakan _message_ yang dikirim ke dalam _queue_. Maka ketika Publisher mengirimkan _message_ dengan cepat, dapat menyebabkan _spike message rate_ di RabbitMQ.