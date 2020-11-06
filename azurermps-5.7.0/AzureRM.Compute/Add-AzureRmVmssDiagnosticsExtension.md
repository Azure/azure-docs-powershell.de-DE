---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 0e28b5df77734645380316af6396f745469637df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499034"
---
# <span data-ttu-id="d62d5-101">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d62d5-101">Add-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="d62d5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d62d5-102">SYNOPSIS</span></span>
<span data-ttu-id="d62d5-103">Fügt der VMSS eine Diagnose Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="d62d5-103">Adds a diagnostics extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d62d5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d62d5-104">SYNTAX</span></span>

```
Add-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d62d5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d62d5-105">DESCRIPTION</span></span>
<span data-ttu-id="d62d5-106">Das **Add-AzureRmVmssDiagnosticsExtension-** Cmdlet fügt der Instanz des virtuellen Computer-Skalierungs Satzes (VMSS) eine Diagnose Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="d62d5-106">The **Add-AzureRmVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="d62d5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d62d5-107">EXAMPLES</span></span>

### <span data-ttu-id="d62d5-108">Beispiel 1: Hinzufügen einer Diagnose Erweiterung zum VMSS</span><span class="sxs-lookup"><span data-stu-id="d62d5-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="d62d5-109">Mit diesem Befehl wird der VMSS eine Diagnose Erweiterung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d62d5-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="d62d5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d62d5-110">PARAMETERS</span></span>

### <span data-ttu-id="d62d5-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d62d5-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d62d5-112">Gibt an, ob mit diesem Cmdlet der Azure Guest-Agent die Erweiterung automatisch auf eine neuere Nebenversion aktualisieren kann.</span><span class="sxs-lookup"><span data-stu-id="d62d5-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="d62d5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d62d5-113">-Force</span></span>
<span data-ttu-id="d62d5-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d62d5-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d62d5-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d62d5-115">-Name</span></span>
<span data-ttu-id="d62d5-116">Gibt den Namen einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="d62d5-116">Specifies the name of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d62d5-117">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="d62d5-117">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="d62d5-118">Gibt den Pfad der privaten Konfigurationsdatei an.</span><span class="sxs-lookup"><span data-stu-id="d62d5-118">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="d62d5-119">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="d62d5-119">-SettingFilePath</span></span>
<span data-ttu-id="d62d5-120">Gibt den Pfad der öffentlichen Konfigurationsdatei an.</span><span class="sxs-lookup"><span data-stu-id="d62d5-120">Specifies the path of the public configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d62d5-121">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d62d5-121">-TypeHandlerVersion</span></span>
<span data-ttu-id="d62d5-122">Gibt die Version der Erweiterung an, die für diesen VMSS verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d62d5-122">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="d62d5-123">Führen Sie zum Abrufen der Version das Cmdlet " [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) " mit einem Wert von "Microsoft. Azure. Diagnostics" für den *PublisherName* -Parameter und IaaSDiagnostics für den *Type* -Parameter aus.</span><span class="sxs-lookup"><span data-stu-id="d62d5-123">To obtain the version, run the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d62d5-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d62d5-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d62d5-125">Geben Sie das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d62d5-125">Specify the VMSS object.</span></span>
<span data-ttu-id="d62d5-126">Sie können das Cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d62d5-126">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="d62d5-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d62d5-127">-Confirm</span></span>
<span data-ttu-id="d62d5-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d62d5-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d62d5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d62d5-129">-WhatIf</span></span>
<span data-ttu-id="d62d5-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d62d5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d62d5-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d62d5-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d62d5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d62d5-132">CommonParameters</span></span>
<span data-ttu-id="d62d5-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d62d5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d62d5-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d62d5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d62d5-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d62d5-135">INPUTS</span></span>

### <span data-ttu-id="d62d5-136">Keine</span><span class="sxs-lookup"><span data-stu-id="d62d5-136">None</span></span>
<span data-ttu-id="d62d5-137">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d62d5-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d62d5-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d62d5-138">OUTPUTS</span></span>

###  
<span data-ttu-id="d62d5-139">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="d62d5-139">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="d62d5-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="d62d5-140">NOTES</span></span>

## <span data-ttu-id="d62d5-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d62d5-141">RELATED LINKS</span></span>

[<span data-ttu-id="d62d5-142">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="d62d5-142">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="d62d5-143">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d62d5-143">Remove-AzureRmVmssDiagnosticsExtension</span></span>](./Remove-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="d62d5-144">Satz-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d62d5-144">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)
