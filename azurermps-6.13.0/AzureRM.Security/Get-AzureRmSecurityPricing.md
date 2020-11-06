---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
ms.openlocfilehash: 27d27cf3df8c41eaa507d9223c73f2b36637a04c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477693"
---
# <span data-ttu-id="4e6d7-101">Get-AzureRmSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="4e6d7-101">Get-AzureRmSecurityPricing</span></span>

## <span data-ttu-id="4e6d7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4e6d7-102">SYNOPSIS</span></span>
<span data-ttu-id="4e6d7-103">Ruft die Preisstufen Daten für das Azure Security Center für einen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="4e6d7-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e6d7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e6d7-104">SYNTAX</span></span>

### <span data-ttu-id="4e6d7-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="4e6d7-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e6d7-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="4e6d7-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e6d7-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="4e6d7-107">ResourceGroupScope</span></span>
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e6d7-108">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="4e6d7-108">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e6d7-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e6d7-109">ResourceId</span></span>
```
Get-AzureRmSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e6d7-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e6d7-110">DESCRIPTION</span></span>
<span data-ttu-id="4e6d7-111">Das Azure Security Center-Preisniveau wird pro Bereich entschieden, mit diesem Cmdlet können Sie die konfigurierten Preisstufen abrufen.</span><span class="sxs-lookup"><span data-stu-id="4e6d7-111">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="4e6d7-112">Die Abonnementpreis Ebene umfasst alle darunter liegenden Ressourcengruppen.</span><span class="sxs-lookup"><span data-stu-id="4e6d7-112">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="4e6d7-113">Die Ressourcengruppen-Preisstufe setzt die Abonnementpreis Ebene außer Kraft.</span><span class="sxs-lookup"><span data-stu-id="4e6d7-113">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="4e6d7-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e6d7-114">EXAMPLES</span></span>

### <span data-ttu-id="4e6d7-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4e6d7-115">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="4e6d7-116">Ruft alle konfigurierten Preisstufen für das Abonnement und die darunter liegenden Ressourcengruppen ab.</span><span class="sxs-lookup"><span data-stu-id="4e6d7-116">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="4e6d7-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4e6d7-117">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="4e6d7-118">Ruft die konfigurierte Preisstufe für das Ressourcen-Gorup "myService1" ab.</span><span class="sxs-lookup"><span data-stu-id="4e6d7-118">Gets the configured pricing tier for the "myService1" resource gorup.</span></span>

## <span data-ttu-id="4e6d7-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e6d7-119">PARAMETERS</span></span>

### <span data-ttu-id="4e6d7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e6d7-120">-DefaultProfile</span></span>
<span data-ttu-id="4e6d7-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4e6d7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e6d7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4e6d7-122">-Name</span></span>
<span data-ttu-id="4e6d7-123">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="4e6d7-123">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e6d7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e6d7-124">-ResourceGroupName</span></span>
<span data-ttu-id="4e6d7-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4e6d7-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e6d7-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4e6d7-126">-ResourceId</span></span>
<span data-ttu-id="4e6d7-127">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="4e6d7-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e6d7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e6d7-128">CommonParameters</span></span>
<span data-ttu-id="4e6d7-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e6d7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e6d7-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e6d7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e6d7-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4e6d7-131">INPUTS</span></span>

### <span data-ttu-id="4e6d7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4e6d7-132">System.String</span></span>

## <span data-ttu-id="4e6d7-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4e6d7-133">OUTPUTS</span></span>

### <span data-ttu-id="4e6d7-134">Microsoft. Azure. Commands. Security. Models. Pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="4e6d7-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="4e6d7-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="4e6d7-135">NOTES</span></span>

## <span data-ttu-id="4e6d7-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4e6d7-136">RELATED LINKS</span></span>
