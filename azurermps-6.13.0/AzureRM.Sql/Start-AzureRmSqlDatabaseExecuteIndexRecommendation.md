---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: c61f1bd988410b696eddd12162958333022dd892
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481958"
---
# <span data-ttu-id="ae720-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ae720-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="ae720-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ae720-102">SYNOPSIS</span></span>
<span data-ttu-id="ae720-103">Startet den Workflow, der einen empfohlenen Indexvorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="ae720-103">Starts the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae720-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae720-104">SYNTAX</span></span>

```
Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae720-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae720-105">DESCRIPTION</span></span>
<span data-ttu-id="ae720-106">Das Cmdlet **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** startet den Workflow, der einen empfohlenen Indexvorgang für eine Azure SQL-Datenbank ausführt.</span><span class="sxs-lookup"><span data-stu-id="ae720-106">The **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="ae720-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae720-107">EXAMPLES</span></span>

### <span data-ttu-id="ae720-108">Beispiel 1: Ausführen einer Indexempfehlung</span><span class="sxs-lookup"><span data-stu-id="ae720-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="ae720-109">Dieser Befehl führt eine Indexempfehlung aus.</span><span class="sxs-lookup"><span data-stu-id="ae720-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="ae720-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae720-110">PARAMETERS</span></span>

### <span data-ttu-id="ae720-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ae720-111">-DatabaseName</span></span>
<span data-ttu-id="ae720-112">Gibt den Namen der Datenbank an, für die dieses Cmdlet den Workflow startet.</span><span class="sxs-lookup"><span data-stu-id="ae720-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae720-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae720-113">-DefaultProfile</span></span>
<span data-ttu-id="ae720-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ae720-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae720-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="ae720-115">-IndexRecommendationName</span></span>
<span data-ttu-id="ae720-116">Gibt den Namen der Indexempfehlung an, die dieses Cmdlet ausführt.</span><span class="sxs-lookup"><span data-stu-id="ae720-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae720-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae720-117">-ResourceGroupName</span></span>
<span data-ttu-id="ae720-118">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ae720-118">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae720-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="ae720-119">-ServerName</span></span>
<span data-ttu-id="ae720-120">Gibt den Server an, der die Datenbank hostet, für die dieses Cmdlet einen Workflow startet.</span><span class="sxs-lookup"><span data-stu-id="ae720-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae720-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae720-121">CommonParameters</span></span>
<span data-ttu-id="ae720-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae720-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae720-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae720-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae720-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ae720-124">INPUTS</span></span>

### <span data-ttu-id="ae720-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ae720-125">System.String</span></span>

## <span data-ttu-id="ae720-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ae720-126">OUTPUTS</span></span>

### <span data-ttu-id="ae720-127">Microsoft. Azure. Commands. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ae720-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="ae720-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="ae720-128">NOTES</span></span>

## <span data-ttu-id="ae720-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ae720-129">RELATED LINKS</span></span>

[<span data-ttu-id="ae720-130">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="ae720-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="ae720-131">Stopp-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ae720-131">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="ae720-132">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="ae720-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


