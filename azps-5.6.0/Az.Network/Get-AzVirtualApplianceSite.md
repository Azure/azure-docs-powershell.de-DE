---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
ms.openlocfilehash: 62e549ef01f77382226eaf83784add7005516230
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950720"
---
# <span data-ttu-id="a030a-101">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="a030a-101">Get-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="a030a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a030a-102">SYNOPSIS</span></span>
<span data-ttu-id="a030a-103">Erstellen oder Auflisten von Websites, die mit Ressourcen der virtuellen Netzwerkgeräte verbunden sind</span><span class="sxs-lookup"><span data-stu-id="a030a-103">Get or List sites connected to Network Virtual Appliance resource(s).</span></span>

## <span data-ttu-id="a030a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a030a-104">SYNTAX</span></span>

### <span data-ttu-id="a030a-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a030a-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzVirtualApplianceSite [-Name <String>] [-NetworkVirtualApplianceId <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a030a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a030a-106">ResourceIdParameterSet</span></span>
```
Get-AzVirtualApplianceSite -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a030a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a030a-107">DESCRIPTION</span></span>
<span data-ttu-id="a030a-108">Die Get-AzVirtualApplianceSite ruft Websites ab oder listet Websites auf, die mit einer oder mehreren Ressourcen der virtuellen Netzwerkgeräte verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="a030a-108">The Get-AzVirtualApplianceSite gets or lists sites connected to one or more Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="a030a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a030a-109">EXAMPLES</span></span>

### <span data-ttu-id="a030a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a030a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -Name testsite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite
```

<span data-ttu-id="a030a-111">Holen Sie sich eine Virtual Appliance-Websiteressource.</span><span class="sxs-lookup"><span data-stu-id="a030a-111">Get a Virtual Appliance site resource.</span></span>

### <span data-ttu-id="a030a-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a030a-112">Example 2</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite

AddressPrefix     : 10.0.2.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite2
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite2
```

<span data-ttu-id="a030a-113">Listen Sie ressourcen der virtuellen Appliance in einer virtuellen Netzwerkgerät auf.</span><span class="sxs-lookup"><span data-stu-id="a030a-113">List Virtual Appliance site resources in a Network Virtual Appliance.</span></span>


## <span data-ttu-id="a030a-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a030a-114">PARAMETERS</span></span>

### <span data-ttu-id="a030a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a030a-115">-DefaultProfile</span></span>
<span data-ttu-id="a030a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a030a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a030a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a030a-117">-Name</span></span>
<span data-ttu-id="a030a-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="a030a-118">The resource name.</span></span>

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

### <span data-ttu-id="a030a-119">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="a030a-119">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="a030a-120">Die virtuelle Netzwerkgerät, der die Website angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="a030a-120">The Network Virtual Appliance that the site is attached.</span></span>

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

### <span data-ttu-id="a030a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a030a-121">-ResourceGroupName</span></span>
<span data-ttu-id="a030a-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a030a-122">The resource group name.</span></span>

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

### <span data-ttu-id="a030a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a030a-123">-ResourceId</span></span>
<span data-ttu-id="a030a-124">Die Ressourcen-ID der Virtuellen Gerätewebsite.</span><span class="sxs-lookup"><span data-stu-id="a030a-124">The resource Id of the Virtual Appliance Site.</span></span>

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

### <span data-ttu-id="a030a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a030a-125">CommonParameters</span></span>
<span data-ttu-id="a030a-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a030a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a030a-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a030a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a030a-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a030a-128">INPUTS</span></span>

### <span data-ttu-id="a030a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a030a-129">System.String</span></span>

## <span data-ttu-id="a030a-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a030a-130">OUTPUTS</span></span>

### <span data-ttu-id="a030a-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="a030a-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="a030a-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a030a-132">NOTES</span></span>

## <span data-ttu-id="a030a-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a030a-133">RELATED LINKS</span></span>
