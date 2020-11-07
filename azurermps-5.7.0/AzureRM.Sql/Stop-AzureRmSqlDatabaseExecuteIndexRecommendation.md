---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: d4cb344f63b871f55668c4de7205ada80ff04f35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663413"
---
# <span data-ttu-id="b9786-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="b9786-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="b9786-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b9786-102">SYNOPSIS</span></span>
<span data-ttu-id="b9786-103">Beendet den Workflow, der einen empfohlenen Indexvorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="b9786-103">Stops the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9786-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9786-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9786-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9786-105">DESCRIPTION</span></span>
<span data-ttu-id="b9786-106">Das Cmdlet **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** beendet den Workflow, der einen empfohlenen Indexvorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="b9786-106">The **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="b9786-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9786-107">EXAMPLES</span></span>

### <span data-ttu-id="b9786-108">Beispiel 1: Beenden der Ausführung einer Indexempfehlung</span><span class="sxs-lookup"><span data-stu-id="b9786-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="b9786-109">Dieser Befehl beendet die Ausführung einer Indexempfehlung.</span><span class="sxs-lookup"><span data-stu-id="b9786-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="b9786-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9786-110">PARAMETERS</span></span>

### <span data-ttu-id="b9786-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b9786-111">-DatabaseName</span></span>
<span data-ttu-id="b9786-112">Gibt den Namen der Datenbank an, für die dieses Cmdlet den Workflow beendet.</span><span class="sxs-lookup"><span data-stu-id="b9786-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9786-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9786-113">-DefaultProfile</span></span>
<span data-ttu-id="b9786-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b9786-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9786-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="b9786-115">-IndexRecommendationName</span></span>
<span data-ttu-id="b9786-116">Gibt den Namen der Indexempfehlung an, die mit diesem Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="b9786-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9786-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9786-117">-ResourceGroupName</span></span>
<span data-ttu-id="b9786-118">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="b9786-118">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9786-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="b9786-119">-ServerName</span></span>
<span data-ttu-id="b9786-120">Gibt den Server an, der die Datenbank hostet, für die dieses Cmdlet einen Workflow beendet.</span><span class="sxs-lookup"><span data-stu-id="b9786-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9786-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9786-121">CommonParameters</span></span>
<span data-ttu-id="b9786-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9786-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9786-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9786-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9786-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b9786-124">INPUTS</span></span>

### <span data-ttu-id="b9786-125">Keine</span><span class="sxs-lookup"><span data-stu-id="b9786-125">None</span></span>
<span data-ttu-id="b9786-126">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="b9786-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b9786-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b9786-127">OUTPUTS</span></span>

## <span data-ttu-id="b9786-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="b9786-128">NOTES</span></span>

## <span data-ttu-id="b9786-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b9786-129">RELATED LINKS</span></span>

[<span data-ttu-id="b9786-130">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="b9786-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="b9786-131">Anfang-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="b9786-131">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="b9786-132">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="b9786-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


