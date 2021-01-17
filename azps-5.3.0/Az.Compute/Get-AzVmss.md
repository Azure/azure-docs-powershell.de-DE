---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 7985a979f9bbb89d6594416575e3fa00640784b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473095"
---
# <span data-ttu-id="515e7-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="515e7-101">Get-AzVmss</span></span>

## <span data-ttu-id="515e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="515e7-102">SYNOPSIS</span></span>
<span data-ttu-id="515e7-103">Ruft die Eigenschaften eines VMSS ab.</span><span class="sxs-lookup"><span data-stu-id="515e7-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="515e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="515e7-104">SYNTAX</span></span>

### <span data-ttu-id="515e7-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="515e7-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="515e7-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="515e7-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="515e7-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="515e7-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="515e7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="515e7-108">DESCRIPTION</span></span>
<span data-ttu-id="515e7-109">Das **Get-AzVmss-Cmdlet** ruft die Modell- und Instanzansicht eines Virtual Machine Scale Set (VMSS) ab.</span><span class="sxs-lookup"><span data-stu-id="515e7-109">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="515e7-110">Die Modellansicht ist die vom Benutzer angegebenen Eigenschaften des Skalierungssets für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="515e7-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="515e7-111">Die Instanzansicht ist der Status der Instanzebene des Skalierungssets für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="515e7-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="515e7-112">Geben Sie den *Parameter "InstanceView"* an, um nur die Instanzansicht eines Skalierungssets für einen virtuellen Computer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="515e7-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="515e7-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="515e7-113">EXAMPLES</span></span>

### <span data-ttu-id="515e7-114">Beispiel 1: Erhalten der Eigenschaften einer VMSS</span><span class="sxs-lookup"><span data-stu-id="515e7-114">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"

ResourceGroupName                           : Group001
Sku                                         :
  Name                                      : Standard_DS1_v2
  Tier                                      : Standard
  Capacity                                  : 2
UpgradePolicy                               :
  Mode                                      : Manual
VirtualMachineProfile                       :
  OsProfile                                 :
    ComputerNamePrefix                      : test
    AdminUsername                           : contoso
    WindowsConfiguration                    :
      ProvisionVMAgent                      : True
      EnableAutomaticUpdates                : True
  StorageProfile                            :
    ImageReference                          :
      Publisher                             : MicrosoftWindowsServer
      Offer                                 : WindowsServer
      Sku                                   : 2016-Datacenter
      Version                               : latest
    OsDisk                                  :
      Caching                               : None
      CreateOption                          : FromImage
      ManagedDisk                           :
        StorageAccountType                  : Premium_LRS
  NetworkProfile                            :
    NetworkInterfaceConfigurations[0]       :
      Name                                  : Group001
      Primary                               : True
      EnableAcceleratedNetworking           : False
      NetworkSecurityGroup                  :
        Id                                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/Group001
/providers/Microsoft.Network/networkSecurityGroups/Group001
      DnsSettings                           :
      IpConfigurations[0]                   :
        Name                                : Group001
        Subnet                              :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/virtualNetworks/Group001/subnets/Group001
        PrivateIPAddressVersion             : IPv4
        LoadBalancerBackendAddressPools[0]  :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/backendAddressPools/Group001
        LoadBalancerInboundNatPools[0]      :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/inboundNatPools/Group001
        LoadBalancerInboundNatPools[1]      :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/inboundNatPools/Group001
      EnableIPForwarding                    : False
ProvisioningState                           : Succeeded
Overprovision                               : True
UniqueId                                    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SinglePlacementGroup                        : False
Id                                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/Group001/
providers/Microsoft.Compute/virtualMachineScaleSets/VMSS001
Name                                        : VMSS001
Type                                        : Microsoft.Compute/virtualMachineScaleSets
Location                                    : eastus
Tags                                        : {}
```

<span data-ttu-id="515e7-115">Dieser Befehl ruft die Eigenschaften der VMSS namens VMSS001 ab, die zur Ressourcengruppe "Group001" gehört.</span><span class="sxs-lookup"><span data-stu-id="515e7-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="515e7-116">Da der Befehl den Parameter des *InstanceView-Schalters* nicht anfordert, ruft das Cmdlet die Modellansicht des Skalierungssets für den virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="515e7-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

### <span data-ttu-id="515e7-117">Beispiel 2: Alle Vms in einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="515e7-117">Example 2: Get all Vmss in a resource group</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001"

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
```

