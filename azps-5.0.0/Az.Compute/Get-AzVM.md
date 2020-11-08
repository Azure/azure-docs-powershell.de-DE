---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: f1103e8fc7ed9646aa6b91bc0336e331f7ada990
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176792"
---
# <span data-ttu-id="638df-101">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="638df-101">Get-AzVM</span></span>

## <span data-ttu-id="638df-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="638df-102">SYNOPSIS</span></span>
<span data-ttu-id="638df-103">Ruft die Eigenschaften eines virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="638df-103">Gets the properties of a virtual machine.</span></span>

## <span data-ttu-id="638df-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="638df-104">SYNTAX</span></span>

### <span data-ttu-id="638df-105">DefaultParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="638df-105">DefaultParamSet (Default)</span></span>
```
Get-AzVM [[-ResourceGroupName] <String>] [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="638df-106">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="638df-106">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="638df-107">ListLocationVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="638df-107">ListLocationVirtualMachinesParamSet</span></span>
```
Get-AzVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="638df-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="638df-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="638df-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="638df-109">DESCRIPTION</span></span>
<span data-ttu-id="638df-110">Das Cmdlet " **Get-AzVM** " Ruft die Modellansicht oder die Instanzen Ansicht eines virtuellen Azure-Computers ab.</span><span class="sxs-lookup"><span data-stu-id="638df-110">The **Get-AzVM** cmdlet gets the model view or the instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="638df-111">Die Modellansicht ist die benutzerdefinierten Eigenschaften des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="638df-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="638df-112">Bei der Instanzansicht handelt es sich um den Status der Instanzebene des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="638df-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="638df-113">Geben Sie den *Status* -Parameter an, um die Instanzen Ansicht eines virtuellen Computers anstelle der Modellansicht abzurufen, die standardmäßig ist.</span><span class="sxs-lookup"><span data-stu-id="638df-113">Specify the *Status* parameter to get the instance view of a virtual machine instead of the model view which is the default.</span></span>

## <span data-ttu-id="638df-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="638df-114">EXAMPLES</span></span>

### <span data-ttu-id="638df-115">Beispiel 1: Abrufen von Modell-und Instanzen Ansichtseigenschaften</span><span class="sxs-lookup"><span data-stu-id="638df-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"

ResourceGroupName        : ResourceGroup11
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/M
icrosoft.Compute/virtualMachines/VirtualMachine07
VmId                     : 00000000-0000-0000-0000-000000000000
Name                     : VirtualMachine07
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {"creationSource":"acs-VirtualMachine07"}
AvailabilitySetReference : {Id}
DiagnosticsProfile       : {BootDiagnostics}
Extensions               : {linuxdiagnostic, waitforleader}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, LinuxConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
```

<span data-ttu-id="638df-116">Mit diesem Befehl werden die Eigenschaften Modellansicht und Instanzen Ansicht des virtuellen Computers mit dem Namen VirtualMachine07 abgerufen.</span><span class="sxs-lookup"><span data-stu-id="638df-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="638df-117">Beispiel 2: Abrufen von Instanzen Ansichtseigenschaften</span><span class="sxs-lookup"><span data-stu-id="638df-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status

ResourceGroupName       : ResourceGroup11
Name                    : VirtualMachine07
Disks[0]                :
  Name                  : VirtualMachine07-osdisk
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Time                : 3/1/2019 12:59:30 AM
Extensions[0]           :
  Name                  : linuxdiagnostic
  Type                  : Microsoft.OSTCExtensions.LinuxDiagnostic
  TypeHandlerVersion    : 2.3.9029
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Message             : Invalid config settings given: Empty storageAccountName. Install will proceed, but enable
can't proceed, in which case it's still considered a success as it's an external error.
Extensions[1]           :
  Name                  : waitforleader
  Type                  : Microsoft.OSTCExtensions.CustomScriptForLinux
  TypeHandlerVersion    : 1.5.4
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Message             : Command is finished.
---stdout---
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
PING leader.mesos (xxx.xx.x.x) 56(84) bytes of data.
64 bytes from xxx.xx.x.x: icmp_seq=1 ttl=64 time=0.022 ms

--- leader.mesos ping statistics ---
1 packets transmitted, 1 received, 0% packet loss, time 0ms
rtt min/avg/max/mdev = 0.022/0.022/0.022/0.000 ms
leader.mesos up

---errout---
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos


PlatformFaultDomain     : 0
PlatformUpdateDomain    : 0
VMAgent                 :
  VmAgentVersion        : 2.2.37
  ExtensionHandlers[0]  :
    Type                : Microsoft.OSTCExtensions.LinuxDiagnostic
    TypeHandlerVersion  : 2.3.9029
    Status              :
      Code              : ProvisioningState/succeeded
      Level             : Info
      DisplayStatus     : Ready
      Message           : Plugin enabled
  ExtensionHandlers[1]  :
    Type                : Microsoft.OSTCExtensions.CustomScriptForLinux
    TypeHandlerVersion  : 1.5.4
    Status              :
      Code              : ProvisioningState/succeeded
      Level             : Info
      DisplayStatus     : Ready
      Message           : Plugin enabled
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Ready
    Message             : Guest Agent is running
    Time                : 3/1/2019 2:04:12 AM
Statuses[0]             :
  Code                  : ProvisioningState/succeeded
  Level                 : Info
  DisplayStatus         : Provisioning succeeded
  Time                  : 3/1/2019 1:01:57 AM
Statuses[1]             :
  Code                  : PowerState/running
  Level                 : Info
  DisplayStatus         : VM running
```

