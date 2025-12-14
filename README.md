Thứ bạn đang thấy trong hình là một website demo công nghệ có tên là "Aether" (hoặc đầy đủ là Aether Particles).

Đây là một ứng dụng chạy trực tiếp trên trình duyệt web, sử dụng công nghệ mô phỏng hạt (particle simulation) kết hợp với trí tuệ nhân tạo (AI) để theo dõi chuyển động tay.

Dưới đây là giải thích chi tiết về cách nó hoạt động:

1. Nó là gì? Đó là một tương tác đồ họa 3D (Interactive 3D Graphics). Hàng ngàn "đốm sáng" mà bạn thấy được gọi là các hạt (particles). Chúng được lập trình để mô phỏng vật lý như trọng lực, lực hút, lực đẩy.

2. Tại sao nắm tay lại thì nó tụ lại, mở tay thì nó bay ra? Ứng dụng này sử dụng Webcam trên laptop để nhìn thấy tay của bạn (bạn có thể thấy chữ "Hand Tracking Active" - Đang theo dõi tay ở góc trên bên trái màn hình).

Khi nắm tay (Fist): Máy tính hiểu đây là lệnh "Hút". Nó tạo ra một lực hấp dẫn ảo tại vị trí nắm tay của bạn, khiến tất cả các hạt bị hút vào tâm và tạo thành một khối cầu đặc.

Khi mở tay (Open Hand): Máy tính hiểu là lệnh "Thả" hoặc "Đẩy". Lực hấp dẫn biến mất hoặc đảo ngược, khiến các hạt mất đi sự liên kết và bay tứ tung ra ngoài không gian ảo, hoặc chuyển động theo luồng gió.

3. Công nghệ đằng sau

WebGL / Three.js: Công nghệ giúp hiển thị đồ họa 3D mượt mà ngay trên trình duyệt web mà không cần cài phần mềm nặng.

Computer Vision (Thị giác máy tính): Thường sử dụng thư viện như MediaPipe (của Google) để nhận diện các khớp xương trên bàn tay bạn qua camera, từ đó biết được bạn đang nắm hay mở tay.

Copy đoạn Prompt dưới đây:
Role: You are an expert Creative Technologist and Front-End Developer specializing in WebGL, Three.js, and Computer Vision.

Task: Create a single-file HTML application (using CDN links) that replicates an interactive "Particle Morphing & Hand Tracking" experience similar to the "Aether" web demo.

Core Features & Technologies:

3D Engine (Three.js):

Create a scene with a dark, cinematic background.

Initialize a Particle System with at least 15,000 particles.

Use THREE.BufferGeometry for performance.

Particles should look like glowing points (use a circular sprite texture or additive blending).

Hand Tracking (MediaPipe Hands):

Integrate Google MediaPipe Hands to track the user's hand via Webcam.

Logic:

Fist (Clenched Hand): Detect when fingertips are close to the palm. When a fist is detected, particles should strongly attract to the center of the 3D shape, forming a solid, dense object.

Open Hand: When the hand is open, particles should loosen up, float slightly, or expand outward (breathing effect), but still maintain the general shape structure.

Hand Position: Map the user's hand position (X, Y) to rotate the 3D object or move the center of gravity.

Particle Morphing Logic:

The particles must be able to morph smoothly between different mathematical shapes.

Pre-calculate target positions for these shapes: Sphere, Cube, Torus (Donut), and a Random Galaxy Cloud.

Implement a smooth linear interpolation (lerp) animation when switching shapes.

UI Implementation (Crucial):

Create a stylish, semi-transparent UI overlay fixed to the bottom-left corner (similar to the reference images provided).

Section 1: "Morph Geometry": Create text labels/buttons for: "Sphere", "Cube", "Torus", "Cloud". When clicked, the particle shape transforms. Highlight the active shape.

Section 2: "Particle Color": Create a row of circular color swatches (e.g., Cyan, Gold, Neon Green, White, Red). When clicked, the particles change color smoothly.

Style the UI with CSS to look modern, minimal, and sci-fi (white text, glassmorphism background).

Code Structure:

Provide the full, working code in a single code block (HTML + CSS + JS).

Handle webcam permissions gracefully.

Ensure the animation loop is optimized (60 FPS).

Visual Style:

The particles should have a "magical" feel.

The transition between shapes must be fluid, not instant snapping.

Hướng dẫn cách chạy code sau khi AI tạo ra:
Bước 1: Copy toàn bộ code mà AI trả về.

Bước 2: Tạo một file mới trên máy tính, đặt tên là index.html.

Bước 3: Dán code vào và lưu lại.

Bước 4 (Quan trọng): Bạn không thể click đúp để mở file này (vì trình duyệt sẽ chặn camera vì lý do bảo mật).

Bạn cần cài VS Code và extension "Live Server".

Chuột phải vào file chọn "Open with Live Server".

Hoặc đơn giản hơn: Upload file index.html đó lên một host miễn phí như Vercel hoặc Netlify để chạy thử trên điện thoại/laptop.

Lưu ý: Nếu bạn muốn các hạt di chuyển phức tạp hơn nữa (như có gió thổi, nhiễu loạn), bạn có thể yêu cầu AI thêm "Curl Noise" vào chuyển động của hạt.
