---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: 6124b3ddb862254d11bd141560a682bb91bb7fb7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009123"
---
# <span data-ttu-id="d96d3-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d96d3-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="d96d3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d96d3-102">SYNOPSIS</span></span>
<span data-ttu-id="d96d3-103">Ruft die Liste aller VpnServerConfigurations ab, die diesem VirtualWan zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d96d3-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="d96d3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d96d3-104">SYNTAX</span></span>

### <span data-ttu-id="d96d3-105">ByVirtualWanName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d96d3-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d96d3-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="d96d3-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d96d3-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="d96d3-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d96d3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d96d3-108">DESCRIPTION</span></span>
<span data-ttu-id="d96d3-109">Das Cmdlet " **Get-AzVirtualWanVpnServerConfiguration** " gibt die Liste aller VpnServerConfigurations zurück, die diesem VirtualWan zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d96d3-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="d96d3-110">dh alle VpnServerConfigurations, die mit einem P2SVpnGateways unter VirutalHubs dieser VirtualWan verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="d96d3-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="d96d3-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d96d3-111">EXAMPLES</span></span>

### <span data-ttu-id="d96d3-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d96d3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="d96d3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d96d3-113">PARAMETERS</span></span>

### <span data-ttu-id="d96d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d96d3-114">-DefaultProfile</span></span>
<span data-ttu-id="d96d3-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d96d3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d96d3-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d96d3-116">-Name</span></span>
<span data-ttu-id="d96d3-117">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="d96d3-117">The resource name.</span></span>

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

### <span data-ttu-id="d96d3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d96d3-118">-ResourceGroupName</span></span>
<span data-ttu-id="d96d3-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d96d3-119">The resource group name.</span></span>

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

### <span data-ttu-id="d96d3-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d96d3-120">-ResourceId</span></span>
<span data-ttu-id="d96d3-121">Die Azure-Ressourcen-ID für das virtuelle WAN.</span><span class="sxs-lookup"><span data-stu-id="d96d3-121">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="d96d3-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="d96d3-122">-VirtualWanObject</span></span>
<span data-ttu-id="d96d3-123">Das virtuelle WAN-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d96d3-123">The virtual wan object.</span></span>

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

### <span data-ttu-id="d96d3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d96d3-124">CommonParameters</span></span>
<span data-ttu-id="d96d3-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d96d3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d96d3-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d96d3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d96d3-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d96d3-127">INPUTS</span></span>

### <span data-ttu-id="d96d3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d96d3-128">System.String</span></span>
<span data-ttu-id="d96d3-129">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="d96d3-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="d96d3-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d96d3-130">OUTPUTS</span></span>

### <span data-ttu-id="d96d3-131">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfigurationsResponse</span><span class="sxs-lookup"><span data-stu-id="d96d3-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="d96d3-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="d96d3-132">NOTES</span></span>

## <span data-ttu-id="d96d3-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d96d3-133">RELATED LINKS</span></span>
