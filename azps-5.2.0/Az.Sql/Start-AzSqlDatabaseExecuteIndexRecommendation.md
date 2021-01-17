---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: e69cffe6955a5bf19636dd519c0906be64ce4413
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362464"
---
# <span data-ttu-id="b8595-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="b8595-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="b8595-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8595-102">SYNOPSIS</span></span>
<span data-ttu-id="b8595-103">Startet den Workflow, der einen empfohlenen Indexvorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8595-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="b8595-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8595-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8595-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8595-105">DESCRIPTION</span></span>
<span data-ttu-id="b8595-106">Das **Cmdlet "Start-AzSqlDatabaseExecuteIndexRecommendation"** startet den Workflow, der einen empfohlenen Indexvorgang für eine Azure SQL ausführt.</span><span class="sxs-lookup"><span data-stu-id="b8595-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="b8595-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b8595-107">EXAMPLES</span></span>

### <span data-ttu-id="b8595-108">Beispiel 1: Ausführen einer Indexempfehlung</span><span class="sxs-lookup"><span data-stu-id="b8595-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="b8595-109">Mit diesem Befehl wird eine Indexempfehlung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8595-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="b8595-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8595-110">PARAMETERS</span></span>

### <span data-ttu-id="b8595-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b8595-111">-DatabaseName</span></span>
<span data-ttu-id="b8595-112">Gibt den Namen der Datenbank an, für die dieses Cmdlet den Workflow startet.</span><span class="sxs-lookup"><span data-stu-id="b8595-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="b8595-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8595-113">-DefaultProfile</span></span>
<span data-ttu-id="b8595-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b8595-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8595-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="b8595-115">-IndexRecommendationName</span></span>
<span data-ttu-id="b8595-116">Gibt den Namen der Indexempfehlung an, die von diesem Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8595-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="b8595-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8595-117">-ResourceGroupName</span></span>
<span data-ttu-id="b8595-118">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="b8595-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="b8595-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b8595-119">-ServerName</span></span>
<span data-ttu-id="b8595-120">Gibt den Server an, der die Datenbank hostet, für die dieses Cmdlet einen Workflow startet.</span><span class="sxs-lookup"><span data-stu-id="b8595-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="b8595-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8595-121">CommonParameters</span></span>
<span data-ttu-id="b8595-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8595-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8595-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8595-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8595-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b8595-124">INPUTS</span></span>

### <span data-ttu-id="b8595-125">System.String</span><span class="sxs-lookup"><span data-stu-id="b8595-125">System.String</span></span>

## <span data-ttu-id="b8595-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b8595-126">OUTPUTS</span></span>

### <span data-ttu-id="b8595-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="b8595-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="b8595-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b8595-128">NOTES</span></span>

## <span data-ttu-id="b8595-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b8595-129">RELATED LINKS</span></span>

[<span data-ttu-id="b8595-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="b8595-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="b8595-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="b8595-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="b8595-132">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="b8595-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


