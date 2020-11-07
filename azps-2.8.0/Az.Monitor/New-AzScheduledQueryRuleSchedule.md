---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 2043a2cf31354c7fc14b1b03794dff6f82af67b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822675"
---
# <span data-ttu-id="97e45-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="97e45-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="97e45-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="97e45-102">SYNOPSIS</span></span>
<span data-ttu-id="97e45-103">Erstellt ein Objekt vom Typ Schedule</span><span class="sxs-lookup"><span data-stu-id="97e45-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="97e45-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="97e45-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97e45-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97e45-105">DESCRIPTION</span></span>
<span data-ttu-id="97e45-106">Erstellt ein Objekt vom Typ Schedule.</span><span class="sxs-lookup"><span data-stu-id="97e45-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="97e45-107">Dieses Objekt soll an den Befehl übergeben werden, der die Warnungsregel für Protokolle erstellt.</span><span class="sxs-lookup"><span data-stu-id="97e45-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="97e45-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="97e45-108">EXAMPLES</span></span>

### <span data-ttu-id="97e45-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="97e45-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="97e45-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="97e45-110">PARAMETERS</span></span>

### <span data-ttu-id="97e45-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97e45-111">-DefaultProfile</span></span>
<span data-ttu-id="97e45-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="97e45-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97e45-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="97e45-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="97e45-114">Warnungs Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="97e45-114">The alert frequency</span></span>

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

### <span data-ttu-id="97e45-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="97e45-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="97e45-116">Das Fenster "Benachrichtigungszeit"</span><span class="sxs-lookup"><span data-stu-id="97e45-116">The alert time window</span></span>

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

### <span data-ttu-id="97e45-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e45-117">CommonParameters</span></span>
<span data-ttu-id="97e45-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97e45-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97e45-119">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97e45-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e45-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="97e45-120">INPUTS</span></span>

### <span data-ttu-id="97e45-121">Keine</span><span class="sxs-lookup"><span data-stu-id="97e45-121">None</span></span>

## <span data-ttu-id="97e45-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="97e45-122">OUTPUTS</span></span>

### <span data-ttu-id="97e45-123">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="97e45-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="97e45-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="97e45-124">NOTES</span></span>

## <span data-ttu-id="97e45-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="97e45-125">RELATED LINKS</span></span>
