---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
ms.openlocfilehash: 4e722e897b23ce1e7ea7c30a6caa393be75f893c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933131"
---
# <span data-ttu-id="914e6-101">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="914e6-101">Get-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="914e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="914e6-102">SYNOPSIS</span></span>
<span data-ttu-id="914e6-103">Ruft Informationen zu einer benutzerdefinierten Skripterweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="914e6-103">Gets information about a custom script extension.</span></span>

## <span data-ttu-id="914e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="914e6-104">SYNTAX</span></span>

```
Get-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="914e6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="914e6-105">DESCRIPTION</span></span>
<span data-ttu-id="914e6-106">Das **Cmdlet Get-AzVMCustomScriptExtension** ruft Informationen zu einem benutzerdefinierten Skript virtual Machine Extension auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="914e6-106">The **Get-AzVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="914e6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="914e6-107">EXAMPLES</span></span>

### <span data-ttu-id="914e6-108">Beispiel 1: Erhalten einer benutzerdefinierten Skripterweiterung</span><span class="sxs-lookup"><span data-stu-id="914e6-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="914e6-109">Dieser Befehl ruft die benutzerdefinierte Skripterweiterung ContosoCustomScript für den virtuellen Computer mit dem Namen VirtualMachine07 ab.</span><span class="sxs-lookup"><span data-stu-id="914e6-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="914e6-110">Beispiel 2: Anzeigen der Instanzansicht einer benutzerdefinierten Skripterweiterung</span><span class="sxs-lookup"><span data-stu-id="914e6-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="914e6-111">Dieser Befehl ruft die Instanzansicht der benutzerdefinierten Skripterweiterung contosoCustomScript für den virtuellen Computer mit dem Namen VirtualMachine07 ab.</span><span class="sxs-lookup"><span data-stu-id="914e6-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="914e6-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="914e6-112">PARAMETERS</span></span>

### <span data-ttu-id="914e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="914e6-113">-DefaultProfile</span></span>
<span data-ttu-id="914e6-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="914e6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="914e6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="914e6-115">-Name</span></span>
<span data-ttu-id="914e6-116">Gibt den Namen der benutzerdefinierten Skripterweiterung an, über die dieses Cmdlet Informationen erhält.</span><span class="sxs-lookup"><span data-stu-id="914e6-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="914e6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="914e6-117">-ResourceGroupName</span></span>
<span data-ttu-id="914e6-118">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="914e6-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="914e6-119">-Status</span><span class="sxs-lookup"><span data-stu-id="914e6-119">-Status</span></span>
<span data-ttu-id="914e6-120">Gibt an, dass dieses Cmdlet die Instanzansicht der benutzerdefinierten Skripterweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="914e6-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="914e6-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="914e6-121">-VMName</span></span>
<span data-ttu-id="914e6-122">Gibt den Namen eines virtuellen Computers an, für den dieses Cmdlet die benutzerdefinierte Skripterweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="914e6-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="914e6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="914e6-123">CommonParameters</span></span>
<span data-ttu-id="914e6-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="914e6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="914e6-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="914e6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="914e6-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="914e6-126">INPUTS</span></span>

### <span data-ttu-id="914e6-127">System.String</span><span class="sxs-lookup"><span data-stu-id="914e6-127">System.String</span></span>

### <span data-ttu-id="914e6-128">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="914e6-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="914e6-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="914e6-129">OUTPUTS</span></span>

### <span data-ttu-id="914e6-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span><span class="sxs-lookup"><span data-stu-id="914e6-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="914e6-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="914e6-131">NOTES</span></span>

## <span data-ttu-id="914e6-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="914e6-132">RELATED LINKS</span></span>

[<span data-ttu-id="914e6-133">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="914e6-133">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="914e6-134">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="914e6-134">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="914e6-135">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="914e6-135">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


