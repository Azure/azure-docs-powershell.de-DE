---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: ad87e4e556263889de23640abad391ee28d7b397
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500241"
---
# <span data-ttu-id="1e896-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="1e896-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="1e896-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e896-102">SYNOPSIS</span></span>
<span data-ttu-id="1e896-103">Fügt der VMSS eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="1e896-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e896-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e896-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e896-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e896-105">DESCRIPTION</span></span>
<span data-ttu-id="1e896-106">Das **Add-AzureRmVmssExtension-** Cmdlet fügt dem virtuellen Computer-Skalierungs Satz (VMSS) eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="1e896-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="1e896-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e896-107">EXAMPLES</span></span>

### <span data-ttu-id="1e896-108">Beispiel 1: Hinzufügen einer Erweiterung zum VMSS</span><span class="sxs-lookup"><span data-stu-id="1e896-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="1e896-109">Mit diesem Befehl wird der VMSS eine Erweiterung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1e896-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="1e896-110">Beispiel 2: Hinzufügen einer Erweiterung zum VMSS mit Einstellungen und geschützten Einstellungen</span><span class="sxs-lookup"><span data-stu-id="1e896-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="1e896-111">Dieser Befehl fügt der VMSS eine Erweiterung mit einem Beispiel-bash-Skript auf einem BLOB-Speicher hinzu, geben Sie die URL des BLOB-Speichers und ausführbaren Befehls in Einstellungen und Sicherheitszugriff in geschützten Einstellungen an.</span><span class="sxs-lookup"><span data-stu-id="1e896-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="1e896-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e896-112">PARAMETERS</span></span>

### <span data-ttu-id="1e896-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1e896-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="1e896-114">Gibt an, ob die Erweiterungsversion automatisch auf eine neuere Nebenversion aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1e896-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="1e896-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e896-115">-DefaultProfile</span></span>
<span data-ttu-id="1e896-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1e896-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e896-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="1e896-117">-ForceUpdateTag</span></span>
<span data-ttu-id="1e896-118">Wenn ein Wert angegeben wird, der vom vorherigen Wert abweicht, wird der Erweiterungshandler auch dann aktualisiert, wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="1e896-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="1e896-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1e896-119">-Name</span></span>
<span data-ttu-id="1e896-120">Gibt den Namen der Erweiterung an, die von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="1e896-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="1e896-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="1e896-121">-ProtectedSetting</span></span>
<span data-ttu-id="1e896-122">Gibt die private Konfiguration für die Erweiterung als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="1e896-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="1e896-123">Dieses Cmdlet verschlüsselt die private Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1e896-123">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="1e896-124">-Publisher</span><span class="sxs-lookup"><span data-stu-id="1e896-124">-Publisher</span></span>
<span data-ttu-id="1e896-125">Gibt den Namen des Erweiterungs Herausgebers an.</span><span class="sxs-lookup"><span data-stu-id="1e896-125">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="1e896-126">Der Herausgeber gibt einen Namen an, wenn der Herausgeber eine Erweiterung registriert.</span><span class="sxs-lookup"><span data-stu-id="1e896-126">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="1e896-127">Dies kann das Cmdlet [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) verwenden, um den Verleger abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1e896-127">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="1e896-128">-Einstellung</span><span class="sxs-lookup"><span data-stu-id="1e896-128">-Setting</span></span>
<span data-ttu-id="1e896-129">Gibt die öffentliche Konfiguration als Zeichenfolge für die Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="1e896-129">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="1e896-130">Dieses Cmdlet verschlüsselt keine öffentliche Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1e896-130">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="1e896-131">-Typ</span><span class="sxs-lookup"><span data-stu-id="1e896-131">-Type</span></span>
<span data-ttu-id="1e896-132">Gibt den Erweiterungstyp an.</span><span class="sxs-lookup"><span data-stu-id="1e896-132">Specifies the extension type.</span></span>
<span data-ttu-id="1e896-133">Sie können das Cmdlet [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) verwenden, um den Erweiterungstyp abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1e896-133">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="1e896-134">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1e896-134">-TypeHandlerVersion</span></span>
<span data-ttu-id="1e896-135">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1e896-135">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="1e896-136">Sie können das Cmdlet [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) verwenden, um die Version der Erweiterung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1e896-136">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="1e896-137">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1e896-137">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1e896-138">Geben Sie das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="1e896-138">Specify the VMSS object.</span></span>
<span data-ttu-id="1e896-139">Sie können das [New-AzureRmVmssConfig-](./New-AzureRmVmssConfig.md) Objekt verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1e896-139">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="1e896-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1e896-140">-Confirm</span></span>
<span data-ttu-id="1e896-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e896-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e896-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e896-142">-WhatIf</span></span>
<span data-ttu-id="1e896-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e896-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e896-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e896-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e896-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e896-145">CommonParameters</span></span>
<span data-ttu-id="1e896-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e896-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e896-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e896-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e896-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e896-148">INPUTS</span></span>

### <span data-ttu-id="1e896-149">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1e896-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="1e896-150">System. String</span><span class="sxs-lookup"><span data-stu-id="1e896-150">System.String</span></span>

### <span data-ttu-id="1e896-151">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1e896-151">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="1e896-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="1e896-152">System.Object</span></span>

## <span data-ttu-id="1e896-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e896-153">OUTPUTS</span></span>

### <span data-ttu-id="1e896-154">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1e896-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="1e896-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e896-155">NOTES</span></span>

## <span data-ttu-id="1e896-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e896-156">RELATED LINKS</span></span>

[<span data-ttu-id="1e896-157">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="1e896-157">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="1e896-158">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="1e896-158">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="1e896-159">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="1e896-159">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="1e896-160">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="1e896-160">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="1e896-161">Neu – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="1e896-161">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
