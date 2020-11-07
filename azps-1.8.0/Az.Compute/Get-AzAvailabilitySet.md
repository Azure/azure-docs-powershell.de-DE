---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
ms.openlocfilehash: 1ebb43f11d0286ca3fef4ab136c9e5a1e6ee031d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661569"
---
# <span data-ttu-id="5011c-101">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5011c-101">Get-AzAvailabilitySet</span></span>

## <span data-ttu-id="5011c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5011c-102">SYNOPSIS</span></span>
<span data-ttu-id="5011c-103">Ruft Azure-Verfügbarkeits Sätze in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="5011c-103">Gets Azure availability sets in a resource group.</span></span>

## <span data-ttu-id="5011c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5011c-104">SYNTAX</span></span>

```
Get-AzAvailabilitySet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5011c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5011c-105">DESCRIPTION</span></span>
<span data-ttu-id="5011c-106">Das Cmdlet " **Get-AzAvailabilitySet** " ruft Azure-Verfügbarkeits Sätze in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="5011c-106">The **Get-AzAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="5011c-107">Sie können den Namen eines bestimmten verfügbaren Verfügbarkeits Satzes angeben, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5011c-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="5011c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5011c-108">EXAMPLES</span></span>

### <span data-ttu-id="5011c-109">Beispiel 1: Abrufen eines bestimmten Verfügbarkeits Satzes</span><span class="sxs-lookup"><span data-stu-id="5011c-109">Example 1: Get a specific availability set</span></span>
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

<span data-ttu-id="5011c-110">Dieser Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="5011c-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="5011c-111">Beispiel 2: Abrufen aller Verfügbarkeits Sätze</span><span class="sxs-lookup"><span data-stu-id="5011c-111">Example 2: Get all availability sets</span></span>
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

<span data-ttu-id="5011c-112">Dieser Befehl ruft alle Verfügbarkeits Sätze in der Ressourcengruppe mit dem Namen ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="5011c-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="5011c-113">Beispiel 3: Abrufen aller Verfügbarkeits Sätze mit Filterung</span><span class="sxs-lookup"><span data-stu-id="5011c-113">Example 3: Get all availability sets with filtering</span></span>
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

<span data-ttu-id="5011c-114">Dieser Befehl ruft alle Verfügbarkeits Sätze in der Ressourcengruppe mit dem Namen "ResourceGroup11" ab, die mit "AvailabilitySet0" beginnen.</span><span class="sxs-lookup"><span data-stu-id="5011c-114">This command gets all the availability sets in the resource group named ResourceGroup11 that start with "AvailabilitySet0".</span></span>

### <span data-ttu-id="5011c-115">Beispiel 4: Abrufen aller Verfügbarkeits Sätze mit dem Namen ab AvailabilitySet0</span><span class="sxs-lookup"><span data-stu-id="5011c-115">Example 4: Get all availability sets with name starting with AvailabilitySet0</span></span>
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

<span data-ttu-id="5011c-116">Dieser Befehl ruft alle Verfügbarkeits Sätze ab, die mit "AvailabilitySet0" beginnen.</span><span class="sxs-lookup"><span data-stu-id="5011c-116">This command gets all the availability sets that start with "AvailabilitySet0".</span></span>

## <span data-ttu-id="5011c-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="5011c-117">PARAMETERS</span></span>

### <span data-ttu-id="5011c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5011c-118">-DefaultProfile</span></span>
<span data-ttu-id="5011c-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5011c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5011c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5011c-120">-Name</span></span>
<span data-ttu-id="5011c-121">Gibt den Namen eines Verfügbarkeits Satzes an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5011c-121">Specifies the name of an availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5011c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5011c-122">-ResourceGroupName</span></span>
<span data-ttu-id="5011c-123">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="5011c-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5011c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5011c-124">CommonParameters</span></span>
<span data-ttu-id="5011c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5011c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5011c-126">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5011c-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5011c-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5011c-127">INPUTS</span></span>

### <span data-ttu-id="5011c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5011c-128">System.String</span></span>

## <span data-ttu-id="5011c-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5011c-129">OUTPUTS</span></span>

### <span data-ttu-id="5011c-130">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5011c-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="5011c-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="5011c-131">NOTES</span></span>

## <span data-ttu-id="5011c-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5011c-132">RELATED LINKS</span></span>

[<span data-ttu-id="5011c-133">Neu – AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5011c-133">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

[<span data-ttu-id="5011c-134">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5011c-134">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


