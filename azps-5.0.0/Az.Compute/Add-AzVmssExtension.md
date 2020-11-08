---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 87ea9af1980948f28477a9f483b3c6429df98d12
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175935"
---
# <span data-ttu-id="a547e-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a547e-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="a547e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a547e-102">SYNOPSIS</span></span>
<span data-ttu-id="a547e-103">Fügt der VMSS eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="a547e-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="a547e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a547e-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a547e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a547e-105">DESCRIPTION</span></span>
<span data-ttu-id="a547e-106">Das **Add-AzVmssExtension-** Cmdlet fügt dem virtuellen Computer-Skalierungs Satz (VMSS) eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="a547e-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="a547e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a547e-107">EXAMPLES</span></span>

### <span data-ttu-id="a547e-108">Beispiel 1: Hinzufügen einer Erweiterung zum VMSS</span><span class="sxs-lookup"><span data-stu-id="a547e-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="a547e-109">Mit diesem Befehl wird der VMSS eine Erweiterung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a547e-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="a547e-110">Beispiel 2: Hinzufügen einer Erweiterung zum VMSS mit Einstellungen und geschützten Einstellungen</span><span class="sxs-lookup"><span data-stu-id="a547e-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="a547e-111">Dieser Befehl fügt der VMSS eine Erweiterung mit einem Beispiel-bash-Skript auf einem BLOB-Speicher hinzu, geben Sie die URL des BLOB-Speichers und ausführbaren Befehls in Einstellungen und Sicherheitszugriff in geschützten Einstellungen an.</span><span class="sxs-lookup"><span data-stu-id="a547e-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="a547e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a547e-112">PARAMETERS</span></span>

### <span data-ttu-id="a547e-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a547e-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="a547e-114">Gibt an, ob die Erweiterungsversion automatisch auf eine neuere Nebenversion aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a547e-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="a547e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a547e-115">-DefaultProfile</span></span>
<span data-ttu-id="a547e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a547e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a547e-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="a547e-117">-ForceUpdateTag</span></span>
<span data-ttu-id="a547e-118">Wenn ein Wert angegeben wird, der vom vorherigen Wert abweicht, wird der Erweiterungshandler auch dann aktualisiert, wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="a547e-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="a547e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a547e-119">-Name</span></span>
<span data-ttu-id="a547e-120">Gibt den Namen der Erweiterung an, die von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="a547e-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="a547e-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="a547e-121">-ProtectedSetting</span></span>
<span data-ttu-id="a547e-122">Gibt die private Konfiguration für die Erweiterung als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="a547e-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="a547e-123">Dieses Cmdlet verschlüsselt die private Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a547e-123">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="a547e-124">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="a547e-124">-ProvisionAfterExtension</span></span>
<span data-ttu-id="a547e-125">Sammlung von Erweiterungsnamen, nach denen diese Erweiterung bereitgestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="a547e-125">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="a547e-126">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a547e-126">-Publisher</span></span>
<span data-ttu-id="a547e-127">Gibt den Namen des Erweiterungs Herausgebers an.</span><span class="sxs-lookup"><span data-stu-id="a547e-127">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="a547e-128">Der Herausgeber gibt einen Namen an, wenn der Herausgeber eine Erweiterung registriert.</span><span class="sxs-lookup"><span data-stu-id="a547e-128">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="a547e-129">Dies kann das Cmdlet [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) verwenden, um den Verleger abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a547e-129">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="a547e-130">-Einstellung</span><span class="sxs-lookup"><span data-stu-id="a547e-130">-Setting</span></span>
<span data-ttu-id="a547e-131">Gibt die öffentliche Konfiguration als Zeichenfolge für die Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="a547e-131">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="a547e-132">Dieses Cmdlet verschlüsselt keine öffentliche Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a547e-132">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="a547e-133">-Typ</span><span class="sxs-lookup"><span data-stu-id="a547e-133">-Type</span></span>
<span data-ttu-id="a547e-134">Gibt den Erweiterungstyp an.</span><span class="sxs-lookup"><span data-stu-id="a547e-134">Specifies the extension type.</span></span>
<span data-ttu-id="a547e-135">Sie können das Cmdlet [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) verwenden, um den Erweiterungstyp abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a547e-135">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="a547e-136">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a547e-136">-TypeHandlerVersion</span></span>
<span data-ttu-id="a547e-137">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a547e-137">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="a547e-138">Sie können das Cmdlet [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) verwenden, um die Version der Erweiterung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a547e-138">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="a547e-139">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a547e-139">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a547e-140">Geben Sie das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a547e-140">Specify the VMSS object.</span></span>
<span data-ttu-id="a547e-141">Sie können das [New-AzVmssConfig-](./New-AzVmssConfig.md) Objekt verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a547e-141">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="a547e-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a547e-142">-Confirm</span></span>
<span data-ttu-id="a547e-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a547e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a547e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a547e-144">-WhatIf</span></span>
<span data-ttu-id="a547e-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a547e-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a547e-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a547e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a547e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a547e-147">CommonParameters</span></span>
<span data-ttu-id="a547e-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a547e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a547e-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a547e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a547e-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a547e-150">INPUTS</span></span>

### <span data-ttu-id="a547e-151">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a547e-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="a547e-152">System. String</span><span class="sxs-lookup"><span data-stu-id="a547e-152">System.String</span></span>

### <span data-ttu-id="a547e-153">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a547e-153">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a547e-154">System. Object</span><span class="sxs-lookup"><span data-stu-id="a547e-154">System.Object</span></span>

## <span data-ttu-id="a547e-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a547e-155">OUTPUTS</span></span>

### <span data-ttu-id="a547e-156">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a547e-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a547e-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="a547e-157">NOTES</span></span>

## <span data-ttu-id="a547e-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a547e-158">RELATED LINKS</span></span>

[<span data-ttu-id="a547e-159">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a547e-159">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="a547e-160">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a547e-160">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="a547e-161">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="a547e-161">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="a547e-162">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="a547e-162">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="a547e-163">Neu – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a547e-163">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
