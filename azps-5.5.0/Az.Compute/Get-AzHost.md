---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
ms.openlocfilehash: 692a32372718ee3100bd0ad0038d7ff89d483654
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167913"
---
# <span data-ttu-id="67228-101">Get-AzHost</span><span class="sxs-lookup"><span data-stu-id="67228-101">Get-AzHost</span></span>

## <span data-ttu-id="67228-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67228-102">SYNOPSIS</span></span>
<span data-ttu-id="67228-103">"Get" oder "Listhosts".</span><span class="sxs-lookup"><span data-stu-id="67228-103">Get or list hosts.</span></span>

## <span data-ttu-id="67228-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67228-104">SYNTAX</span></span>

### <span data-ttu-id="67228-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="67228-105">DefaultParameter (Default)</span></span>
```
Get-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67228-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="67228-106">ResourceIdParameter</span></span>
```
Get-AzHost [-ResourceId] <String> [-InstanceView] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67228-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67228-107">DESCRIPTION</span></span>
<span data-ttu-id="67228-108">Dieses Cmdlet bekommt einen Host in einer Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="67228-108">This cmdlet will get a host in a host group.</span></span>
<span data-ttu-id="67228-109">Dieses Cmdlet listet auch alle Hosts in einer Hostgruppe auf, wenn kein Hostname angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="67228-109">This cmdlet also lists all hosts in a host group if a host name is not given.</span></span>

## <span data-ttu-id="67228-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="67228-110">EXAMPLES</span></span>

### <span data-ttu-id="67228-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="67228-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName

ResourceGroupName    : myrg01
PlatformFaultDomain  : 1
AutoReplaceOnFailure : True
HostId               : 00000000-0000-0000-0000-000000000000
VirtualMachines[0]   : 
  Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/virtualMachines/myvm01
VirtualMachines[1]   : 
  Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/virtualMachines/myvm02
ProvisioningTime     : 7/27/2019 3:22:59 AM
ProvisioningState    : Succeeded
Sku                  : 
  Name               : ESv3-Type1
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                 : myhost01
Location             : eastus
Tags                 : {"key1":"val2"}
```

<span data-ttu-id="67228-112">Dieser Befehl gibt einen Host zurück.</span><span class="sxs-lookup"><span data-stu-id="67228-112">This command returns a host.</span></span>

### <span data-ttu-id="67228-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="67228-113">Example 2</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName -InstanceView

ResourceGroupName      : myrg01
PlatformFaultDomain    : 0
AutoReplaceOnFailure   : True
HostId                 : 00000000-0000-0000-0000-000000000000
ProvisioningTime       : 8/19/2019 9:13:19 PM
ProvisioningState      : Succeeded
InstanceView           : 
  AssetId              : 00000000-0000-0000-0000-000000000000
  AvailableCapacity    : 
    AllocatableVMs[0]  : 
      VmSize           : Standard_E2s_v3
      Count            : 28
    AllocatableVMs[1]  : 
      VmSize           : Standard_E4-2s_v3
      Count            : 14
    AllocatableVMs[2]  : 
      VmSize           : Standard_E4s_v3
      Count            : 14
  Statuses[0]          : 
    Code               : ProvisioningState/succeeded
    Level              : Info
    DisplayStatus      : Provisioning succeeded
    Time               : 8/19/2019 9:13:19 PM
  Statuses[1]          : 
    Code               : HealthState/available
    Level              : Info
    DisplayStatus      : Host available
Sku                    : 
  Name                 : ESv3-Type1
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                   : crptestps2264host
Location               : eastus
Tags                   : {"key1":"val2"}
```

<span data-ttu-id="67228-114">Dieser Befehl gibt die Instanzansicht eines Hosts zurück.</span><span class="sxs-lookup"><span data-stu-id="67228-114">This command returns the instance view of a host.</span></span>

### <span data-ttu-id="67228-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="67228-115">Example 3</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName       Name Location           Tags        Sku FD
-----------------       ---- --------           ----        --- --
myrg01              myhost01   eastus {[key1, val2]} ESv3-Type1  0
myrg01              myhost02   eastus {[key1, val2]} ESv3-Type1  1
```

<span data-ttu-id="67228-116">Dieser Befehl gibt alle Hosts in der angegebenen Hostgruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="67228-116">This command returns all hosts in the given host group.</span></span>

## <span data-ttu-id="67228-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67228-117">PARAMETERS</span></span>

### <span data-ttu-id="67228-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67228-118">-DefaultProfile</span></span>
<span data-ttu-id="67228-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67228-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67228-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="67228-120">-HostGroupName</span></span>
<span data-ttu-id="67228-121">Der Name der Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="67228-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67228-122">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="67228-122">-InstanceView</span></span>
<span data-ttu-id="67228-123">Gibt an, dass dieses Cmdlet nur die Instanzansicht des Hosts erhält.</span><span class="sxs-lookup"><span data-stu-id="67228-123">Indicates that this cmdlet gets only the instance view of the host.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67228-124">-Name</span><span class="sxs-lookup"><span data-stu-id="67228-124">-Name</span></span>
<span data-ttu-id="67228-125">Der Name des Hosts.</span><span class="sxs-lookup"><span data-stu-id="67228-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67228-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67228-126">-ResourceGroupName</span></span>
<span data-ttu-id="67228-127">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="67228-127">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67228-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67228-128">-ResourceId</span></span>
<span data-ttu-id="67228-129">Die ID der Ressource.</span><span class="sxs-lookup"><span data-stu-id="67228-129">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67228-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67228-130">CommonParameters</span></span>
<span data-ttu-id="67228-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67228-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67228-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67228-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67228-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="67228-133">INPUTS</span></span>

### <span data-ttu-id="67228-134">System.String</span><span class="sxs-lookup"><span data-stu-id="67228-134">System.String</span></span>

## <span data-ttu-id="67228-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="67228-135">OUTPUTS</span></span>

### <span data-ttu-id="67228-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="67228-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="67228-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="67228-137">NOTES</span></span>

## <span data-ttu-id="67228-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="67228-138">RELATED LINKS</span></span>
