<h1><strong>Simple AWS Web Server Deployment</strong></h1>
<p>This project documents my main configuration for deploying a simple web server utilizing Terraform HCL and AWS. The steps outlined:</p>
<ol>
<li style="font-weight: 400;" aria-level="1"><span style="font-weight: 400;">Create VPC</span></li>
<li style="font-weight: 400;" aria-level="1"><span style="font-weight: 400;">Create Internet Gateway</span>
<ul>
<li style="font-weight: 400;" aria-level="1"><span style="font-weight: 400;">Used to send web traffic out to the internet.</span></li>
</ul>
</li>
<li style="font-weight: 400;" aria-level="1"><span style="font-weight: 400;">Create Custom Route Table</span></li>
<li style="font-weight: 400;" aria-level="1"><span style="font-weight: 400;">Create a Subnet</span></li>
<li style="font-weight: 400;" aria-level="1"><span style="font-weight: 400;">Associate subnet with route table</span>
<ul>
<li style="font-weight: 400;" aria-level="1"><span style="font-weight: 400;">Must do whenever we have a subnet and route table.</span></li>
</ul>
</li>
<li style="font-weight: 400;" aria-level="1"><span style="font-weight: 400;">Create Security Group to allow ports 22, 80, 443</span>
<ul>
<li style="font-weight: 400;" aria-level="1"><span style="font-weight: 400;">Security groups/ firewalls allows what type of traffic to flow to any EC2 (VM) instance</span></li>
</ul>
</li>
<li style="font-weight: 400;" aria-level="1"><span style="font-weight: 400;">Create a Network Interface with an IP in the subnet (that was created in step 4)</span></li>
<li style="font-weight: 400;" aria-level="1"><span style="font-weight: 400;">Assign an Elastic IP to the network interface (that was created in step 7)</span>
<ul>
<li style="font-weight: 400;" aria-level="1"><span style="font-weight: 400;">Elastic IP = public IP - route it to the network interface</span></li>
</ul>
</li>
<li style="font-weight: 400;" aria-level="1"><span style="font-weight: 400;">Create Ubuntu server and install/ enable Apache2</span></li>
</ol>
