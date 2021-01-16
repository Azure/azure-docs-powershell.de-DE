---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
ms.openlocfilehash: b21fe2cc51668548d4fedc8eb6fc9404d5626a41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296639"
---
# <span data-ttu-id="bca70-101">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="bca70-101">Get-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="bca70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bca70-102">SYNOPSIS</span></span>
<span data-ttu-id="bca70-103">Erstellen oder Auflisten von Websites, die mit Ressourcen des virtuellen Geräts (Network Virtual Appliance) verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="bca70-103">Get or List sites connected to Network Virtual Appliance resource(s).</span></span>

## <span data-ttu-id="bca70-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bca70-104">SYNTAX</span></span>

### <span data-ttu-id="bca70-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bca70-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzVirtualApplianceSite [-Name <String>] [-NetworkVirtualApplianceId <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bca70-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bca70-106">ResourceIdParameterSet</span></span>
```
Get-AzVirtualApplianceSite -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bca70-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bca70-107">DESCRIPTION</span></span>
<span data-ttu-id="bca70-108">Die Get-AzVirtualApplianceSite ruft Websites ab oder listet Websites auf, die mit einer oder mehreren Ressourcen für virtuelle Network Appliance verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="bca70-108">The Get-AzVirtualApplianceSite gets or lists sites connected to one or more Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="bca70-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bca70-109">EXAMPLES</span></span>

### <span data-ttu-id="bca70-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bca70-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -Name testsite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite
```

<span data-ttu-id="bca70-111">Holen Sie sich eine Websiteressource für virtuelle Geräte.</span><span class="sxs-lookup"><span data-stu-id="bca70-111">Get a Virtual Appliance site resource.</span></span>

### <span data-ttu-id="bca70-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bca70-112">Example 2</span></span>
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

<span data-ttu-id="bca70-113">Listen Sie Ressourcen für virtuelle Geräte in einer virtuellen Network Appliance auf.</span><span class="sxs-lookup"><span data-stu-id="bca70-113">List Virtual Appliance site resources in a Network Virtual Appliance.</span></span>


## <span data-ttu-id="bca70-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bca70-114">PARAMETERS</span></span>

### <span data-ttu-id="bca70-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bca70-115">-DefaultProfile</span></span>
<span data-ttu-id="bca70-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bca70-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bca70-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bca70-117">-Name</span></span>
<span data-ttu-id="bca70-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="bca70-118">The resource name.</span></span>

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

### <span data-ttu-id="bca70-119">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="bca70-119">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="bca70-120">Die virtuelle Network Appliance, an die die Website angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="bca70-120">The Network Virtual Appliance that the site is attached.</span></span>

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

### <span data-ttu-id="bca70-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bca70-121">-ResourceGroupName</span></span>
<span data-ttu-id="bca70-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bca70-122">The resource group name.</span></span>

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

### <span data-ttu-id="bca70-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bca70-123">-ResourceId</span></span>
<span data-ttu-id="bca70-124">Die Ressourcen-ID der Website des virtuellen Geräts.</span><span class="sxs-lookup"><span data-stu-id="bca70-124">The resource Id of the Virtual Appliance Site.</span></span>

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

### <span data-ttu-id="bca70-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bca70-125">CommonParameters</span></span>
<span data-ttu-id="bca70-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bca70-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bca70-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bca70-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bca70-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bca70-128">INPUTS</span></span>

### <span data-ttu-id="bca70-129">System.String</span><span class="sxs-lookup"><span data-stu-id="bca70-129">System.String</span></span>

## <span data-ttu-id="bca70-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bca70-130">OUTPUTS</span></span>

### <span data-ttu-id="bca70-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="bca70-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="bca70-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bca70-132">NOTES</span></span>

## <span data-ttu-id="bca70-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bca70-133">RELATED LINKS</span></span>
