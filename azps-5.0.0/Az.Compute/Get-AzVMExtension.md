---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: 2c36408b520268acaaa6ae2fa4c4c6030fbd2111
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302805"
---
# <span data-ttu-id="13bf1-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="13bf1-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="13bf1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="13bf1-102">SYNOPSIS</span></span>
<span data-ttu-id="13bf1-103">Ruft Eigenschaften der auf einem virtuellen Computer installierten Virtual Machine-Erweiterungen ab.</span><span class="sxs-lookup"><span data-stu-id="13bf1-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="13bf1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="13bf1-104">SYNTAX</span></span>

```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13bf1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13bf1-105">DESCRIPTION</span></span>
<span data-ttu-id="13bf1-106">Das Cmdlet " **Get-AzVMExtension** " Ruft Eigenschaften der auf einem virtuellen Computer installierten Virtual Machine-Erweiterungen ab.</span><span class="sxs-lookup"><span data-stu-id="13bf1-106">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="13bf1-107">Geben Sie den Namen einer Erweiterung an, für die Eigenschaften abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="13bf1-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="13bf1-108">Um nur die Instanzen Ansicht einer Erweiterung abzurufen, geben Sie den Parameter Status an.</span><span class="sxs-lookup"><span data-stu-id="13bf1-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="13bf1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13bf1-109">EXAMPLES</span></span>

### <span data-ttu-id="13bf1-110">Beispiel 1: Abrufen von Eigenschaften einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="13bf1-110">Example 1: Get properties of an extension</span></span>
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

<span data-ttu-id="13bf1-111">Dieser Befehl ruft Eigenschaften für die Erweiterung mit dem Namen CustomScriptExtension auf dem virtuellen Computer mit dem Namen VirtualMachine22 in der Ressourcengruppe ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="13bf1-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="13bf1-112">Beispiel 2: Abrufen der Instanzen Ansicht einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="13bf1-112">Example 2: Get instance view of an extension</span></span>
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

<span data-ttu-id="13bf1-113">Dieser Befehl ruft die Instanzen Ansicht für die Erweiterung mit dem Namen CustomScriptExtension auf dem virtuellen Computer mit dem Namen VirtualMachine22 in der Ressourcengruppe ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="13bf1-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="13bf1-114">Beispiel 3: Abrufen aller auf einem virtuellen Computer installierten Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="13bf1-114">Example 3: Get all extensions installed on a VM</span></span>
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

<span data-ttu-id="13bf1-115">Dieser Befehl ruft die Liste der Erweiterungen ab, die auf dem virtuellen Computer mit dem Namen VirtualMachine22 in der Ressourcengruppe ResourceGroup11 installiert sind.</span><span class="sxs-lookup"><span data-stu-id="13bf1-115">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="13bf1-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="13bf1-116">PARAMETERS</span></span>

### <span data-ttu-id="13bf1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13bf1-117">-DefaultProfile</span></span>
<span data-ttu-id="13bf1-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="13bf1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13bf1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="13bf1-119">-Name</span></span>
<span data-ttu-id="13bf1-120">Gibt den Namen einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="13bf1-120">Specifies the name of an extension.</span></span>
<span data-ttu-id="13bf1-121">Dieses Cmdlet ruft Eigenschaften für die Erweiterung ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="13bf1-121">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="13bf1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13bf1-122">-ResourceGroupName</span></span>
<span data-ttu-id="13bf1-123">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="13bf1-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="13bf1-124">-Status</span><span class="sxs-lookup"><span data-stu-id="13bf1-124">-Status</span></span>
<span data-ttu-id="13bf1-125">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht einer Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="13bf1-125">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="13bf1-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="13bf1-126">-VMName</span></span>
<span data-ttu-id="13bf1-127">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="13bf1-127">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="13bf1-128">Dieses Cmdlet ruft Eigenschaften einer Erweiterung vom virtuellen Computer ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="13bf1-128">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="13bf1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13bf1-129">CommonParameters</span></span>
<span data-ttu-id="13bf1-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13bf1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13bf1-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13bf1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13bf1-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="13bf1-132">INPUTS</span></span>

### <span data-ttu-id="13bf1-133">System. String</span><span class="sxs-lookup"><span data-stu-id="13bf1-133">System.String</span></span>

### <span data-ttu-id="13bf1-134">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="13bf1-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="13bf1-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="13bf1-135">OUTPUTS</span></span>

### <span data-ttu-id="13bf1-136">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="13bf1-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="13bf1-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="13bf1-137">NOTES</span></span>

## <span data-ttu-id="13bf1-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="13bf1-138">RELATED LINKS</span></span>

[<span data-ttu-id="13bf1-139">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="13bf1-139">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="13bf1-140">Satz-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="13bf1-140">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


