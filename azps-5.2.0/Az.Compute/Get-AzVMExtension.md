---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: 2c36408b520268acaaa6ae2fa4c4c6030fbd2111
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302936"
---
# <span data-ttu-id="cacea-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="cacea-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="cacea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cacea-102">SYNOPSIS</span></span>
<span data-ttu-id="cacea-103">Ruft Eigenschaften von Virtual Machine Extensions ab, die auf einem virtuellen Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="cacea-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="cacea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cacea-104">SYNTAX</span></span>

```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cacea-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cacea-105">DESCRIPTION</span></span>
<span data-ttu-id="cacea-106">Das **Cmdlet "Get-AzVMExtension"** ruft Eigenschaften von Virtual Machine Extensions ab, die auf einem virtuellen Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="cacea-106">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="cacea-107">Geben Sie den Namen einer Erweiterung an, für die Eigenschaften angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cacea-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="cacea-108">Um nur die Instanzansicht einer Erweiterung zu erhalten, geben Sie den Parameter "Status" an.</span><span class="sxs-lookup"><span data-stu-id="cacea-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="cacea-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cacea-109">EXAMPLES</span></span>

### <span data-ttu-id="cacea-110">Beispiel 1: Erhalten von Eigenschaften einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="cacea-110">Example 1: Get properties of an extension</span></span>
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

<span data-ttu-id="cacea-111">Dieser Befehl ruft Eigenschaften für die Erweiterung "CustomScriptExtension" auf dem virtuellen Computer "VirtualMachine22" in der Ressourcengruppe "ResourceGroup11" ab.</span><span class="sxs-lookup"><span data-stu-id="cacea-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="cacea-112">Beispiel 2: Erhalten der Instanzansicht einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="cacea-112">Example 2: Get instance view of an extension</span></span>
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

<span data-ttu-id="cacea-113">Dieser Befehl ruft die Instanzansicht für die Erweiterung "CustomScriptExtension" auf dem virtuellen Computer namens "VirtualMachine22" in der Ressourcengruppe "ResourceGroup11" ab.</span><span class="sxs-lookup"><span data-stu-id="cacea-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="cacea-114">Beispiel 3: Installieren aller Erweiterungen auf einer VM</span><span class="sxs-lookup"><span data-stu-id="cacea-114">Example 3: Get all extensions installed on a VM</span></span>
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

<span data-ttu-id="cacea-115">Dieser Befehl ruft die Liste der Erweiterungen ab, die auf dem virtuellen Computer "VirtualMachine22" in der Ressourcengruppe "ResourceGroup11" installiert sind.</span><span class="sxs-lookup"><span data-stu-id="cacea-115">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="cacea-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cacea-116">PARAMETERS</span></span>

### <span data-ttu-id="cacea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cacea-117">-DefaultProfile</span></span>
<span data-ttu-id="cacea-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cacea-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cacea-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cacea-119">-Name</span></span>
<span data-ttu-id="cacea-120">Gibt den Namen einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="cacea-120">Specifies the name of an extension.</span></span>
<span data-ttu-id="cacea-121">Dieses Cmdlet ruft Eigenschaften für die erweiterung ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="cacea-121">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cacea-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cacea-122">-ResourceGroupName</span></span>
<span data-ttu-id="cacea-123">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="cacea-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cacea-124">-Status</span><span class="sxs-lookup"><span data-stu-id="cacea-124">-Status</span></span>
<span data-ttu-id="cacea-125">Gibt an, dass dieses Cmdlet nur die Instanzansicht einer Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="cacea-125">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="cacea-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="cacea-126">-VMName</span></span>
<span data-ttu-id="cacea-127">Gibt den Namen eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="cacea-127">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="cacea-128">Dieses Cmdlet ruft eigenschaften einer Erweiterung von dem virtuellen Computer ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="cacea-128">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cacea-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cacea-129">CommonParameters</span></span>
<span data-ttu-id="cacea-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cacea-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cacea-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cacea-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cacea-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cacea-132">INPUTS</span></span>

### <span data-ttu-id="cacea-133">System.String</span><span class="sxs-lookup"><span data-stu-id="cacea-133">System.String</span></span>

### <span data-ttu-id="cacea-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cacea-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cacea-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cacea-135">OUTPUTS</span></span>

### <span data-ttu-id="cacea-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="cacea-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="cacea-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cacea-137">NOTES</span></span>

## <span data-ttu-id="cacea-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cacea-138">RELATED LINKS</span></span>

[<span data-ttu-id="cacea-139">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="cacea-139">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="cacea-140">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="cacea-140">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


