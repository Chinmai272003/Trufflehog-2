import os

def main():
    print("Hello Secure World")

     Read credentials from environment variables
    aws_access_key = os.getenv("AWS_ACCESS_KEY_ID")
    aws_secret_key = os.getenv("AWS_SECRET_ACCESS_KEY")
    api_endpoint = os.getenv("API_ENDPOINT", "https://api.example.com/v1/data")

    if not aws_access_key or not aws_secret_key:
        print("AWS credentials are not set.")
        return

    print("AWS credentials loaded successfully")
    print("API Endpoint:", api_endpoint)

if __name__ == "__main__":
    main()