<span data-ttu-id="515e7-118">Get all Vmss in resource group "Group001"</span><span class="sxs-lookup"><span data-stu-id="515e7-118">Get all Vmss in resource group "Group001"</span></span>

### <span data-ttu-id="515e7-119">Beispiel 3: Alle Vms in einem Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="515e7-119">Example 3: Get all Vmss in a subscription</span></span>
```
PS C:\> Get-AzVmss

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="515e7-120">Holen Sie sich alle Vmss im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="515e7-120">Get all Vmss in subscription.</span></span>

### <span data-ttu-id="515e7-121">Beispiel 4: "Get all Vmss using filtering" (Alle Vmss mithilfe der Filterung erhalten)</span><span class="sxs-lookup"><span data-stu-id="515e7-121">Example 4: Get all Vmss using filtering</span></span>
```
PS C:\> Get-AzVmss -Name VMSS00*

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="515e7-122">Holen Sie sich alle Vmss im Abonnement, die mit "VMSS00" beginnen.</span><span class="sxs-lookup"><span data-stu-id="515e7-122">Get all Vmss in subscription that start with "VMSS00".</span></span>

## <span data-ttu-id="515e7-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="515e7-123">PARAMETERS</span></span>

### <span data-ttu-id="515e7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="515e7-124">-DefaultProfile</span></span>
<span data-ttu-id="515e7-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="515e7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="515e7-126">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="515e7-126">-InstanceView</span></span>
<span data-ttu-id="515e7-127">Gibt an, dass dieses Cmdlet nur die Instanzansicht des Skalierungssets für den virtuellen Computer erhält.</span><span class="sxs-lookup"><span data-stu-id="515e7-127">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515e7-128">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="515e7-128">-OSUpgradeHistory</span></span>
<span data-ttu-id="515e7-129">Gibt an, dass dieses Cmdlet den Upgradeverlauf des Betriebssystems des Skalierungssets für den virtuellen Computer auflistet.</span><span class="sxs-lookup"><span data-stu-id="515e7-129">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OSUpgradeHistoryMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515e7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="515e7-130">-ResourceGroupName</span></span>
<span data-ttu-id="515e7-131">Gibt den Namen der Ressourcengruppe der VMSS an.</span><span class="sxs-lookup"><span data-stu-id="515e7-131">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="515e7-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="515e7-132">-VMScaleSetName</span></span>
<span data-ttu-id="515e7-133">Arten des Namens der VMSS.</span><span class="sxs-lookup"><span data-stu-id="515e7-133">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="515e7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="515e7-134">CommonParameters</span></span>
<span data-ttu-id="515e7-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="515e7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="515e7-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="515e7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="515e7-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="515e7-137">INPUTS</span></span>

### <span data-ttu-id="515e7-138">System.String</span><span class="sxs-lookup"><span data-stu-id="515e7-138">System.String</span></span>

## <span data-ttu-id="515e7-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="515e7-139">OUTPUTS</span></span>

### <span data-ttu-id="515e7-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="515e7-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="515e7-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="515e7-141">NOTES</span></span>

## <span data-ttu-id="515e7-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="515e7-142">RELATED LINKS</span></span>

[<span data-ttu-id="515e7-143">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="515e7-143">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="515e7-144">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="515e7-144">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="515e7-145">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="515e7-145">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="515e7-146">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="515e7-146">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="515e7-147">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="515e7-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="515e7-148">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="515e7-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="515e7-149">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="515e7-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


