# TCP_Client

you can use void tcp_client_connect(uint16_t _PortNumber,uint8_t *_IPAddress); to connect to a server<br/>
and use void tcp_client_connection_close(struct tcp_pcb *tpcb); for close each connection<br/>
void tcp_Client_SendString(struct tcp_pcb *tpcb,uint8_t * str , uint16_t len); to send a uint8_t buffer to each connection<br/>
add this callback to your project file (main.c or ...) that you need to process recieved buffer like this :<br/>
void tcp_Client_Recieve(struct tcp_pcb *tpcb,uint8_t *Buf,uint32_t _Len)<br/>
{<br/>
  //your code;<br/>
}<br/>
add this callback to your project file (main.c or ...) that you need to process new connections :<br/>
void tcp_Client_NewConnection(struct tcp_pcb *newpcb)<br/>
{<br/>
  //your code;<br/>
}<br/>
