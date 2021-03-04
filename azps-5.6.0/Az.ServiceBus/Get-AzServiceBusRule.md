---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
ms.openlocfilehash: 0dc9c54b3d2a080d7bb40c8560371b31f4ad3acf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939952"
---
# <span data-ttu-id="5fea3-101">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="5fea3-101">Get-AzServiceBusRule</span></span>

## <span data-ttu-id="5fea3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fea3-102">SYNOPSIS</span></span>
<span data-ttu-id="5fea3-103">Ruft die Definition einer vorhandenen Regel in einem bestimmten Abonnement von Thema ab.</span><span class="sxs-lookup"><span data-stu-id="5fea3-103">Retrieves the definition of an existing rule in a given Subscription of Topic.</span></span> 

## <span data-ttu-id="5fea3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5fea3-104">SYNTAX</span></span>

```
Get-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5fea3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fea3-105">DESCRIPTION</span></span>
<span data-ttu-id="5fea3-106">Das **Get-AzServiceBusRule-Cmdlet** ruft die Beschreibung der angegebenen Regel im angegebenen Abonnement des Themas ab.</span><span class="sxs-lookup"><span data-stu-id="5fea3-106">The **Get-AzServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="5fea3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5fea3-107">EXAMPLES</span></span>

### <span data-ttu-id="5fea3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5fea3-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="5fea3-109">Gibt die angegebene Regelbeschreibung für ein angegebenes Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="5fea3-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="5fea3-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5fea3-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="5fea3-111">Gibt eine Liste der Regelbeschreibungen für ein angegebenes Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="5fea3-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="5fea3-112">Standardmäßig wird die 100-Regel zurückgegeben. Wenn mehr als 100 Regeln zurückgegeben werden sollen, verwenden Sie den -MaxCount-Parameter.</span><span class="sxs-lookup"><span data-stu-id="5fea3-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="5fea3-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5fea3-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="5fea3-114">Gibt eine Liste der ersten 150 Regelbeschreibungen für ein angegebenes Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="5fea3-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="5fea3-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5fea3-115">PARAMETERS</span></span>

### <span data-ttu-id="5fea3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fea3-116">-DefaultProfile</span></span>
<span data-ttu-id="5fea3-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5fea3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fea3-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="5fea3-118">-MaxCount</span></span>
<span data-ttu-id="5fea3-119">Bestimmen Sie die maximale Anzahl von Regeln, die sie zurückgeben sollen.</span><span class="sxs-lookup"><span data-stu-id="5fea3-119">Determine the maximum number of Rules to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fea3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5fea3-120">-Name</span></span>
<span data-ttu-id="5fea3-121">Regelname</span><span class="sxs-lookup"><span data-stu-id="5fea3-121">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fea3-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5fea3-122">-Namespace</span></span>
<span data-ttu-id="5fea3-123">Namespacename</span><span class="sxs-lookup"><span data-stu-id="5fea3-123">Namespace Name</span></span>

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

### <span data-ttu-id="5fea3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fea3-124">-ResourceGroupName</span></span>
<span data-ttu-id="5fea3-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5fea3-125">The name of the resource group</span></span>

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

### <span data-ttu-id="5fea3-126">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="5fea3-126">-Subscription</span></span>
<span data-ttu-id="5fea3-127">Abonnementname</span><span class="sxs-lookup"><span data-stu-id="5fea3-127">Subscription Name</span></span>

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

### <span data-ttu-id="5fea3-128">-Topic</span><span class="sxs-lookup"><span data-stu-id="5fea3-128">-Topic</span></span>
<span data-ttu-id="5fea3-129">Topic Name</span><span class="sxs-lookup"><span data-stu-id="5fea3-129">Topic Name</span></span>

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

### <span data-ttu-id="5fea3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fea3-130">CommonParameters</span></span>
<span data-ttu-id="5fea3-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fea3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fea3-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fea3-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fea3-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5fea3-133">INPUTS</span></span>

### <span data-ttu-id="5fea3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5fea3-134">System.String</span></span>

## <span data-ttu-id="5fea3-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5fea3-135">OUTPUTS</span></span>

### <span data-ttu-id="5fea3-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="5fea3-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="5fea3-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5fea3-137">NOTES</span></span>

## <span data-ttu-id="5fea3-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5fea3-138">RELATED LINKS</span></span>
