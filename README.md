# python-script-of-cost-optimization-

As I move toward the AWS cloud this is a demo of how the AWS Lambda function works and also on COST OPTIMISATION 

# problem statement 
The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if it exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.

# steps 
1. first I created one simple EC2 instance with one volume attached to it.
2. Then I attached one snapshot over that volume created to the EC2 instance.
3. Then go to lambda function and create one lambda function with default configurations.
4. I write some of the Python code which present in the script.py file.
5. It shows me the error of the permissions after testing the code.
6. Then I went to the IAM Role service to grant permission to EC2 snapshot. ( Here IAM Role is defaultly created y lambda function )
8. It runs, Then I just delete the EC2 instance hence the volume is also deleted.
9. again I tested the function, and it runs my script.py file which contains conditions i.e. if volume gets 0 then delete the snapshot attached to it.
As the Demo performs :)

# conclusion 
when a snapshot is attached to volume get deleted automatically it may reduse an organization cost !!
