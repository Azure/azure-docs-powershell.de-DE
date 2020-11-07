---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulesource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
ms.openlocfilehash: 0679f4281d9528a7124f4a9a5235d47dd8af107c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841948"
---
# <span data-ttu-id="6dde6-101">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="6dde6-101">New-AzScheduledQueryRuleSource</span></span>

## <span data-ttu-id="6dde6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6dde6-102">SYNOPSIS</span></span>
<span data-ttu-id="6dde6-103">Erstellt ein Objekt vom Typ "Quelle"</span><span class="sxs-lookup"><span data-stu-id="6dde6-103">Creates an object of type Source</span></span>

## <span data-ttu-id="6dde6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6dde6-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSource -Query <String> [-AuthorizedResource <String[]>] -DataSourceId <String>
 [-QueryType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dde6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6dde6-105">DESCRIPTION</span></span>
<span data-ttu-id="6dde6-106">Erstellt ein Objekt vom Typ Source.</span><span class="sxs-lookup"><span data-stu-id="6dde6-106">Creates an object of type Source.</span></span>
<span data-ttu-id="6dde6-107">Dieses Objekt soll an den Befehl übergeben werden, der die Protokoll Warnungsregel erstellt</span><span class="sxs-lookup"><span data-stu-id="6dde6-107">This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="6dde6-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6dde6-108">EXAMPLES</span></span>

### <span data-ttu-id="6dde6-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6dde6-109">Example 1</span></span>
```powershell
PS C:\> $source = New-AzScheduledQueryRuleSource -Query "Heartbeat | summarize AggregatedValue = count() by bin(TimeGenerated, 5m)"
                  -DataSourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace" 
                  -QueryType "ResultCount"
```

## <span data-ttu-id="6dde6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6dde6-110">PARAMETERS</span></span>

### <span data-ttu-id="6dde6-111">-AuthorizedResource</span><span class="sxs-lookup"><span data-stu-id="6dde6-111">-AuthorizedResource</span></span>
<span data-ttu-id="6dde6-112">Die Liste der autorisierten Ressourcen für diese Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="6dde6-112">The list of authorized resources for this alert</span></span>

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

### <span data-ttu-id="6dde6-113">-DataSourceID</span><span class="sxs-lookup"><span data-stu-id="6dde6-113">-DataSourceId</span></span>
<span data-ttu-id="6dde6-114">Die Datenquelle, für die diese Warnung erstellt wird</span><span class="sxs-lookup"><span data-stu-id="6dde6-114">The data source on which this alert is created</span></span>

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

### <span data-ttu-id="6dde6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dde6-115">-DefaultProfile</span></span>
<span data-ttu-id="6dde6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6dde6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dde6-117">-Query</span><span class="sxs-lookup"><span data-stu-id="6dde6-117">-Query</span></span>
<span data-ttu-id="6dde6-118">Warnungs Abfrage</span><span class="sxs-lookup"><span data-stu-id="6dde6-118">The alert query</span></span>

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

### <span data-ttu-id="6dde6-119">-QueryType</span><span class="sxs-lookup"><span data-stu-id="6dde6-119">-QueryType</span></span>
<span data-ttu-id="6dde6-120">Art der Abfrage – derzeit unterstützte Werte: ResultCount</span><span class="sxs-lookup"><span data-stu-id="6dde6-120">Type of Query - currently supported values : ResultCount</span></span>

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

### <span data-ttu-id="6dde6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dde6-121">CommonParameters</span></span>
<span data-ttu-id="6dde6-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dde6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dde6-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6dde6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dde6-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6dde6-124">INPUTS</span></span>

### <span data-ttu-id="6dde6-125">Keine</span><span class="sxs-lookup"><span data-stu-id="6dde6-125">None</span></span>

## <span data-ttu-id="6dde6-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6dde6-126">OUTPUTS</span></span>

### <span data-ttu-id="6dde6-127">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="6dde6-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

## <span data-ttu-id="6dde6-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="6dde6-128">NOTES</span></span>

## <span data-ttu-id="6dde6-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6dde6-129">RELATED LINKS</span></span>
