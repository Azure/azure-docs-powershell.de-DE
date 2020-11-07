---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 22e54316bd38907c1ab22e3b2c35e1b6949b0034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663425"
---
# <span data-ttu-id="c24a2-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="c24a2-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="c24a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c24a2-102">SYNOPSIS</span></span>
<span data-ttu-id="c24a2-103">Erstellt eine neue Regel für ein bestimmtes Abonnement des Themas.</span><span class="sxs-lookup"><span data-stu-id="c24a2-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c24a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c24a2-104">SYNTAX</span></span>

```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c24a2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c24a2-105">DESCRIPTION</span></span>
<span data-ttu-id="c24a2-106">Das Cmdlet **New-AzureRmServiceBusRule** erstellt eine neue Regel für ein bestimmtes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c24a2-106">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="c24a2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c24a2-107">EXAMPLES</span></span>

### <span data-ttu-id="c24a2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c24a2-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="c24a2-109">Das New-AzureRmServiceBusRule-Cmdlet erstellt eine neue Regel für das angegebene Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c24a2-109">The New-AzureRmServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

## <span data-ttu-id="c24a2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c24a2-110">PARAMETERS</span></span>

### <span data-ttu-id="c24a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c24a2-111">-DefaultProfile</span></span>
<span data-ttu-id="c24a2-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c24a2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c24a2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c24a2-113">-Name</span></span>
<span data-ttu-id="c24a2-114">Regelname</span><span class="sxs-lookup"><span data-stu-id="c24a2-114">Rule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c24a2-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c24a2-115">-Namespace</span></span>
<span data-ttu-id="c24a2-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="c24a2-116">Namespace Name.</span></span>

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

### <span data-ttu-id="c24a2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c24a2-117">-ResourceGroupName</span></span>
<span data-ttu-id="c24a2-118">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c24a2-118">The name of the resource group</span></span>

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

### <span data-ttu-id="c24a2-119">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="c24a2-119">-SqlExpression</span></span>
<span data-ttu-id="c24a2-120">SQL Fillter-Ausdruck</span><span class="sxs-lookup"><span data-stu-id="c24a2-120">Sql Fillter Expression</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c24a2-121">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="c24a2-121">-Subscription</span></span>
<span data-ttu-id="c24a2-122">Name des Abonnements</span><span class="sxs-lookup"><span data-stu-id="c24a2-122">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c24a2-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="c24a2-123">-Topic</span></span>
<span data-ttu-id="c24a2-124">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="c24a2-124">Topic Name.</span></span>

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

### <span data-ttu-id="c24a2-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c24a2-125">-Confirm</span></span>
<span data-ttu-id="c24a2-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c24a2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c24a2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c24a2-127">-WhatIf</span></span>
<span data-ttu-id="c24a2-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c24a2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c24a2-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c24a2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c24a2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c24a2-130">CommonParameters</span></span>
<span data-ttu-id="c24a2-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c24a2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c24a2-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c24a2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c24a2-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c24a2-133">INPUTS</span></span>

### <span data-ttu-id="c24a2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c24a2-134">System.String</span></span>

## <span data-ttu-id="c24a2-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c24a2-135">OUTPUTS</span></span>

### <span data-ttu-id="c24a2-136">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="c24a2-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="c24a2-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="c24a2-137">NOTES</span></span>

## <span data-ttu-id="c24a2-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c24a2-138">RELATED LINKS</span></span>

