# Paddle Pulse
---
---


## Inspiration
---


Our idea for Paddle Pulse stemmed from the seismic research and earthquake detection systems. In studying geologists to determine earthquake epicenters, we learned that piezoelectric sensors can be used to trace energy released during impact events. In particular, research from MIT demonstrated how vibrational energy from earthquakes could be measured and analyzed to better understand where that energy propagates.

This sparked the fundamental question, "If piezoelectric sensing can be used to analyze large-scale geological impacts, could the same principle be applied to smaller, everyday impact events?"

From this line of thinking, we turned to the rapidly growing sport, pickleball. We wondered if we could measure the energy transferred during a paddle strike using thin, embedded sensors. Could real-time impact data help players track performance, improve consistency, and refine technique? Our recorded data would also be able to be utilized beyond.

---

## What It Does
---


The Paddle Pulse is a unique attachment that takes your pickleball performance to the next level. During your session, our Paddle Pulse detects your: energy per hit, frequency of the hit, movement of the paddle, and speed of the swing.

The Paddle Pulse comes with its own app and wireless connection. Performance data collected during the session will be analyzed and compared to that of professional athletes. We’ll have a professional athlete perform all types of swings with our model and record that as a standard swing movement. After the session is done, the player can check their performance.

From the movement data, we'll map 3D movement of the racket and also detect what kind of swing the player did. Movement playback function is available for user reflection.  Sessions will also be recorded in the long term, showing up as calendar streaks and performance progression graphs in the history tab.

With Paddle Pulse, you’ll feel like carrying around a coach with you on your racket, and you’ll be able to analyze your performance in depth.

---

## How We Built It
---


The Paddle Pulse system was built to revolve around the Arduino Uno Q microcontroller. This allowed for the implementation of a wide variety of sensors and onboard data processing.

### Impact Detection

To detect ball contact, we integrated a piezoelectric sensor onto the back surface of the paddle, with the microcontroller mounted on the grip for stability and accessibility. The piezoelectric sensor generates voltage when mechanical stress is applied, whether that be a strike or a sound wave.

This signal was then utilized to trigger an external interrupt to ensure precise timestamping for each hit event. Compared to polling for the event, this results in a much more efficient system that can capture the hit event at any time.

### Motion Tracking – IMU Integration

To capture swing dynamics, the use of an Inertial Measurement Unit (IMU) would be ideal. This IMU measures acceleration and angular velocity, providing insight into paddle orientation and motion throughout a swing. These measurements would then be processed by the board for a more complete understanding of the swing behavior.

### Wireless Communication & Portability

The built-in wireless module on the Arduino Uno Q allowed the system to connect to a host device over the internet, enabling wireless data transmission. This eliminated the need for wired data extraction and improved portability during play.

With high-bandwidth throughput, the system supports high-resolution data communication, creating opportunities for real-time analysis, performance tracking, and long-term data storage.

---

## Challenges We Ran Into

Throughout the development of the project, it is safe to say that it was very much easier said than done. Our initial vision was to have a connection to the paddle that would record and track data such as ball collision onto the paddle, swing data, and ball trajectory. However, there were a multitude of challenges faced, which led to some compromises, but also led to many opportunities to learn and overcome.

### Piezo-Electric Sensor Challenges

Our initial concept for utilizing piezoelectric sensors was inspired by earthquake detection systems and the methods used to determine epicenters. By measuring the arrival times of waves across multiple sensors, it is possible to triangulate the origin of an event. We aimed to apply this same principle to a pickleball paddle by using piezoelectric sensors to detect and localize hit placement based on precise timing data.

During development, we observed that the piezoelectric sensors produced high-voltage spikes when subjected to mechanical stress. These rapid transients created signal instability, making reliable detection difficult and occasionally causing board resets due to voltage overload on the Arduino. To address this, we added a resistor in parallel with the piezoelectric sensor to improve signal conditioning and increase sensitivity, while also incorporating a series resistor on the analog input to protect the microcontroller from excessive voltage spikes.

After validating a single sensor configuration, we expanded toward a three-sensor setup to enable trilateration. Using the two onboard external interrupt pins on the Arduino Uno, we successfully configured two sensors for precise time stamping. However, integrating a third sensor revealed a hardware limitation, as no additional dedicated external interrupt pins were available. To work around this, we implemented a pin change interrupt for the third sensor. While functional, this approach introduced measurable timing delays. The sensors connected to dedicated external interrupts produced consistent timestamps, but the pin change interrupt frequently returned delayed values, resulting in inaccurate time-of-arrival measurements and invalid position calculations. Due to this limitation in timing precision, we chose to step back from the three-sensor configuration and continue development with a single-sensor system.

