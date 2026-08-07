# MdfeSefazIde

Identificação do MDF-e.

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**c_uf** | **int** | Código da UF do emitente do MDF-e.  Código da UF do emitente do Documento Fiscal. Utilizar a  Tabela do IBGE de código de unidades da federação. | 
**tp_amb** | **int** | Tipo do Ambiente.  * 1 - Produção  * 2 - Homologação | [opcional] 
**tp_emit** | **int** | Tipo do Emitente.  * 1 - Prestador de serviço de transporte  * 2 - Transportador de Carga Própria 3 - Prestador de serviço de transporte que emitirá CT-e Globalizado  OBS: Deve ser preenchido com 2 para emitentes de NF-e e pelas transportadoras quando estiverem fazendo transporte de carga própria. Deve ser preenchido com 3 para transportador de carga que emitirá à posteriori CT-e Globalizado relacionando as NF-e. | 
**tp_transp** | **int** | Tipo do Transportador.  * 1 - ETC  * 2 - TAC  * 3 - CTC | [opcional] 
**mod** | **int** | Modelo do Manifesto Eletrônico.  Utilizar o código 58 para identificação do MDF-e. | [opcional] 
**serie** | **int** | Série do Manifesto.  Informar a série do documento fiscal (informar zero se inexistente).  Série na faixa [920-969]: Reservada para emissão por contribuinte pessoa física com inscrição estadual. | 
**n_mdf** | **int** | Número do Manifesto.  Número que identifica o Manifesto. 1 a 999999999. | 
**c_mdf** | **str** | Código numérico que compõe a Chave de Acesso.  Código aleatório gerado pelo emitente, com o objetivo de evitar acessos indevidos ao documento.    *Geramos automaticamente quando nenhum valor é informado.* | [opcional] 
**c_dv** | **int** | Digito verificador da chave de acesso do Manifesto.  Informar o dígito  de controle da chave de acesso do MDF-e, que deve ser calculado com a aplicação do algoritmo módulo 11 (base 2,9) da chave de acesso.    *Geramos automaticamente quando nenhum valor é informado.* | [opcional] 
**modal** | **int** | Modalidade de transporte.  * 1 - Rodoviário  * 2 - Aéreo  * 3 - Aquaviário  * 4 - Ferroviário | 
**dh_emi** | **datetime** | Data e hora de emissão do Manifesto.  Formato AAAA-MM-DDTHH:MM:DD TZD. | 
**tp_emis** | **int** | Forma de emissão do Manifesto.  * 1 - Normal  * 2 - Contingência  * 3 - Regime Especial NFF | 
**proc_emi** | **str** | Identificação do processo de emissão do Manifesto.  * 0 - emissão de MDFe com aplicativo do contribuinte  * 4 - emissão de MDFe por Provedor de Assinatura e Autorização - PAA | 
**ver_proc** | **str** | Versão do processo de emissão.  Informar a versão do aplicativo emissor de MDF-e. | 
**uf_ini** | **str** | Sigla da UF do Carregamento.  Utilizar a Tabela do IBGE de código de unidades da federação.  Informar &#39;EX&#39; para operações com o exterior. | 
**uf_fim** | **str** | Sigla da UF do Descarregamento.  Utilizar a Tabela do IBGE de código de unidades da federação.  Informar &#39;EX&#39; para operações com o exterior. | 
**inf_mun_carrega** | [**list[MdfeSefazInfMunCarrega]**](MdfeSefazInfMunCarrega.md) |  | 
**inf_percurso** | [**list[MdfeSefazInfPercurso]**](MdfeSefazInfPercurso.md) |  | [opcional] 
**dh_ini_viagem** | **datetime** | Data e hora previstos de inicio da viagem.  Formato AAAA-MM-DDTHH:MM:DD TZD. | [opcional] 
**ind_canal_verde** | **int** | Indicador de participação do Canal Verde. | [opcional] 
**ind_carrega_posterior** | **int** | Indicador de MDF-e com inclusão da Carga posterior a emissão por evento de inclusão de DF-e. | [opcional] 

[[Voltar à lista de DTOs]](../README.md#documentation-for-models) [[Voltar à listagem da API]](../README.md#documentation-for-api-endpoints) [[Voltar ao README]](../README.md)


