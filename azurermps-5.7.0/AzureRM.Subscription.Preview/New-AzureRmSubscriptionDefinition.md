---
external help file: Microsoft.Azure.Commands.SubscriptionDefinition.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription.preview/new-azurermsubscriptiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
ms.openlocfilehash: 7acaca4977114a1a57f88f5050f658753a9b6214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501314"
---
# <span data-ttu-id="43fb6-101">New-AzureRmSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="43fb6-101">New-AzureRmSubscriptionDefinition</span></span>

## <span data-ttu-id="43fb6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="43fb6-103">Erstellt eine Abonnementdefinition.</span><span class="sxs-lookup"><span data-stu-id="43fb6-103">Creates a subscription definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43fb6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43fb6-104">SYNTAX</span></span>

### <span data-ttu-id="43fb6-105">Erstellen einer Abonnementdefinition</span><span class="sxs-lookup"><span data-stu-id="43fb6-105">Create subscription definition</span></span>
```
New-AzureRmSubscriptionDefinition -Name <String> -OfferType <String> [-SubscriptionDisplayName <String>]
```

## <span data-ttu-id="43fb6-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43fb6-106">DESCRIPTION</span></span>
<span data-ttu-id="43fb6-107">Das Cmdlet **New-AzureRmSubscriptionDefinition** erstellt eine Abonnementdefinition.</span><span class="sxs-lookup"><span data-stu-id="43fb6-107">The **New-AzureRmSubscriptionDefinition** cmdlet creates a subscription definition.</span></span>

## <span data-ttu-id="43fb6-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43fb6-108">EXAMPLES</span></span>

### <span data-ttu-id="43fb6-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="43fb6-109">Example 1</span></span>
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MySubDef
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="43fb6-110">Erstellt eine Abonnementdefinition mit einem standardmäßigen Abonnement Anzeige Namen.</span><span class="sxs-lookup"><span data-stu-id="43fb6-110">Creates a subscription definition with a default subscription display name.</span></span>

### <span data-ttu-id="43fb6-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="43fb6-111">Example 2</span></span>
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P -SubscriptionDisplayName MyPaygoSub

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MyPaygoSub
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="43fb6-112">Erstellt eine Abonnementdefinition mit einem benutzerdefinierten Anzeige Namen für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43fb6-112">Creates a subscription definition with a custom subscription display name.</span></span>

## <span data-ttu-id="43fb6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="43fb6-113">PARAMETERS</span></span>

### <span data-ttu-id="43fb6-114">-Name</span><span class="sxs-lookup"><span data-stu-id="43fb6-114">-Name</span></span>
<span data-ttu-id="43fb6-115">Der Name der zu erstellende Abonnementdefinition.</span><span class="sxs-lookup"><span data-stu-id="43fb6-115">The name of the subscription definition to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43fb6-116">-Angebottype</span><span class="sxs-lookup"><span data-stu-id="43fb6-116">-OfferType</span></span>
<span data-ttu-id="43fb6-117">Der Typ des Angebots, das beim Erstellen des zugrunde liegenden Abonnements verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43fb6-117">The type of offer to use when creating the underlying subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43fb6-118">-SubscriptionDisplayName</span><span class="sxs-lookup"><span data-stu-id="43fb6-118">-SubscriptionDisplayName</span></span>
<span data-ttu-id="43fb6-119">Der Anzeigename, der beim Erstellen des zugrunde liegenden Abonnements der Abonnementdefinition zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="43fb6-119">The display name to use when creating the subscription definition's underlying subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43fb6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43fb6-120">CommonParameters</span></span>
<span data-ttu-id="43fb6-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43fb6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43fb6-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43fb6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43fb6-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43fb6-123">INPUTS</span></span>

### <span data-ttu-id="43fb6-124">Keine</span><span class="sxs-lookup"><span data-stu-id="43fb6-124">None</span></span>

## <span data-ttu-id="43fb6-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43fb6-125">OUTPUTS</span></span>

### <span data-ttu-id="43fb6-126">Microsoft. Azure. Commands. SubscriptionDefinition. Models. PSSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="43fb6-126">Microsoft.Azure.Commands.SubscriptionDefinition.Models.PSSubscriptionDefinition</span></span>

## <span data-ttu-id="43fb6-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="43fb6-127">NOTES</span></span>

## <span data-ttu-id="43fb6-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43fb6-128">RELATED LINKS</span></span>

