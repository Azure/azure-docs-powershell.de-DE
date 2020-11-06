---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
ms.openlocfilehash: a5febccec0ed09cde866925ce03d7025408b27f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503302"
---
# <span data-ttu-id="59b09-101">New-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="59b09-101">New-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="59b09-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59b09-102">SYNOPSIS</span></span>
<span data-ttu-id="59b09-103">Erstellt eine Instanz von PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="59b09-103">Creates an instance of PsApiManagementRegion.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59b09-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59b09-104">SYNTAX</span></span>

```
New-AzureRmApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59b09-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59b09-105">DESCRIPTION</span></span>
<span data-ttu-id="59b09-106">Hilfsbefehl zum Erstellen einer Instanz von PsApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="59b09-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="59b09-107">Dieser Befehl ist mit New-AzureRmApiManagement Befehl zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="59b09-107">This command is to be used with New-AzureRmApiManagement command.</span></span>

## <span data-ttu-id="59b09-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59b09-108">EXAMPLES</span></span>

### <span data-ttu-id="59b09-109">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="59b09-109">--------------------------  Example 1  --------------------------</span></span>
```
$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="59b09-110">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="59b09-110">--------------------------  Example 2  --------------------------</span></span>
```
$apimRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="59b09-111">Erstellt einen ApiManagement-Dienst für externe VpnType in der Region West Amerika mit einer zusätzlichen Region in Zentralamerika.</span><span class="sxs-lookup"><span data-stu-id="59b09-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="59b09-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="59b09-112">PARAMETERS</span></span>

### <span data-ttu-id="59b09-113">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="59b09-113">-Capacity</span></span>
<span data-ttu-id="59b09-114">SKU-Kapazität des Azure API-Verwaltungsdiensts (zusätzlicher Bereich).</span><span class="sxs-lookup"><span data-stu-id="59b09-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="59b09-115">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="59b09-115">Default value is 1.</span></span>

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

### <span data-ttu-id="59b09-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="59b09-116">-Location</span></span>
<span data-ttu-id="59b09-117">Der Speicherort des zusätzlichen Bereitstellungsbereichs.</span><span class="sxs-lookup"><span data-stu-id="59b09-117">Location of the additional deployment region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b09-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59b09-118">-VirtualNetwork</span></span>
<span data-ttu-id="59b09-119">Virtuelle Netzwerkkonfiguration des Azure API Management Deployment-Bereichs.</span><span class="sxs-lookup"><span data-stu-id="59b09-119">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="59b09-120">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="59b09-120">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59b09-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59b09-121">-DefaultProfile</span></span>
<span data-ttu-id="59b09-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="59b09-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59b09-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59b09-123">CommonParameters</span></span>
<span data-ttu-id="59b09-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59b09-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59b09-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59b09-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59b09-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59b09-126">INPUTS</span></span>

## <span data-ttu-id="59b09-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59b09-127">OUTPUTS</span></span>

### <span data-ttu-id="59b09-128">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="59b09-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="59b09-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="59b09-129">NOTES</span></span>

## <span data-ttu-id="59b09-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59b09-130">RELATED LINKS</span></span>

