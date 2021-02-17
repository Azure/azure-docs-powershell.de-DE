---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 7f13b1a1a5daad4e7c97de962943bb859f6a09df
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402183"
---
# <span data-ttu-id="0fcb3-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="0fcb3-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="0fcb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fcb3-102">SYNOPSIS</span></span>
<span data-ttu-id="0fcb3-103">Beendet den Workflow, der einen empfohlenen Indexvorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0fcb3-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="0fcb3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0fcb3-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0fcb3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0fcb3-105">DESCRIPTION</span></span>
<span data-ttu-id="0fcb3-106">Das **Cmdlet "Stop-AzSqlDatabaseExecuteIndexRecommendation"** beendet den Workflow, der einen empfohlenen Indexvorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="0fcb3-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="0fcb3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0fcb3-107">EXAMPLES</span></span>

### <span data-ttu-id="0fcb3-108">Beispiel 1: Beenden der Ausführung einer Indexempfehlung</span><span class="sxs-lookup"><span data-stu-id="0fcb3-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="0fcb3-109">Mit diesem Befehl wird die Ausführung einer Indexempfehlung beendet.</span><span class="sxs-lookup"><span data-stu-id="0fcb3-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="0fcb3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fcb3-110">PARAMETERS</span></span>

### <span data-ttu-id="0fcb3-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0fcb3-111">-DatabaseName</span></span>
<span data-ttu-id="0fcb3-112">Gibt den Namen der Datenbank an, für die dieses Cmdlet den Workflow beendet.</span><span class="sxs-lookup"><span data-stu-id="0fcb3-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="0fcb3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fcb3-113">-DefaultProfile</span></span>
<span data-ttu-id="0fcb3-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0fcb3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0fcb3-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="0fcb3-115">-IndexRecommendationName</span></span>
<span data-ttu-id="0fcb3-116">Gibt den Namen der Indexempfehlung an, die dieses Cmdlet stoppt.</span><span class="sxs-lookup"><span data-stu-id="0fcb3-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="0fcb3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fcb3-117">-ResourceGroupName</span></span>
<span data-ttu-id="0fcb3-118">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="0fcb3-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="0fcb3-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0fcb3-119">-ServerName</span></span>
<span data-ttu-id="0fcb3-120">Gibt den Server an, der die Datenbank hostet, für die dieses Cmdlet einen Workflow beendet.</span><span class="sxs-lookup"><span data-stu-id="0fcb3-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="0fcb3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fcb3-121">CommonParameters</span></span>
<span data-ttu-id="0fcb3-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fcb3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fcb3-123">Weitere Informationen finden Sie unter [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fcb3-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fcb3-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0fcb3-124">INPUTS</span></span>

### <span data-ttu-id="0fcb3-125">System.String</span><span class="sxs-lookup"><span data-stu-id="0fcb3-125">System.String</span></span>

## <span data-ttu-id="0fcb3-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0fcb3-126">OUTPUTS</span></span>

### <span data-ttu-id="0fcb3-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="0fcb3-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="0fcb3-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0fcb3-128">NOTES</span></span>

## <span data-ttu-id="0fcb3-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0fcb3-129">RELATED LINKS</span></span>


[<span data-ttu-id="0fcb3-130">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="0fcb3-130">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="0fcb3-131">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="0fcb3-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


