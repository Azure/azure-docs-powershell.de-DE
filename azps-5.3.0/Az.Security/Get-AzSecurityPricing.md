---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: 59d1c7fa5d546652d8976dc42739c2e483164999
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472030"
---
# <span data-ttu-id="c96df-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="c96df-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="c96df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c96df-102">SYNOPSIS</span></span>

<span data-ttu-id="c96df-103">Ruft die Azure Defender-Pläne für ein Abonnement im Azure Security Center ab.</span><span class="sxs-lookup"><span data-stu-id="c96df-103">Gets the Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="c96df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c96df-104">SYNTAX</span></span>

### <span data-ttu-id="c96df-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="c96df-105">SubscriptionScope (Default)</span></span>

```powershell
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c96df-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="c96df-106">SubscriptionLevelResource</span></span>

```powershell
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c96df-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c96df-107">ResourceId</span></span>

```powershell
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c96df-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c96df-108">DESCRIPTION</span></span>

<span data-ttu-id="c96df-109">Sie können jeden Azure Defender Plan pro Abonnement mit diesem Cmdlet anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c96df-109">You can view each Azure Defender plan, per subscription, using this cmdlet.</span></span>

<span data-ttu-id="c96df-110">Details zu Azure Defender und den verfügbaren Plänen finden Sie in [der Einführung in Azure Defender.](https://docs.microsoft.com/azure/security-center/azure-defender)</span><span class="sxs-lookup"><span data-stu-id="c96df-110">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="c96df-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c96df-111">EXAMPLES</span></span>

### <span data-ttu-id="c96df-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c96df-112">Example 1</span></span>

```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                   Name                      PricingTier    FreeTrialRemainingTime
--                                                                                                                   ----                      -----------    ----------------------
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/VirtualMachines            VirtualMachines           Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/Sqlservers                 SqlServers                Standard       00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/AppServices                AppServices               Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/StorageAccounts            StorageAccounts           Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlserverVirtualMachines   SqlservervirtualMachines  Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KubernetesService          KubernetesService         Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/ContainerRegistry          ContainerRegistry         Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KeyVaults                  KeyVaults                 Free           00:00:00
```

<span data-ttu-id="c96df-113">Ruft den Status der einzelnen Azure Defender-Pläne für das Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="c96df-113">Gets the status of each Azure Defender plan for the subscription.</span></span>



### <span data-ttu-id="c96df-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c96df-114">Example 2</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -ResourceId
```

<span data-ttu-id="c96df-115">Ruft Preisdetails für die spezifische Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="c96df-115">Gets pricing details of the specific resource ID.</span></span> <span data-ttu-id="c96df-116">Dabei ist "ResourceId" eine der IDs, die von zurückgegeben `Get-AzSecurityPricing` werden.</span><span class="sxs-lookup"><span data-stu-id="c96df-116">Where ResourceId is one of the IDs returned by `Get-AzSecurityPricing`.</span></span>

### <span data-ttu-id="c96df-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c96df-117">Example 3</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -Name
```

<span data-ttu-id="c96df-118">Ruft Preisdetails des benannten Azure Defender-Plans ab.</span><span class="sxs-lookup"><span data-stu-id="c96df-118">Gets pricing details of the named Azure Defender plan.</span></span> <span data-ttu-id="c96df-119">Dabei `name` handelt es sich um einen der von " zurückgegebenen Namen". `Get-AzSecurityPricing`</span><span class="sxs-lookup"><span data-stu-id="c96df-119">Where `name` is one of the names returned by `Get-AzSecurityPricing`.</span></span>


## <span data-ttu-id="c96df-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c96df-120">PARAMETERS</span></span>

### <span data-ttu-id="c96df-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c96df-121">-DefaultProfile</span></span>

<span data-ttu-id="c96df-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c96df-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c96df-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c96df-123">-Name</span></span>

<span data-ttu-id="c96df-124">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="c96df-124">Resource name.</span></span>

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

### <span data-ttu-id="c96df-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c96df-125">-ResourceId</span></span>

<span data-ttu-id="c96df-126">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="c96df-126">Resource ID.</span></span>

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

### <span data-ttu-id="c96df-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c96df-127">CommonParameters</span></span>

<span data-ttu-id="c96df-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c96df-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c96df-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c96df-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c96df-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c96df-130">INPUTS</span></span>

### <span data-ttu-id="c96df-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c96df-131">System.String</span></span>

## <span data-ttu-id="c96df-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c96df-132">OUTPUTS</span></span>

### <span data-ttu-id="c96df-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="c96df-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="c96df-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c96df-134">NOTES</span></span>

## <span data-ttu-id="c96df-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c96df-135">RELATED LINKS</span></span>
