---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: aeb07f9d9e2faaaf9fc09867fcfee045a5bc8351
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661475"
---
# <span data-ttu-id="dec30-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="dec30-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="dec30-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dec30-102">SYNOPSIS</span></span>
<span data-ttu-id="dec30-103">Entfernt eine Erweiterung aus der VMSS.</span><span class="sxs-lookup"><span data-stu-id="dec30-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="dec30-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dec30-104">SYNTAX</span></span>

### <span data-ttu-id="dec30-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dec30-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dec30-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dec30-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dec30-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dec30-107">DESCRIPTION</span></span>
<span data-ttu-id="dec30-108">Das Cmdlet **Remove-AzVmssExtension** entfernt eine Erweiterung aus dem Skalierungs Satz virtueller Computer (VMSS).</span><span class="sxs-lookup"><span data-stu-id="dec30-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="dec30-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dec30-109">EXAMPLES</span></span>

### <span data-ttu-id="dec30-110">Beispiel 1: Entfernen einer VMSS-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="dec30-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="dec30-111">Dieser Befehl entfernt die Erweiterung eines VMSS und aktualisiert die VMSS nach der Änderung.</span><span class="sxs-lookup"><span data-stu-id="dec30-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="dec30-112">Beispiel 2: Entfernen einer Instanz innerhalb einer VMSS</span><span class="sxs-lookup"><span data-stu-id="dec30-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="dec30-113">Dieser Befehl entfernt die Angabe der Erweiterungs-ID aus dem VMSS, das zur Ressourcengruppe mit dem Namen Group002 gehört.</span><span class="sxs-lookup"><span data-stu-id="dec30-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="dec30-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="dec30-114">PARAMETERS</span></span>

### <span data-ttu-id="dec30-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dec30-115">-DefaultProfile</span></span>
<span data-ttu-id="dec30-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dec30-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dec30-117">-ID</span><span class="sxs-lookup"><span data-stu-id="dec30-117">-Id</span></span>
<span data-ttu-id="dec30-118">Gibt die ID der Erweiterung an, die dieses Cmdlet aus der VMSS entfernt.</span><span class="sxs-lookup"><span data-stu-id="dec30-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec30-119">-Name</span><span class="sxs-lookup"><span data-stu-id="dec30-119">-Name</span></span>
<span data-ttu-id="dec30-120">Gibt den Namen der Erweiterung an, die dieses Cmdlet aus der VMSS entfernt.</span><span class="sxs-lookup"><span data-stu-id="dec30-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec30-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="dec30-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="dec30-122">Gibt den VMSS an, aus dem die Erweiterung entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dec30-122">Specifies the VMSS from which to remove the extension from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dec30-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dec30-123">-Confirm</span></span>
<span data-ttu-id="dec30-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dec30-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dec30-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dec30-125">-WhatIf</span></span>
<span data-ttu-id="dec30-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dec30-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dec30-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dec30-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dec30-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dec30-128">CommonParameters</span></span>
<span data-ttu-id="dec30-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dec30-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dec30-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dec30-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dec30-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dec30-131">INPUTS</span></span>

### <span data-ttu-id="dec30-132">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="dec30-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="dec30-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dec30-133">System.String</span></span>

## <span data-ttu-id="dec30-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dec30-134">OUTPUTS</span></span>

### <span data-ttu-id="dec30-135">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="dec30-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="dec30-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="dec30-136">NOTES</span></span>

## <span data-ttu-id="dec30-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dec30-137">RELATED LINKS</span></span>

[<span data-ttu-id="dec30-138">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="dec30-138">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
