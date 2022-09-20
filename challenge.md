1. Make a new directory called `pulumi-challenge-september`: `mkdir pulumi-challenge-september`.
2. Change into that directory: `cd pulumi-challenge-september`.
3. Run `pulumi new serverless-aws-python`.
4. Accept all defaults.
5. Ensure you are logged in with the AWS CLI.
6. If you so choose, you can run `pulumi up` to explore the infrastructure created by the blueprint.
7. Make and change into a new policy directory: `mkdir policy && cd policy`
8. Run `pulumi policy new aws-python`.
9. Replace the contents of `__main__.py` with the contents of https://github.com/nimbinatus/pulumi-challenge-september/blob/main/policy/__main__.py.
10. Return to the main directory: `cd ../`
11. Create a file called `swag.json`, replacing the contents with your own data:
    ```json
    {
      "pulumi-challenge-swag": {
        "name": "<your name>",
        "email": "<your email>",
        "address": "<your address>",
        "size": "<one of XS, S, M, L, XL>"
      }
    }
    ```
12. Run `pulumi preview --policy-pack policy --policy-pack-config swag.json` to submit for swag! Learn more about policy packs.