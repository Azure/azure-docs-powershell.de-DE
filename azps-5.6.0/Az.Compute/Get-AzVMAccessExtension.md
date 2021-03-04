---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: f89260b083d07ca717e1e302c2fb0bb747005d43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933136"
---
# <span data-ttu-id="f9740-101">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f9740-101">Get-AzVMAccessExtension</span></span>

## <span data-ttu-id="f9740-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9740-102">SYNOPSIS</span></span>
<span data-ttu-id="f9740-103">Ruft Informationen zur VMAccess-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="f9740-103">Gets information about the VMAccess extension.</span></span>

## <span data-ttu-id="f9740-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9740-104">SYNTAX</span></span>

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9740-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9740-105">DESCRIPTION</span></span>
<span data-ttu-id="f9740-106">Das **Cmdlet Get-AzVMAccessExtension** ruft Informationen zur Virtual Machine Access (VMAccess) Virtual Machine Extension ab.</span><span class="sxs-lookup"><span data-stu-id="f9740-106">The **Get-AzVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="f9740-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f9740-107">EXAMPLES</span></span>

### <span data-ttu-id="f9740-108">Beispiel 1: Holen Sie sich die ERWEITERUNG VMAccess</span><span class="sxs-lookup"><span data-stu-id="f9740-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="f9740-109">Dieser Befehl ruft die VMAccess-Erweiterung namens ContosoTest für den virtuellen Computer mit dem Namen VirtualMachine07 ab.</span><span class="sxs-lookup"><span data-stu-id="f9740-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="f9740-110">Beispiel 2: Anzeigen der Instanzansicht der VMAccess-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="f9740-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="f9740-111">Dieser Befehl ruft die Instanzansicht der VMAccess-Erweiterung namens ContosoTest für den virtuellen Computer mit dem Namen VirtualMachine07 ab.</span><span class="sxs-lookup"><span data-stu-id="f9740-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="f9740-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f9740-112">PARAMETERS</span></span>

### <span data-ttu-id="f9740-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9740-113">-DefaultProfile</span></span>
<span data-ttu-id="f9740-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9740-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9740-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f9740-115">-Name</span></span>
<span data-ttu-id="f9740-116">Gibt den Namen der Erweiterung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="f9740-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f9740-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9740-117">-ResourceGroupName</span></span>
<span data-ttu-id="f9740-118">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="f9740-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f9740-119">-Status</span><span class="sxs-lookup"><span data-stu-id="f9740-119">-Status</span></span>
<span data-ttu-id="f9740-120">Gibt an, dass dieses Cmdlet nur die Instanzansicht der Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="f9740-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="f9740-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="f9740-121">-VMName</span></span>
<span data-ttu-id="f9740-122">Gibt den Namen eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="f9740-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f9740-123">Dieses Cmdlet ruft Informationen zu VMAccess für den virtuellen Computer ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f9740-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f9740-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9740-124">CommonParameters</span></span>
<span data-ttu-id="f9740-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9740-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9740-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9740-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9740-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f9740-127">INPUTS</span></span>

### <span data-ttu-id="f9740-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f9740-128">System.String</span></span>

### <span data-ttu-id="f9740-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f9740-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f9740-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f9740-130">OUTPUTS</span></span>

### <span data-ttu-id="f9740-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="f9740-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="f9740-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f9740-132">NOTES</span></span>

## <span data-ttu-id="f9740-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f9740-133">RELATED LINKS</span></span>

[<span data-ttu-id="f9740-134">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f9740-134">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="f9740-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f9740-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="f9740-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="f9740-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)


