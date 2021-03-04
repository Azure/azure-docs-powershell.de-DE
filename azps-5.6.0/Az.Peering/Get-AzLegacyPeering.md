---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azlegacypeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
ms.openlocfilehash: 2f1bdfd317a5578c5ce3a023f1c3cd0151026b80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937795"
---
# <span data-ttu-id="6b66a-101">Get-AzLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="6b66a-101">Get-AzLegacyPeering</span></span>

## <span data-ttu-id="6b66a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b66a-102">SYNOPSIS</span></span>
<span data-ttu-id="6b66a-103">Wird verwendet, um Ältere Peeringressourcen in Azure Resource Management (ARM) zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="6b66a-103">Used to Convert Legacy Peering resources to Azure Resource Management (ARM) Resources.</span></span> 

## <span data-ttu-id="6b66a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b66a-104">SYNTAX</span></span>

```
Get-AzLegacyPeering [-PeeringLocation] <String> [-Kind] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b66a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b66a-105">DESCRIPTION</span></span>
<span data-ttu-id="6b66a-106">Mit dem Befehl werden ältere Peeringressourcen angezeigt, die Sie alle zum Konvertieren in Azure Resource Management (ARM) Ressourcen verwenden.</span><span class="sxs-lookup"><span data-stu-id="6b66a-106">The command is used to view legacy Peering resources which all you to convert them to Azure Resource Management (ARM) Resources.</span></span>

## <span data-ttu-id="6b66a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6b66a-107">EXAMPLES</span></span>

### <span data-ttu-id="6b66a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6b66a-108">Example 1</span></span>
```powershell
PS C:> Get-AzLegacyPeering -PeeringLocation "Seattle" -Kind Direct

Name                       :
Sku                        : Basic_Direct_Free
Kind                       : Direct
PeeringLocation            : Seattle
UseForPeeringService       : False
PeerAsn.Id                 :
Connection                 : ------------------------
PeeringDBFacilityId        : 71
SessionPrefixIPv4          : 173.205.50.236/30
PeerSessionIPv4Address     : 173.205.50.237
MicrosoftIPv4Address       : 173.205.50.238
SessionStateV4             : Established
MaxPrefixesAdvertisedV4    : 20000
SessionPrefixIPv6          : 2001:668:0:3:ffff:0:adcd:32ec/126
PeerSessionIPv6Address     : 2001:668:0:3:ffff:0:adcd:32ed
MicrosoftIPv6Address       : 2001:668:0:3:ffff:0:adcd:32ee
SessionStateV6             : Established
MaxPrefixesAdvertisedV6    : 2000
ConnectionState            : Active
BandwidthInMbps            : 0
ProvisionedBandwidthInMbps : 20000
ProvisioningState          : Succeeded
```

<span data-ttu-id="6b66a-109">Ruft das ältere Peering für Seattle ab.</span><span class="sxs-lookup"><span data-stu-id="6b66a-109">Gets the legacy peering for Seattle</span></span>

## <span data-ttu-id="6b66a-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6b66a-110">PARAMETERS</span></span>

### <span data-ttu-id="6b66a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b66a-111">-DefaultProfile</span></span>
<span data-ttu-id="6b66a-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b66a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b66a-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="6b66a-113">-Kind</span></span>
<span data-ttu-id="6b66a-114">Zeigt alle Peeringressourcen nach Art an.</span><span class="sxs-lookup"><span data-stu-id="6b66a-114">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b66a-115">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="6b66a-115">-PeeringLocation</span></span>
<span data-ttu-id="6b66a-116">Zeigt alle Peeringressourcen nach Art an.</span><span class="sxs-lookup"><span data-stu-id="6b66a-116">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b66a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b66a-117">CommonParameters</span></span>
<span data-ttu-id="6b66a-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b66a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b66a-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b66a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b66a-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6b66a-120">INPUTS</span></span>

### <span data-ttu-id="6b66a-121">Keine</span><span class="sxs-lookup"><span data-stu-id="6b66a-121">None</span></span>

## <span data-ttu-id="6b66a-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6b66a-122">OUTPUTS</span></span>

### <span data-ttu-id="6b66a-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="6b66a-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="6b66a-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6b66a-124">NOTES</span></span>

## <span data-ttu-id="6b66a-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6b66a-125">RELATED LINKS</span></span>
