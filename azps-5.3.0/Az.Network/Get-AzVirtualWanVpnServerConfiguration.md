---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: 6124b3ddb862254d11bd141560a682bb91bb7fb7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379754"
---
# <span data-ttu-id="f0a4b-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0a4b-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="f0a4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="f0a4b-103">Ruft die Liste aller VpnServerConfigurations ab, die diesem VirtualWan zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f0a4b-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="f0a4b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0a4b-104">SYNTAX</span></span>

### <span data-ttu-id="f0a4b-105">ByVirtualWanName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f0a4b-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0a4b-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="f0a4b-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0a4b-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="f0a4b-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0a4b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0a4b-108">DESCRIPTION</span></span>
<span data-ttu-id="f0a4b-109">Das **Cmdlet "Get-AzVirtualWanVpnServerConfiguration"** gibt die Liste aller VpnServerConfigurations zurück, die diesem VirtualWan zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f0a4b-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="f0a4b-110">d. h. alle VpnServerConfigurations, die an alle P2SVpnGateways unter VirutalHubs dieses VirtualWan angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="f0a4b-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="f0a4b-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f0a4b-111">EXAMPLES</span></span>

### <span data-ttu-id="f0a4b-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f0a4b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="f0a4b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0a4b-113">PARAMETERS</span></span>

### <span data-ttu-id="f0a4b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0a4b-114">-DefaultProfile</span></span>
<span data-ttu-id="f0a4b-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0a4b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0a4b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f0a4b-116">-Name</span></span>
<span data-ttu-id="f0a4b-117">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="f0a4b-117">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a4b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0a4b-118">-ResourceGroupName</span></span>
<span data-ttu-id="f0a4b-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f0a4b-119">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a4b-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0a4b-120">-ResourceId</span></span>
<span data-ttu-id="f0a4b-121">Die Azure-Ressourcen-ID für das virtuelle Wan.</span><span class="sxs-lookup"><span data-stu-id="f0a4b-121">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a4b-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="f0a4b-122">-VirtualWanObject</span></span>
<span data-ttu-id="f0a4b-123">Das virtuelle WAN-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f0a4b-123">The virtual wan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a4b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0a4b-124">CommonParameters</span></span>
<span data-ttu-id="f0a4b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0a4b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0a4b-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0a4b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0a4b-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f0a4b-127">INPUTS</span></span>

### <span data-ttu-id="f0a4b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f0a4b-128">System.String</span></span>
<span data-ttu-id="f0a4b-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f0a4b-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="f0a4b-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f0a4b-130">OUTPUTS</span></span>

### <span data-ttu-id="f0a4b-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span><span class="sxs-lookup"><span data-stu-id="f0a4b-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="f0a4b-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f0a4b-132">NOTES</span></span>

## <span data-ttu-id="f0a4b-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f0a4b-133">RELATED LINKS</span></span>
