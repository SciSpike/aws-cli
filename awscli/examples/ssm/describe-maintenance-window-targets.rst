**To list all targets for a maintenance window**

This example lists all of the targets for a specified maintenance window.

Command::

  aws ssm describe-maintenance-window-targets --window-id "mw-06cf17cbefcb4bf4f"

Output::

  {
    "Targets": [
        {
            "ResourceType": "INSTANCE",
            "OwnerInformation": "Single instance",
            "WindowId": "mw-06cf17cbefcb4bf4f",
            "Targets": [
                {
                    "Values": [
                        "i-0000293ffd8c57862"
                    ],
                    "Key": "InstanceIds"
                }
            ],
            "WindowTargetId": "350d44e6-28cc-44e2-951f-4b2c985838f6"
        },
        {
            "ResourceType": "INSTANCE",
            "OwnerInformation": "Two instances in a list",
            "WindowId": "mw-06cf17cbefcb4bf4f",
            "Targets": [
                {
                    "Values": [
                        "i-0000293ffd8c57862",
                        "i-0cb2b964d3e14fd9f"
                    ],
                    "Key": "InstanceIds"
                }
            ],
            "WindowTargetId": "e078a987-2866-47be-bedd-d9cf49177d3a"
        }
    ]
  }

**To list all targets for a maintenance window matching a specific owner information value**

This example lists all of the targets for maintenance window ``mw-ab12cd34ef56gh78`` with value ``Single instance``.

Command::

  aws ssm describe-maintenance-window-targets --window-id "mw-ab12cd34ef56gh78" --filters "Key=OwnerInformation,Values=Single instance"
