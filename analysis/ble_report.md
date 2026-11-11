# CloudESL APK v1.0.23 — BLE 静态分析初筛

- APK SHA-256: 1ea7f94dfd00ff2faec9b42a61fa1b0dd02c2e8e62650f7b661b73b03d7552f9
- 工具：JADX 1.5.1
- 命中行数（初筛，可能含重复/无关项）: 2

## sources/okhttp3/internal/ws/RealWebSocket.java
- L152: String base64 = ByteString.encodeUtf8(this.key + "258EAFA5-E914-47DA-95CA-C5AB0DC85B11").sha1().base64();

## sources/okhttp3/internal/ws/WebSocketProtocol.java
- L8: static final String ACCEPT_MAGIC = "258EAFA5-E914-47DA-95CA-C5AB0DC85B11";

\n> 注：本报告仅为静态字符串/反编译代码命中，不等同于已确认价签协议。