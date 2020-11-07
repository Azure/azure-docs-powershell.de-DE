---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 881908cf85ff4f22fb76b7222a2c09d40a1e9e32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820715"
---
# <span data-ttu-id="89268-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89268-101">Get-AzVmss</span></span>

## <span data-ttu-id="89268-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="89268-102">SYNOPSIS</span></span>
<span data-ttu-id="89268-103">Ruft die Eigenschaften eines VMSS ab.</span><span class="sxs-lookup"><span data-stu-id="89268-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="89268-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="89268-104">SYNTAX</span></span>

### <span data-ttu-id="89268-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="89268-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89268-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="89268-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89268-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="89268-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89268-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89268-108">DESCRIPTION</span></span>
<span data-ttu-id="89268-109">Das Cmdlet " **Get-AzVmss** " Ruft die Modell-und Instanzen Ansicht eines virtuellen Computer-Skalierungs Satzes (VMSS) ab.</span><span class="sxs-lookup"><span data-stu-id="89268-109">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="89268-110">Die Modellansicht ist die benutzerdefinierten Eigenschaften des Skalierungs Satzes für virtuelle Maschinen.</span><span class="sxs-lookup"><span data-stu-id="89268-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="89268-111">Bei der Instanzansicht handelt es sich um den Status der Instanzebene für den Skalierungs Satz der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="89268-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="89268-112">Geben Sie den *InstanceView* -Parameter an, um nur die Instanzen Ansicht eines Skalierungs Satzes für virtuelle Maschinen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="89268-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="89268-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89268-113">EXAMPLES</span></span>

### <span data-ttu-id="89268-114">Beispiel 1: Abrufen der Eigenschaften eines VMSS</span><span class="sxs-lookup"><span data-stu-id="89268-114">Example 1: Get the properties of a VMSS</span></span>
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

<span data-ttu-id="89268-115">Dieser Befehl ruft die Eigenschaften des VMSS mit dem Namen VMSS001 ab, das zur Ressourcengruppe mit dem Namen Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="89268-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="89268-116">Da der Befehl den *InstanceView* -Schalterparameter nicht angibt, ruft das Cmdlet die Modellansicht des Skalierungs Satzes für virtuelle Maschinen ab.</span><span class="sxs-lookup"><span data-stu-id="89268-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

### <span data-ttu-id="89268-117">Beispiel 2: Abrufen aller VMSS in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="89268-117">Example 2: Get all Vmss in a resource group</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001"

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
```

<span data-ttu-id="89268-118">Abrufen aller VMSS in der Ressourcengruppe "Group001"</span><span class="sxs-lookup"><span data-stu-id="89268-118">Get all Vmss in resource group "Group001"</span></span>

### <span data-ttu-id="89268-119">Beispiel 3: Abrufen aller VMSS in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="89268-119">Example 3: Get all Vmss in a subscription</span></span>
```
PS C:\> Get-AzVmss

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="89268-120">Abrufen aller VMSS im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="89268-120">Get all Vmss in subscription.</span></span>

### <span data-ttu-id="89268-121">Beispiel 4: Abrufen aller VMSS mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="89268-121">Example 4: Get all Vmss using filtering</span></span>
```
PS C:\> Get-AzVmss -Name VMSS00*

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="89268-122">Rufen Sie alle VMSS im Abonnement ab, die mit "VMSS00" beginnen.</span><span class="sxs-lookup"><span data-stu-id="89268-122">Get all Vmss in subscription that start with "VMSS00".</span></span>

## <span data-ttu-id="89268-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="89268-123">PARAMETERS</span></span>

### <span data-ttu-id="89268-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89268-124">-DefaultProfile</span></span>
<span data-ttu-id="89268-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="89268-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89268-126">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="89268-126">-InstanceView</span></span>
<span data-ttu-id="89268-127">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht des Skalierungs Satzes für virtuelle Maschinen abruft.</span><span class="sxs-lookup"><span data-stu-id="89268-127">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="89268-128">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="89268-128">-OSUpgradeHistory</span></span>
<span data-ttu-id="89268-129">Gibt an, dass dieses Cmdlet das Betriebssystem-Upgrade-Protokoll des Skalierungs Satzes für virtuelle Maschinen aufführt.</span><span class="sxs-lookup"><span data-stu-id="89268-129">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="89268-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89268-130">-ResourceGroupName</span></span>
<span data-ttu-id="89268-131">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="89268-131">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="89268-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="89268-132">-VMScaleSetName</span></span>
<span data-ttu-id="89268-133">Art der Name des VMSS.</span><span class="sxs-lookup"><span data-stu-id="89268-133">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="89268-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89268-134">CommonParameters</span></span>
<span data-ttu-id="89268-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89268-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89268-136">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89268-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89268-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="89268-137">INPUTS</span></span>

### <span data-ttu-id="89268-138">System. String</span><span class="sxs-lookup"><span data-stu-id="89268-138">System.String</span></span>

## <span data-ttu-id="89268-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="89268-139">OUTPUTS</span></span>

### <span data-ttu-id="89268-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="89268-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="89268-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="89268-141">NOTES</span></span>

## <span data-ttu-id="89268-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="89268-142">RELATED LINKS</span></span>

[<span data-ttu-id="89268-143">Neu – AzVmss</span><span class="sxs-lookup"><span data-stu-id="89268-143">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="89268-144">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89268-144">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="89268-145">Neustart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89268-145">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="89268-146">Satz-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89268-146">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="89268-147">Anfang-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89268-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="89268-148">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89268-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="89268-149">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89268-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


