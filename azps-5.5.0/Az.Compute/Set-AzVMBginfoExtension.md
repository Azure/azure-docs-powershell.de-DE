---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: a98a2f5cbc8034e8cec4d324bb7ecaa28297e772
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167900"
---
# <span data-ttu-id="9460f-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="9460f-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="9460f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9460f-102">SYNOPSIS</span></span>
<span data-ttu-id="9460f-103">Fügt die Erweiterung BGInfo einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="9460f-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="9460f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9460f-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9460f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9460f-105">DESCRIPTION</span></span>
<span data-ttu-id="9460f-106">Das **Cmdlet Set-AzVMBGInfoExtension** fügt einem virtuellen Computer die Erweiterung BGInfo hinzu.</span><span class="sxs-lookup"><span data-stu-id="9460f-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="9460f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9460f-107">EXAMPLES</span></span>

### <span data-ttu-id="9460f-108">Beispiel 1: Hinzufügen der Erweiterung BGInfo für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="9460f-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="9460f-109">Mit diesem Befehl wird die Erweiterung BGInfo dem virtuellen Computer "ContosoVM" hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="9460f-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="9460f-110">Der Befehl gibt die Ressourcengruppe und den Speicherort des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="9460f-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="9460f-111">Der Befehl gibt den Namen und die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="9460f-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="9460f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9460f-112">PARAMETERS</span></span>

### <span data-ttu-id="9460f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9460f-113">-DefaultProfile</span></span>
<span data-ttu-id="9460f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9460f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9460f-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="9460f-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="9460f-116">Gibt an, dass dieses Cmdlet verhindert, dass der Azure-Gast-Agent die Erweiterung automatisch auf eine neuere Nebenversion aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9460f-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="9460f-117">Standardmäßig ermöglicht dieses Cmdlet dem Gast-Agent, die Erweiterung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9460f-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9460f-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="9460f-118">-ForceRerun</span></span>
<span data-ttu-id="9460f-119">Gibt an, dass die Erweiterung erneut mit denselben öffentlichen oder geschützten Einstellungen ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9460f-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="9460f-120">Bei dem Wert kann sich eine beliebige Zeichenfolge vom aktuellen Wert unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="9460f-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="9460f-121">Wenn "forceUpdateTag" nicht geändert wird, werden Aktualisierungen öffentlicher oder geschützter Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="9460f-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="9460f-122">-Location</span><span class="sxs-lookup"><span data-stu-id="9460f-122">-Location</span></span>
<span data-ttu-id="9460f-123">Gibt den Speicherort des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="9460f-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="9460f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9460f-124">-Name</span></span>
<span data-ttu-id="9460f-125">Gibt den Namen der BGInfo-Erweiterung an, die dieses Cmdlet einem virtuellen Computer hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="9460f-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9460f-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9460f-126">-NoWait</span></span>
<span data-ttu-id="9460f-127">Der Vorgang wird gestartet und unmittelbar vor Abschluss des Vorgangs beendet.</span><span class="sxs-lookup"><span data-stu-id="9460f-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="9460f-128">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="9460f-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="9460f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9460f-129">-ResourceGroupName</span></span>
<span data-ttu-id="9460f-130">Gibt den Namen der Ressourcengruppe des virtuellen Computers an, dem dieses Cmdlet eine Erweiterung hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="9460f-130">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9460f-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="9460f-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="9460f-132">Gibt die Version der Erweiterung an, die dieses Cmdlet dem virtuellen Computer hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="9460f-132">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9460f-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="9460f-133">-VMName</span></span>
<span data-ttu-id="9460f-134">Gibt den Namen des virtuellen Computers an, dem dieses Cmdlet die Erweiterung BGInfo hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="9460f-134">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9460f-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9460f-135">-Confirm</span></span>
<span data-ttu-id="9460f-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9460f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9460f-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9460f-137">-WhatIf</span></span>
<span data-ttu-id="9460f-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9460f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9460f-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9460f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9460f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9460f-140">CommonParameters</span></span>
<span data-ttu-id="9460f-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9460f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9460f-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9460f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9460f-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9460f-143">INPUTS</span></span>

### <span data-ttu-id="9460f-144">System.String</span><span class="sxs-lookup"><span data-stu-id="9460f-144">System.String</span></span>

### <span data-ttu-id="9460f-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9460f-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9460f-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9460f-146">OUTPUTS</span></span>

### <span data-ttu-id="9460f-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9460f-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9460f-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9460f-148">NOTES</span></span>

## <span data-ttu-id="9460f-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9460f-149">RELATED LINKS</span></span>
