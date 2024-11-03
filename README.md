<!DOCTYPE html>
<html>
<head>
<style>
  body {
    background-color: #000;
    color: #fff;
    font-family: 'Consolas', monospace;
    margin: 0;
    padding: 20px;
  }
  
  .terminal {
    background: #0C0C0C;
    border-radius: 10px;
    box-shadow: 0 0 20px rgba(255, 0, 0, 0.2);
    margin: 20px auto;
    max-width: 900px;
    overflow: hidden;
    animation: bootUp 1s ease-out;
  }

  .terminal-header {
    background: #1F1F1F;
    padding: 10px;
    display: flex;
    align-items: center;
    border-bottom: 1px solid #FF0000;
  }

  .terminal-buttons {
    display: flex;
    gap: 8px;
    margin-right: 15px;
  }

  .terminal-button {
    width: 12px;
    height: 12px;
    border-radius: 50%;
    border: none;
  }

  .close { background: #FF0000; }
  .minimize { background: #8C8C8C; }
  .maximize { background: #404040; }

  .terminal-title {
    color: #8C8C8C;
    font-size: 14px;
    flex-grow: 1;
    text-align: center;
  }

  .terminal-content {
    padding: 20px;
    line-height: 1.4;
  }

  .command-prompt {
    color: #FF0000;
    margin-bottom: 10px;
  }

  .command-prompt::before {
    content: "G4br1e3l@system:~$ ";
    color: #8C8C8C;
  }

  .typing {
    border-right: 2px solid #FF0000;
    animation: typing 3s steps(40) 1s 1 normal both,
               blink 1s steps(1) infinite;
    white-space: nowrap;
    overflow: hidden;
  }

  .output {
    color: #8C8C8C;
    margin: 10px 0;
    opacity: 0;
    animation: fadeIn 0.5s ease-out forwards;
    animation-delay: 2s;
  }

  .matrix {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
    margin: 20px 0;
    animation: slideIn 0.8s ease-out forwards;
    animation-delay: 2.5s;
    opacity: 0;
  }

  .matrix-item {
    background: #1A1A1A;
    border: 1px solid #FF0000;
    padding: 15px;
    border-radius: 5px;
    text-align: center;
  }

  .status-bar {
    background: #1F1F1F;
    padding: 10px;
    display: flex;
    justify-content: space-between;
    border-top: 1px solid #FF0000;
    font-size: 12px;
    color: #8C8C8C;
  }

  .ascii-art {
    color: #FF0000;
    font-family: monospace;
    white-space: pre;
    margin: 20px 0;
    animation: glitch 1s ease-out forwards;
    animation-delay: 3s;
  }

  @keyframes bootUp {
    from { transform: translateY(-20px); opacity: 0; }
    to { transform: translateY(0); opacity: 1; }
  }

  @keyframes typing {
    from { width: 0; }
    to { width: 100%; }
  }

  @keyframes blink {
    50% { border-color: transparent; }
  }

  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
  }

  @keyframes slideIn {
    from { opacity: 0; transform: translateX(-20px); }
    to { opacity: 1; transform: translateX(0); }
  }

  @keyframes glitch {
    0% { transform: skew(0deg); }
    20% { transform: skew(20deg); filter: blur(1px); }
    40% { transform: skew(-20deg); filter: blur(0px); }
    60% { transform: skew(0deg); }
    100% { transform: skew(0deg); }
  }

  .system-info {
    display: grid;
    grid-template-columns: auto 1fr;
    gap: 10px;
    margin: 20px 0;
    animation: fadeIn 0.5s ease-out forwards;
    animation-delay: 3.5s;
    opacity: 0;
  }

  .system-info dt {
    color: #FF0000;
    font-weight: bold;
  }

  .system-info dd {
    color: #8C8C8C;
    margin: 0;
  }

  .progress-bar {
    background: #1A1A1A;
    border: 1px solid #FF0000;
    height: 20px;
    margin: 10px 0;
    overflow: hidden;
  }

  .progress {
    background: #FF0000;
    height: 100%;
    width: 0;
    animation: progress 2s ease-out forwards;
    animation-delay: 4s;
  }

  @keyframes progress {
    to { width: 100%; }
  }
</style>
</head>
<body>
  <div class="terminal">
    <div class="terminal-header">
      <div class="terminal-buttons">
        <div class="terminal-button close"></div>
        <div class="terminal-button minimize"></div>
        <div class="terminal-button maximize"></div>
      </div>
      <div class="terminal-title">G4br1e3l@Enterprise-System ~ Identity & Security Architecture</div>
    </div>
    
    <div class="terminal-content">
      <div class="command-prompt typing">
        identity-system --initialize --mode=enterprise
      </div>

      <div class="output">
        [SUCCESS] Identity Management System Initialized
        [STATUS] Enterprise Security Protocols Active
        [ACCESS] Level 7 Clearance Granted
      </div>

      <div class="ascii-art">
  ██████╗ ██╗  ██╗██████╗ ██████╗  ██╗███████╗██████╗ ██╗     
 ██╔════╝ ██║  ██║██╔══██╗██╔══██╗███║██╔════╝██╔══██╗██║     
 ██║  ███╗███████║██████╔╝██████╔╝╚██║█████╗  ██████╔╝██║     
 ██║   ██║╚════██║██╔══██╗██╔══██╗ ██║██╔══╝  ██╔══██╗██║     
 ╚██████╔╝     ██║██████╔╝██║  ██║ ██║███████╗██║  ██║███████╗
  ╚═════╝      ╚═╝╚═════╝ ╚═╝  ╚═╝ ╚═╝╚══════╝╚═╝  ╚═╝╚══════╝
      </div>

      <div class="matrix">
        <div class="matrix-item">
          <h3>IAM Architecture</h3>
          <p>Enterprise Identity Solutions</p>
          <div class="progress-bar"><div class="progress"></div></div>
        </div>
        <div class="matrix-item">
          <h3>Security Development</h3>
          <p>Zero Trust Implementation</p>
          <div class="progress-bar"><div class="progress"></div></div>
        </div>
        <div class="matrix-item">
          <h3>Cloud Infrastructure</h3>
          <p>Secure Platform Design</p>
          <div class="progress-bar"><div class="progress"></div></div>
        </div>
      </div>

      <dl class="system-info">
        <dt>Identity Protocols:</dt>
        <dd>OAuth 2.0 | SAML 2.0 | OpenID Connect</dd>
        
        <dt>Security Framework:</dt>
        <dd>Zero Trust Architecture | NIST 800-53</dd>
        
        <dt>Infrastructure:</dt>
        <dd>Cloud-Native | Container Orchestration</dd>
        
        <dt>Development:</dt>
        <dd>API Security | Microservices | DevSecOps</dd>
      </dl>

      <div class="command-prompt typing">
        system-status --check all
      </div>

      <div class="output">
        [ACTIVE] Identity Provider
        [ACTIVE] Authentication Services
        [ACTIVE] Authorization Framework
        [ACTIVE] Security Monitoring
        [ACTIVE] Compliance Engine
      </div>
    </div>

    <div class="status-bar">
      <span>System: ACTIVE</span>
      <span>Security Level: MAXIMUM</span>
      <span>Connection: ENCRYPTED</span>
    </div>
  </div>
</body>
</html>
