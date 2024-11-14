#!/bin/bash
#!/chickennoodlesrecipes

function directconnectacceptance() {
    echo " ----------------------------------------------------------------"
    echo "     Input the Details below for Direct Connect Acceptance       "
    echo " ----------------------------------------------------------------"

    echo " "
    echo " Direct Connect Gateway ID: "
    read gatewayid

    echo " "
    echo " Proposal ID: "
    read proposalid

    echo " "
    echo " Associated Gateway Owner Account: "
    read associatedgateway

    # Execute the AWS CLI command
    aws directconnect accept-direct-connect-gateway-association-proposal \
        --direct-connect-gateway-id $gatewayid \
        --proposal-id $proposalid \
        --associated-gateway-owner-account $associatedgateway
}

directconnectacceptance



function vpccreation() {

    echo " ----------------------------------------------------------------"
    echo "            Input the Details below for VPC Creation             "
    echo " ----------------------------------------------------------------"



    echo " "
    echo " CIDR Block (Example 10.0.0.0/24)"
    read cidr


aws ec2 create-vpc --instance-tenancy "default" --cidr-block $cidr


}

vpccreation




function subnetcreation() {

    echo " ----------------------------------------------------------------"
    echo "            Input the Details below for the Subnets              "
    echo " ----------------------------------------------------------------"



    echo " "
    echo "VPC ID"
    read vpcid

    echo " "
    echo "Public Subnet"
    read subnetpublic




aws ec2 create-subnet --vpc-id $vpcid --cidr-block $subnetpublic



    echo " "
    echo "Private Subnet"
    read subnetprivate

    aws ec2 create-subnet --vpc-id $vpcid --cidr-block $subnetprivate

}

subnetcreation




