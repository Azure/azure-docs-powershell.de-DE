---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: fbf9d8c38c10465c565e40a284171b3232ba2949
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501926"
---
# <span data-ttu-id="cc4a7-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="cc4a7-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="cc4a7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc4a7-102">SYNOPSIS</span></span>
<span data-ttu-id="cc4a7-103">Fügt der VMSS eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc4a7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc4a7-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cc4a7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc4a7-105">DESCRIPTION</span></span>
<span data-ttu-id="cc4a7-106">Das **Add-AzureRmVmssExtension-** Cmdlet fügt dem virtuellen Computer-Skalierungs Satz (VMSS) eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="cc4a7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc4a7-107">EXAMPLES</span></span>

### <span data-ttu-id="cc4a7-108">Beispiel 1: Hinzufügen einer Erweiterung zum VMSS</span><span class="sxs-lookup"><span data-stu-id="cc4a7-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="cc4a7-109">Mit diesem Befehl wird der VMMS eine Erweiterung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="cc4a7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc4a7-110">PARAMETERS</span></span>

### <span data-ttu-id="cc4a7-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="cc4a7-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="cc4a7-112">Gibt an, ob die Erweiterungsversion automatisch auf eine neuere Nebenversion aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="cc4a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc4a7-113">-DefaultProfile</span></span>
<span data-ttu-id="cc4a7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc4a7-115">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="cc4a7-115">-ForceUpdateTag</span></span>
<span data-ttu-id="cc4a7-116">Wenn ein Wert angegeben wird, der vom vorherigen Wert abweicht, wird der Erweiterungshandler auch dann aktualisiert, wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-116">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="cc4a7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cc4a7-117">-Name</span></span>
<span data-ttu-id="cc4a7-118">Gibt den Namen der Erweiterung an, die von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-118">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="cc4a7-119">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="cc4a7-119">-ProtectedSetting</span></span>
<span data-ttu-id="cc4a7-120">Gibt die private Konfiguration für die Erweiterung als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-120">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="cc4a7-121">Dieses Cmdlet verschlüsselt die private Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-121">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="cc4a7-122">-Publisher</span><span class="sxs-lookup"><span data-stu-id="cc4a7-122">-Publisher</span></span>
<span data-ttu-id="cc4a7-123">Gibt den Namen des Erweiterungs Herausgebers an.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-123">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="cc4a7-124">Der Herausgeber gibt einen Namen an, wenn der Herausgeber eine Erweiterung registriert.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-124">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="cc4a7-125">Dies kann das Cmdlet [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) verwenden, um den Verleger abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-125">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="cc4a7-126">-Einstellung</span><span class="sxs-lookup"><span data-stu-id="cc4a7-126">-Setting</span></span>
<span data-ttu-id="cc4a7-127">Gibt die öffentliche Konfiguration als Zeichenfolge für die Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-127">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="cc4a7-128">Dieses Cmdlet verschlüsselt keine öffentliche Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-128">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="cc4a7-129">-Typ</span><span class="sxs-lookup"><span data-stu-id="cc4a7-129">-Type</span></span>
<span data-ttu-id="cc4a7-130">Gibt den Erweiterungstyp an.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-130">Specifies the extension type.</span></span>
<span data-ttu-id="cc4a7-131">Sie können das Cmdlet [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) verwenden, um den Erweiterungstyp abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-131">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="cc4a7-132">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="cc4a7-132">-TypeHandlerVersion</span></span>
<span data-ttu-id="cc4a7-133">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-133">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="cc4a7-134">Sie können das Cmdlet [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) verwenden, um die Version der Erweiterung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-134">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="cc4a7-135">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cc4a7-135">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="cc4a7-136">Geben Sie das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-136">Specify the VMSS object.</span></span>
<span data-ttu-id="cc4a7-137">Sie können das [New-AzureRmVmssConfig-](./New-AzureRmVmssConfig.md) Objekt verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-137">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="cc4a7-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cc4a7-138">-Confirm</span></span>
<span data-ttu-id="cc4a7-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc4a7-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc4a7-140">-WhatIf</span></span>
<span data-ttu-id="cc4a7-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc4a7-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc4a7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc4a7-143">CommonParameters</span></span>
<span data-ttu-id="cc4a7-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc4a7-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc4a7-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc4a7-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc4a7-146">INPUTS</span></span>

## <span data-ttu-id="cc4a7-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc4a7-147">OUTPUTS</span></span>

###  
<span data-ttu-id="cc4a7-148">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-148">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="cc4a7-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc4a7-149">NOTES</span></span>

## <span data-ttu-id="cc4a7-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc4a7-150">RELATED LINKS</span></span>

[<span data-ttu-id="cc4a7-151">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="cc4a7-151">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="cc4a7-152">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="cc4a7-152">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="cc4a7-153">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="cc4a7-153">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="cc4a7-154">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="cc4a7-154">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="cc4a7-155">Neu – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="cc4a7-155">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
