---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
ms.openlocfilehash: d01919008adf8c15fa9b4a0c8144e279a3997a92
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162297"
---
# <span data-ttu-id="0f868-101">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0f868-101">Get-AzAvailabilitySet</span></span>

## <span data-ttu-id="0f868-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f868-102">SYNOPSIS</span></span>
<span data-ttu-id="0f868-103">Ruft Die Verfügbarkeitssätze von Azure in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="0f868-103">Gets Azure availability sets in a resource group.</span></span>

## <span data-ttu-id="0f868-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f868-104">SYNTAX</span></span>

```
Get-AzAvailabilitySet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f868-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f868-105">DESCRIPTION</span></span>
<span data-ttu-id="0f868-106">Das **Cmdlet "Get-AzAvailabilitySet"** ruft Die Verfügbarkeitssätze von Azure in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="0f868-106">The **Get-AzAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="0f868-107">Sie können den Namen eines bestimmten Verfügbarkeitssets angeben, den Sie erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="0f868-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="0f868-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0f868-108">EXAMPLES</span></span>

### <span data-ttu-id="0f868-109">Beispiel 1: Einen bestimmten Verfügbarkeitssatz erhalten</span><span class="sxs-lookup"><span data-stu-id="0f868-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="0f868-110">Dieser Befehl ruft den Verfügbarkeitssatz namens "AvailabilitySet03" in der Ressourcengruppe mit dem Namen "ResourceGroup11" ab.</span><span class="sxs-lookup"><span data-stu-id="0f868-110">This command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="0f868-111">Beispiel 2: Alle Verfügbarkeitssätze erhalten</span><span class="sxs-lookup"><span data-stu-id="0f868-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet10
Name                      : AvailabilitySet10
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="0f868-112">Dieser Befehl ruft alle Verfügbarkeitssätze in der Ressourcengruppe mit dem Namen "ResourceGroup11" ab.</span><span class="sxs-lookup"><span data-stu-id="0f868-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="0f868-113">Beispiel 3: Erhalten aller Verfügbarkeitssätze mit Filterung</span><span class="sxs-lookup"><span data-stu-id="0f868-113">Example 3: Get all availability sets with filtering</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup1*" -Name "AvailabilitySet0*"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="0f868-114">Dieser Befehl ruft alle Verfügbarkeitssätze in der Ressourcengruppe mit dem Namen "ResourceGroup11" ab, die mit "AvailabilitySet0" beginnen.</span><span class="sxs-lookup"><span data-stu-id="0f868-114">This command gets all the availability sets in the resource group named ResourceGroup11 that start with "AvailabilitySet0".</span></span>

### <span data-ttu-id="0f868-115">Beispiel 4: Alle Verfügbarkeitssätze mit Name ab "AvailabilitySet0" erhalten</span><span class="sxs-lookup"><span data-stu-id="0f868-115">Example 4: Get all availability sets with name starting with AvailabilitySet0</span></span>
```
PS C:\> Get-AzAvailabilitySet -Name AvailabilitySet0*

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup12
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup12/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="0f868-116">Dieser Befehl ruft alle Verfügbarkeitssätze ab, die mit "AvailabilitySet0" beginnen.</span><span class="sxs-lookup"><span data-stu-id="0f868-116">This command gets all the availability sets that start with "AvailabilitySet0".</span></span>

## <span data-ttu-id="0f868-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f868-117">PARAMETERS</span></span>

### <span data-ttu-id="0f868-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f868-118">-DefaultProfile</span></span>
<span data-ttu-id="0f868-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0f868-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f868-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0f868-120">-Name</span></span>
<span data-ttu-id="0f868-121">Gibt den Namen eines Verfügbarkeitssets an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="0f868-121">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0f868-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f868-122">-ResourceGroupName</span></span>
<span data-ttu-id="0f868-123">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0f868-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0f868-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f868-124">CommonParameters</span></span>
<span data-ttu-id="0f868-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f868-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f868-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f868-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f868-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0f868-127">INPUTS</span></span>

### <span data-ttu-id="0f868-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0f868-128">System.String</span></span>

## <span data-ttu-id="0f868-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0f868-129">OUTPUTS</span></span>

### <span data-ttu-id="0f868-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0f868-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="0f868-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0f868-131">NOTES</span></span>

## <span data-ttu-id="0f868-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0f868-132">RELATED LINKS</span></span>

[<span data-ttu-id="0f868-133">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0f868-133">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

[<span data-ttu-id="0f868-134">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0f868-134">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


