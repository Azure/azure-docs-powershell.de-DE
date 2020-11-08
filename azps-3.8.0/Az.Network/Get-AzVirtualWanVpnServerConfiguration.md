---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: de25e096be96e54d2a8aa18f24bf9915a2f16538
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003752"
---
# <span data-ttu-id="60b3e-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="60b3e-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="60b3e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="60b3e-103">Ruft die Liste aller VpnServerConfigurations ab, die diesem VirtualWan zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="60b3e-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="60b3e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60b3e-104">SYNTAX</span></span>

### <span data-ttu-id="60b3e-105">ByVirtualWanName (Standard)</span><span class="sxs-lookup"><span data-stu-id="60b3e-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60b3e-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="60b3e-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60b3e-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="60b3e-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60b3e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60b3e-108">DESCRIPTION</span></span>
<span data-ttu-id="60b3e-109">Das Cmdlet " **Get-AzVirtualWanVpnServerConfiguration** " gibt die Liste aller VpnServerConfigurations zurück, die diesem VirtualWan zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="60b3e-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="60b3e-110">dh alle VpnServerConfigurations, die mit einem P2SVpnGateways unter VirutalHubs dieser VirtualWan verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="60b3e-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="60b3e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60b3e-111">EXAMPLES</span></span>

### <span data-ttu-id="60b3e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="60b3e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="60b3e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="60b3e-113">PARAMETERS</span></span>

### <span data-ttu-id="60b3e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60b3e-114">-DefaultProfile</span></span>
<span data-ttu-id="60b3e-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="60b3e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60b3e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="60b3e-116">-Name</span></span>
<span data-ttu-id="60b3e-117">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="60b3e-117">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60b3e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60b3e-118">-ResourceGroupName</span></span>
<span data-ttu-id="60b3e-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="60b3e-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60b3e-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="60b3e-120">-ResourceId</span></span>
<span data-ttu-id="60b3e-121">Die Azure-Ressourcen-ID für das virtuelle WAN.</span><span class="sxs-lookup"><span data-stu-id="60b3e-121">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60b3e-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="60b3e-122">-VirtualWanObject</span></span>
<span data-ttu-id="60b3e-123">Das virtuelle WAN-Objekt.</span><span class="sxs-lookup"><span data-stu-id="60b3e-123">The virtual wan object.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60b3e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60b3e-124">CommonParameters</span></span>
<span data-ttu-id="60b3e-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60b3e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60b3e-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60b3e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60b3e-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60b3e-127">INPUTS</span></span>

### <span data-ttu-id="60b3e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="60b3e-128">System.String</span></span>
<span data-ttu-id="60b3e-129">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="60b3e-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="60b3e-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60b3e-130">OUTPUTS</span></span>

### <span data-ttu-id="60b3e-131">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfigurationsResponse</span><span class="sxs-lookup"><span data-stu-id="60b3e-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="60b3e-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="60b3e-132">NOTES</span></span>

## <span data-ttu-id="60b3e-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60b3e-133">RELATED LINKS</span></span>
