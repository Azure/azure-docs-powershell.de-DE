---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: 176ef6d90fed93a65da10a1f1174f2b81f1fe094
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996298"
---
# <span data-ttu-id="678f6-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="678f6-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="678f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="678f6-102">SYNOPSIS</span></span>
<span data-ttu-id="678f6-103">Ruft die Preisstufen Daten für das Azure Security Center für einen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="678f6-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

## <span data-ttu-id="678f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="678f6-104">SYNTAX</span></span>

### <span data-ttu-id="678f6-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="678f6-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="678f6-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="678f6-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="678f6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="678f6-107">ResourceId</span></span>
```
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="678f6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="678f6-108">DESCRIPTION</span></span>
<span data-ttu-id="678f6-109">Das Azure Security Center-Preisniveau wird pro Bereich entschieden, mit diesem Cmdlet können Sie die konfigurierten Preisstufen abrufen.</span><span class="sxs-lookup"><span data-stu-id="678f6-109">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="678f6-110">Die Abonnementpreis Ebene umfasst alle darunter liegenden Ressourcengruppen.</span><span class="sxs-lookup"><span data-stu-id="678f6-110">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="678f6-111">Die Ressourcengruppen-Preisstufe setzt die Abonnementpreis Ebene außer Kraft.</span><span class="sxs-lookup"><span data-stu-id="678f6-111">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="678f6-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="678f6-112">EXAMPLES</span></span>

### <span data-ttu-id="678f6-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="678f6-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="678f6-114">Ruft alle konfigurierten Preisstufen für das Abonnement und die darunter liegenden Ressourcengruppen ab.</span><span class="sxs-lookup"><span data-stu-id="678f6-114">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="678f6-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="678f6-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="678f6-116">Ruft die konfigurierte Preisstufe für die Ressourcengruppe "myService1" ab.</span><span class="sxs-lookup"><span data-stu-id="678f6-116">Gets the configured pricing tier for the "myService1" resource group.</span></span>

## <span data-ttu-id="678f6-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="678f6-117">PARAMETERS</span></span>

### <span data-ttu-id="678f6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="678f6-118">-DefaultProfile</span></span>
<span data-ttu-id="678f6-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="678f6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="678f6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="678f6-120">-Name</span></span>
<span data-ttu-id="678f6-121">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="678f6-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="678f6-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="678f6-122">-ResourceId</span></span>
<span data-ttu-id="678f6-123">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="678f6-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="678f6-124">CommonParameters</span></span>
<span data-ttu-id="678f6-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="678f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="678f6-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="678f6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="678f6-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="678f6-127">INPUTS</span></span>

### <span data-ttu-id="678f6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="678f6-128">System.String</span></span>

## <span data-ttu-id="678f6-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="678f6-129">OUTPUTS</span></span>

### <span data-ttu-id="678f6-130">Microsoft. Azure. Commands. Security. Models. Pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="678f6-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="678f6-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="678f6-131">NOTES</span></span>

## <span data-ttu-id="678f6-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="678f6-132">RELATED LINKS</span></span>
