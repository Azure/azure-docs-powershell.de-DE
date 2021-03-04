---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: cc813b4d6b3c5efbd1c54c25b5e198c5b0ce94e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935315"
---
# <span data-ttu-id="c4fae-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="c4fae-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="c4fae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4fae-102">SYNOPSIS</span></span>
<span data-ttu-id="c4fae-103">Entfernt eine Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="c4fae-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="c4fae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4fae-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4fae-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c4fae-105">DESCRIPTION</span></span>
<span data-ttu-id="c4fae-106">Das **Cmdlet Remove-AzVMExtension** entfernt eine Erweiterung aus den Virtual Machine Extensions eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="c4fae-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="c4fae-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c4fae-107">EXAMPLES</span></span>

### <span data-ttu-id="c4fae-108">Beispiel 1: Entfernen einer Erweiterung von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="c4fae-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="c4fae-109">Mit diesem Befehl wird die Erweiterung ContosoTest vom virtuellen Computer "VirtualMachine22" in ResourceGroup11 entfernt.</span><span class="sxs-lookup"><span data-stu-id="c4fae-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="c4fae-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c4fae-110">PARAMETERS</span></span>

### <span data-ttu-id="c4fae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4fae-111">-DefaultProfile</span></span>
<span data-ttu-id="c4fae-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4fae-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4fae-113">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="c4fae-113">-Force</span></span>
<span data-ttu-id="c4fae-114">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="c4fae-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fae-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c4fae-115">-Name</span></span>
<span data-ttu-id="c4fae-116">Gibt den Namen der Erweiterung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c4fae-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c4fae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4fae-117">-ResourceGroupName</span></span>
<span data-ttu-id="c4fae-118">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="c4fae-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c4fae-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="c4fae-119">-VMName</span></span>
<span data-ttu-id="c4fae-120">Gibt den Namen eines virtuellen Computers an, von dem dieses Cmdlet die Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="c4fae-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="c4fae-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c4fae-121">-Confirm</span></span>
<span data-ttu-id="c4fae-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4fae-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fae-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4fae-123">-WhatIf</span></span>
<span data-ttu-id="c4fae-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4fae-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4fae-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4fae-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4fae-126">CommonParameters</span></span>
<span data-ttu-id="c4fae-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4fae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4fae-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4fae-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4fae-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c4fae-129">INPUTS</span></span>

### <span data-ttu-id="c4fae-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c4fae-130">System.String</span></span>

## <span data-ttu-id="c4fae-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c4fae-131">OUTPUTS</span></span>

### <span data-ttu-id="c4fae-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c4fae-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c4fae-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c4fae-133">NOTES</span></span>

## <span data-ttu-id="c4fae-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c4fae-134">RELATED LINKS</span></span>

[<span data-ttu-id="c4fae-135">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="c4fae-135">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="c4fae-136">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="c4fae-136">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


