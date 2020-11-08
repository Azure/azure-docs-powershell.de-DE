---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulesource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
ms.openlocfilehash: 0fe5684805dfc3047abb39040d80eb8a388cf5a2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995085"
---
# <span data-ttu-id="1e36d-101">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="1e36d-101">New-AzScheduledQueryRuleSource</span></span>

## <span data-ttu-id="1e36d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e36d-102">SYNOPSIS</span></span>
<span data-ttu-id="1e36d-103">Erstellt ein Objekt vom Typ "Quelle"</span><span class="sxs-lookup"><span data-stu-id="1e36d-103">Creates an object of type Source</span></span>

## <span data-ttu-id="1e36d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e36d-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSource -Query <String> [-AuthorizedResource <String[]>] -DataSourceId <String>
 [-QueryType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e36d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e36d-105">DESCRIPTION</span></span>
<span data-ttu-id="1e36d-106">Erstellt ein Objekt vom Typ Source.</span><span class="sxs-lookup"><span data-stu-id="1e36d-106">Creates an object of type Source.</span></span>
<span data-ttu-id="1e36d-107">Dieses Objekt soll an den Befehl übergeben werden, der die Protokoll Warnungsregel erstellt</span><span class="sxs-lookup"><span data-stu-id="1e36d-107">This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="1e36d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e36d-108">EXAMPLES</span></span>

### <span data-ttu-id="1e36d-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1e36d-109">Example 1</span></span>
```powershell
PS C:\> $source = New-AzScheduledQueryRuleSource -Query "Heartbeat | summarize AggregatedValue = count() by bin(TimeGenerated, 5m)"
                  -DataSourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace" 
                  -QueryType "ResultCount"
```

## <span data-ttu-id="1e36d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e36d-110">PARAMETERS</span></span>

### <span data-ttu-id="1e36d-111">-AuthorizedResource</span><span class="sxs-lookup"><span data-stu-id="1e36d-111">-AuthorizedResource</span></span>
<span data-ttu-id="1e36d-112">Die Liste der autorisierten Ressourcen für diese Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="1e36d-112">The list of authorized resources for this alert</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e36d-113">-DataSourceID</span><span class="sxs-lookup"><span data-stu-id="1e36d-113">-DataSourceId</span></span>
<span data-ttu-id="1e36d-114">Die Datenquelle, für die diese Warnung erstellt wird</span><span class="sxs-lookup"><span data-stu-id="1e36d-114">The data source on which this alert is created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e36d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e36d-115">-DefaultProfile</span></span>
<span data-ttu-id="1e36d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1e36d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e36d-117">-Query</span><span class="sxs-lookup"><span data-stu-id="1e36d-117">-Query</span></span>
<span data-ttu-id="1e36d-118">Warnungs Abfrage</span><span class="sxs-lookup"><span data-stu-id="1e36d-118">The alert query</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e36d-119">-QueryType</span><span class="sxs-lookup"><span data-stu-id="1e36d-119">-QueryType</span></span>
<span data-ttu-id="1e36d-120">Art der Abfrage – derzeit unterstützte Werte: ResultCount</span><span class="sxs-lookup"><span data-stu-id="1e36d-120">Type of Query - currently supported values : ResultCount</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e36d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e36d-121">CommonParameters</span></span>
<span data-ttu-id="1e36d-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e36d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e36d-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e36d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e36d-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e36d-124">INPUTS</span></span>

### <span data-ttu-id="1e36d-125">Keine</span><span class="sxs-lookup"><span data-stu-id="1e36d-125">None</span></span>

## <span data-ttu-id="1e36d-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e36d-126">OUTPUTS</span></span>

### <span data-ttu-id="1e36d-127">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="1e36d-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

## <span data-ttu-id="1e36d-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e36d-128">NOTES</span></span>

## <span data-ttu-id="1e36d-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e36d-129">RELATED LINKS</span></span>
