---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 41ce3c066651cb2bc6ea13ddd0a7a3bb15d28879
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177500"
---
# <span data-ttu-id="8bf32-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="8bf32-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="8bf32-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8bf32-102">SYNOPSIS</span></span>
<span data-ttu-id="8bf32-103">Erstellt ein Objekt vom Typ Warnungsaktion</span><span class="sxs-lookup"><span data-stu-id="8bf32-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="8bf32-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bf32-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bf32-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8bf32-105">DESCRIPTION</span></span>
<span data-ttu-id="8bf32-106">Erstellt ein Objekt vom Typ Warnungsaktion dieses Objekt wird an den Befehl übergeben, der die Warnungsregel für Protokolle erstellt.</span><span class="sxs-lookup"><span data-stu-id="8bf32-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="8bf32-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8bf32-107">EXAMPLES</span></span>

### <span data-ttu-id="8bf32-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8bf32-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="8bf32-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8bf32-109">PARAMETERS</span></span>

### <span data-ttu-id="8bf32-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="8bf32-110">-AznsAction</span></span>
<span data-ttu-id="8bf32-111">Details zur AzNS-Aktion</span><span class="sxs-lookup"><span data-stu-id="8bf32-111">The AzNS action details</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf32-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bf32-112">-DefaultProfile</span></span>
<span data-ttu-id="8bf32-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8bf32-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bf32-114">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="8bf32-114">-Severity</span></span>
<span data-ttu-id="8bf32-115">Der Schweregrad für diese Warnung</span><span class="sxs-lookup"><span data-stu-id="8bf32-115">The severity for this alert</span></span>

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

### <span data-ttu-id="8bf32-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="8bf32-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="8bf32-117">Die Dauer in Minuten, für die eine Warnung gedrosselt werden soll</span><span class="sxs-lookup"><span data-stu-id="8bf32-117">The duration in minutes for which alert should be throttled</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf32-118">-Trigger</span><span class="sxs-lookup"><span data-stu-id="8bf32-118">-Trigger</span></span>
<span data-ttu-id="8bf32-119">Warnungs Trigger-Bedingung</span><span class="sxs-lookup"><span data-stu-id="8bf32-119">The alert trigger condition</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf32-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bf32-120">CommonParameters</span></span>
<span data-ttu-id="8bf32-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bf32-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bf32-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8bf32-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bf32-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8bf32-123">INPUTS</span></span>

### <span data-ttu-id="8bf32-124">Keine</span><span class="sxs-lookup"><span data-stu-id="8bf32-124">None</span></span>

## <span data-ttu-id="8bf32-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8bf32-125">OUTPUTS</span></span>

### <span data-ttu-id="8bf32-126">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="8bf32-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="8bf32-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="8bf32-127">NOTES</span></span>

## <span data-ttu-id="8bf32-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8bf32-128">RELATED LINKS</span></span>