### Wireless Communication Challenges

We wanted the system to be wireless, as it would make the system more portable and easy to use. Although the onboard wireless module on the Arduino Uno Q is fast and reliable, we faced challenges with getting a reliable wireless stream of data between the device and the host device.

The solution was to take advantage of the high bandwidth throughput of the WiFi connection through data batching. This involves collecting larger chunks of data from the sensors before sending them as a bigger packet wirelessly. Although this does not solve the inherent update frequency issue that causes latency, these bigger chunks allow us to keep up with the large amount of sensor data that must be transmitted.

---

## Accomplishments That We’re Proud Of
---

Reliable Hit Detection with Interrupt-Based Time Stamping  
Successfully implemented hardware interrupt-driven impact detection using a piezoelectric sensor, enabling precise and consistent hit time stamping during live gameplay.

UI Tracking, Replay, and Data Interpolation  
Developed a user interface capable of tracking recorded hits, replaying session data, and applying interpolation techniques to smooth and visualize performance metrics over time.

Stable IMU Integration  
Integrated an Inertial Measurement Unit (IMU) to reliably capture acceleration and angular velocity data, allowing correlation between swing dynamics and impact timing.

High-Bandwidth Wireless Communication  
Established stable wireless communication using the onboard WiFi module, enabling high-throughput data transmission for real-time tracking and remote analysis.

---

## What We Learned

We are a team of four diverse majors: Computer Science, Computer Engineering, Electrical Engineering, and Biomedical Engineering. While working together, each one of us had to learn new things about others’ fields of expertise, while also teaching each other to ensure communication went across the team. Through our challenges came many opportunities to learn. From working with the piezoelectric sensor, we gained a deeper understanding of signal behavior, signal conditioning, and the importance of hardware interrupts in real-time systems. We learned how voltage transients can affect microcontroller stability and how proper circuit design ensures reliable detection. The IMU integration strengthened our understanding of inertial measurements and how acceleration and angular velocity data can be processed to reconstruct swing behavior. We also learned the impact of bandwidth and latency on wireless communication, using techniques like data batching to maintain stable transmission. Overall, this project reinforced the importance of hardware-software integration, system-level thinking, and making informed engineering trade-offs when faced with real-world constraints. We had fun exchanging knowledge.




---

## What’s Next for Paddle Pulse
---

Due to time constraints, we were not able to implement all of the ideas we envisioned for the project. These ideas include: detecting ball impact location on the racket, hit timing rating, ball trajectory calculation, smart health therapy integration, and collecting real professional athletes’ data.

### Detecting Ball Impact Location

We initially planned to place multiple piezoelectric sensors on the racket. This would allow us to determine the precise location where the ball impacts the paddle surface. Knowing the exact impact position would significantly enhance performance tracking, particularly for sweet-spot analysis and consistency mapping. However, when attempting to implement multiple piezoelectric sensors, we encountered hardware interrupt limitations that affected timing precision. Due to this constraint, we focused on reliable hit detection for this iteration, with impact localization remaining a key goal for future development.

### Detecting Hit Timing Rating

With refined timing resolution and additional data sampling, we aim to classify hits as early, optimal, or late. This would provide players with direct feedback on reaction timing and swing preparation, translating raw sensor data into actionable performance metrics.

### Collecting Real Professional Athletes' Data and AI Coaching

Within the project timeframe, it was not feasible to collaborate directly with professional athletes to obtain benchmark performance data. Instead, we utilized controlled sample data for testing. In the future, collecting real athlete data would allow us to build accurate performance models and enable meaningful comparisons for users. There will also be an AI coach that can provide feedback per hit (if you are swinging in the wrong posture) and feedback for the overall performance. The AI will show how much you’ve progressed and how else you can improve.

### Ball Trajectory Calculation

By combining impact force data with IMU-based swing motion measurements, future iterations could estimate ball trajectory. Integrating these parameters would extend the system from simple impact detection to predictive shot analytics.

### Smart Health Therapy

One of the most important features we envision is a health therapy mode. For users recovering from muscle injuries, the system could monitor energy output and movement intensity. This would help ensure that users exercise enough to strengthen muscles without overexerting themselves. The system could provide warnings when fatigue thresholds are exceeded, supporting safe rehabilitation and training.

### Expanding to Other Sports

The underlying sensor architecture has the potential to be adapted to other racket-based sports, broadening the applicability of the platform beyond pickleball.