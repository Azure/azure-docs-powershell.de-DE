---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: a0c2b1dbad943a690ae2965a9ea9520063909b9c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470943"
---
# <span data-ttu-id="fd8f2-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fd8f2-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="fd8f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd8f2-102">SYNOPSIS</span></span>
<span data-ttu-id="fd8f2-103">Fügt dem VMSS eine Diagnoseerweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="fd8f2-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="fd8f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd8f2-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-SettingFilePath] <String>
 [[-ProtectedSettingFilePath] <String>] [[-Name] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd8f2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd8f2-105">DESCRIPTION</span></span>
<span data-ttu-id="fd8f2-106">Das **Cmdlet "Add-AzVmssDiagnosticsExtension"** fügt der Instanz des Virtual Machine Scale Set (VMSS) eine Diagnoseerweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="fd8f2-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="fd8f2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fd8f2-107">EXAMPLES</span></span>

### <span data-ttu-id="fd8f2-108">Beispiel 1: Hinzufügen einer Diagnoseerweiterung zu VMSS</span><span class="sxs-lookup"><span data-stu-id="fd8f2-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="fd8f2-109">Dieser Befehl fügt dem VMSS eine Diagnoseerweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="fd8f2-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="fd8f2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd8f2-110">PARAMETERS</span></span>

### <span data-ttu-id="fd8f2-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="fd8f2-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="fd8f2-112">Gibt an, ob dieses Cmdlet es dem Azure-Gast-Agent erlaubt, die Erweiterung automatisch auf eine neuere Nebenversion zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="fd8f2-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="fd8f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd8f2-113">-DefaultProfile</span></span>
<span data-ttu-id="fd8f2-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd8f2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd8f2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fd8f2-115">-Force</span></span>
<span data-ttu-id="fd8f2-116">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="fd8f2-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fd8f2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fd8f2-117">-Name</span></span>
<span data-ttu-id="fd8f2-118">Gibt den Namen einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="fd8f2-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="fd8f2-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="fd8f2-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="fd8f2-120">Gibt den Pfad der privaten Konfigurationsdatei an.</span><span class="sxs-lookup"><span data-stu-id="fd8f2-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="fd8f2-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="fd8f2-121">-SettingFilePath</span></span>
<span data-ttu-id="fd8f2-122">Gibt den Pfad der öffentlichen Konfigurationsdatei an.</span><span class="sxs-lookup"><span data-stu-id="fd8f2-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="fd8f2-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="fd8f2-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="fd8f2-124">Gibt die Version der Erweiterung an, die für diese VMSS verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd8f2-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="fd8f2-125">Führen Sie zum Abrufen der Version das [Cmdlet "Get-AzVMExtensionImage"](./Get-AzVMExtensionImage.md) mit dem Wert "Microsoft.Azure.Diagnostics" für den Parameter *"PublisherName"* und "IaaSDiagnostics" für den Parameter *"Type"* aus.</span><span class="sxs-lookup"><span data-stu-id="fd8f2-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="fd8f2-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fd8f2-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fd8f2-127">Geben Sie das "VMSS"-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="fd8f2-127">Specify the VMSS object.</span></span>
<span data-ttu-id="fd8f2-128">Sie können das [Cmdlet "New-AzVmssConfig"](./New-AzVmssConfig.md) verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fd8f2-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="fd8f2-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd8f2-129">-Confirm</span></span>
<span data-ttu-id="fd8f2-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd8f2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd8f2-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fd8f2-131">-WhatIf</span></span>
<span data-ttu-id="fd8f2-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd8f2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd8f2-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd8f2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd8f2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd8f2-134">CommonParameters</span></span>
<span data-ttu-id="fd8f2-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd8f2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd8f2-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd8f2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd8f2-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fd8f2-137">INPUTS</span></span>

### <span data-ttu-id="fd8f2-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fd8f2-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="fd8f2-139">System.String</span><span class="sxs-lookup"><span data-stu-id="fd8f2-139">System.String</span></span>

### <span data-ttu-id="fd8f2-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fd8f2-140">System.Boolean</span></span>

## <span data-ttu-id="fd8f2-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fd8f2-141">OUTPUTS</span></span>

### <span data-ttu-id="fd8f2-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fd8f2-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="fd8f2-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fd8f2-143">NOTES</span></span>

## <span data-ttu-id="fd8f2-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fd8f2-144">RELATED LINKS</span></span>

[<span data-ttu-id="fd8f2-145">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="fd8f2-145">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="fd8f2-146">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fd8f2-146">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="fd8f2-147">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fd8f2-147">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)
