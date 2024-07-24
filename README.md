# tokyo-olympic-azure-data-engineering
No geral, construi um pipeline que copia os dados, faz algumas transformações básicas e por fim disponibiliza os dados para visualização.

Diagrama da arquitetura:

![image](https://github.com/user-attachments/assets/90580c53-6c01-4457-80c7-9772bae3cd0e)

No data factory construí um pipeline para pegar os dados brutos e fazer o upload dos dados no Data Lake Gen2.

Depois, utilizei o Databricks para fazer trasnformações e subir novamente os dados no Data Lake Gen 2.

Depois, usei o Azure Synapse Analytics como data warehouse e fazer operações de consultas.
