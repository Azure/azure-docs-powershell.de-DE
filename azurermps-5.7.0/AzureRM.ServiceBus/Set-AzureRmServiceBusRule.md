---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
ms.openlocfilehash: 8a8c60f486980fef6005cb4f4070af31689fae92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480893"
---
# <span data-ttu-id="8760a-101">Set-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="8760a-101">Set-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="8760a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8760a-102">SYNOPSIS</span></span>
<span data-ttu-id="8760a-103">Aktualisiert die angegebene Regelbeschreibung für das angegebene Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8760a-103">Updates the specified rule description for the given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8760a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8760a-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <RulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8760a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8760a-105">DESCRIPTION</span></span>
<span data-ttu-id="8760a-106">Das Cmdlet " **Satz-AzureRmServiceBusRule** " aktualisiert die Beschreibung für die angegebene Regel des angegebenen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="8760a-106">The **Set-AzureRmServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="8760a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8760a-107">EXAMPLES</span></span>

### <span data-ttu-id="8760a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8760a-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="8760a-109">Aktualisiert den sqlausdruck **MySQL Expression = "Bedingung"** der Regel `SBEule` des Abonnements `SBSubscription` im Thema `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="8760a-109">updates the sqlexpression **mysqlexpression='condition'** of the rule `SBEule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="8760a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8760a-110">PARAMETERS</span></span>

### <span data-ttu-id="8760a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8760a-111">-DefaultProfile</span></span>
<span data-ttu-id="8760a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8760a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8760a-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8760a-113">-InputObject</span></span>
<span data-ttu-id="8760a-114">ServiceBus-Regeldefinition</span><span class="sxs-lookup"><span data-stu-id="8760a-114">ServiceBus Rules definition.</span></span>

```yaml
Type: PSRulesAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8760a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8760a-115">-Name</span></span>
<span data-ttu-id="8760a-116">Regelname</span><span class="sxs-lookup"><span data-stu-id="8760a-116">Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8760a-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8760a-117">-Namespace</span></span>
<span data-ttu-id="8760a-118">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="8760a-118">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8760a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8760a-119">-ResourceGroupName</span></span>
<span data-ttu-id="8760a-120">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="8760a-120">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8760a-121">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="8760a-121">-Subscription</span></span>
<span data-ttu-id="8760a-122">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="8760a-122">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8760a-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="8760a-123">-Topic</span></span>
<span data-ttu-id="8760a-124">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="8760a-124">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8760a-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8760a-125">-Confirm</span></span>
<span data-ttu-id="8760a-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8760a-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8760a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8760a-127">-WhatIf</span></span>
<span data-ttu-id="8760a-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8760a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8760a-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8760a-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8760a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8760a-130">CommonParameters</span></span>
<span data-ttu-id="8760a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8760a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8760a-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8760a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8760a-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8760a-133">INPUTS</span></span>

### <span data-ttu-id="8760a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8760a-134">System.String</span></span>
<span data-ttu-id="8760a-135">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="8760a-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="8760a-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8760a-136">OUTPUTS</span></span>

### <span data-ttu-id="8760a-137">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="8760a-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="8760a-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="8760a-138">NOTES</span></span>

## <span data-ttu-id="8760a-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8760a-139">RELATED LINKS</span></span>