<span data-ttu-id="638df-118">Dieser Befehl ruft Eigenschaften des virtuellen Computers mit dem Namen VirtualMachine07 ab.</span><span class="sxs-lookup"><span data-stu-id="638df-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="638df-119">Mit diesem Befehl wird der *Status* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="638df-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="638df-120">Daher ruft der Befehl nur die Eigenschaften der Instanzen Ansicht ab.</span><span class="sxs-lookup"><span data-stu-id="638df-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="638df-121">Beispiel 3: Abrufen von Eigenschaften für alle virtuellen Computer in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="638df-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
ResourceGroup11     test1         eastus Standard_DS1_v2 Windows          test1
ResourceGroup11     test2         westus Standard_DS1_v2 Windows          test2
ResourceGroup11     test3         eastus Standard_DS1_v2 Windows          test3
```

<span data-ttu-id="638df-122">Dieser Befehl ruft Eigenschaften für alle virtuellen Computer in der Ressourcengruppe mit dem Namen ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="638df-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="638df-123">Beispiel 4: Abrufen aller virtuellen Computer in Ihrem Abonnement</span><span class="sxs-lookup"><span data-stu-id="638df-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzVM

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test1         eastus Standard_DS1_v2 Windows          test1
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST1               test3         eastus Standard_DS1_v2 Windows          test3
TEST2               test4         westus Standard_DS1_v2 Windows          test4
TEST2               test5         eastus Standard_DS1_v2 Windows          test5
```

<span data-ttu-id="638df-124">Dieser Befehl ruft alle virtuellen Computer in Ihrem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="638df-124">This command gets all the virtual machines in your subscription.</span></span>

### <span data-ttu-id="638df-125">Beispiel 5: Abrufen aller virtuellen Computer am Standort.</span><span class="sxs-lookup"><span data-stu-id="638df-125">Example 5: Get all virtual machines in the location.</span></span>
```
PS C:\> Get-AzVM -Location "westus"

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST2               test4         westus Standard_DS1_v2 Windows          test4
```

<span data-ttu-id="638df-126">Dieser Befehl ruft alle virtuellen Computer in der West US-Region ab.</span><span class="sxs-lookup"><span data-stu-id="638df-126">This command gets all the virtual machines in West US region.</span></span>

### <span data-ttu-id="638df-127">Beispiel 6: Abrufen aller virtuellen Computer mithilfe der Filterung</span><span class="sxs-lookup"><span data-stu-id="638df-127">Example 6: Get all virtual machines using filtering</span></span>
```
PS C:\> Get-AzVM -Name test*

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test1         eastus Standard_DS1_v2 Windows          test1
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST1               test3         eastus Standard_DS1_v2 Windows          test3
TEST2               test4         westus Standard_DS1_v2 Windows          test4
TEST2               test5         eastus Standard_DS1_v2 Windows          test5
```

