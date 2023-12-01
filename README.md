# Named-Entity-Extraction

Overview

This code utilizes the Llama-2-7b Large Language Model to extract named entities from highly unstructured employment agreements. The primary goal is to identify and categorize entities such as names, dates, roles, and other relevant information within the document.

Sample Schema

person_schema = Object(
    id="Witnesses",

    # Natural language description about your object
    description="Names of the witnesses",

    # Fields you'd like to capture from a piece of text about your object.
    attributes=[
        Text(
            id="first_name",
            description="The first name of the witness.",
        ),
        Text(
            id="last_name",
            description="The last name of the witness.",
        )
    ],
    examples=[
        ("The name of the witness is Tejas Thorat", [{"first_name": "Tejas"}, {"last_name": "Thorat"}])
    ]
)
