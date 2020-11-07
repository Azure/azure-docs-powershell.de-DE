---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
ms.openlocfilehash: 4fb10e2bb438cbc4f40936f9f9ead5c0bb36d861
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664721"
---
# <span data-ttu-id="64c64-101">Set-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="64c64-101">Set-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="64c64-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="64c64-102">SYNOPSIS</span></span>
<span data-ttu-id="64c64-103">Aktualisiert die angegebene Regelbeschreibung für das angegebene Abonnement.</span><span class="sxs-lookup"><span data-stu-id="64c64-103">Updates the specified rule description for the given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64c64-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="64c64-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <RulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64c64-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64c64-105">DESCRIPTION</span></span>
<span data-ttu-id="64c64-106">Das Cmdlet " **Satz-AzureRmServiceBusRule** " aktualisiert die Beschreibung für die angegebene Regel des angegebenen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="64c64-106">The **Set-AzureRmServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="64c64-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64c64-107">EXAMPLES</span></span>

### <span data-ttu-id="64c64-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="64c64-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="64c64-109">Aktualisiert den sqlausdruck **MySQL Expression = "Bedingung"** der Regel `SBEule` des Abonnements `SBSubscription` im Thema `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="64c64-109">updates the sqlexpression **mysqlexpression='condition'** of the rule `SBEule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="64c64-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="64c64-110">PARAMETERS</span></span>

### <span data-ttu-id="64c64-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="64c64-111">-Confirm</span></span>
<span data-ttu-id="64c64-112">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="64c64-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64c64-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="64c64-113">-InputObject</span></span>
<span data-ttu-id="64c64-114">ServiceBus-Regeldefinition</span><span class="sxs-lookup"><span data-stu-id="64c64-114">ServiceBus Rules definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64c64-115">-Name</span><span class="sxs-lookup"><span data-stu-id="64c64-115">-Name</span></span>
<span data-ttu-id="64c64-116">Regelname</span><span class="sxs-lookup"><span data-stu-id="64c64-116">Rule Name.</span></span>

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

### <span data-ttu-id="64c64-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="64c64-117">-Namespace</span></span>
<span data-ttu-id="64c64-118">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="64c64-118">Namespace Name.</span></span>

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

### <span data-ttu-id="64c64-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64c64-119">-ResourceGroupName</span></span>
<span data-ttu-id="64c64-120">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="64c64-120">The name of the resource group</span></span>

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

### <span data-ttu-id="64c64-121">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="64c64-121">-Subscription</span></span>
<span data-ttu-id="64c64-122">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="64c64-122">Subscription Name.</span></span>

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

### <span data-ttu-id="64c64-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="64c64-123">-Topic</span></span>
<span data-ttu-id="64c64-124">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="64c64-124">Topic Name.</span></span>

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

### <span data-ttu-id="64c64-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64c64-125">-WhatIf</span></span>
<span data-ttu-id="64c64-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="64c64-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64c64-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64c64-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64c64-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64c64-128">-DefaultProfile</span></span>
<span data-ttu-id="64c64-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="64c64-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c64-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64c64-130">CommonParameters</span></span>
<span data-ttu-id="64c64-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64c64-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64c64-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64c64-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64c64-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="64c64-133">INPUTS</span></span>

### <span data-ttu-id="64c64-134">System. String</span><span class="sxs-lookup"><span data-stu-id="64c64-134">System.String</span></span>
<span data-ttu-id="64c64-135">Microsoft. Azure. Commands. ServiceBus. Models. RulesAttributes</span><span class="sxs-lookup"><span data-stu-id="64c64-135">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>

## <span data-ttu-id="64c64-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="64c64-136">OUTPUTS</span></span>

### <span data-ttu-id="64c64-137">Microsoft. Azure. Commands. ServiceBus. Models. RulesAttributes</span><span class="sxs-lookup"><span data-stu-id="64c64-137">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>

## <span data-ttu-id="64c64-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="64c64-138">NOTES</span></span>

## <span data-ttu-id="64c64-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="64c64-139">RELATED LINKS</span></span>

