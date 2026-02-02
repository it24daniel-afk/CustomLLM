```
CustomLLM/
│
├── .env.example                    # Environment variables template
├── .gitignore                      # Git ignore file
├── pyproject.toml                  # Project dependencies (using UV)
├── requirements.txt                # Fallback pip requirements
├── README.md                       # Project documentation
│
├── data/                           # Datasets and processed data
│   ├── raw/                        # Raw datasets
│   ├── processed/                  # Processed/tokenized data
│   ├── instructions/               # Instruction finetuning datasets
│   └── spam/                       # Spam classification dataset
│
├── notebooks/                      # Jupyter notebooks for experimentation
│   ├── 01_environment_setup.ipynb
│   ├── 02_text_tokenization.ipynb
│   ├── 03_attention_mechanisms.ipynb
│   ├── 04_gpt_implementation.ipynb
│   ├── 05_pretraining_experiments.ipynb
│   ├── 06_classification_finetuning.ipynb
│   └── 07_instruction_finetuning.ipynb
│
├── src/                            # Main source code
│   ├── __init__.py
│   │
│   ├── data/                       # Data processing modules
│   │   ├── __init__.py
│   │   ├── tokenizer.py           # Tokenizer implementation (BPE, etc.)
│   │   ├── dataset.py             # Dataset classes and loaders
│   │   └── preprocessing.py       # Text preprocessing utilities
│   │
│   ├── model/                      # Model architecture
│   │   ├── __init__.py
│   │   ├── attention.py           # Self-attention, multi-head attention
│   │   ├── transformer.py         # Transformer blocks
│   │   ├── gpt.py                 # GPT model implementation
│   │   ├── layers.py              # Feed-forward, normalization, embeddings
│   │   └── heads.py               # Classification heads
│   │
│   ├── training/                   # Training utilities
│   │   ├── __init__.py
│   │   ├── trainer.py             # Training loop
│   │   ├── loss.py                # Loss functions
│   │   ├── scheduler.py           # Learning rate schedulers
│   │   └── metrics.py             # Evaluation metrics
│   │
│   ├── inference/                  # Inference and generation
│   │   ├── __init__.py
│   │   ├── generator.py           # Text generation functions
│   │   ├── decoding.py            # Sampling strategies (temp, top-k, etc.)
│   │   └── utils.py               # Inference utilities
│   │
│   ├── utils/                      # General utilities
│   │   ├── __init__.py
│   │   ├── config.py              # Configuration management
│   │   ├── logging.py             # Logging setup
│   │   └── io.py                  # Model loading/saving
│   │
│   └── scripts/                    # Standalone scripts
│       ├── pretrain.py            # Pretraining script
│       ├── finetune_classification.py
│       ├── finetune_instructions.py
│       ├── evaluate.py            # Evaluation script
│       └── generate_text.py       # Text generation script
│
├── configs/                        # Configuration files
│   ├── base.yaml                  # Base configuration
│   ├── pretrain.yaml              # Pretraining configuration
│   ├── finetune_classification.yaml
│   └── finetune_instructions.yaml
│
├── experiments/                    # Experiment tracking
│   ├── pretrain/                  # Pretraining experiments
│   ├── classification/            # Classification experiments
│   └── instructions/              # Instruction tuning experiments
│
├── weights/                        # Model checkpoints
│   ├── pretrained/                # Pretrained weights
│   ├── finetuned_classification/  # Classification fine-tuned weights
│   └── finetuned_instructions/    # Instruction fine-tuned weights
│
├── tests/                          # Unit tests
│   ├── test_tokenizer.py
│   ├── test_attention.py
│   ├── test_model.py
│   └── test_training.py
│
└── docs/                           # Documentation
    ├── setup.md                   # Environment setup instructions
    ├── architecture.md            # Model architecture details
    └── api.md                     # API documentation
```
