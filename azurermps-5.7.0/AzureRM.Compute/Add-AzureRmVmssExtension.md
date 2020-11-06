---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: 20446fc7c93000b29680689001d9e3c40c4862e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476997"
---
# <span data-ttu-id="ae4c7-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ae4c7-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="ae4c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ae4c7-102">SYNOPSIS</span></span>
<span data-ttu-id="ae4c7-103">Fügt der VMSS eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae4c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae4c7-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae4c7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae4c7-105">DESCRIPTION</span></span>
<span data-ttu-id="ae4c7-106">Das **Add-AzureRmVmssExtension-** Cmdlet fügt dem virtuellen Computer-Skalierungs Satz (VMSS) eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="ae4c7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae4c7-107">EXAMPLES</span></span>

### <span data-ttu-id="ae4c7-108">Beispiel 1: Hinzufügen einer Erweiterung zum VMSS</span><span class="sxs-lookup"><span data-stu-id="ae4c7-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="ae4c7-109">Mit diesem Befehl wird der VMMS eine Erweiterung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="ae4c7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae4c7-110">PARAMETERS</span></span>

### <span data-ttu-id="ae4c7-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="ae4c7-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="ae4c7-112">Gibt an, ob die Erweiterungsversion automatisch auf eine neuere Nebenversion aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="ae4c7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ae4c7-113">-Name</span></span>
<span data-ttu-id="ae4c7-114">Gibt den Namen der Erweiterung an, die von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-114">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="ae4c7-115">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="ae4c7-115">-ProtectedSetting</span></span>
<span data-ttu-id="ae4c7-116">Gibt die private Konfiguration für die Erweiterung als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-116">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="ae4c7-117">Dieses Cmdlet verschlüsselt die private Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-117">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="ae4c7-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ae4c7-118">-Publisher</span></span>
<span data-ttu-id="ae4c7-119">Gibt den Namen des Erweiterungs Herausgebers an.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-119">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="ae4c7-120">Der Herausgeber gibt einen Namen an, wenn der Herausgeber eine Erweiterung registriert.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-120">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="ae4c7-121">Dies kann das Cmdlet [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) verwenden, um den Verleger abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-121">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="ae4c7-122">-Einstellung</span><span class="sxs-lookup"><span data-stu-id="ae4c7-122">-Setting</span></span>
<span data-ttu-id="ae4c7-123">Gibt die öffentliche Konfiguration als Zeichenfolge für die Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-123">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="ae4c7-124">Dieses Cmdlet verschlüsselt keine öffentliche Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-124">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="ae4c7-125">-Typ</span><span class="sxs-lookup"><span data-stu-id="ae4c7-125">-Type</span></span>
<span data-ttu-id="ae4c7-126">Gibt den Erweiterungstyp an.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-126">Specifies the extension type.</span></span>
<span data-ttu-id="ae4c7-127">Sie können das Cmdlet [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) verwenden, um den Erweiterungstyp abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-127">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="ae4c7-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="ae4c7-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="ae4c7-129">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-129">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="ae4c7-130">Sie können das Cmdlet [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) verwenden, um die Version der Erweiterung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-130">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="ae4c7-131">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ae4c7-131">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ae4c7-132">Geben Sie das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-132">Specify the VMSS object.</span></span>
<span data-ttu-id="ae4c7-133">Sie können das [New-AzureRmVmssConfig-](./New-AzureRmVmssConfig.md) Objekt verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-133">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae4c7-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ae4c7-134">-Confirm</span></span>
<span data-ttu-id="ae4c7-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae4c7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae4c7-136">-WhatIf</span></span>
<span data-ttu-id="ae4c7-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae4c7-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae4c7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae4c7-139">CommonParameters</span></span>
<span data-ttu-id="ae4c7-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae4c7-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae4c7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae4c7-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ae4c7-142">INPUTS</span></span>

### <span data-ttu-id="ae4c7-143">Keine</span><span class="sxs-lookup"><span data-stu-id="ae4c7-143">None</span></span>
<span data-ttu-id="ae4c7-144">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ae4c7-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ae4c7-145">OUTPUTS</span></span>

###  
<span data-ttu-id="ae4c7-146">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-146">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="ae4c7-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="ae4c7-147">NOTES</span></span>

## <span data-ttu-id="ae4c7-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ae4c7-148">RELATED LINKS</span></span>

[<span data-ttu-id="ae4c7-149">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ae4c7-149">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="ae4c7-150">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="ae4c7-150">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="ae4c7-151">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="ae4c7-151">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="ae4c7-152">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="ae4c7-152">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="ae4c7-153">Neu – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ae4c7-153">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
