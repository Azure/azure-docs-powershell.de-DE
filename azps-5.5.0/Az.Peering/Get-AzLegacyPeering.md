---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azlegacypeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
ms.openlocfilehash: e7b5ef8ef41c66cc3c19fd5ebdcfd53ddcc6f3a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153924"
---
# <span data-ttu-id="36c1f-101">Get-AzLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="36c1f-101">Get-AzLegacyPeering</span></span>

## <span data-ttu-id="36c1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="36c1f-103">Wird verwendet, um ältere Peeringressourcen in Ressourcen der Azure Resource Management (ARM) zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="36c1f-103">Used to Convert Legacy Peering resources to Azure Resource Management (ARM) Resources.</span></span> 

## <span data-ttu-id="36c1f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36c1f-104">SYNTAX</span></span>

```
Get-AzLegacyPeering [-PeeringLocation] <String> [-Kind] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36c1f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36c1f-105">DESCRIPTION</span></span>
<span data-ttu-id="36c1f-106">Der Befehl wird verwendet, um ältere Peeringressourcen zu sehen, die alle Von Ihnen zum Konvertieren in Azure-Ressourcenverwaltungsressourcen (ARM) verwenden.</span><span class="sxs-lookup"><span data-stu-id="36c1f-106">The command is used to view legacy Peering resources which all you to convert them to Azure Resource Management (ARM) Resources.</span></span>

## <span data-ttu-id="36c1f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="36c1f-107">EXAMPLES</span></span>

### <span data-ttu-id="36c1f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="36c1f-108">Example 1</span></span>
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

<span data-ttu-id="36c1f-109">Ruft das alte Peering für Seattle ab.</span><span class="sxs-lookup"><span data-stu-id="36c1f-109">Gets the legacy peering for Seattle</span></span>

## <span data-ttu-id="36c1f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36c1f-110">PARAMETERS</span></span>

### <span data-ttu-id="36c1f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36c1f-111">-DefaultProfile</span></span>
<span data-ttu-id="36c1f-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36c1f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36c1f-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="36c1f-113">-Kind</span></span>
<span data-ttu-id="36c1f-114">Zeigt alle Peeringressourcen nach Art an.</span><span class="sxs-lookup"><span data-stu-id="36c1f-114">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="36c1f-115">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="36c1f-115">-PeeringLocation</span></span>
<span data-ttu-id="36c1f-116">Zeigt alle Peeringressourcen nach Art an.</span><span class="sxs-lookup"><span data-stu-id="36c1f-116">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="36c1f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36c1f-117">CommonParameters</span></span>
<span data-ttu-id="36c1f-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36c1f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36c1f-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36c1f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36c1f-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="36c1f-120">INPUTS</span></span>

### <span data-ttu-id="36c1f-121">Keine</span><span class="sxs-lookup"><span data-stu-id="36c1f-121">None</span></span>

## <span data-ttu-id="36c1f-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="36c1f-122">OUTPUTS</span></span>

### <span data-ttu-id="36c1f-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="36c1f-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="36c1f-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="36c1f-124">NOTES</span></span>

## <span data-ttu-id="36c1f-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="36c1f-125">RELATED LINKS</span></span>
