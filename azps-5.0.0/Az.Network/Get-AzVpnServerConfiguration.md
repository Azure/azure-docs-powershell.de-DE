---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
ms.openlocfilehash: 47450d65b883f23bda8141df6be0eb11bc0fa908
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178329"
---
# <span data-ttu-id="7cb02-101">Get-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="7cb02-101">Get-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="7cb02-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7cb02-102">SYNOPSIS</span></span>
<span data-ttu-id="7cb02-103">Ruft eine vorhandene VpnServerConfiguration für Point-to-Site-Konnektivität ab.</span><span class="sxs-lookup"><span data-stu-id="7cb02-103">Gets an existing VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="7cb02-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cb02-104">SYNTAX</span></span>

### <span data-ttu-id="7cb02-105">ListBySubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="7cb02-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnServerConfiguration [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cb02-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cb02-106">ListByResourceGroupName</span></span>
```
Get-AzVpnServerConfiguration [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cb02-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7cb02-107">DESCRIPTION</span></span>
<span data-ttu-id="7cb02-108">Das Cmdlet " **Get-AzVpnServerConfiguration** " gibt die vorhandene VpnServerConfiguration für Point-to-Site-Konnektivität zurück.</span><span class="sxs-lookup"><span data-stu-id="7cb02-108">The **Get-AzVpnServerConfiguration** cmdlet returns the existing VpnServerConfiguration for Point to site connectivity.</span></span>

## <span data-ttu-id="7cb02-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7cb02-109">EXAMPLES</span></span>

### <span data-ttu-id="7cb02-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7cb02-110">Example 1</span></span>
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

<span data-ttu-id="7cb02-111">Der obige Befehl erhält die vorhandene VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7cb02-111">The above command will get the existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="7cb02-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7cb02-112">PARAMETERS</span></span>

### <span data-ttu-id="7cb02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cb02-113">-DefaultProfile</span></span>
<span data-ttu-id="7cb02-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7cb02-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cb02-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7cb02-115">-Name</span></span>
<span data-ttu-id="7cb02-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="7cb02-116">The resource name.</span></span>

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

### <span data-ttu-id="7cb02-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cb02-117">-ResourceGroupName</span></span>
<span data-ttu-id="7cb02-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7cb02-118">The resource group name.</span></span>

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

### <span data-ttu-id="7cb02-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cb02-119">CommonParameters</span></span>
<span data-ttu-id="7cb02-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cb02-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cb02-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cb02-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cb02-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7cb02-122">INPUTS</span></span>

### <span data-ttu-id="7cb02-123">Keine</span><span class="sxs-lookup"><span data-stu-id="7cb02-123">None</span></span>

## <span data-ttu-id="7cb02-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7cb02-124">OUTPUTS</span></span>

### <span data-ttu-id="7cb02-125">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="7cb02-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="7cb02-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="7cb02-126">NOTES</span></span>

## <span data-ttu-id="7cb02-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7cb02-127">RELATED LINKS</span></span>
