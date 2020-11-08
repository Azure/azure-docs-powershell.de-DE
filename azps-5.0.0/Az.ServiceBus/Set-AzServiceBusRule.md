---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: b86b9629062515afb1ee70e7c7372cbc7687bfa5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177738"
---
# <span data-ttu-id="7c1f6-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="7c1f6-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="7c1f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7c1f6-102">SYNOPSIS</span></span>
<span data-ttu-id="7c1f6-103">Aktualisiert die angegebene Regelbeschreibung für das angegebene Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7c1f6-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="7c1f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c1f6-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c1f6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c1f6-105">DESCRIPTION</span></span>
<span data-ttu-id="7c1f6-106">Das Cmdlet " **Satz-AzServiceBusRule** " aktualisiert die Beschreibung für die angegebene Regel des angegebenen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="7c1f6-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="7c1f6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c1f6-107">EXAMPLES</span></span>

### <span data-ttu-id="7c1f6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7c1f6-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="7c1f6-109">Aktualisiert den SQL **-Ausdruck MySQL Expression = "Bedingung"** der Regel `SBRule` des Abonnements `SBSubscription` im Thema `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="7c1f6-109">Updates the sql expression **mysqlexpression='condition'** of the rule `SBRule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="7c1f6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c1f6-110">PARAMETERS</span></span>

### <span data-ttu-id="7c1f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c1f6-111">-DefaultProfile</span></span>
<span data-ttu-id="7c1f6-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7c1f6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c1f6-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7c1f6-113">-InputObject</span></span>
<span data-ttu-id="7c1f6-114">ServiceBus-Regeldefinition</span><span class="sxs-lookup"><span data-stu-id="7c1f6-114">ServiceBus Rules definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c1f6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7c1f6-115">-Name</span></span>
<span data-ttu-id="7c1f6-116">Regelname</span><span class="sxs-lookup"><span data-stu-id="7c1f6-116">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c1f6-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7c1f6-117">-Namespace</span></span>
<span data-ttu-id="7c1f6-118">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="7c1f6-118">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c1f6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c1f6-119">-ResourceGroupName</span></span>
<span data-ttu-id="7c1f6-120">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7c1f6-120">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c1f6-121">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="7c1f6-121">-Subscription</span></span>
<span data-ttu-id="7c1f6-122">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="7c1f6-122">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c1f6-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="7c1f6-123">-Topic</span></span>
<span data-ttu-id="7c1f6-124">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="7c1f6-124">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c1f6-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7c1f6-125">-Confirm</span></span>
<span data-ttu-id="7c1f6-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c1f6-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c1f6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c1f6-127">-WhatIf</span></span>
<span data-ttu-id="7c1f6-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c1f6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c1f6-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c1f6-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c1f6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c1f6-130">CommonParameters</span></span>
<span data-ttu-id="7c1f6-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c1f6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c1f6-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c1f6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c1f6-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7c1f6-133">INPUTS</span></span>

### <span data-ttu-id="7c1f6-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7c1f6-134">System.String</span></span>

### <span data-ttu-id="7c1f6-135">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="7c1f6-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="7c1f6-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7c1f6-136">OUTPUTS</span></span>

### <span data-ttu-id="7c1f6-137">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="7c1f6-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="7c1f6-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c1f6-138">NOTES</span></span>

## <span data-ttu-id="7c1f6-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7c1f6-139">RELATED LINKS</span></span>
