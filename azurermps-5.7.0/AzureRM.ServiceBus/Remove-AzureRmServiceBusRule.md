---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
ms.openlocfilehash: 08f3fb2654d4c0b64900a4f15bbb7816e6d44c6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498810"
---
# <span data-ttu-id="72cad-101">Remove-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="72cad-101">Remove-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="72cad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72cad-102">SYNOPSIS</span></span>
<span data-ttu-id="72cad-103">Entfernt die angegeben-Regel eines angegebenen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="72cad-103">Removes the speficied rule of a given subscription .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72cad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72cad-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72cad-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72cad-105">DESCRIPTION</span></span>
<span data-ttu-id="72cad-106">Das Cmdlet **Remove-AzureRmServiceBusRule** entfernt die Regel eines Abonnements eines angegebenen Themas.</span><span class="sxs-lookup"><span data-stu-id="72cad-106">The **Remove-AzureRmServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="72cad-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72cad-107">EXAMPLES</span></span>

### <span data-ttu-id="72cad-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="72cad-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="72cad-109">Entfernt die `SBRule` Abonnementregel `SBSubscription` des angegebenen Themas `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="72cad-109">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

## <span data-ttu-id="72cad-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="72cad-110">PARAMETERS</span></span>

### <span data-ttu-id="72cad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72cad-111">-DefaultProfile</span></span>
<span data-ttu-id="72cad-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="72cad-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72cad-113">-Force</span><span class="sxs-lookup"><span data-stu-id="72cad-113">-Force</span></span>
<span data-ttu-id="72cad-114">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="72cad-114">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72cad-115">-Name</span><span class="sxs-lookup"><span data-stu-id="72cad-115">-Name</span></span>
<span data-ttu-id="72cad-116">Regelname</span><span class="sxs-lookup"><span data-stu-id="72cad-116">Rule Name.</span></span>

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

### <span data-ttu-id="72cad-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="72cad-117">-Namespace</span></span>
<span data-ttu-id="72cad-118">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="72cad-118">Namespace Name.</span></span>

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

### <span data-ttu-id="72cad-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72cad-119">-PassThru</span></span>
<span data-ttu-id="72cad-120">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="72cad-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72cad-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72cad-121">-ResourceGroupName</span></span>
<span data-ttu-id="72cad-122">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="72cad-122">The name of the resource group</span></span>

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

### <span data-ttu-id="72cad-123">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="72cad-123">-Subscription</span></span>
<span data-ttu-id="72cad-124">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="72cad-124">Subscription Name.</span></span>

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

### <span data-ttu-id="72cad-125">-Topic</span><span class="sxs-lookup"><span data-stu-id="72cad-125">-Topic</span></span>
<span data-ttu-id="72cad-126">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="72cad-126">Topic Name.</span></span>

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

### <span data-ttu-id="72cad-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="72cad-127">-Confirm</span></span>
<span data-ttu-id="72cad-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72cad-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72cad-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72cad-129">-WhatIf</span></span>
<span data-ttu-id="72cad-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72cad-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72cad-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72cad-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72cad-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72cad-132">CommonParameters</span></span>
<span data-ttu-id="72cad-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72cad-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72cad-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72cad-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72cad-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72cad-135">INPUTS</span></span>

### <span data-ttu-id="72cad-136">System. String</span><span class="sxs-lookup"><span data-stu-id="72cad-136">System.String</span></span>

## <span data-ttu-id="72cad-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72cad-137">OUTPUTS</span></span>

### <span data-ttu-id="72cad-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72cad-138">System.Boolean</span></span>

## <span data-ttu-id="72cad-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="72cad-139">NOTES</span></span>

## <span data-ttu-id="72cad-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72cad-140">RELATED LINKS</span></span>

