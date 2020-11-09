---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
ms.openlocfilehash: b21fe2cc51668548d4fedc8eb6fc9404d5626a41
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301990"
---
# <span data-ttu-id="84a8d-101">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="84a8d-101">Get-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="84a8d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="84a8d-102">SYNOPSIS</span></span>
<span data-ttu-id="84a8d-103">Abrufen oder Auflisten von Websites, die mit der Virtual Appliance-Ressource (n) verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="84a8d-103">Get or List sites connected to Network Virtual Appliance resource(s).</span></span>

## <span data-ttu-id="84a8d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="84a8d-104">SYNTAX</span></span>

### <span data-ttu-id="84a8d-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="84a8d-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzVirtualApplianceSite [-Name <String>] [-NetworkVirtualApplianceId <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84a8d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84a8d-106">ResourceIdParameterSet</span></span>
```
Get-AzVirtualApplianceSite -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84a8d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84a8d-107">DESCRIPTION</span></span>
<span data-ttu-id="84a8d-108">Die Get-AzVirtualApplianceSite ruft Websites auf, die mit mindestens einer Netzwerk-Virtual Appliance-Ressource verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="84a8d-108">The Get-AzVirtualApplianceSite gets or lists sites connected to one or more Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="84a8d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="84a8d-109">EXAMPLES</span></span>

### <span data-ttu-id="84a8d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="84a8d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -Name testsite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite
```

<span data-ttu-id="84a8d-111">Abrufen einer virtuellen Appliance-Website Ressource</span><span class="sxs-lookup"><span data-stu-id="84a8d-111">Get a Virtual Appliance site resource.</span></span>

### <span data-ttu-id="84a8d-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="84a8d-112">Example 2</span></span>
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

<span data-ttu-id="84a8d-113">Listen Sie Virtual Appliance-Website Ressourcen in einer virtuellen Netzwerkanwendung auf.</span><span class="sxs-lookup"><span data-stu-id="84a8d-113">List Virtual Appliance site resources in a Network Virtual Appliance.</span></span>


## <span data-ttu-id="84a8d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="84a8d-114">PARAMETERS</span></span>

### <span data-ttu-id="84a8d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84a8d-115">-DefaultProfile</span></span>
<span data-ttu-id="84a8d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="84a8d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84a8d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="84a8d-117">-Name</span></span>
<span data-ttu-id="84a8d-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="84a8d-118">The resource name.</span></span>

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

### <span data-ttu-id="84a8d-119">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="84a8d-119">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="84a8d-120">Die virtuelle Netzwerk-Appliance, an die die Website angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="84a8d-120">The Network Virtual Appliance that the site is attached.</span></span>

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

### <span data-ttu-id="84a8d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84a8d-121">-ResourceGroupName</span></span>
<span data-ttu-id="84a8d-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="84a8d-122">The resource group name.</span></span>

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

### <span data-ttu-id="84a8d-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="84a8d-123">-ResourceId</span></span>
<span data-ttu-id="84a8d-124">Die Ressourcen-ID der virtuellen Appliance-Website.</span><span class="sxs-lookup"><span data-stu-id="84a8d-124">The resource Id of the Virtual Appliance Site.</span></span>

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

### <span data-ttu-id="84a8d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84a8d-125">CommonParameters</span></span>
<span data-ttu-id="84a8d-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84a8d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84a8d-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84a8d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84a8d-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="84a8d-128">INPUTS</span></span>

### <span data-ttu-id="84a8d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="84a8d-129">System.String</span></span>

## <span data-ttu-id="84a8d-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="84a8d-130">OUTPUTS</span></span>

### <span data-ttu-id="84a8d-131">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="84a8d-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="84a8d-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="84a8d-132">NOTES</span></span>

## <span data-ttu-id="84a8d-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="84a8d-133">RELATED LINKS</span></span>
