---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 97c8824bca395ddd8fb23ebb4750ab35931c5d51
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844711"
---
# <span data-ttu-id="09e8c-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="09e8c-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="09e8c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="09e8c-103">Fügt der VMSS eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="09e8c-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="09e8c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09e8c-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="09e8c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09e8c-105">DESCRIPTION</span></span>
<span data-ttu-id="09e8c-106">Das **Add-AzVmssExtension-** Cmdlet fügt dem virtuellen Computer-Skalierungs Satz (VMSS) eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="09e8c-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="09e8c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09e8c-107">EXAMPLES</span></span>

### <span data-ttu-id="09e8c-108">Beispiel 1: Hinzufügen einer Erweiterung zum VMSS</span><span class="sxs-lookup"><span data-stu-id="09e8c-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="09e8c-109">Mit diesem Befehl wird der VMMS eine Erweiterung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="09e8c-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="09e8c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="09e8c-110">PARAMETERS</span></span>

### <span data-ttu-id="09e8c-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="09e8c-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="09e8c-112">Gibt an, ob die Erweiterungsversion automatisch auf eine neuere Nebenversion aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="09e8c-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09e8c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09e8c-113">-DefaultProfile</span></span>
<span data-ttu-id="09e8c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="09e8c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e8c-115">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="09e8c-115">-ForceUpdateTag</span></span>
<span data-ttu-id="09e8c-116">Wenn ein Wert angegeben wird, der vom vorherigen Wert abweicht, wird der Erweiterungshandler auch dann aktualisiert, wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="09e8c-116">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09e8c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="09e8c-117">-Name</span></span>
<span data-ttu-id="09e8c-118">Gibt den Namen der Erweiterung an, die von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="09e8c-118">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09e8c-119">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="09e8c-119">-ProtectedSetting</span></span>
<span data-ttu-id="09e8c-120">Gibt die private Konfiguration für die Erweiterung als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="09e8c-120">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="09e8c-121">Dieses Cmdlet verschlüsselt die private Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="09e8c-121">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09e8c-122">-Publisher</span><span class="sxs-lookup"><span data-stu-id="09e8c-122">-Publisher</span></span>
<span data-ttu-id="09e8c-123">Gibt den Namen des Erweiterungs Herausgebers an.</span><span class="sxs-lookup"><span data-stu-id="09e8c-123">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="09e8c-124">Der Herausgeber gibt einen Namen an, wenn der Herausgeber eine Erweiterung registriert.</span><span class="sxs-lookup"><span data-stu-id="09e8c-124">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="09e8c-125">Dies kann das Cmdlet [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) verwenden, um den Verleger abzurufen.</span><span class="sxs-lookup"><span data-stu-id="09e8c-125">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09e8c-126">-Einstellung</span><span class="sxs-lookup"><span data-stu-id="09e8c-126">-Setting</span></span>
<span data-ttu-id="09e8c-127">Gibt die öffentliche Konfiguration als Zeichenfolge für die Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="09e8c-127">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="09e8c-128">Dieses Cmdlet verschlüsselt keine öffentliche Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="09e8c-128">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09e8c-129">-Typ</span><span class="sxs-lookup"><span data-stu-id="09e8c-129">-Type</span></span>
<span data-ttu-id="09e8c-130">Gibt den Erweiterungstyp an.</span><span class="sxs-lookup"><span data-stu-id="09e8c-130">Specifies the extension type.</span></span>
<span data-ttu-id="09e8c-131">Sie können das Cmdlet [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) verwenden, um den Erweiterungstyp abzurufen.</span><span class="sxs-lookup"><span data-stu-id="09e8c-131">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09e8c-132">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="09e8c-132">-TypeHandlerVersion</span></span>
<span data-ttu-id="09e8c-133">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="09e8c-133">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="09e8c-134">Sie können das Cmdlet [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) verwenden, um die Version der Erweiterung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="09e8c-134">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09e8c-135">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="09e8c-135">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="09e8c-136">Geben Sie das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="09e8c-136">Specify the VMSS object.</span></span>
<span data-ttu-id="09e8c-137">Sie können das [New-AzVmssConfig-](./New-AzVmssConfig.md) Objekt verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="09e8c-137">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09e8c-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="09e8c-138">-Confirm</span></span>
<span data-ttu-id="09e8c-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="09e8c-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e8c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09e8c-140">-WhatIf</span></span>
<span data-ttu-id="09e8c-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09e8c-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09e8c-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="09e8c-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e8c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09e8c-143">CommonParameters</span></span>
<span data-ttu-id="09e8c-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09e8c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09e8c-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09e8c-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09e8c-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09e8c-146">INPUTS</span></span>

### <span data-ttu-id="09e8c-147">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="09e8c-147">VirtualMachineScaleSet</span></span>
<span data-ttu-id="09e8c-148">Der Parameter "VirtualMachineScaleSet" akzeptiert den Wert vom Typ "VirtualMachineScaleSet" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="09e8c-148">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="09e8c-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09e8c-149">OUTPUTS</span></span>

###  
<span data-ttu-id="09e8c-150">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="09e8c-150">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="09e8c-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="09e8c-151">NOTES</span></span>

## <span data-ttu-id="09e8c-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09e8c-152">RELATED LINKS</span></span>

[<span data-ttu-id="09e8c-153">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="09e8c-153">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="09e8c-154">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="09e8c-154">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="09e8c-155">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="09e8c-155">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="09e8c-156">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="09e8c-156">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="09e8c-157">Neu – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="09e8c-157">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
