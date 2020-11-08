---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 657ffd65bd6dd477700002862060b931979de456
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165790"
---
# <span data-ttu-id="974a2-101">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="974a2-101">Get-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="974a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="974a2-102">SYNOPSIS</span></span>
<span data-ttu-id="974a2-103">Abrufen oder auflisten virtueller Netzwerk-Appliances.</span><span class="sxs-lookup"><span data-stu-id="974a2-103">Get or List Network Virtual Appliances.</span></span>

## <span data-ttu-id="974a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="974a2-104">SYNTAX</span></span>

### <span data-ttu-id="974a2-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="974a2-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzNetworkVirtualAppliance [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="974a2-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="974a2-106">ResourceIdParameterSet</span></span>
```
Get-AzNetworkVirtualAppliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="974a2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="974a2-107">DESCRIPTION</span></span>
<span data-ttu-id="974a2-108">Die Get-AzNetworkVirtualAppliance-Befehle ruft Netzwerk-Virtual Appliance-Ressourcen ab oder listet Sie auf.</span><span class="sxs-lookup"><span data-stu-id="974a2-108">The Get-AzNetworkVirtualAppliance commands gets or lists Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="974a2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="974a2-109">EXAMPLES</span></span>

### <span data-ttu-id="974a2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="974a2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva                                                                                                                      

BootStrapConfigurationBlobs : {}
VirtualHub                  : Microsoft.Azure.Commands.Network.Models.PSResourceId
CloudInitConfigurationBlobs : {}
CloudInitConfiguration      : echo hi
VirtualApplianceAsn         : 1270
VirtualApplianceNics        : {privatenicipconfig, publicnicipconfig, privatenicipconfig, publicnicipconfig}
VirtualApplianceSites       : {}
ProvisioningState           : Succeeded
Identity                    :
NvaSku                      : Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
ResourceGroupName           : testrg
Location                    : eastus2
ResourceGuid                :
Type                        : Microsoft.Network/NetworkVirtualAppliances
Tag                         :
TagsTable                   :
Name                        : nva
Etag                        : 00000000-0000-0000-0000-000000000000
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva
```

<span data-ttu-id="974a2-111">Abrufen einer virtuellen Netzwerk-Appliance-Ressource.</span><span class="sxs-lookup"><span data-stu-id="974a2-111">Get a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="974a2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="974a2-112">PARAMETERS</span></span>

### <span data-ttu-id="974a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="974a2-113">-DefaultProfile</span></span>
<span data-ttu-id="974a2-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="974a2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="974a2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="974a2-115">-Name</span></span>
<span data-ttu-id="974a2-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="974a2-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="974a2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="974a2-117">-ResourceGroupName</span></span>
<span data-ttu-id="974a2-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="974a2-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="974a2-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="974a2-119">-ResourceId</span></span>
<span data-ttu-id="974a2-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="974a2-120">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="974a2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="974a2-121">CommonParameters</span></span>
<span data-ttu-id="974a2-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="974a2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="974a2-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="974a2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="974a2-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="974a2-124">INPUTS</span></span>

### <span data-ttu-id="974a2-125">System. String</span><span class="sxs-lookup"><span data-stu-id="974a2-125">System.String</span></span>

## <span data-ttu-id="974a2-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="974a2-126">OUTPUTS</span></span>

### <span data-ttu-id="974a2-127">Microsoft. Azure. Commands. Network. Models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="974a2-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="974a2-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="974a2-128">NOTES</span></span>

## <span data-ttu-id="974a2-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="974a2-129">RELATED LINKS</span></span>
