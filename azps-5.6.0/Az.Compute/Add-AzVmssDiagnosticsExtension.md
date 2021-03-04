---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 93e9f660b0667286e5ce8c799b5404caae0ba0c0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927395"
---
# <span data-ttu-id="a4cd6-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a4cd6-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="a4cd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="a4cd6-103">Fügt dem VMSS eine Diagnoseerweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="a4cd6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4cd6-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-SettingFilePath] <String>
 [[-ProtectedSettingFilePath] <String>] [[-Name] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4cd6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4cd6-105">DESCRIPTION</span></span>
<span data-ttu-id="a4cd6-106">Das **Cmdlet Add-AzVmssDiagnosticsExtension** fügt der VmSS-Instanz (Virtual Machine Scale Set) eine Diagnoseerweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="a4cd6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a4cd6-107">EXAMPLES</span></span>

### <span data-ttu-id="a4cd6-108">Beispiel 1: Hinzufügen einer Diagnoseerweiterung zum VMSS</span><span class="sxs-lookup"><span data-stu-id="a4cd6-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="a4cd6-109">Mit diesem Befehl wird dem VMSS eine Diagnoseerweiterung hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="a4cd6-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a4cd6-110">PARAMETERS</span></span>

### <span data-ttu-id="a4cd6-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a4cd6-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="a4cd6-112">Gibt an, ob dieses Cmdlet es dem Azure-Gast-Agent ermöglicht, die Erweiterung automatisch auf eine neuere Nebenversion zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="a4cd6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4cd6-113">-DefaultProfile</span></span>
<span data-ttu-id="a4cd6-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4cd6-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="a4cd6-115">-Force</span></span>
<span data-ttu-id="a4cd6-116">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a4cd6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a4cd6-117">-Name</span></span>
<span data-ttu-id="a4cd6-118">Gibt den Namen einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="a4cd6-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="a4cd6-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="a4cd6-120">Gibt den Pfad der privaten Konfigurationsdatei an.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="a4cd6-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="a4cd6-121">-SettingFilePath</span></span>
<span data-ttu-id="a4cd6-122">Gibt den Pfad der öffentlichen Konfigurationsdatei an.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="a4cd6-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a4cd6-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="a4cd6-124">Gibt die Version der Erweiterung an, die für diesen VMSS verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="a4cd6-125">Führen Sie zum Abrufen der Version das [Get-AzVMExtensionImage-Cmdlet](./Get-AzVMExtensionImage.md) mit dem Wert Microsoft.Azure.Diagnostics für den *Parameter PublisherName* und IaaSDiagnostics für den Parameter *Type* aus.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="a4cd6-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a4cd6-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a4cd6-127">Geben Sie das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-127">Specify the VMSS object.</span></span>
<span data-ttu-id="a4cd6-128">Sie können das [Cmdlet New-AzVmssConfig](./New-AzVmssConfig.md) verwenden, um das -Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="a4cd6-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a4cd6-129">-Confirm</span></span>
<span data-ttu-id="a4cd6-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4cd6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4cd6-131">-WhatIf</span></span>
<span data-ttu-id="a4cd6-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4cd6-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4cd6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4cd6-134">CommonParameters</span></span>
<span data-ttu-id="a4cd6-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4cd6-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4cd6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4cd6-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a4cd6-137">INPUTS</span></span>

### <span data-ttu-id="a4cd6-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a4cd6-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="a4cd6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a4cd6-139">System.String</span></span>

### <span data-ttu-id="a4cd6-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a4cd6-140">System.Boolean</span></span>

## <span data-ttu-id="a4cd6-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a4cd6-141">OUTPUTS</span></span>

### <span data-ttu-id="a4cd6-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a4cd6-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a4cd6-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a4cd6-143">NOTES</span></span>

## <span data-ttu-id="a4cd6-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a4cd6-144">RELATED LINKS</span></span>

[<span data-ttu-id="a4cd6-145">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a4cd6-145">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="a4cd6-146">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a4cd6-146">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="a4cd6-147">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a4cd6-147">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)
