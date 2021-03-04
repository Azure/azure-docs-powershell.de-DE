---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
ms.openlocfilehash: 0d669aca3eaf330322ff814f51bd0c412400f457
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925459"
---
# <span data-ttu-id="0ab92-101">Get-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ab92-101">Get-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="0ab92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ab92-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab92-103">Ruft eine vorhandene VpnServerConfiguration für die Punkt-zu-Website-Konnektivität ab.</span><span class="sxs-lookup"><span data-stu-id="0ab92-103">Gets an existing VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="0ab92-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ab92-104">SYNTAX</span></span>

### <span data-ttu-id="0ab92-105">ListBySubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="0ab92-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnServerConfiguration [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ab92-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ab92-106">ListByResourceGroupName</span></span>
```
Get-AzVpnServerConfiguration [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ab92-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ab92-107">DESCRIPTION</span></span>
<span data-ttu-id="0ab92-108">Das **Get-AzVpnServerConfiguration-Cmdlet** gibt die vorhandene VpnServerConfiguration für die Konnektivität von Punkt auf Website zurück.</span><span class="sxs-lookup"><span data-stu-id="0ab92-108">The **Get-AzVpnServerConfiguration** cmdlet returns the existing VpnServerConfiguration for Point to site connectivity.</span></span>

## <span data-ttu-id="0ab92-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0ab92-109">EXAMPLES</span></span>

### <span data-ttu-id="0ab92-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0ab92-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name test1config

ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2, OpenVPN}
VpnAuthenticationTypes       : {Certificate}
VpnClientRootCertificates    :
VpnClientRevokedCertificates : [
                                 {
                                   "Name": "cert2",
                                   "Thumbprint": "83FFBFC8848B5A5836C94D0112367E16148A286F"
                                 }
                               ]
RadiusServerAddress          :
RadiusServerRootCertificates : []
RadiusClientRootCertificates : []
VpnClientIpsecPolicies       : []
AadAuthenticationParameters  : null
P2sVpnGateways               : []
Type                         : Microsoft.Network/vpnServerConfigurations
ProvisioningState            : Succeeded
```

<span data-ttu-id="0ab92-111">Der obige Befehl wird die vorhandene VpnServerConfiguration erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ab92-111">The above command will get the existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="0ab92-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0ab92-112">PARAMETERS</span></span>

### <span data-ttu-id="0ab92-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ab92-113">-DefaultProfile</span></span>
<span data-ttu-id="0ab92-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ab92-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ab92-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0ab92-115">-Name</span></span>
<span data-ttu-id="0ab92-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="0ab92-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnServerConfigurationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab92-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ab92-117">-ResourceGroupName</span></span>
<span data-ttu-id="0ab92-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0ab92-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab92-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab92-119">CommonParameters</span></span>
<span data-ttu-id="0ab92-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ab92-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab92-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ab92-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab92-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0ab92-122">INPUTS</span></span>

### <span data-ttu-id="0ab92-123">Keine</span><span class="sxs-lookup"><span data-stu-id="0ab92-123">None</span></span>

## <span data-ttu-id="0ab92-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0ab92-124">OUTPUTS</span></span>

### <span data-ttu-id="0ab92-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ab92-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="0ab92-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0ab92-126">NOTES</span></span>

## <span data-ttu-id="0ab92-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0ab92-127">RELATED LINKS</span></span>
