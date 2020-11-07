---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssextension
schema: 2.0.0
ms.openlocfilehash: f69b8901b2bc2c07bdf158da4c92deba0330109d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848340"
---
# <span data-ttu-id="f75b4-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="f75b4-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="f75b4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f75b4-102">SYNOPSIS</span></span>
<span data-ttu-id="f75b4-103">Fügt der VMSS eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="f75b4-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f75b4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f75b4-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f75b4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f75b4-105">DESCRIPTION</span></span>
<span data-ttu-id="f75b4-106">Das **Add-AzureRmVmssExtension-** Cmdlet fügt dem virtuellen Computer-Skalierungs Satz (VMSS) eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="f75b4-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="f75b4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f75b4-107">EXAMPLES</span></span>

### <span data-ttu-id="f75b4-108">Beispiel 1: Hinzufügen einer Erweiterung zum VMSS</span><span class="sxs-lookup"><span data-stu-id="f75b4-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="f75b4-109">Mit diesem Befehl wird der VMMS eine Erweiterung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f75b4-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="f75b4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f75b4-110">PARAMETERS</span></span>

### <span data-ttu-id="f75b4-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f75b4-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="f75b4-112">Gibt an, ob die Erweiterungsversion automatisch auf eine neuere Nebenversion aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f75b4-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="f75b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f75b4-113">-DefaultProfile</span></span>
<span data-ttu-id="f75b4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f75b4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f75b4-115">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="f75b4-115">-ForceUpdateTag</span></span>
<span data-ttu-id="f75b4-116">Wenn ein Wert angegeben wird, der vom vorherigen Wert abweicht, wird der Erweiterungshandler auch dann aktualisiert, wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="f75b4-116">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="f75b4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f75b4-117">-Name</span></span>
<span data-ttu-id="f75b4-118">Gibt den Namen der Erweiterung an, die von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f75b4-118">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="f75b4-119">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="f75b4-119">-ProtectedSetting</span></span>
<span data-ttu-id="f75b4-120">Gibt die private Konfiguration für die Erweiterung als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="f75b4-120">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="f75b4-121">Dieses Cmdlet verschlüsselt die private Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f75b4-121">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="f75b4-122">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f75b4-122">-Publisher</span></span>
<span data-ttu-id="f75b4-123">Gibt den Namen des Erweiterungs Herausgebers an.</span><span class="sxs-lookup"><span data-stu-id="f75b4-123">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="f75b4-124">Der Herausgeber gibt einen Namen an, wenn der Herausgeber eine Erweiterung registriert.</span><span class="sxs-lookup"><span data-stu-id="f75b4-124">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="f75b4-125">Dies kann das Cmdlet [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) verwenden, um den Verleger abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f75b4-125">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="f75b4-126">-Einstellung</span><span class="sxs-lookup"><span data-stu-id="f75b4-126">-Setting</span></span>
<span data-ttu-id="f75b4-127">Gibt die öffentliche Konfiguration als Zeichenfolge für die Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="f75b4-127">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="f75b4-128">Dieses Cmdlet verschlüsselt keine öffentliche Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f75b4-128">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="f75b4-129">-Typ</span><span class="sxs-lookup"><span data-stu-id="f75b4-129">-Type</span></span>
<span data-ttu-id="f75b4-130">Gibt den Erweiterungstyp an.</span><span class="sxs-lookup"><span data-stu-id="f75b4-130">Specifies the extension type.</span></span>
<span data-ttu-id="f75b4-131">Sie können das Cmdlet [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) verwenden, um den Erweiterungstyp abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f75b4-131">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="f75b4-132">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f75b4-132">-TypeHandlerVersion</span></span>
<span data-ttu-id="f75b4-133">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f75b4-133">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="f75b4-134">Sie können das Cmdlet [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) verwenden, um die Version der Erweiterung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f75b4-134">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="f75b4-135">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f75b4-135">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f75b4-136">Geben Sie das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f75b4-136">Specify the VMSS object.</span></span>
<span data-ttu-id="f75b4-137">Sie können das [New-AzureRmVmssConfig-](./New-AzureRmVmssConfig.md) Objekt verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f75b4-137">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="f75b4-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f75b4-138">-Confirm</span></span>
<span data-ttu-id="f75b4-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f75b4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f75b4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f75b4-140">-WhatIf</span></span>
<span data-ttu-id="f75b4-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f75b4-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f75b4-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f75b4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f75b4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f75b4-143">CommonParameters</span></span>
<span data-ttu-id="f75b4-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f75b4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f75b4-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f75b4-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f75b4-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f75b4-146">INPUTS</span></span>

### <span data-ttu-id="f75b4-147">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f75b4-147">VirtualMachineScaleSet</span></span>
<span data-ttu-id="f75b4-148">Der Parameter "VirtualMachineScaleSet" akzeptiert den Wert vom Typ "VirtualMachineScaleSet" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f75b4-148">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="f75b4-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f75b4-149">OUTPUTS</span></span>

###  
<span data-ttu-id="f75b4-150">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="f75b4-150">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f75b4-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="f75b4-151">NOTES</span></span>

## <span data-ttu-id="f75b4-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f75b4-152">RELATED LINKS</span></span>

[<span data-ttu-id="f75b4-153">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="f75b4-153">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="f75b4-154">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f75b4-154">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="f75b4-155">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="f75b4-155">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="f75b4-156">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="f75b4-156">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="f75b4-157">Neu – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f75b4-157">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
