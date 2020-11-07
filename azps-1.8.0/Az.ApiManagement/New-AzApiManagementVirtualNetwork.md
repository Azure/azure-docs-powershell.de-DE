---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: 67020f99129dfa920aa1bbc5e22ac59c16affb32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821123"
---
# <span data-ttu-id="3730e-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3730e-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="3730e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3730e-102">SYNOPSIS</span></span>
<span data-ttu-id="3730e-103">Erstellt eine Instanz von PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="3730e-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="3730e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3730e-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3730e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3730e-105">DESCRIPTION</span></span>
<span data-ttu-id="3730e-106">Das Cmdlet **New-AzApiManagementVirtualNetwork** ist ein Hilfsbefehl zum Erstellen einer Instanz von **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="3730e-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="3730e-107">Dieser Befehl wird mit dem Cmdlet **Update-AzApiManagementDeployment** verwendet.</span><span class="sxs-lookup"><span data-stu-id="3730e-107">This command is used with **Update-AzApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="3730e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3730e-108">EXAMPLES</span></span>

### <span data-ttu-id="3730e-109">Beispiel 1: Erstellen eines virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="3730e-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$vnetName = "myvnet"
PS C:\>$subnetName = "default"
PS C:\>$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.1.0/24
PS C:\>$vnet = New-AzvirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix 10.0.0.0/16 -Subnet $subnet

# Create a Virtual Network Object
PS C:\>$virtualNetwork = New-AzApiManagementVirtualNetwork -Location $location -SubnetResourceId $vnet.Subnets[0].Id

# Get the service
PS C:\>$service = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName    
PS C:\>$service.VirtualNetwork = $virtualNetwork
PS C:\>$service.VpnType = "External"

# Update the Deployment with Virtual Network
PS C:\>Update-AzApiManagementDeployment -ApiManagement $service
```

<span data-ttu-id="3730e-110">In diesem Beispiel wird ein virtuelles Netzwerk erstellt und anschließend das Cmdlet **Update-AzApiManagementDeployment** aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="3730e-110">This example creates a virtual network and then calls the **Update-AzApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="3730e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3730e-111">PARAMETERS</span></span>

### <span data-ttu-id="3730e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3730e-112">-DefaultProfile</span></span>
<span data-ttu-id="3730e-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3730e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3730e-114">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="3730e-114">-SubnetResourceId</span></span>
<span data-ttu-id="3730e-115">Gibt die Subnetz-Ressourcen-ID des virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="3730e-115">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="3730e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3730e-116">CommonParameters</span></span>
<span data-ttu-id="3730e-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3730e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3730e-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3730e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3730e-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3730e-119">INPUTS</span></span>

### <span data-ttu-id="3730e-120">Keine</span><span class="sxs-lookup"><span data-stu-id="3730e-120">None</span></span>

## <span data-ttu-id="3730e-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3730e-121">OUTPUTS</span></span>

### <span data-ttu-id="3730e-122">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3730e-122">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="3730e-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="3730e-123">NOTES</span></span>

## <span data-ttu-id="3730e-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3730e-124">RELATED LINKS</span></span>

[<span data-ttu-id="3730e-125">Update-AzApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="3730e-125">Update-AzApiManagementDeployment</span></span>](./Update-AzApiManagementDeployment.md)

