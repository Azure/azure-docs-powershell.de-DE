---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 56973d23e59a3d34b2caadce3677ca0bfd5f3c5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929072"
---
# <span data-ttu-id="717f6-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="717f6-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="717f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="717f6-102">SYNOPSIS</span></span>
<span data-ttu-id="717f6-103">Entfernt die Cheferweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="717f6-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="717f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="717f6-104">SYNTAX</span></span>

### <span data-ttu-id="717f6-105">Linux</span><span class="sxs-lookup"><span data-stu-id="717f6-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="717f6-106">Windows</span><span class="sxs-lookup"><span data-stu-id="717f6-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="717f6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="717f6-107">DESCRIPTION</span></span>
<span data-ttu-id="717f6-108">Das **Cmdlet Remove-AzVMChefExtension** entfernt die Chef-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="717f6-108">The **Remove-AzVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="717f6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="717f6-109">EXAMPLES</span></span>

### <span data-ttu-id="717f6-110">Beispiel 1: Entfernen einer Cheferweiterung von einem virtuellen Windows-Computer</span><span class="sxs-lookup"><span data-stu-id="717f6-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="717f6-111">Mit diesem Befehl wird eine Cheferweiterung von einem Windows-basierten virtuellen Computer namens WindowsVM001 entfernt, der zur Ressourcengruppe "ResourceGroup001" gehört.</span><span class="sxs-lookup"><span data-stu-id="717f6-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="717f6-112">Beispiel 2: Entfernen einer Cheferweiterung von einem virtuellen Linux-Computer</span><span class="sxs-lookup"><span data-stu-id="717f6-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="717f6-113">Mit diesem Befehl wird eine Cheferweiterung von einem linuxbasierten virtuellen Computer namens LinuxVM001 entfernt, der zur Ressourcengruppe "ResourceGroup002" gehört.</span><span class="sxs-lookup"><span data-stu-id="717f6-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="717f6-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="717f6-114">PARAMETERS</span></span>

### <span data-ttu-id="717f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="717f6-115">-DefaultProfile</span></span>
<span data-ttu-id="717f6-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="717f6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="717f6-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="717f6-117">-Linux</span></span>
<span data-ttu-id="717f6-118">Gibt an, dass dieses Cmdlet auf einen virtuellen Linux-Computer zielt.</span><span class="sxs-lookup"><span data-stu-id="717f6-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="717f6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="717f6-119">-Name</span></span>
<span data-ttu-id="717f6-120">Gibt den Namen der Durchwahl "Chef" an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="717f6-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="717f6-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="717f6-121">-NoWait</span></span>
<span data-ttu-id="717f6-122">Startet den Vorgang und gibt sofort zurück, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="717f6-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="717f6-123">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="717f6-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="717f6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="717f6-124">-ResourceGroupName</span></span>
<span data-ttu-id="717f6-125">Gibt den Namen der Ressourcengruppe an, die den virtuellen Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="717f6-125">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="717f6-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="717f6-126">-VMName</span></span>
<span data-ttu-id="717f6-127">Gibt den Namen eines virtuellen Computers an, für den dieses Cmdlet die Cheferweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="717f6-127">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="717f6-128">-Windows</span><span class="sxs-lookup"><span data-stu-id="717f6-128">-Windows</span></span>
<span data-ttu-id="717f6-129">Gibt an, dass dieses Cmdlet auf einen virtuellen Windows-Computer zielt.</span><span class="sxs-lookup"><span data-stu-id="717f6-129">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="717f6-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="717f6-130">-Confirm</span></span>
<span data-ttu-id="717f6-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="717f6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="717f6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="717f6-132">-WhatIf</span></span>
<span data-ttu-id="717f6-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="717f6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="717f6-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="717f6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="717f6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="717f6-135">CommonParameters</span></span>
<span data-ttu-id="717f6-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="717f6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="717f6-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="717f6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="717f6-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="717f6-138">INPUTS</span></span>

### <span data-ttu-id="717f6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="717f6-139">System.String</span></span>

## <span data-ttu-id="717f6-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="717f6-140">OUTPUTS</span></span>

### <span data-ttu-id="717f6-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="717f6-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="717f6-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="717f6-142">NOTES</span></span>

## <span data-ttu-id="717f6-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="717f6-143">RELATED LINKS</span></span>

[<span data-ttu-id="717f6-144">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="717f6-144">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="717f6-145">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="717f6-145">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
