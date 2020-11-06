---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 30a237f0f87286be8f6cd18e804d80850df7a8be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505861"
---
# <span data-ttu-id="18b83-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="18b83-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="18b83-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="18b83-102">SYNOPSIS</span></span>
<span data-ttu-id="18b83-103">Erstellt eine Instanz von PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="18b83-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18b83-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="18b83-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18b83-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18b83-105">DESCRIPTION</span></span>
<span data-ttu-id="18b83-106">Das Cmdlet **New-AzureRmApiManagementVirtualNetwork** ist ein Hilfsbefehl zum Erstellen einer Instanz von **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="18b83-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="18b83-107">Dieser Befehl wird mit dem Cmdlet **Update-AzureRmApiManagementDeployment** verwendet.</span><span class="sxs-lookup"><span data-stu-id="18b83-107">This command is used with **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="18b83-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18b83-108">EXAMPLES</span></span>

### <span data-ttu-id="18b83-109">Beispiel 1: Erstellen eines virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="18b83-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$vnetName = "myvnet"
PS C:\>$subnetName = "default"
PS C:\>$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.1.0/24
PS C:\>$vnet = New-AzureRmvirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix 10.0.0.0/16 -Subnet $subnet

# Create a Virtual Network Object
PS C:\>$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location $location -SubnetResourceId $vnet.Subnets[0].Id

# Get the service
PS C:\>$service = Get-AzureRmApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName    
PS C:\>$service.VirtualNetwork = $virtualNetwork
PS C:\>$service.VpnType = "External"

# Update the Deployment with Virtual Network
PS C:\>Update-AzureRmApiManagementDeployment -ApiManagement $service
```

<span data-ttu-id="18b83-110">In diesem Beispiel wird ein virtuelles Netzwerk erstellt und anschließend das Cmdlet **Update-AzureRmApiManagementDeployment** aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="18b83-110">This example creates a virtual network and then calls the **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="18b83-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="18b83-111">PARAMETERS</span></span>

### <span data-ttu-id="18b83-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b83-112">-DefaultProfile</span></span>
<span data-ttu-id="18b83-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="18b83-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="18b83-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="18b83-114">-Location</span></span>
<span data-ttu-id="18b83-115">Gibt den Speicherort des API-Verwaltungsdiensts für den unterstützten Bereich an.</span><span class="sxs-lookup"><span data-stu-id="18b83-115">Specifies the location amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="18b83-116">Verwenden Sie zum Abrufen gültiger Speicherorte das Cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | wobei {$ _. Hilfswerte [0]. "-EQ"-Dienst "} | Select-Object Standorte</span><span class="sxs-lookup"><span data-stu-id="18b83-116">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="18b83-117">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="18b83-117">-SubnetResourceId</span></span>
<span data-ttu-id="18b83-118">Gibt die Subnetz-Ressourcen-ID des virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="18b83-118">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="18b83-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b83-119">CommonParameters</span></span>
<span data-ttu-id="18b83-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18b83-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b83-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18b83-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b83-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="18b83-122">INPUTS</span></span>

### <span data-ttu-id="18b83-123">Keine</span><span class="sxs-lookup"><span data-stu-id="18b83-123">None</span></span>
<span data-ttu-id="18b83-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="18b83-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="18b83-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="18b83-125">OUTPUTS</span></span>

### <span data-ttu-id="18b83-126">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="18b83-126">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="18b83-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="18b83-127">NOTES</span></span>

## <span data-ttu-id="18b83-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="18b83-128">RELATED LINKS</span></span>

[<span data-ttu-id="18b83-129">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="18b83-129">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)

