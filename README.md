# Classificação de Câncer de Mama com Transfer Learning usando VGG19

Este projeto utiliza Transfer Learning com a arquitetura VGG19 para classificar imagens relacionadas ao câncer de mama em três categorias: **câncer maligno**, **câncer benigno** e **normal**. 

## 📂 Estrutura do Projeto

- **Dataset**: As imagens de treinamento, teste e validação estão organizadas em pastas no Google Drive:
  - `/content/drive/MyDrive/Dataset/train` - Dados de treinamento.
  - `/content/drive/MyDrive/Dataset/test` - Dados de teste.
  - `/content/drive/MyDrive/Dataset/validation` - Dados de validação.

- **Modelo**: O modelo base é o **VGG19** pré-treinado no ImageNet, com camadas densas personalizadas adicionadas para classificação.

---

## 🚀 Como Executar

1. **Monte o Google Drive**:
   Certifique-se de que o Google Drive está montado corretamente.
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
modelo.fit(
    gerador_treinamento,
    steps_per_epoch=gerador_treinamento.samples // tamanho_lote,
    epochs=epocas,
    validation_data=gerador_teste,
    validation_steps=gerador_teste.samples // tamanho_lote
)
modelo = load_model('modelo_cancer_mama_vgg19.keras')
predicoes = modelo.predict(gerador_validacao)
⚙️ Dependências
As bibliotecas utilizadas incluem:

tensorflow.keras para construção e treinamento do modelo.
ImageDataGenerator para pré-processamento e aumento de dados.
matplotlib e seaborn para visualização dos resultados.
sklearn para cálculo de métricas e matriz de confusão.
📊 Visualizações
Gráficos de Métricas: Um gráfico de barras exibe as métricas precisão, recall e F1-Score para cada classe.

Matriz de Confusão: Um mapa de calor exibe a matriz de confusão, mostrando a correspondência entre classes verdadeiras e preditas.

🔑 Observações
Performance: Certifique-se de ajustar o número de épocas e a taxa de aprendizado para otimizar os resultados.
Classes: As classes devem ser nomeadas como câncer maligno, câncer benigno e normal.
Diretórios: Verifique os caminhos das pastas do dataset antes de iniciar.

