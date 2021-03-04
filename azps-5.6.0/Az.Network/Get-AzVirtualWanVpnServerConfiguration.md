---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: 2919c007852961386fb1ab444e43d855ced2a8d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924736"
---
# <span data-ttu-id="28ee9-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="28ee9-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="28ee9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28ee9-102">SYNOPSIS</span></span>
<span data-ttu-id="28ee9-103">Ruft die Liste aller VpnServerConfigurationen ab, die diesem VirtualWan zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="28ee9-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="28ee9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28ee9-104">SYNTAX</span></span>

### <span data-ttu-id="28ee9-105">ByVirtualWanName (Standard)</span><span class="sxs-lookup"><span data-stu-id="28ee9-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28ee9-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="28ee9-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28ee9-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="28ee9-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28ee9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28ee9-108">DESCRIPTION</span></span>
<span data-ttu-id="28ee9-109">Das **Cmdlet Get-AzVirtualWanVpnServerConfiguration** gibt die Liste aller VpnServerConfigurationen zurück, die diesem VirtualWan zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="28ee9-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="28ee9-110">d. h. alle VpnServerConfigurations, die an alle P2SVpnGateways unter VirutalHubs dieses VirtualWan angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="28ee9-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="28ee9-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="28ee9-111">EXAMPLES</span></span>

### <span data-ttu-id="28ee9-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="28ee9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="28ee9-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="28ee9-113">PARAMETERS</span></span>

### <span data-ttu-id="28ee9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28ee9-114">-DefaultProfile</span></span>
<span data-ttu-id="28ee9-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="28ee9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28ee9-116">-Name</span><span class="sxs-lookup"><span data-stu-id="28ee9-116">-Name</span></span>
<span data-ttu-id="28ee9-117">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="28ee9-117">The resource name.</span></span>

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

### <span data-ttu-id="28ee9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28ee9-118">-ResourceGroupName</span></span>
<span data-ttu-id="28ee9-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="28ee9-119">The resource group name.</span></span>

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

### <span data-ttu-id="28ee9-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28ee9-120">-ResourceId</span></span>
<span data-ttu-id="28ee9-121">Die Azure-Ressourcen-ID für das virtuelle Wan.</span><span class="sxs-lookup"><span data-stu-id="28ee9-121">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="28ee9-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="28ee9-122">-VirtualWanObject</span></span>
<span data-ttu-id="28ee9-123">Das virtuelle Wan-Objekt.</span><span class="sxs-lookup"><span data-stu-id="28ee9-123">The virtual wan object.</span></span>

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

### <span data-ttu-id="28ee9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28ee9-124">CommonParameters</span></span>
<span data-ttu-id="28ee9-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28ee9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28ee9-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28ee9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28ee9-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="28ee9-127">INPUTS</span></span>

### <span data-ttu-id="28ee9-128">System.String</span><span class="sxs-lookup"><span data-stu-id="28ee9-128">System.String</span></span>
<span data-ttu-id="28ee9-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="28ee9-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="28ee9-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="28ee9-130">OUTPUTS</span></span>

### <span data-ttu-id="28ee9-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span><span class="sxs-lookup"><span data-stu-id="28ee9-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="28ee9-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="28ee9-132">NOTES</span></span>

## <span data-ttu-id="28ee9-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="28ee9-133">RELATED LINKS</span></span>
