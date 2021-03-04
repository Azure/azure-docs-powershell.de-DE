---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 231b9250509ed463f7f9b2a2d9563dbb1e378ee0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931824"
---
# <span data-ttu-id="d3687-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="d3687-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="d3687-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3687-102">SYNOPSIS</span></span>
<span data-ttu-id="d3687-103">Erstellt ein Objekt vom Typ "Zeitplan"</span><span class="sxs-lookup"><span data-stu-id="d3687-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="d3687-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3687-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3687-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3687-105">DESCRIPTION</span></span>
<span data-ttu-id="d3687-106">Erstellt ein Objekt vom Typ Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="d3687-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="d3687-107">Dieses Objekt muss an den Befehl übergeben werden, mit dem die Protokollbenachrichtigungsregel erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d3687-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="d3687-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d3687-108">EXAMPLES</span></span>

### <span data-ttu-id="d3687-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d3687-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="d3687-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d3687-110">PARAMETERS</span></span>

### <span data-ttu-id="d3687-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3687-111">-DefaultProfile</span></span>
<span data-ttu-id="d3687-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3687-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3687-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="d3687-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="d3687-114">Die Warnungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="d3687-114">The alert frequency</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3687-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="d3687-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="d3687-116">Das Fenster "Benachrichtigungszeit"</span><span class="sxs-lookup"><span data-stu-id="d3687-116">The alert time window</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3687-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3687-117">CommonParameters</span></span>
<span data-ttu-id="d3687-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3687-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3687-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3687-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3687-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d3687-120">INPUTS</span></span>

### <span data-ttu-id="d3687-121">Keine</span><span class="sxs-lookup"><span data-stu-id="d3687-121">None</span></span>

## <span data-ttu-id="d3687-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d3687-122">OUTPUTS</span></span>

### <span data-ttu-id="d3687-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="d3687-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="d3687-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d3687-124">NOTES</span></span>

## <span data-ttu-id="d3687-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d3687-125">RELATED LINKS</span></span>
