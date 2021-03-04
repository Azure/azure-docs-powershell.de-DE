---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: 9b8eafaead04c2e2f727676c78bd717b1c6e97c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941280"
---
# <span data-ttu-id="b8c96-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="b8c96-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="b8c96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8c96-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c96-103">Fügt die BGInfo-Erweiterung einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="b8c96-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="b8c96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8c96-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8c96-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8c96-105">DESCRIPTION</span></span>
<span data-ttu-id="b8c96-106">Das **Cmdlet Set-AzVMBGInfoExtension** fügt die BGInfo-Erweiterung einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="b8c96-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="b8c96-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b8c96-107">EXAMPLES</span></span>

### <span data-ttu-id="b8c96-108">Beispiel 1: Hinzufügen der BGInfo-Erweiterung für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="b8c96-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="b8c96-109">Mit diesem Befehl wird die BGInfo-Erweiterung dem virtuellen Computer ContosoVM hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="b8c96-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="b8c96-110">Der Befehl gibt die Ressourcengruppe und den Speicherort des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="b8c96-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="b8c96-111">Der Befehl gibt den Namen und die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="b8c96-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="b8c96-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b8c96-112">PARAMETERS</span></span>

### <span data-ttu-id="b8c96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c96-113">-DefaultProfile</span></span>
<span data-ttu-id="b8c96-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8c96-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8c96-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="b8c96-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="b8c96-116">Gibt an, dass dieses Cmdlet verhindert, dass der Azure-Gast-Agent die Erweiterung automatisch auf eine neuere Nebenversion aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b8c96-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="b8c96-117">Standardmäßig ermöglicht dieses Cmdlet dem Gast-Agent das Aktualisieren der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="b8c96-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

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

### <span data-ttu-id="b8c96-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="b8c96-118">-ForceRerun</span></span>
<span data-ttu-id="b8c96-119">Gibt an, dass die Erweiterung erneut mit denselben öffentlichen oder geschützten Einstellungen ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8c96-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="b8c96-120">Der Wert kann eine beliebige Zeichenfolge sein, die sich vom aktuellen Wert ab unterscheiden kann.</span><span class="sxs-lookup"><span data-stu-id="b8c96-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="b8c96-121">Wenn forceUpdateTag nicht geändert wird, werden Updates an öffentlichen oder geschützten Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="b8c96-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="b8c96-122">-Location</span><span class="sxs-lookup"><span data-stu-id="b8c96-122">-Location</span></span>
<span data-ttu-id="b8c96-123">Gibt den Speicherort des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="b8c96-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="b8c96-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b8c96-124">-Name</span></span>
<span data-ttu-id="b8c96-125">Gibt den Namen der BGInfo-Erweiterung an, die dieses Cmdlet einem virtuellen Computer hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="b8c96-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

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

### <span data-ttu-id="b8c96-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b8c96-126">-NoWait</span></span>
<span data-ttu-id="b8c96-127">Startet den Vorgang und gibt sofort zurück, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b8c96-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="b8c96-128">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="b8c96-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="b8c96-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8c96-129">-ResourceGroupName</span></span>
<span data-ttu-id="b8c96-130">Gibt den Namen der Ressourcengruppe des virtuellen Computers an, dem dieses Cmdlet eine Erweiterung hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="b8c96-130">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="b8c96-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="b8c96-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="b8c96-132">Gibt die Version der Erweiterung an, die dieses Cmdlet dem virtuellen Computer hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="b8c96-132">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

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

### <span data-ttu-id="b8c96-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="b8c96-133">-VMName</span></span>
<span data-ttu-id="b8c96-134">Gibt den Namen des virtuellen Computers an, dem dieses Cmdlet die BGInfo-Erweiterung hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="b8c96-134">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="b8c96-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b8c96-135">-Confirm</span></span>
<span data-ttu-id="b8c96-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8c96-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8c96-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8c96-137">-WhatIf</span></span>
<span data-ttu-id="b8c96-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8c96-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8c96-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8c96-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8c96-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c96-140">CommonParameters</span></span>
<span data-ttu-id="b8c96-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8c96-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c96-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8c96-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c96-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b8c96-143">INPUTS</span></span>

### <span data-ttu-id="b8c96-144">System.String</span><span class="sxs-lookup"><span data-stu-id="b8c96-144">System.String</span></span>

### <span data-ttu-id="b8c96-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b8c96-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b8c96-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b8c96-146">OUTPUTS</span></span>

### <span data-ttu-id="b8c96-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b8c96-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b8c96-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b8c96-148">NOTES</span></span>

## <span data-ttu-id="b8c96-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b8c96-149">RELATED LINKS</span></span>
