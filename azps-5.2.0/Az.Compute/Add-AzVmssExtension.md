---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 87ea9af1980948f28477a9f483b3c6429df98d12
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370780"
---
# <span data-ttu-id="83f29-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="83f29-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="83f29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83f29-102">SYNOPSIS</span></span>
<span data-ttu-id="83f29-103">Fügt dem VMSS eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="83f29-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="83f29-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83f29-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83f29-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="83f29-105">DESCRIPTION</span></span>
<span data-ttu-id="83f29-106">Das **Cmdlet "Add-AzVmssExtension"** fügt dem Virtual Machine Scale Set (VMSS) eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="83f29-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="83f29-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="83f29-107">EXAMPLES</span></span>

### <span data-ttu-id="83f29-108">Beispiel 1: Hinzufügen einer Erweiterung zu VMSS</span><span class="sxs-lookup"><span data-stu-id="83f29-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="83f29-109">Dieser Befehl fügt dem VMSS eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="83f29-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="83f29-110">Beispiel 2: Hinzufügen einer Erweiterung zu VMSS mit Einstellungen und geschützten Einstellungen</span><span class="sxs-lookup"><span data-stu-id="83f29-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="83f29-111">Dieser Befehl fügt dem VMSS eine Erweiterung mit einem Beispiel-Bash-Skript für einen BLOB-Speicher hinzu, und geben Sie die URL des BLOB-Speichers und ausführbaren Befehls in den Einstellungen und dem Sicherheitszugriff in den geschützten Einstellungen an.</span><span class="sxs-lookup"><span data-stu-id="83f29-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="83f29-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83f29-112">PARAMETERS</span></span>

### <span data-ttu-id="83f29-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="83f29-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="83f29-114">Gibt an, ob die Erweiterungsversion automatisch auf eine neuere Nebenversion aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="83f29-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="83f29-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83f29-115">-DefaultProfile</span></span>
<span data-ttu-id="83f29-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83f29-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83f29-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="83f29-117">-ForceUpdateTag</span></span>
<span data-ttu-id="83f29-118">Wenn ein Wert angegeben wird und sich vom vorherigen Wert abwechselt, ist der Erweiterungshandler gezwungen, eine Aktualisierung selbst dann zu aktualisieren, wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="83f29-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="83f29-119">-Name</span><span class="sxs-lookup"><span data-stu-id="83f29-119">-Name</span></span>
<span data-ttu-id="83f29-120">Gibt den Namen der Erweiterung an, die dieses Cmdlet hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="83f29-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="83f29-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="83f29-121">-ProtectedSetting</span></span>
<span data-ttu-id="83f29-122">Gibt die private Konfiguration für die Erweiterung als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="83f29-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="83f29-123">Dieses Cmdlet verschlüsselt die private Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="83f29-123">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="83f29-124">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="83f29-124">-ProvisionAfterExtension</span></span>
<span data-ttu-id="83f29-125">Sammlung von Erweiterungsnamen, nach denen diese Erweiterung bereitgestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="83f29-125">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="83f29-126">-Publisher</span><span class="sxs-lookup"><span data-stu-id="83f29-126">-Publisher</span></span>
<span data-ttu-id="83f29-127">Gibt den Namen des Erweiterungsherausgebers an.</span><span class="sxs-lookup"><span data-stu-id="83f29-127">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="83f29-128">Der Herausgeber gibt einen Namen an, wenn der Herausgeber eine Erweiterung registriert.</span><span class="sxs-lookup"><span data-stu-id="83f29-128">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="83f29-129">Dies kann das [Cmdlet "Get-AzVMImagePublisher"](./Get-AzVMImagePublisher.md) verwenden, um den Herausgeber zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="83f29-129">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="83f29-130">-Einstellung</span><span class="sxs-lookup"><span data-stu-id="83f29-130">-Setting</span></span>
<span data-ttu-id="83f29-131">Gibt die öffentliche Konfiguration als Zeichenfolge für die Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="83f29-131">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="83f29-132">Mit diesem Cmdlet wird die öffentliche Konfiguration nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="83f29-132">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="83f29-133">-Type</span><span class="sxs-lookup"><span data-stu-id="83f29-133">-Type</span></span>
<span data-ttu-id="83f29-134">Gibt den Erweiterungstyp an.</span><span class="sxs-lookup"><span data-stu-id="83f29-134">Specifies the extension type.</span></span>
<span data-ttu-id="83f29-135">Sie können das [Cmdlet "Get-AzVMExtensionImageType"](./Get-AzVMExtensionImageType.md) verwenden, um den Erweiterungstyp zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="83f29-135">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="83f29-136">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="83f29-136">-TypeHandlerVersion</span></span>
<span data-ttu-id="83f29-137">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="83f29-137">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="83f29-138">Sie können das [Cmdlet "Get-AzVMExtensionImage"](./Get-AzVMExtensionImage.md) verwenden, um die Version der Erweiterung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="83f29-138">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="83f29-139">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="83f29-139">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="83f29-140">Geben Sie das "VMSS"-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="83f29-140">Specify the VMSS object.</span></span>
<span data-ttu-id="83f29-141">Sie können ["New-AzVmssConfig" verwenden,](./New-AzVmssConfig.md) um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="83f29-141">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="83f29-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83f29-142">-Confirm</span></span>
<span data-ttu-id="83f29-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="83f29-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83f29-144">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="83f29-144">-WhatIf</span></span>
<span data-ttu-id="83f29-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83f29-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83f29-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="83f29-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83f29-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83f29-147">CommonParameters</span></span>
<span data-ttu-id="83f29-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83f29-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83f29-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83f29-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83f29-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="83f29-150">INPUTS</span></span>

### <span data-ttu-id="83f29-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="83f29-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="83f29-152">System.String</span><span class="sxs-lookup"><span data-stu-id="83f29-152">System.String</span></span>

### <span data-ttu-id="83f29-153">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="83f29-153">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="83f29-154">System.Object</span><span class="sxs-lookup"><span data-stu-id="83f29-154">System.Object</span></span>

## <span data-ttu-id="83f29-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="83f29-155">OUTPUTS</span></span>

### <span data-ttu-id="83f29-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="83f29-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="83f29-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="83f29-157">NOTES</span></span>

## <span data-ttu-id="83f29-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="83f29-158">RELATED LINKS</span></span>

[<span data-ttu-id="83f29-159">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="83f29-159">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="83f29-160">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="83f29-160">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="83f29-161">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="83f29-161">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="83f29-162">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="83f29-162">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="83f29-163">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="83f29-163">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
