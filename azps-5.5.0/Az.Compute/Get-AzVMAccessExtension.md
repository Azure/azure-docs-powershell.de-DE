---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: c139e1bac6f910a1759e4482abdd7c67d2e7fa55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144964"
---
# <span data-ttu-id="d775d-101">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d775d-101">Get-AzVMAccessExtension</span></span>

## <span data-ttu-id="d775d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d775d-102">SYNOPSIS</span></span>
<span data-ttu-id="d775d-103">Ruft Informationen zur Erweiterung VMAccess ab.</span><span class="sxs-lookup"><span data-stu-id="d775d-103">Gets information about the VMAccess extension.</span></span>

## <span data-ttu-id="d775d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d775d-104">SYNTAX</span></span>

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d775d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d775d-105">DESCRIPTION</span></span>
<span data-ttu-id="d775d-106">Das **Cmdlet "Get-AzVMAccessExtension"** ruft Informationen zur Virtual Machine Access (VMAccess) Virtual Machine Extension ab.</span><span class="sxs-lookup"><span data-stu-id="d775d-106">The **Get-AzVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="d775d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d775d-107">EXAMPLES</span></span>

### <span data-ttu-id="d775d-108">Beispiel 1: Erhalten der Erweiterung VMAccess</span><span class="sxs-lookup"><span data-stu-id="d775d-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="d775d-109">Dieser Befehl ruft die Erweiterung VMAccess namens ContosoTest für den virtuellen Computer "VirtualMachine07" ab.</span><span class="sxs-lookup"><span data-stu-id="d775d-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="d775d-110">Beispiel 2: Anzeigen der Instanzansicht der Erweiterung VMAccess</span><span class="sxs-lookup"><span data-stu-id="d775d-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="d775d-111">Dieser Befehl ruft die Instanzansicht der Erweiterung VMAccess namens ContosoTest für den virtuellen Computer "VirtualMachine07" ab.</span><span class="sxs-lookup"><span data-stu-id="d775d-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="d775d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d775d-112">PARAMETERS</span></span>

### <span data-ttu-id="d775d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d775d-113">-DefaultProfile</span></span>
<span data-ttu-id="d775d-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d775d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d775d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d775d-115">-Name</span></span>
<span data-ttu-id="d775d-116">Gibt den Namen der Erweiterung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d775d-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d775d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d775d-117">-ResourceGroupName</span></span>
<span data-ttu-id="d775d-118">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="d775d-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d775d-119">-Status</span><span class="sxs-lookup"><span data-stu-id="d775d-119">-Status</span></span>
<span data-ttu-id="d775d-120">Gibt an, dass dieses Cmdlet nur die Instanzansicht der Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="d775d-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="d775d-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="d775d-121">-VMName</span></span>
<span data-ttu-id="d775d-122">Gibt den Namen eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="d775d-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d775d-123">Dieses Cmdlet ruft Informationen zu VMAccess für den virtuellen Computer ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d775d-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="d775d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d775d-124">CommonParameters</span></span>
<span data-ttu-id="d775d-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d775d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d775d-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d775d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d775d-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d775d-127">INPUTS</span></span>

### <span data-ttu-id="d775d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d775d-128">System.String</span></span>

### <span data-ttu-id="d775d-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d775d-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d775d-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d775d-130">OUTPUTS</span></span>

### <span data-ttu-id="d775d-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="d775d-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="d775d-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d775d-132">NOTES</span></span>

## <span data-ttu-id="d775d-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d775d-133">RELATED LINKS</span></span>

[<span data-ttu-id="d775d-134">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d775d-134">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="d775d-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d775d-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="d775d-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="d775d-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)


