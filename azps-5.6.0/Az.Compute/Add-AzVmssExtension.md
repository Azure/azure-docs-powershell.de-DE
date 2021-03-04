---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 774fb61f2394c5634c8415a7a18ce63f4e696a3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938904"
---
# <span data-ttu-id="22ce7-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="22ce7-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="22ce7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="22ce7-103">Fügt dem VMSS eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="22ce7-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="22ce7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22ce7-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22ce7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22ce7-105">DESCRIPTION</span></span>
<span data-ttu-id="22ce7-106">Das **Add-AzVmssExtension-Cmdlet** fügt dem VmSS (Virtual Machine Scale Set) eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="22ce7-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="22ce7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="22ce7-107">EXAMPLES</span></span>

### <span data-ttu-id="22ce7-108">Beispiel 1: Hinzufügen einer Erweiterung zum VMSS</span><span class="sxs-lookup"><span data-stu-id="22ce7-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="22ce7-109">Dieser Befehl fügt dem VMSS eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="22ce7-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="22ce7-110">Beispiel 2: Hinzufügen einer Erweiterung zum VMSS mit Einstellungen und geschützten Einstellungen</span><span class="sxs-lookup"><span data-stu-id="22ce7-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="22ce7-111">Dieser Befehl fügt dem VMSS eine Erweiterung mit einem Beispiel-Bash-Skript für einen Blobspeicher hinzu, und geben Sie die URL des Blobspeichers und des ausführbaren Befehls in Den Einstellungen und dem Sicherheitszugriff in geschützten Einstellungen an.</span><span class="sxs-lookup"><span data-stu-id="22ce7-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="22ce7-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="22ce7-112">PARAMETERS</span></span>

### <span data-ttu-id="22ce7-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="22ce7-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="22ce7-114">Gibt an, ob die Erweiterungsversion automatisch auf eine neuere Nebenversion aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="22ce7-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ce7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ce7-115">-DefaultProfile</span></span>
<span data-ttu-id="22ce7-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22ce7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22ce7-117">-EnableAutomaticUpgrade</span><span class="sxs-lookup"><span data-stu-id="22ce7-117">-EnableAutomaticUpgrade</span></span>
<span data-ttu-id="22ce7-118">Gibt an, ob die Erweiterung automatisch von der Plattform aktualisiert werden soll, wenn eine neuere Version der Erweiterung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="22ce7-118">Indicates whether the extension should be automatically upgraded by the platform if there is a newer version of the extension available.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ce7-119">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="22ce7-119">-ForceUpdateTag</span></span>
<span data-ttu-id="22ce7-120">Wenn ein Wert angegeben wird und sich vom vorherigen Wert abwechselt, wird der Erweiterungshandler gezwungen, zu aktualisieren, auch wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="22ce7-120">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ce7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="22ce7-121">-Name</span></span>
<span data-ttu-id="22ce7-122">Gibt den Namen der Erweiterung an, die von diesem Cmdlet addiert wird.</span><span class="sxs-lookup"><span data-stu-id="22ce7-122">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ce7-123">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="22ce7-123">-ProtectedSetting</span></span>
<span data-ttu-id="22ce7-124">Gibt die private Konfiguration für die Erweiterung als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="22ce7-124">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="22ce7-125">Dieses Cmdlet verschlüsselt die private Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="22ce7-125">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ce7-126">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="22ce7-126">-ProvisionAfterExtension</span></span>
<span data-ttu-id="22ce7-127">Sammlung von Erweiterungsnamen, nach der diese Erweiterung bereitgestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="22ce7-127">Collection of extension names after which this extension needs to be provisioned.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ce7-128">-Publisher</span><span class="sxs-lookup"><span data-stu-id="22ce7-128">-Publisher</span></span>
<span data-ttu-id="22ce7-129">Gibt den Namen des Erweiterungsherausgebers an.</span><span class="sxs-lookup"><span data-stu-id="22ce7-129">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="22ce7-130">Der Herausgeber gibt einen Namen an, wenn der Herausgeber eine Erweiterung registriert.</span><span class="sxs-lookup"><span data-stu-id="22ce7-130">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="22ce7-131">Dies kann das [Get-AzVMImagePublisher-Cmdlet](./Get-AzVMImagePublisher.md) verwenden, um den Herausgeber zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="22ce7-131">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ce7-132">-Einstellung</span><span class="sxs-lookup"><span data-stu-id="22ce7-132">-Setting</span></span>
<span data-ttu-id="22ce7-133">Gibt die öffentliche Konfiguration als Zeichenfolge für die Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="22ce7-133">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="22ce7-134">Dieses Cmdlet verschlüsselt die öffentliche Konfiguration nicht.</span><span class="sxs-lookup"><span data-stu-id="22ce7-134">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ce7-135">-Type</span><span class="sxs-lookup"><span data-stu-id="22ce7-135">-Type</span></span>
<span data-ttu-id="22ce7-136">Gibt den Erweiterungstyp an.</span><span class="sxs-lookup"><span data-stu-id="22ce7-136">Specifies the extension type.</span></span>
<span data-ttu-id="22ce7-137">Sie können das [Get-AzVMExtensionImageType-Cmdlet](./Get-AzVMExtensionImageType.md) verwenden, um den Erweiterungstyp zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="22ce7-137">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ce7-138">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="22ce7-138">-TypeHandlerVersion</span></span>
<span data-ttu-id="22ce7-139">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="22ce7-139">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="22ce7-140">Sie können das [Get-AzVMExtensionImage-Cmdlet](./Get-AzVMExtensionImage.md) verwenden, um die Version der Erweiterung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="22ce7-140">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ce7-141">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="22ce7-141">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="22ce7-142">Geben Sie das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="22ce7-142">Specify the VMSS object.</span></span>
<span data-ttu-id="22ce7-143">Sie können die [New-AzVmssConfig verwenden,](./New-AzVmssConfig.md) um das -Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="22ce7-143">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="22ce7-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="22ce7-144">-Confirm</span></span>
<span data-ttu-id="22ce7-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="22ce7-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22ce7-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22ce7-146">-WhatIf</span></span>
<span data-ttu-id="22ce7-147">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="22ce7-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22ce7-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="22ce7-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22ce7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ce7-149">CommonParameters</span></span>
<span data-ttu-id="22ce7-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22ce7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ce7-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22ce7-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ce7-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="22ce7-152">INPUTS</span></span>

### <span data-ttu-id="22ce7-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="22ce7-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="22ce7-154">System.String</span><span class="sxs-lookup"><span data-stu-id="22ce7-154">System.String</span></span>

### <span data-ttu-id="22ce7-155">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="22ce7-155">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="22ce7-156">System.Object</span><span class="sxs-lookup"><span data-stu-id="22ce7-156">System.Object</span></span>

## <span data-ttu-id="22ce7-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="22ce7-157">OUTPUTS</span></span>

### <span data-ttu-id="22ce7-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="22ce7-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="22ce7-159">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="22ce7-159">NOTES</span></span>

## <span data-ttu-id="22ce7-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="22ce7-160">RELATED LINKS</span></span>

[<span data-ttu-id="22ce7-161">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="22ce7-161">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="22ce7-162">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="22ce7-162">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="22ce7-163">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="22ce7-163">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="22ce7-164">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="22ce7-164">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="22ce7-165">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="22ce7-165">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
