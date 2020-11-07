---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: e62c8861f370f9e7e7c5b31fea629f3f8e11aa32
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841944"
---
# <span data-ttu-id="2a8f5-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="2a8f5-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="2a8f5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2a8f5-102">SYNOPSIS</span></span>
<span data-ttu-id="2a8f5-103">Erstellt ein Objekt vom Typ Schedule</span><span class="sxs-lookup"><span data-stu-id="2a8f5-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="2a8f5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a8f5-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a8f5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2a8f5-105">DESCRIPTION</span></span>
<span data-ttu-id="2a8f5-106">Erstellt ein Objekt vom Typ Schedule.</span><span class="sxs-lookup"><span data-stu-id="2a8f5-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="2a8f5-107">Dieses Objekt soll an den Befehl übergeben werden, der die Warnungsregel für Protokolle erstellt.</span><span class="sxs-lookup"><span data-stu-id="2a8f5-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="2a8f5-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2a8f5-108">EXAMPLES</span></span>

### <span data-ttu-id="2a8f5-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2a8f5-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="2a8f5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a8f5-110">PARAMETERS</span></span>

### <span data-ttu-id="2a8f5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a8f5-111">-DefaultProfile</span></span>
<span data-ttu-id="2a8f5-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2a8f5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a8f5-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="2a8f5-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="2a8f5-114">Warnungs Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="2a8f5-114">The alert frequency</span></span>

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

### <span data-ttu-id="2a8f5-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="2a8f5-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="2a8f5-116">Das Fenster "Benachrichtigungszeit"</span><span class="sxs-lookup"><span data-stu-id="2a8f5-116">The alert time window</span></span>

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

### <span data-ttu-id="2a8f5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a8f5-117">CommonParameters</span></span>
<span data-ttu-id="2a8f5-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a8f5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a8f5-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a8f5-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a8f5-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2a8f5-120">INPUTS</span></span>

### <span data-ttu-id="2a8f5-121">Keine</span><span class="sxs-lookup"><span data-stu-id="2a8f5-121">None</span></span>

## <span data-ttu-id="2a8f5-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2a8f5-122">OUTPUTS</span></span>

### <span data-ttu-id="2a8f5-123">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="2a8f5-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="2a8f5-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="2a8f5-124">NOTES</span></span>

## <span data-ttu-id="2a8f5-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2a8f5-125">RELATED LINKS</span></span>