<span data-ttu-id="638df-128">Dieser Befehl ruft alle virtuellen Computer in Ihrem Abonnement ab, die mit "Test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="638df-128">This command gets all the virtual machines in your subscription that start with "test".</span></span>

## <span data-ttu-id="638df-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="638df-129">PARAMETERS</span></span>

### <span data-ttu-id="638df-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="638df-130">-DefaultProfile</span></span>
<span data-ttu-id="638df-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="638df-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="638df-132">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="638df-132">-DisplayHint</span></span>
<span data-ttu-id="638df-133">Bestimmt, wie das Objekt des virtuellen Computers angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="638df-133">Determines how the virtual machine object is displayed.</span></span>
<span data-ttu-id="638df-134">Gültige Werte sind:--Compact: zeigt nur Eigenschaften der obersten Ebene an--Expand: zeigt alle Eigenschaften auf allen Ebenen an.</span><span class="sxs-lookup"><span data-stu-id="638df-134">Valid values are: -- Compact: displays only top level properties -- Expand: displays all properties in all levels</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="638df-135">-Standort</span><span class="sxs-lookup"><span data-stu-id="638df-135">-Location</span></span>
<span data-ttu-id="638df-136">Gibt einen Speicherort für die Liste der virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="638df-136">Specifies a location for the virtual machines to list.</span></span>

```yaml
Type: System.String
Parameter Sets: ListLocationVirtualMachinesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="638df-137">-Name</span><span class="sxs-lookup"><span data-stu-id="638df-137">-Name</span></span>
<span data-ttu-id="638df-138">Gibt den Namen des abzurufenden virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="638df-138">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParamSet
Aliases: ResourceName, VMName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="638df-139">-Nextlink</span><span class="sxs-lookup"><span data-stu-id="638df-139">-NextLink</span></span>
<span data-ttu-id="638df-140">Gibt den nächsten Link an.</span><span class="sxs-lookup"><span data-stu-id="638df-140">Specifies the next link.</span></span>

```yaml
Type: System.Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="638df-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="638df-141">-ResourceGroupName</span></span>
<span data-ttu-id="638df-142">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="638df-142">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="638df-143">-Status</span><span class="sxs-lookup"><span data-stu-id="638df-143">-Status</span></span>
<span data-ttu-id="638df-144">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht des virtuellen Computers abruft.</span><span class="sxs-lookup"><span data-stu-id="638df-144">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="638df-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="638df-145">CommonParameters</span></span>
<span data-ttu-id="638df-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="638df-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="638df-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="638df-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="638df-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="638df-148">INPUTS</span></span>

### <span data-ttu-id="638df-149">System. String</span><span class="sxs-lookup"><span data-stu-id="638df-149">System.String</span></span>

### <span data-ttu-id="638df-150">System. Uri</span><span class="sxs-lookup"><span data-stu-id="638df-150">System.Uri</span></span>

### <span data-ttu-id="638df-151">Microsoft. Azure. Commands. Compute. Models. DisplayHintType</span><span class="sxs-lookup"><span data-stu-id="638df-151">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span></span>

## <span data-ttu-id="638df-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="638df-152">OUTPUTS</span></span>

### <span data-ttu-id="638df-153">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="638df-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="638df-154">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="638df-154">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="638df-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="638df-155">NOTES</span></span>

## <span data-ttu-id="638df-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="638df-156">RELATED LINKS</span></span>

[<span data-ttu-id="638df-157">Neu – AzVM</span><span class="sxs-lookup"><span data-stu-id="638df-157">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="638df-158">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="638df-158">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="638df-159">Neustart-AzVM</span><span class="sxs-lookup"><span data-stu-id="638df-159">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="638df-160">Anfang-AzVM</span><span class="sxs-lookup"><span data-stu-id="638df-160">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="638df-161">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="638df-161">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="638df-162">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="638df-162">Update-AzVM</span></span>](./Update-AzVM.md)


