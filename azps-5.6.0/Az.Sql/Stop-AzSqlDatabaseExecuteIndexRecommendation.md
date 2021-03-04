---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 4882ada2348a8b878cfaab04a85ac50ae58d9daf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946840"
---
# <span data-ttu-id="6e3dd-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="6e3dd-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="6e3dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="6e3dd-103">Beendet den Workflow, der einen empfohlenen Indexvorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e3dd-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="6e3dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e3dd-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e3dd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6e3dd-105">DESCRIPTION</span></span>
<span data-ttu-id="6e3dd-106">Das **Cmdlet Stop-AzSqlDatabaseExecuteIndexRecommendation** beendet den Workflow, der einen empfohlenen Indexvorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="6e3dd-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="6e3dd-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6e3dd-107">EXAMPLES</span></span>

### <span data-ttu-id="6e3dd-108">Beispiel 1: Beenden der Ausführung einer Indexempfehlung</span><span class="sxs-lookup"><span data-stu-id="6e3dd-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="6e3dd-109">Mit diesem Befehl wird die Ausführung einer Indexempfehlung beendet.</span><span class="sxs-lookup"><span data-stu-id="6e3dd-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="6e3dd-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6e3dd-110">PARAMETERS</span></span>

### <span data-ttu-id="6e3dd-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6e3dd-111">-DatabaseName</span></span>
<span data-ttu-id="6e3dd-112">Gibt den Namen der Datenbank an, für die dieses Cmdlet den Workflow beendet.</span><span class="sxs-lookup"><span data-stu-id="6e3dd-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="6e3dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e3dd-113">-DefaultProfile</span></span>
<span data-ttu-id="6e3dd-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6e3dd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e3dd-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="6e3dd-115">-IndexRecommendationName</span></span>
<span data-ttu-id="6e3dd-116">Gibt den Namen der Indexempfehlung an, die dieses Cmdlet beendet.</span><span class="sxs-lookup"><span data-stu-id="6e3dd-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="6e3dd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e3dd-117">-ResourceGroupName</span></span>
<span data-ttu-id="6e3dd-118">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="6e3dd-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="6e3dd-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="6e3dd-119">-ServerName</span></span>
<span data-ttu-id="6e3dd-120">Gibt den Server an, der die Datenbank hostet, für die dieses Cmdlet einen Workflow beendet.</span><span class="sxs-lookup"><span data-stu-id="6e3dd-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="6e3dd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e3dd-121">CommonParameters</span></span>
<span data-ttu-id="6e3dd-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e3dd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e3dd-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e3dd-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e3dd-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6e3dd-124">INPUTS</span></span>

### <span data-ttu-id="6e3dd-125">System.String</span><span class="sxs-lookup"><span data-stu-id="6e3dd-125">System.String</span></span>

## <span data-ttu-id="6e3dd-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6e3dd-126">OUTPUTS</span></span>

### <span data-ttu-id="6e3dd-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="6e3dd-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="6e3dd-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6e3dd-128">NOTES</span></span>

## <span data-ttu-id="6e3dd-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6e3dd-129">RELATED LINKS</span></span>

[<span data-ttu-id="6e3dd-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="6e3dd-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="6e3dd-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="6e3dd-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="6e3dd-132">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="6e3dd-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


