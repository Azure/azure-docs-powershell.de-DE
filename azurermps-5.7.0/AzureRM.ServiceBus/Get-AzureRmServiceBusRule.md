---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
ms.openlocfilehash: 3eb629665f8bc4ed030b5c616410fb47455136e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502433"
---
# <span data-ttu-id="0902f-101">Get-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="0902f-101">Get-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="0902f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0902f-102">SYNOPSIS</span></span>
<span data-ttu-id="0902f-103">Ruft eine Beschreibung der angegebenen Regel für ein angegebenes Abonnement des Themas ab.</span><span class="sxs-lookup"><span data-stu-id="0902f-103">Gets a description of the specified rule for a given Subscription of  Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0902f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0902f-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0902f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0902f-105">DESCRIPTION</span></span>
<span data-ttu-id="0902f-106">Das Cmdlet " **Get-AzureRmServiceBusRule** " Ruft die Beschreibung der angegebenen Regel im angegebenen Abonnement des Themas ab.</span><span class="sxs-lookup"><span data-stu-id="0902f-106">The **Get-AzureRmServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="0902f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0902f-107">EXAMPLES</span></span>

### <span data-ttu-id="0902f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0902f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -NAme SBRule
```

<span data-ttu-id="0902f-109">Gibt die angegebene Regelbeschreibung für ein angegebenes Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="0902f-109">Returns the specified rule description for a specified subscription.</span></span>

## <span data-ttu-id="0902f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0902f-110">PARAMETERS</span></span>

### <span data-ttu-id="0902f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0902f-111">-DefaultProfile</span></span>
<span data-ttu-id="0902f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0902f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0902f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="0902f-113">-Name</span></span>
<span data-ttu-id="0902f-114">Regelname</span><span class="sxs-lookup"><span data-stu-id="0902f-114">Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0902f-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0902f-115">-Namespace</span></span>
<span data-ttu-id="0902f-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="0902f-116">Namespace Name.</span></span>

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

### <span data-ttu-id="0902f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0902f-117">-ResourceGroupName</span></span>
<span data-ttu-id="0902f-118">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0902f-118">The name of the resource group</span></span>

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

### <span data-ttu-id="0902f-119">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="0902f-119">-Subscription</span></span>
<span data-ttu-id="0902f-120">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="0902f-120">Subscription Name.</span></span>

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

### <span data-ttu-id="0902f-121">-Topic</span><span class="sxs-lookup"><span data-stu-id="0902f-121">-Topic</span></span>
<span data-ttu-id="0902f-122">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="0902f-122">Topic Name.</span></span>

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

### <span data-ttu-id="0902f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0902f-123">CommonParameters</span></span>
<span data-ttu-id="0902f-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0902f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0902f-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0902f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0902f-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0902f-126">INPUTS</span></span>

### <span data-ttu-id="0902f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0902f-127">System.String</span></span>

## <span data-ttu-id="0902f-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0902f-128">OUTPUTS</span></span>

### <span data-ttu-id="0902f-129">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="0902f-129">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="0902f-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="0902f-130">NOTES</span></span>

## <span data-ttu-id="0902f-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0902f-131">RELATED LINKS</span></span>

