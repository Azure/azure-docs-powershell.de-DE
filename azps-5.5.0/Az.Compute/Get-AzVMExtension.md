---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: ca9693f715d72366a6cc78030d0a8328bf0abc50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171240"
---
# <span data-ttu-id="7d3c0-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="7d3c0-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="7d3c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d3c0-102">SYNOPSIS</span></span>
<span data-ttu-id="7d3c0-103">Ruft Eigenschaften von Virtual Machine Extensions ab, die auf einem virtuellen Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="7d3c0-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="7d3c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d3c0-104">SYNTAX</span></span>

### <span data-ttu-id="7d3c0-105">GetExtensionParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7d3c0-105">GetExtensionParameterSet (Default)</span></span>
```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d3c0-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d3c0-106">VMParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-VMObject <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d3c0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d3c0-107">ResourceIdParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-ResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d3c0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d3c0-108">DESCRIPTION</span></span>
<span data-ttu-id="7d3c0-109">Das **Cmdlet "Get-AzVMExtension"** ruft Eigenschaften von Virtual Machine Extensions ab, die auf einem virtuellen Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="7d3c0-109">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="7d3c0-110">Geben Sie den Namen einer Erweiterung an, für die Eigenschaften angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7d3c0-110">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="7d3c0-111">Um nur die Instanzansicht einer Erweiterung zu erhalten, geben Sie den Parameter "Status" an.</span><span class="sxs-lookup"><span data-stu-id="7d3c0-111">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="7d3c0-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7d3c0-112">EXAMPLES</span></span>

### <span data-ttu-id="7d3c0-113">Beispiel 1: Erhalten von Eigenschaften einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="7d3c0-113">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="7d3c0-114">Dieser Befehl ruft Eigenschaften für die Erweiterung "CustomScriptExtension" auf dem virtuellen Computer "VirtualMachine22" in der Ressourcengruppe "ResourceGroup11" ab.</span><span class="sxs-lookup"><span data-stu-id="7d3c0-114">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="7d3c0-115">Beispiel 2: Erhalten der Instanzansicht einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="7d3c0-115">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                : {Microsoft.Azure.Management.Compute.Models.InstanceViewStatus}
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="7d3c0-116">Dieser Befehl ruft die Instanzansicht für die Erweiterung "CustomScriptExtension" auf dem virtuellen Computer namens "VirtualMachine22" in der Ressourcengruppe "ResourceGroup11" ab.</span><span class="sxs-lookup"><span data-stu-id="7d3c0-116">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="7d3c0-117">Beispiel 3: Installieren aller Erweiterungen auf einer VM</span><span class="sxs-lookup"><span data-stu-id="7d3c0-117">Example 3: Get all extensions installed on a VM</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

### <span data-ttu-id="7d3c0-118">Beispiel 4: Erhalten von Eigenschaften einer Erweiterung mit dem Parameter "VM"</span><span class="sxs-lookup"><span data-stu-id="7d3c0-118">Example 4: Get properties of an extension using the VM parameter</span></span>
```
PS C:\> $vm = Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine22"
PS C:\> Get-AzVMExtension -VM $vm

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="7d3c0-119">Dieser Befehl ruft die Liste der Erweiterungen ab, die auf dem virtuellen Computer "VirtualMachine22" in der Ressourcengruppe "ResourceGroup11" installiert sind.</span><span class="sxs-lookup"><span data-stu-id="7d3c0-119">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="7d3c0-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d3c0-120">PARAMETERS</span></span>

### <span data-ttu-id="7d3c0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d3c0-121">-DefaultProfile</span></span>
<span data-ttu-id="7d3c0-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7d3c0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d3c0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7d3c0-123">-Name</span></span>
<span data-ttu-id="7d3c0-124">Gibt den Namen einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="7d3c0-124">Specifies the name of an extension.</span></span>
<span data-ttu-id="7d3c0-125">Dieses Cmdlet ruft Eigenschaften für die erweiterung ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="7d3c0-125">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3c0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d3c0-126">-ResourceGroupName</span></span>
<span data-ttu-id="7d3c0-127">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7d3c0-127">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3c0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d3c0-128">-ResourceId</span></span>
<span data-ttu-id="7d3c0-129">Ressourcen-ID, die das Objekt des virtuellen Computers an, auf dem sich die Erweiterung befindet.</span><span class="sxs-lookup"><span data-stu-id="7d3c0-129">Resource Id specifying the virtual machine object the extension is on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3c0-130">-Status</span><span class="sxs-lookup"><span data-stu-id="7d3c0-130">-Status</span></span>
<span data-ttu-id="7d3c0-131">Gibt an, dass dieses Cmdlet nur die Instanzansicht einer Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="7d3c0-131">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3c0-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="7d3c0-132">-VMName</span></span>
<span data-ttu-id="7d3c0-133">Gibt den Namen eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="7d3c0-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="7d3c0-134">Dieses Cmdlet ruft die Eigenschaften einer Erweiterung von dem virtuellen Computer ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="7d3c0-134">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3c0-135">-VMObject</span><span class="sxs-lookup"><span data-stu-id="7d3c0-135">-VMObject</span></span>
<span data-ttu-id="7d3c0-136">Gibt das Objekt des virtuellen Computers an, auf dem sich die Erweiterung befindet.</span><span class="sxs-lookup"><span data-stu-id="7d3c0-136">Specifies the virtual machine object the extension is on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3c0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d3c0-137">CommonParameters</span></span>
<span data-ttu-id="7d3c0-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d3c0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d3c0-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d3c0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d3c0-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7d3c0-140">INPUTS</span></span>

### <span data-ttu-id="7d3c0-141">System.String</span><span class="sxs-lookup"><span data-stu-id="7d3c0-141">System.String</span></span>

### <span data-ttu-id="7d3c0-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7d3c0-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7d3c0-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7d3c0-143">OUTPUTS</span></span>

### <span data-ttu-id="7d3c0-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="7d3c0-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="7d3c0-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7d3c0-145">NOTES</span></span>

## <span data-ttu-id="7d3c0-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7d3c0-146">RELATED LINKS</span></span>

[<span data-ttu-id="7d3c0-147">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="7d3c0-147">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="7d3c0-148">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="7d3c0-148">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


