---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: a714730a416d7554cba53e96428c9813fe4e720d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922195"
---
# <span data-ttu-id="64310-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="64310-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="64310-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64310-102">SYNOPSIS</span></span>
<span data-ttu-id="64310-103">Erstellt eine Instanz von PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="64310-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="64310-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64310-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64310-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64310-105">DESCRIPTION</span></span>
<span data-ttu-id="64310-106">Das **Cmdlet New-AzApiManagementVirtualNetwork** ist ein Hilfsbefehl zum Erstellen einer Instanz von **PsApiManagementVirtualNetwork.**</span><span class="sxs-lookup"><span data-stu-id="64310-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="64310-107">Dieser Befehl wird mit **dem Cmdlet Set-AzApiManagement** und **New-AzApiManagement** verwendet.</span><span class="sxs-lookup"><span data-stu-id="64310-107">This command is used with **Set-AzApiManagement** and **New-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="64310-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="64310-108">EXAMPLES</span></span>

### <span data-ttu-id="64310-109">Beispiel 1: Erstellen eines virtuellen Netzwerks und Aktualisieren eines vorhandenen APIM-Diensts in das VNET</span><span class="sxs-lookup"><span data-stu-id="64310-109">Example 1: Create a virtual network and Update an existing APIM service into the VNET</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="64310-110">In diesem Beispiel wird ein virtuelles Netzwerk erstellt und dann das **Cmdlet Set-AzApiManagement** aufruft.</span><span class="sxs-lookup"><span data-stu-id="64310-110">This example creates a virtual network and then calls the **Set-AzApiManagement** cmdlet.</span></span>

### <span data-ttu-id="64310-111">Beispiel 2: Erstellen eines API-Verwaltungsdiensts für ein externes virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="64310-111">Example 2: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="64310-112">In diesem Beispiel wird ein neuer APIM-Dienst in einem virtuellen Netzwerk im Modus `External` erstellt.</span><span class="sxs-lookup"><span data-stu-id="64310-112">This example creates a new APIM service into a Virtual Network in `External` mode</span></span>

## <span data-ttu-id="64310-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="64310-113">PARAMETERS</span></span>

### <span data-ttu-id="64310-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64310-114">-DefaultProfile</span></span>
<span data-ttu-id="64310-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64310-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64310-116">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="64310-116">-SubnetResourceId</span></span>
<span data-ttu-id="64310-117">Gibt die Subnetzressourcen-ID des virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="64310-117">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="64310-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64310-118">CommonParameters</span></span>
<span data-ttu-id="64310-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64310-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64310-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64310-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64310-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="64310-121">INPUTS</span></span>

### <span data-ttu-id="64310-122">Keine</span><span class="sxs-lookup"><span data-stu-id="64310-122">None</span></span>

## <span data-ttu-id="64310-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="64310-123">OUTPUTS</span></span>

### <span data-ttu-id="64310-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="64310-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="64310-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="64310-125">NOTES</span></span>

## <span data-ttu-id="64310-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="64310-126">RELATED LINKS</span></span>

<span data-ttu-id="64310-127">[Set-AzApiManagement](./Set-AzApiManagement.md) 
 [New-AzApiManagement](./New-AzApiManagement.md)</span><span class="sxs-lookup"><span data-stu-id="64310-127">[Set-AzApiManagement](./Set-AzApiManagement.md)
[New-AzApiManagement](./New-AzApiManagement.md)</span></span>

