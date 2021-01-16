---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 52f929cea9f2017ad6a2c2ea16475ec7d5d8a5a0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301027"
---
# <span data-ttu-id="c5ce3-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="c5ce3-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="c5ce3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5ce3-102">SYNOPSIS</span></span>
<span data-ttu-id="c5ce3-103">Erstellt ein Objekt vom Typ "Zeitplan".</span><span class="sxs-lookup"><span data-stu-id="c5ce3-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="c5ce3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5ce3-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5ce3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5ce3-105">DESCRIPTION</span></span>
<span data-ttu-id="c5ce3-106">Erstellt ein Objekt vom Typ "Zeitplan".</span><span class="sxs-lookup"><span data-stu-id="c5ce3-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="c5ce3-107">Dieses Objekt wird an den Befehl übergeben, mit dem eine Protokollwarnungsregel erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c5ce3-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="c5ce3-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c5ce3-108">EXAMPLES</span></span>

### <span data-ttu-id="c5ce3-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c5ce3-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="c5ce3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5ce3-110">PARAMETERS</span></span>

### <span data-ttu-id="c5ce3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5ce3-111">-DefaultProfile</span></span>
<span data-ttu-id="c5ce3-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5ce3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5ce3-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="c5ce3-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="c5ce3-114">Die Warnungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="c5ce3-114">The alert frequency</span></span>

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

### <span data-ttu-id="c5ce3-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="c5ce3-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="c5ce3-116">Das Fenster "Benachrichtigungszeit"</span><span class="sxs-lookup"><span data-stu-id="c5ce3-116">The alert time window</span></span>

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

### <span data-ttu-id="c5ce3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5ce3-117">CommonParameters</span></span>
<span data-ttu-id="c5ce3-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5ce3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5ce3-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5ce3-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5ce3-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c5ce3-120">INPUTS</span></span>

### <span data-ttu-id="c5ce3-121">Keine</span><span class="sxs-lookup"><span data-stu-id="c5ce3-121">None</span></span>

## <span data-ttu-id="c5ce3-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c5ce3-122">OUTPUTS</span></span>

### <span data-ttu-id="c5ce3-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="c5ce3-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="c5ce3-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c5ce3-124">NOTES</span></span>

## <span data-ttu-id="c5ce3-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c5ce3-125">RELATED LINKS</span></span>
