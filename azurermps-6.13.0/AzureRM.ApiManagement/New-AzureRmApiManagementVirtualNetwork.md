---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: abfcbec55ba3f53986a63a8c0964320c10fc91ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501246"
---
# <span data-ttu-id="35cf6-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="35cf6-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="35cf6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35cf6-102">SYNOPSIS</span></span>
<span data-ttu-id="35cf6-103">Erstellt eine Instanz von PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="35cf6-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35cf6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35cf6-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35cf6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35cf6-105">DESCRIPTION</span></span>
<span data-ttu-id="35cf6-106">Das Cmdlet **New-AzureRmApiManagementVirtualNetwork** ist ein Hilfsbefehl zum Erstellen einer Instanz von **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="35cf6-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="35cf6-107">Dieser Befehl wird mit dem Cmdlet **Update-AzureRmApiManagementDeployment** verwendet.</span><span class="sxs-lookup"><span data-stu-id="35cf6-107">This command is used with **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="35cf6-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35cf6-108">EXAMPLES</span></span>

### <span data-ttu-id="35cf6-109">Beispiel 1: Erstellen eines virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="35cf6-109">Example 1: Create a virtual network</span></span>
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

<span data-ttu-id="35cf6-110">In diesem Beispiel wird ein virtuelles Netzwerk erstellt und anschließend das Cmdlet **Update-AzureRmApiManagementDeployment** aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="35cf6-110">This example creates a virtual network and then calls the **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="35cf6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="35cf6-111">PARAMETERS</span></span>

### <span data-ttu-id="35cf6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35cf6-112">-DefaultProfile</span></span>
<span data-ttu-id="35cf6-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="35cf6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35cf6-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="35cf6-114">-Location</span></span>
<span data-ttu-id="35cf6-115">Gibt den Speicherort des API-Verwaltungsdiensts für den unterstützten Bereich an.</span><span class="sxs-lookup"><span data-stu-id="35cf6-115">Specifies the location amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="35cf6-116">Verwenden Sie zum Abrufen gültiger Speicherorte das Cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | wobei {$ _. Hilfswerte [0]. "-EQ"-Dienst "} | Select-Object Standorte</span><span class="sxs-lookup"><span data-stu-id="35cf6-116">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="35cf6-117">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="35cf6-117">-SubnetResourceId</span></span>
<span data-ttu-id="35cf6-118">Gibt die Subnetz-Ressourcen-ID des virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="35cf6-118">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="35cf6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35cf6-119">CommonParameters</span></span>
<span data-ttu-id="35cf6-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35cf6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35cf6-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35cf6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35cf6-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35cf6-122">INPUTS</span></span>

### <span data-ttu-id="35cf6-123">Keine</span><span class="sxs-lookup"><span data-stu-id="35cf6-123">None</span></span>

## <span data-ttu-id="35cf6-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35cf6-124">OUTPUTS</span></span>

### <span data-ttu-id="35cf6-125">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="35cf6-125">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="35cf6-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="35cf6-126">NOTES</span></span>

## <span data-ttu-id="35cf6-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35cf6-127">RELATED LINKS</span></span>

[<span data-ttu-id="35cf6-128">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="35cf6-128">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)

