---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: a0c2b1dbad943a690ae2965a9ea9520063909b9c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175940"
---
# <span data-ttu-id="5d33a-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5d33a-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="5d33a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d33a-102">SYNOPSIS</span></span>
<span data-ttu-id="5d33a-103">Fügt der VMSS eine Diagnose Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="5d33a-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="5d33a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d33a-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-SettingFilePath] <String>
 [[-ProtectedSettingFilePath] <String>] [[-Name] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d33a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d33a-105">DESCRIPTION</span></span>
<span data-ttu-id="5d33a-106">Das **Add-AzVmssDiagnosticsExtension-** Cmdlet fügt der Instanz des virtuellen Computer-Skalierungs Satzes (VMSS) eine Diagnose Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="5d33a-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="5d33a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d33a-107">EXAMPLES</span></span>

### <span data-ttu-id="5d33a-108">Beispiel 1: Hinzufügen einer Diagnose Erweiterung zum VMSS</span><span class="sxs-lookup"><span data-stu-id="5d33a-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="5d33a-109">Mit diesem Befehl wird der VMSS eine Diagnose Erweiterung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5d33a-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="5d33a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d33a-110">PARAMETERS</span></span>

### <span data-ttu-id="5d33a-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="5d33a-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="5d33a-112">Gibt an, ob mit diesem Cmdlet der Azure Guest-Agent die Erweiterung automatisch auf eine neuere Nebenversion aktualisieren kann.</span><span class="sxs-lookup"><span data-stu-id="5d33a-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d33a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d33a-113">-DefaultProfile</span></span>
<span data-ttu-id="5d33a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5d33a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d33a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5d33a-115">-Force</span></span>
<span data-ttu-id="5d33a-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="5d33a-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d33a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5d33a-117">-Name</span></span>
<span data-ttu-id="5d33a-118">Gibt den Namen einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="5d33a-118">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d33a-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="5d33a-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="5d33a-120">Gibt den Pfad der privaten Konfigurationsdatei an.</span><span class="sxs-lookup"><span data-stu-id="5d33a-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="5d33a-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="5d33a-121">-SettingFilePath</span></span>
<span data-ttu-id="5d33a-122">Gibt den Pfad der öffentlichen Konfigurationsdatei an.</span><span class="sxs-lookup"><span data-stu-id="5d33a-122">Specifies the path of the public configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d33a-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="5d33a-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="5d33a-124">Gibt die Version der Erweiterung an, die für diesen VMSS verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d33a-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="5d33a-125">Führen Sie zum Abrufen der Version das Cmdlet " [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) " mit einem Wert von "Microsoft. Azure. Diagnostics" für den *PublisherName* -Parameter und IaaSDiagnostics für den *Type* -Parameter aus.</span><span class="sxs-lookup"><span data-stu-id="5d33a-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d33a-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5d33a-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5d33a-127">Geben Sie das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="5d33a-127">Specify the VMSS object.</span></span>
<span data-ttu-id="5d33a-128">Sie können das Cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5d33a-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="5d33a-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5d33a-129">-Confirm</span></span>
<span data-ttu-id="5d33a-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d33a-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d33a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d33a-131">-WhatIf</span></span>
<span data-ttu-id="5d33a-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d33a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d33a-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d33a-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d33a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d33a-134">CommonParameters</span></span>
<span data-ttu-id="5d33a-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d33a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d33a-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d33a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d33a-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d33a-137">INPUTS</span></span>

### <span data-ttu-id="5d33a-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5d33a-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="5d33a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5d33a-139">System.String</span></span>

### <span data-ttu-id="5d33a-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5d33a-140">System.Boolean</span></span>

## <span data-ttu-id="5d33a-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d33a-141">OUTPUTS</span></span>

### <span data-ttu-id="5d33a-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5d33a-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="5d33a-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d33a-143">NOTES</span></span>

## <span data-ttu-id="5d33a-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d33a-144">RELATED LINKS</span></span>

[<span data-ttu-id="5d33a-145">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="5d33a-145">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="5d33a-146">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5d33a-146">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="5d33a-147">Satz-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5d33a-147">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)
