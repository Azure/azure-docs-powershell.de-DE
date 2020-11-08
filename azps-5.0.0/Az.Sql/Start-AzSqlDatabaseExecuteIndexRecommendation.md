---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: e69cffe6955a5bf19636dd519c0906be64ce4413
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175382"
---
# <span data-ttu-id="9a73c-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="9a73c-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="9a73c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a73c-102">SYNOPSIS</span></span>
<span data-ttu-id="9a73c-103">Startet den Workflow, der einen empfohlenen Indexvorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="9a73c-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="9a73c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a73c-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a73c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a73c-105">DESCRIPTION</span></span>
<span data-ttu-id="9a73c-106">Das Cmdlet **Start-AzSqlDatabaseExecuteIndexRecommendation** startet den Workflow, der einen empfohlenen Indexvorgang für eine Azure SQL-Datenbank ausführt.</span><span class="sxs-lookup"><span data-stu-id="9a73c-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="9a73c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a73c-107">EXAMPLES</span></span>

### <span data-ttu-id="9a73c-108">Beispiel 1: Ausführen einer Indexempfehlung</span><span class="sxs-lookup"><span data-stu-id="9a73c-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="9a73c-109">Dieser Befehl führt eine Indexempfehlung aus.</span><span class="sxs-lookup"><span data-stu-id="9a73c-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="9a73c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a73c-110">PARAMETERS</span></span>

### <span data-ttu-id="9a73c-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9a73c-111">-DatabaseName</span></span>
<span data-ttu-id="9a73c-112">Gibt den Namen der Datenbank an, für die dieses Cmdlet den Workflow startet.</span><span class="sxs-lookup"><span data-stu-id="9a73c-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="9a73c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a73c-113">-DefaultProfile</span></span>
<span data-ttu-id="9a73c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9a73c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a73c-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="9a73c-115">-IndexRecommendationName</span></span>
<span data-ttu-id="9a73c-116">Gibt den Namen der Indexempfehlung an, die dieses Cmdlet ausführt.</span><span class="sxs-lookup"><span data-stu-id="9a73c-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="9a73c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a73c-117">-ResourceGroupName</span></span>
<span data-ttu-id="9a73c-118">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9a73c-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="9a73c-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="9a73c-119">-ServerName</span></span>
<span data-ttu-id="9a73c-120">Gibt den Server an, der die Datenbank hostet, für die dieses Cmdlet einen Workflow startet.</span><span class="sxs-lookup"><span data-stu-id="9a73c-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="9a73c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a73c-121">CommonParameters</span></span>
<span data-ttu-id="9a73c-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a73c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a73c-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a73c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a73c-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a73c-124">INPUTS</span></span>

### <span data-ttu-id="9a73c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9a73c-125">System.String</span></span>

## <span data-ttu-id="9a73c-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a73c-126">OUTPUTS</span></span>

### <span data-ttu-id="9a73c-127">Microsoft. Azure. Commands. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="9a73c-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="9a73c-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a73c-128">NOTES</span></span>

## <span data-ttu-id="9a73c-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a73c-129">RELATED LINKS</span></span>

[<span data-ttu-id="9a73c-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="9a73c-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="9a73c-131">Stopp-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="9a73c-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="9a73c-132">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="9a73c-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


