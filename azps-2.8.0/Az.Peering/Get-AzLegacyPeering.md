---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azlegacypeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
ms.openlocfilehash: 9a2fcb87b05d4478ab7b3e3490feae92fd727ce7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824052"
---
# <span data-ttu-id="5da48-101">Get-AzLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="5da48-101">Get-AzLegacyPeering</span></span>

## <span data-ttu-id="5da48-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5da48-102">SYNOPSIS</span></span>
<span data-ttu-id="5da48-103">Wird verwendet, um Legacy-Peering Ressourcen in Azure Resource Management (Arm)-Ressourcen umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="5da48-103">Used to Convert Legacy Peering resources to Azure Resource Management (ARM) Resources.</span></span> 

## <span data-ttu-id="5da48-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5da48-104">SYNTAX</span></span>

```
Get-AzLegacyPeering [-PeeringLocation] <String> [-Kind] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5da48-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5da48-105">DESCRIPTION</span></span>
<span data-ttu-id="5da48-106">Der Befehl wird verwendet, um Legacy-Peering Ressourcen anzuzeigen, die Sie alle in Azure Resource Management (Arm)-Ressourcen konvertieren können.</span><span class="sxs-lookup"><span data-stu-id="5da48-106">The command is used to view legacy Peering resources which all you to convert them to Azure Resource Management (ARM) Resources.</span></span>

## <span data-ttu-id="5da48-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5da48-107">EXAMPLES</span></span>

### <span data-ttu-id="5da48-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5da48-108">Example 1</span></span>
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

<span data-ttu-id="5da48-109">Ruft das Legacy-Peering für Seattle ab</span><span class="sxs-lookup"><span data-stu-id="5da48-109">Gets the legacy peering for Seattle</span></span>

## <span data-ttu-id="5da48-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5da48-110">PARAMETERS</span></span>

### <span data-ttu-id="5da48-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5da48-111">-DefaultProfile</span></span>
<span data-ttu-id="5da48-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5da48-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5da48-113">-Art</span><span class="sxs-lookup"><span data-stu-id="5da48-113">-Kind</span></span>
<span data-ttu-id="5da48-114">Zeigt alle Peering-Ressourcen nach Art.</span><span class="sxs-lookup"><span data-stu-id="5da48-114">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="5da48-115">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="5da48-115">-PeeringLocation</span></span>
<span data-ttu-id="5da48-116">Zeigt alle Peering-Ressourcen nach Art.</span><span class="sxs-lookup"><span data-stu-id="5da48-116">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="5da48-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da48-117">CommonParameters</span></span>
<span data-ttu-id="5da48-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5da48-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da48-119">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5da48-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da48-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5da48-120">INPUTS</span></span>

### <span data-ttu-id="5da48-121">Keine</span><span class="sxs-lookup"><span data-stu-id="5da48-121">None</span></span>

## <span data-ttu-id="5da48-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5da48-122">OUTPUTS</span></span>

### <span data-ttu-id="5da48-123">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="5da48-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="5da48-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="5da48-124">NOTES</span></span>

## <span data-ttu-id="5da48-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5da48-125">RELATED LINKS</span></span>
