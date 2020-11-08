---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
ms.openlocfilehash: 47450d65b883f23bda8141df6be0eb11bc0fa908
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005060"
---
# <span data-ttu-id="7b3db-101">Get-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b3db-101">Get-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="7b3db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b3db-102">SYNOPSIS</span></span>
<span data-ttu-id="7b3db-103">Ruft eine vorhandene VpnServerConfiguration für Point-to-Site-Konnektivität ab.</span><span class="sxs-lookup"><span data-stu-id="7b3db-103">Gets an existing VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="7b3db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b3db-104">SYNTAX</span></span>

### <span data-ttu-id="7b3db-105">ListBySubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="7b3db-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnServerConfiguration [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b3db-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b3db-106">ListByResourceGroupName</span></span>
```
Get-AzVpnServerConfiguration [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b3db-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b3db-107">DESCRIPTION</span></span>
<span data-ttu-id="7b3db-108">Das Cmdlet " **Get-AzVpnServerConfiguration** " gibt die vorhandene VpnServerConfiguration für Point-to-Site-Konnektivität zurück.</span><span class="sxs-lookup"><span data-stu-id="7b3db-108">The **Get-AzVpnServerConfiguration** cmdlet returns the existing VpnServerConfiguration for Point to site connectivity.</span></span>

## <span data-ttu-id="7b3db-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b3db-109">EXAMPLES</span></span>

### <span data-ttu-id="7b3db-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7b3db-110">Example 1</span></span>
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

<span data-ttu-id="7b3db-111">Der obige Befehl erhält die vorhandene VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7b3db-111">The above command will get the existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="7b3db-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b3db-112">PARAMETERS</span></span>

### <span data-ttu-id="7b3db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b3db-113">-DefaultProfile</span></span>
<span data-ttu-id="7b3db-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7b3db-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b3db-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7b3db-115">-Name</span></span>
<span data-ttu-id="7b3db-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="7b3db-116">The resource name.</span></span>

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

### <span data-ttu-id="7b3db-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b3db-117">-ResourceGroupName</span></span>
<span data-ttu-id="7b3db-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7b3db-118">The resource group name.</span></span>

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

### <span data-ttu-id="7b3db-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b3db-119">CommonParameters</span></span>
<span data-ttu-id="7b3db-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b3db-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b3db-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b3db-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b3db-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b3db-122">INPUTS</span></span>

### <span data-ttu-id="7b3db-123">Keine</span><span class="sxs-lookup"><span data-stu-id="7b3db-123">None</span></span>

## <span data-ttu-id="7b3db-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b3db-124">OUTPUTS</span></span>

### <span data-ttu-id="7b3db-125">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b3db-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="7b3db-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b3db-126">NOTES</span></span>

## <span data-ttu-id="7b3db-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b3db-127">RELATED LINKS</span></span>
