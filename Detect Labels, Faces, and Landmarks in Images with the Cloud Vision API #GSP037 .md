# GSP037
>🚨 [PLEASE SUBSCRIBE OUR CHANNEL SARC](([https://www.youtube.com/@sarc1608])) **&** [JOIN OUR COMMUNITY](https://www.instagram.com/_.sarc._/)
## CREATE AN API_KEY > APIs & Services > Credentials > Create Credentials>API key
## Run in cloudshell
```cmd
gcloud alpha services api-keys create --display-name="arcade" 
KEY_NAME=$(gcloud alpha services api-keys list --format="value(name)" --filter "displayName=arcade")
export API_KEY=$(gcloud alpha services api-keys get-key-string $KEY_NAME --format="value(keyString)")
export PROJECT_ID=$(gcloud config list --format 'value(core.project)')
gsutil mb gs://$PROJECT_ID
git clone https://github.com/siddharth7000/practice.git
gsutil cp practice/donuts.png gs://$PROJECT_ID
gsutil cp practice/selfie.png gs://$PROJECT_ID
gsutil cp practice/city.png gs://$PROJECT_ID
gsutil acl ch -u AllUsers:R gs://$PROJECT_ID/donuts.png
gsutil acl ch -u AllUsers:R gs://$PROJECT_ID/selfie.png
gsutil acl ch -u AllUsers:R gs://$PROJECT_ID/city.png
```
