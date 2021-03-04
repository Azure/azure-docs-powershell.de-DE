---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: 33be258858a6ace456b7aa3c5b25594a373ccfd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949531"
---
# <span data-ttu-id="572ff-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="572ff-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="572ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="572ff-102">SYNOPSIS</span></span>
<span data-ttu-id="572ff-103">Ruft Eigenschaften von Virtual Machine Extensions ab, die auf einem virtuellen Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="572ff-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="572ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="572ff-104">SYNTAX</span></span>

### <span data-ttu-id="572ff-105">GetExtensionParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="572ff-105">GetExtensionParameterSet (Default)</span></span>
```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="572ff-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="572ff-106">VMParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-VMObject <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="572ff-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="572ff-107">ResourceIdParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-ResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="572ff-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="572ff-108">DESCRIPTION</span></span>
<span data-ttu-id="572ff-109">Das **Get-AzVMExtension-Cmdlet** ruft Eigenschaften von Virtual Machine Extensions ab, die auf einem virtuellen Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="572ff-109">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="572ff-110">Geben Sie den Namen einer Erweiterung an, für die Eigenschaften angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="572ff-110">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="572ff-111">Um nur die Instanzansicht einer Erweiterung zu erhalten, geben Sie den Parameter Status an.</span><span class="sxs-lookup"><span data-stu-id="572ff-111">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="572ff-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="572ff-112">EXAMPLES</span></span>

### <span data-ttu-id="572ff-113">Beispiel 1: Erhalten von Eigenschaften einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="572ff-113">Example 1: Get properties of an extension</span></span>
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

<span data-ttu-id="572ff-114">Dieser Befehl ruft Eigenschaften für die Erweiterung "CustomScriptExtension" auf dem virtuellen Computer mit dem Namen VirtualMachine22 in der Ressourcengruppe ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="572ff-114">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="572ff-115">Beispiel 2: Anzeigen der Instanzansicht einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="572ff-115">Example 2: Get instance view of an extension</span></span>
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

<span data-ttu-id="572ff-116">Dieser Befehl ruft die Instanzansicht für die Erweiterung "CustomScriptExtension" auf dem virtuellen Computer mit dem Namen VirtualMachine22 in der Ressourcengruppe ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="572ff-116">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="572ff-117">Beispiel 3: Installieren aller Erweiterungen auf einer VM</span><span class="sxs-lookup"><span data-stu-id="572ff-117">Example 3: Get all extensions installed on a VM</span></span>
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

### <span data-ttu-id="572ff-118">Beispiel 4: Erhalten von Eigenschaften einer Erweiterung mithilfe des Parameters "VM"</span><span class="sxs-lookup"><span data-stu-id="572ff-118">Example 4: Get properties of an extension using the VM parameter</span></span>
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

<span data-ttu-id="572ff-119">Dieser Befehl ruft die Liste der Erweiterungen ab, die auf dem virtuellen Computer mit dem Namen VirtualMachine22 in der Ressourcengruppe ResourceGroup11 installiert sind.</span><span class="sxs-lookup"><span data-stu-id="572ff-119">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="572ff-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="572ff-120">PARAMETERS</span></span>

### <span data-ttu-id="572ff-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="572ff-121">-DefaultProfile</span></span>
<span data-ttu-id="572ff-122">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="572ff-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="572ff-123">-Name</span><span class="sxs-lookup"><span data-stu-id="572ff-123">-Name</span></span>
<span data-ttu-id="572ff-124">Gibt den Namen einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="572ff-124">Specifies the name of an extension.</span></span>
<span data-ttu-id="572ff-125">Dieses Cmdlet ruft Eigenschaften für die erweiterung ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="572ff-125">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="572ff-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="572ff-126">-ResourceGroupName</span></span>
<span data-ttu-id="572ff-127">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="572ff-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="572ff-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="572ff-128">-ResourceId</span></span>
<span data-ttu-id="572ff-129">Ressourcen-ID, die das Objekt des virtuellen Computers an gibt, auf dem sich die Erweiterung befindet.</span><span class="sxs-lookup"><span data-stu-id="572ff-129">Resource Id specifying the virtual machine object the extension is on.</span></span>

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

### <span data-ttu-id="572ff-130">-Status</span><span class="sxs-lookup"><span data-stu-id="572ff-130">-Status</span></span>
<span data-ttu-id="572ff-131">Gibt an, dass dieses Cmdlet nur die Instanzansicht einer Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="572ff-131">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="572ff-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="572ff-132">-VMName</span></span>
<span data-ttu-id="572ff-133">Gibt den Namen eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="572ff-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="572ff-134">Dieses Cmdlet ruft Eigenschaften einer Erweiterung von dem virtuellen Computer ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="572ff-134">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="572ff-135">-VMObject</span><span class="sxs-lookup"><span data-stu-id="572ff-135">-VMObject</span></span>
<span data-ttu-id="572ff-136">Gibt das Objekt des virtuellen Computers an, auf dem sich die Erweiterung befindet.</span><span class="sxs-lookup"><span data-stu-id="572ff-136">Specifies the virtual machine object the extension is on.</span></span>

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

### <span data-ttu-id="572ff-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="572ff-137">CommonParameters</span></span>
<span data-ttu-id="572ff-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="572ff-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="572ff-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="572ff-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="572ff-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="572ff-140">INPUTS</span></span>

### <span data-ttu-id="572ff-141">System.String</span><span class="sxs-lookup"><span data-stu-id="572ff-141">System.String</span></span>

### <span data-ttu-id="572ff-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="572ff-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="572ff-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="572ff-143">OUTPUTS</span></span>

### <span data-ttu-id="572ff-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="572ff-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="572ff-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="572ff-145">NOTES</span></span>

## <span data-ttu-id="572ff-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="572ff-146">RELATED LINKS</span></span>

[<span data-ttu-id="572ff-147">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="572ff-147">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="572ff-148">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="572ff-148">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


