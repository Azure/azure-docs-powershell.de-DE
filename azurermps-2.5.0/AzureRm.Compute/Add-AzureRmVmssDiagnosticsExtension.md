---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: 8e6a0ec7002f211e660c3ca71d190faf719bbd6c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848543"
---
# <span data-ttu-id="a9fc2-101">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a9fc2-101">Add-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="a9fc2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9fc2-102">SYNOPSIS</span></span>
<span data-ttu-id="a9fc2-103">Fügt der VMSS eine Diagnose Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="a9fc2-103">Adds a diagnostics extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9fc2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9fc2-104">SYNTAX</span></span>

```
Add-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9fc2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9fc2-105">DESCRIPTION</span></span>
<span data-ttu-id="a9fc2-106">Das **Add-AzureRmVmssDiagnosticsExtension-** Cmdlet fügt der Instanz des virtuellen Computer-Skalierungs Satzes (VMSS) eine Diagnose Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="a9fc2-106">The **Add-AzureRmVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="a9fc2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9fc2-107">EXAMPLES</span></span>

### <span data-ttu-id="a9fc2-108">Beispiel 1: Hinzufügen einer Diagnose Erweiterung zum VMSS</span><span class="sxs-lookup"><span data-stu-id="a9fc2-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="a9fc2-109">Mit diesem Befehl wird der VMSS eine Diagnose Erweiterung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a9fc2-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="a9fc2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9fc2-110">PARAMETERS</span></span>

### <span data-ttu-id="a9fc2-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a9fc2-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="a9fc2-112">Gibt an, ob mit diesem Cmdlet der Azure Guest-Agent die Erweiterung automatisch auf eine neuere Nebenversion aktualisieren kann.</span><span class="sxs-lookup"><span data-stu-id="a9fc2-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="a9fc2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9fc2-113">-DefaultProfile</span></span>
<span data-ttu-id="a9fc2-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9fc2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9fc2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a9fc2-115">-Force</span></span>
<span data-ttu-id="a9fc2-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="a9fc2-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a9fc2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a9fc2-117">-Name</span></span>
<span data-ttu-id="a9fc2-118">Gibt den Namen einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="a9fc2-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="a9fc2-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="a9fc2-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="a9fc2-120">Gibt den Pfad der privaten Konfigurationsdatei an.</span><span class="sxs-lookup"><span data-stu-id="a9fc2-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="a9fc2-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="a9fc2-121">-SettingFilePath</span></span>
<span data-ttu-id="a9fc2-122">Gibt den Pfad der öffentlichen Konfigurationsdatei an.</span><span class="sxs-lookup"><span data-stu-id="a9fc2-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="a9fc2-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a9fc2-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="a9fc2-124">Gibt die Version der Erweiterung an, die für diesen VMSS verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9fc2-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="a9fc2-125">Führen Sie zum Abrufen der Version das Cmdlet " [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) " mit einem Wert von "Microsoft. Azure. Diagnostics" für den *PublisherName* -Parameter und IaaSDiagnostics für den *Type* -Parameter aus.</span><span class="sxs-lookup"><span data-stu-id="a9fc2-125">To obtain the version, run the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="a9fc2-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a9fc2-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a9fc2-127">Geben Sie das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a9fc2-127">Specify the VMSS object.</span></span>
<span data-ttu-id="a9fc2-128">Sie können das Cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a9fc2-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="a9fc2-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a9fc2-129">-Confirm</span></span>
<span data-ttu-id="a9fc2-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9fc2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9fc2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9fc2-131">-WhatIf</span></span>
<span data-ttu-id="a9fc2-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9fc2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9fc2-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9fc2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9fc2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9fc2-134">CommonParameters</span></span>
<span data-ttu-id="a9fc2-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9fc2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9fc2-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9fc2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9fc2-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9fc2-137">INPUTS</span></span>

### <span data-ttu-id="a9fc2-138">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a9fc2-138">VirtualMachineScaleSet</span></span>
<span data-ttu-id="a9fc2-139">Der Parameter "VirtualMachineScaleSet" akzeptiert den Wert vom Typ "VirtualMachineScaleSet" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a9fc2-139">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="a9fc2-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9fc2-140">OUTPUTS</span></span>

###  
<span data-ttu-id="a9fc2-141">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="a9fc2-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="a9fc2-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9fc2-142">NOTES</span></span>

## <span data-ttu-id="a9fc2-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9fc2-143">RELATED LINKS</span></span>

[<span data-ttu-id="a9fc2-144">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a9fc2-144">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="a9fc2-145">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a9fc2-145">Remove-AzureRmVmssDiagnosticsExtension</span></span>](./Remove-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="a9fc2-146">Satz-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a9fc2-146">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)
