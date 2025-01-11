# SoleMates Data Repository

Welcome to the **SoleMates Data Repository**, a supporting dataset for the [step-by-step AI walkthrough](https://norahsakal.com/blog/ai-agent-solemates) on building an AI agent capable of handling complex product queries like **"I need women's black shoes with red details."**

This repository is designed to help you follow along with the guide and experiment with AI concepts, such as vectorization, multi-color filtering, and Retrieval-Augmented Generation (RAG) systems.

---

## Repository Contents

This repository includes all the resources you need to work through the tutorial:

1. **Shoe Dataset**:
   - A CSV file containing fictional shoe data for the SoleMates online store:  
     `data/solemates_shoe_directory.csv`
   - Fields include:
     - **Product Name**
     - **Shoe Type**
     - **Colors**
     - **Heel Height**
     - **Additional Metadata**

2. **Footwear Images**:
   - A folder named `footwear/` with over 100 MB of fictional shoe images
   - These images simulate a product catalog for the SoleMates store

3. **Pre-Embedded Dataset**:
   - For convenience, a **pre-embedded dataset** with all text and image embeddings is available:  
     `data/solemates_shoe_directory_pre_embedded_shoes.csv`
   - This dataset is ideal if you want to skip the embedding step or don't have access to AWS

4. **Requirements File**:
   - A `requirements.txt` file listing all Python dependencies for the walkthrough

## How to Use This Repository

### Step 1: Clone the Repository

Start by cloning the repository to your local machine:

```bash
git clone https://github.com/norahsakal/solemates-data.git
```

### Step 2: Navigate to the Repository

Move into the cloned folder:

```bash
cd solemates-data
```

### Step 3: Install Dependencies

Install the Python libraries needed for the walkthrough:

```bash
pip install -r requirements.txt
```

### Step 4: Access the Dataset

You can now access:

- The shoe dataset CSV: `data/solemates_shoe_directory.csv`
- The pre-embedded dataset CSV: `data/solemates_shoe_directory_pre_embedded_shoes.csv`
- The image folder: `footwear/`

#### Pre-Embedded Dataset

If you prefer not to generate embeddings or don't have access to AWS, you can use the pre-embedded dataset. This CSV file includes all text and image embeddings, along with token counts, so you can focus on the AI workflow without incurring additional costs.

**Loading the Pre-Embedded Dataset**
To load the pre-embedded dataset in your Jupyter Notebook, use the following code:

```python
df_shoes_with_embeddings = pd.read_csv('data/solemates_shoe_directory_pre_embedded_shoes.csv')
```

### Step 5: Follow the Walkthrough

Use the data in this repository to follow along with the full guide:

- [Building an AI Agent for Multi-Color Product Queries]()

## Example Dataset Preview

Here’s a preview of the CSV file structure:

| product_title                                   | gender   | product_type   | color   | usage   | color_details   |   heel_height |   heel_type |   price_usd | brand    |   product_id | image   |
|:------------------------------------------------|:---------|:---------------|:--------|:--------|:----------------|--------------:|------------:|------------:|:---------|-------------:|:--------|
| Puma men future cat remix sf black casual shoes | men      | casual shoes   | black   | casual  | []              |           nan |         nan |         220 | puma     |            1 | 1.jpg   |
| Buckaroo men flores black formal shoes          | men      | formal shoes   | black   | formal  | []              |           nan |         nan |         155 | buckaroo |            2 | 2.jpg   |
| Gas men europa white shoes                      | men      | casual shoes   | white   | casual  | []              |           nan |         nan |         105 | gas      |            3 | 3.jpg   |
| Nike men's incinerate msl white blue shoe       | men      | sports shoes   | white   | sports  | ['blue']        |           nan |         nan |         125 | nike     |            4 | 4.jpg   |
| Clarks men hang work leather black formal shoes | men      | formal shoes   | black   | formal  | []              |           nan |         nan |         220 | clarks   |            5 | 5.jpg   |

## About SoleMates

SoleMates is a fictional online shoe store created as part of the tutorial.

The goal is to demonstrate how an AI agent can improve upon simple chatbots by handling complex queries, enhancing the user experience.

### Key Features of the AI Walkthrough

- Query Understanding: Handle multi-color and specific requirements
- Vectorization: Transform product data into embeddings
- Cloud Integration: Store data in a vector database (e.g., Pinecone)

## Contributing

If you find any issues or have suggestions for improvement, feel free to open an issue or submit a pull request.

## Acknowledgments

This project is part of the AI walkthrough series by [Norah Sakal]().

Check out the full tutorial for more insights and code examples:
[Building an AI Agent for Multi-Color Product Queries.]()