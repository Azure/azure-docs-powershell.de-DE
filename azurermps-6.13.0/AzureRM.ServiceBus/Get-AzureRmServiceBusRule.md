---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
ms.openlocfilehash: 2d249d8935b79c310e4ca0aa1270ee67bf33ece3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663105"
---
# <span data-ttu-id="42a01-101">Get-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="42a01-101">Get-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="42a01-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42a01-102">SYNOPSIS</span></span>
<span data-ttu-id="42a01-103">Erstellt eine neue Regel für ein bestimmtes Abonnement des Themas.</span><span class="sxs-lookup"><span data-stu-id="42a01-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42a01-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42a01-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42a01-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42a01-105">DESCRIPTION</span></span>
<span data-ttu-id="42a01-106">Das Cmdlet " **Get-AzureRmServiceBusRule** " Ruft die Beschreibung der angegebenen Regel im angegebenen Abonnement des Themas ab.</span><span class="sxs-lookup"><span data-stu-id="42a01-106">The **Get-AzureRmServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="42a01-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42a01-107">EXAMPLES</span></span>

### <span data-ttu-id="42a01-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="42a01-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="42a01-109">Gibt die angegebene Regelbeschreibung für ein angegebenes Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="42a01-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="42a01-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="42a01-110">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="42a01-111">Gibt eine Liste der Regelbeschreibungen für ein angegebenes Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="42a01-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="42a01-112">Standardmäßig wird die 100-Regel zurückgegeben, wenn mehr als 100-Regel zurückgegeben werden soll, verwenden Sie bitte-MaxCount-Parameter.</span><span class="sxs-lookup"><span data-stu-id="42a01-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="42a01-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="42a01-113">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="42a01-114">Gibt eine Liste der ersten 150-Regelbeschreibungen für ein angegebenes Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="42a01-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="42a01-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="42a01-115">PARAMETERS</span></span>

### <span data-ttu-id="42a01-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42a01-116">-DefaultProfile</span></span>
<span data-ttu-id="42a01-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42a01-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42a01-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="42a01-118">-MaxCount</span></span>
<span data-ttu-id="42a01-119">Ermitteln Sie die maximale Anzahl von Regeln, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="42a01-119">Determine the maximum number of Rules to return.</span></span>

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

### <span data-ttu-id="42a01-120">-Name</span><span class="sxs-lookup"><span data-stu-id="42a01-120">-Name</span></span>
<span data-ttu-id="42a01-121">Regelname</span><span class="sxs-lookup"><span data-stu-id="42a01-121">Rule Name</span></span>

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

### <span data-ttu-id="42a01-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="42a01-122">-Namespace</span></span>
<span data-ttu-id="42a01-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="42a01-123">Namespace Name</span></span>

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

### <span data-ttu-id="42a01-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42a01-124">-ResourceGroupName</span></span>
<span data-ttu-id="42a01-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="42a01-125">The name of the resource group</span></span>

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

### <span data-ttu-id="42a01-126">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="42a01-126">-Subscription</span></span>
<span data-ttu-id="42a01-127">Name des Abonnements</span><span class="sxs-lookup"><span data-stu-id="42a01-127">Subscription Name</span></span>

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

### <span data-ttu-id="42a01-128">-Topic</span><span class="sxs-lookup"><span data-stu-id="42a01-128">-Topic</span></span>
<span data-ttu-id="42a01-129">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="42a01-129">Topic Name</span></span>

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

### <span data-ttu-id="42a01-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42a01-130">CommonParameters</span></span>
<span data-ttu-id="42a01-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42a01-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42a01-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42a01-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42a01-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42a01-133">INPUTS</span></span>

### <span data-ttu-id="42a01-134">System. String</span><span class="sxs-lookup"><span data-stu-id="42a01-134">System.String</span></span>

## <span data-ttu-id="42a01-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42a01-135">OUTPUTS</span></span>

### <span data-ttu-id="42a01-136">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="42a01-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="42a01-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="42a01-137">NOTES</span></span>

## <span data-ttu-id="42a01-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42a01-138">RELATED LINKS</span></span>
