---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
ms.openlocfilehash: 051228464b2f1e9770507ceacd4eaabfce5236b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145012"
---
# <span data-ttu-id="03e10-101">Add-AzVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="03e10-101">Add-AzVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="03e10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03e10-102">SYNOPSIS</span></span>
<span data-ttu-id="03e10-103">Fügt der unbeaufsichtigten Antwortdatei für Windows Setup Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="03e10-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="03e10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03e10-104">SYNTAX</span></span>

```
Add-AzVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03e10-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03e10-105">DESCRIPTION</span></span>
<span data-ttu-id="03e10-106">Das **Cmdlet "Add-AzVmssAdditionalUnattendContent"** fügt der unbeaufsichtigten Antwortdatei für Windows Setup Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="03e10-106">The **Add-AzVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="03e10-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="03e10-107">EXAMPLES</span></span>

### <span data-ttu-id="03e10-108">Beispiel 1: Hinzufügen von Informationen zur unbeaufsichtigten Antwortdatei für Windows Setup</span><span class="sxs-lookup"><span data-stu-id="03e10-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="03e10-109">Dieser Befehl fügt der unbeaufsichtigten Antwortdatei für Windows Setup Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="03e10-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="03e10-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03e10-110">PARAMETERS</span></span>

### <span data-ttu-id="03e10-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="03e10-111">-ComponentName</span></span>
<span data-ttu-id="03e10-112">Gibt den Namen der Komponente an, die mit dem hinzugefügten Inhalt konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="03e10-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="03e10-113">Der einzige zulässige Wert ist Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="03e10-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ComponentNames]
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftWindowsShellSetup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03e10-114">-Content</span><span class="sxs-lookup"><span data-stu-id="03e10-114">-Content</span></span>
<span data-ttu-id="03e10-115">Gibt den XML-formatierten Inhalt an, der der unattend.xml für den angegebenen Pfad und die angegebene Komponente hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="03e10-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

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

### <span data-ttu-id="03e10-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03e10-116">-DefaultProfile</span></span>
<span data-ttu-id="03e10-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="03e10-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03e10-118">-PassName</span><span class="sxs-lookup"><span data-stu-id="03e10-118">-PassName</span></span>
<span data-ttu-id="03e10-119">Gibt den Namen des Durchtritts an, auf den der Inhalt zutrifft.</span><span class="sxs-lookup"><span data-stu-id="03e10-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="03e10-120">Der einzige zulässige Wert ist "oobeSystem".</span><span class="sxs-lookup"><span data-stu-id="03e10-120">The only allowable value is oobeSystem.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.PassNames]
Parameter Sets: (All)
Aliases:
Accepted values: OobeSystem

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03e10-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="03e10-121">-SettingName</span></span>
<span data-ttu-id="03e10-122">Gibt den Namen der Einstellung an, auf die der Inhalt angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="03e10-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="03e10-123">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="03e10-123">The acceptable values for this parameter are::</span></span>
- <span data-ttu-id="03e10-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="03e10-124">FirstLogonCommands</span></span>
- <span data-ttu-id="03e10-125">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="03e10-125">AutoLogon</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03e10-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="03e10-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="03e10-127">Geben Sie das Scale **Set-Objekt des virtuellen** Computers an.</span><span class="sxs-lookup"><span data-stu-id="03e10-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="03e10-128">Sie können das [Cmdlet "New-AzVmssConfig"](./New-AzVmssConfig.md) verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="03e10-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="03e10-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03e10-129">-Confirm</span></span>
<span data-ttu-id="03e10-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="03e10-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03e10-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="03e10-131">-WhatIf</span></span>
<span data-ttu-id="03e10-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="03e10-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03e10-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="03e10-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03e10-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03e10-134">CommonParameters</span></span>
<span data-ttu-id="03e10-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03e10-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03e10-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03e10-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03e10-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="03e10-137">INPUTS</span></span>

### <span data-ttu-id="03e10-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="03e10-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="03e10-139">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="03e10-139">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="03e10-140">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="03e10-140">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="03e10-141">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="03e10-141">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="03e10-142">System.String</span><span class="sxs-lookup"><span data-stu-id="03e10-142">System.String</span></span>

## <span data-ttu-id="03e10-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="03e10-143">OUTPUTS</span></span>

### <span data-ttu-id="03e10-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="03e10-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="03e10-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="03e10-145">NOTES</span></span>

## <span data-ttu-id="03e10-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="03e10-146">RELATED LINKS</span></span>

[<span data-ttu-id="03e10-147">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="03e10-147">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
