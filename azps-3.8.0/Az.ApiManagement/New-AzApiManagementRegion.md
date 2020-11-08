---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
ms.openlocfilehash: 2259990c568dbf6fd5b7bc6f8bff34c464a082ec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996921"
---
# <span data-ttu-id="e1d3a-101">New-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="e1d3a-101">New-AzApiManagementRegion</span></span>

## <span data-ttu-id="e1d3a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1d3a-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d3a-103">Erstellt eine Instanz von PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="e1d3a-103">Creates an instance of PsApiManagementRegion.</span></span>

## <span data-ttu-id="e1d3a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1d3a-104">SYNTAX</span></span>

```
New-AzApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1d3a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1d3a-105">DESCRIPTION</span></span>
<span data-ttu-id="e1d3a-106">Hilfsbefehl zum Erstellen einer Instanz von PsApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="e1d3a-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="e1d3a-107">Dieser Befehl ist mit New-AzApiManagement Befehl zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e1d3a-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="e1d3a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1d3a-108">EXAMPLES</span></span>

### <span data-ttu-id="e1d3a-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e1d3a-109">Example 1</span></span>
```
$apimRegion = New-AzApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="e1d3a-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e1d3a-110">Example 2</span></span>
```
$apimRegionVirtualNetwork = New-AzApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="e1d3a-111">Erstellt einen ApiManagement-Dienst für externe VpnType in der Region West Amerika mit einer zusätzlichen Region in Zentralamerika.</span><span class="sxs-lookup"><span data-stu-id="e1d3a-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="e1d3a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1d3a-112">PARAMETERS</span></span>

### <span data-ttu-id="e1d3a-113">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="e1d3a-113">-Capacity</span></span>
<span data-ttu-id="e1d3a-114">SKU-Kapazität des Azure API-Verwaltungsdiensts (zusätzlicher Bereich).</span><span class="sxs-lookup"><span data-stu-id="e1d3a-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="e1d3a-115">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="e1d3a-115">Default value is 1.</span></span>

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

### <span data-ttu-id="e1d3a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d3a-116">-DefaultProfile</span></span>
<span data-ttu-id="e1d3a-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e1d3a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1d3a-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="e1d3a-118">-Location</span></span>
<span data-ttu-id="e1d3a-119">Gibt den Speicherort des neuen Bereitstellungsbereichs zwischen dem unterstützten Bereich für den API-Verwaltungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="e1d3a-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="e1d3a-120">Verwenden Sie zum Abrufen gültiger Speicherorte das Cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | wobei {$ _. Hilfswerte [0]. "-EQ"-Dienst "} | Select-Object Standorte</span><span class="sxs-lookup"><span data-stu-id="e1d3a-120">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="e1d3a-121">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e1d3a-121">-VirtualNetwork</span></span>
<span data-ttu-id="e1d3a-122">Virtuelle Netzwerkkonfiguration des Azure API Management Deployment-Bereichs.</span><span class="sxs-lookup"><span data-stu-id="e1d3a-122">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="e1d3a-123">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="e1d3a-123">Default value is $null.</span></span>

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

### <span data-ttu-id="e1d3a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d3a-124">CommonParameters</span></span>
<span data-ttu-id="e1d3a-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1d3a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d3a-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1d3a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d3a-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1d3a-127">INPUTS</span></span>

### <span data-ttu-id="e1d3a-128">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e1d3a-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="e1d3a-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1d3a-129">OUTPUTS</span></span>

### <span data-ttu-id="e1d3a-130">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="e1d3a-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="e1d3a-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1d3a-131">NOTES</span></span>

## <span data-ttu-id="e1d3a-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1d3a-132">RELATED LINKS</span></span>
