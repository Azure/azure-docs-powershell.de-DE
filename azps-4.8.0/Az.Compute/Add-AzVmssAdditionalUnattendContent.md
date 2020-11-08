---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
ms.openlocfilehash: 051228464b2f1e9770507ceacd4eaabfce5236b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173099"
---
# <span data-ttu-id="cb706-101">Add-AzVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="cb706-101">Add-AzVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="cb706-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cb706-102">SYNOPSIS</span></span>
<span data-ttu-id="cb706-103">Fügt der Antwortdatei für das unbeaufsichtigte Windows Setup Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="cb706-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="cb706-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb706-104">SYNTAX</span></span>

```
Add-AzVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb706-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb706-105">DESCRIPTION</span></span>
<span data-ttu-id="cb706-106">Das Cmdlet **Add-AzVmssAdditionalUnattendContent** fügt der Antwortdatei für das unbeaufsichtigte Windows Setup Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="cb706-106">The **Add-AzVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="cb706-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb706-107">EXAMPLES</span></span>

### <span data-ttu-id="cb706-108">Beispiel 1: Hinzufügen von Informationen zur Antwortdatei für das unbeaufsichtigte Windows-Setup</span><span class="sxs-lookup"><span data-stu-id="cb706-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="cb706-109">Dieser Befehl fügt der Antwortdatei für das unbeaufsichtigte Windows Setup Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="cb706-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="cb706-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb706-110">PARAMETERS</span></span>

### <span data-ttu-id="cb706-111">-Komponentenname</span><span class="sxs-lookup"><span data-stu-id="cb706-111">-ComponentName</span></span>
<span data-ttu-id="cb706-112">Gibt den Namen der Komponente an, die mit dem hinzugefügten Inhalt konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb706-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="cb706-113">Der einzige zulässige Wert ist Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="cb706-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

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

### <span data-ttu-id="cb706-114">– Inhalt</span><span class="sxs-lookup"><span data-stu-id="cb706-114">-Content</span></span>
<span data-ttu-id="cb706-115">Gibt den XML-formatierten Inhalt an, der der unattend.xml-Datei für den angegebenen Pfad und die angegebene Komponente hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="cb706-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

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

### <span data-ttu-id="cb706-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb706-116">-DefaultProfile</span></span>
<span data-ttu-id="cb706-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cb706-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb706-118">-Passname</span><span class="sxs-lookup"><span data-stu-id="cb706-118">-PassName</span></span>
<span data-ttu-id="cb706-119">Gibt den Namen des Passes an, auf den sich der Inhalt bezieht.</span><span class="sxs-lookup"><span data-stu-id="cb706-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="cb706-120">Der einzige zulässige Wert ist oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="cb706-120">The only allowable value is oobeSystem.</span></span>

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

### <span data-ttu-id="cb706-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="cb706-121">-SettingName</span></span>
<span data-ttu-id="cb706-122">Gibt den Namen der Einstellung an, auf die der Inhalt angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="cb706-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="cb706-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cb706-123">The acceptable values for this parameter are::</span></span>
- <span data-ttu-id="cb706-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="cb706-124">FirstLogonCommands</span></span>
- <span data-ttu-id="cb706-125">Autologon</span><span class="sxs-lookup"><span data-stu-id="cb706-125">AutoLogon</span></span>

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

### <span data-ttu-id="cb706-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cb706-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="cb706-127">Geben Sie das **Scale** -Objekt für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="cb706-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="cb706-128">Sie können das Cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cb706-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="cb706-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cb706-129">-Confirm</span></span>
<span data-ttu-id="cb706-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cb706-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb706-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb706-131">-WhatIf</span></span>
<span data-ttu-id="cb706-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cb706-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb706-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cb706-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb706-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb706-134">CommonParameters</span></span>
<span data-ttu-id="cb706-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb706-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb706-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb706-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb706-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cb706-137">INPUTS</span></span>

### <span data-ttu-id="cb706-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cb706-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="cb706-139">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. PassNames, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="cb706-139">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="cb706-140">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ComponentNames, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="cb706-140">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="cb706-141">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. SettingNames, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="cb706-141">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="cb706-142">System. String</span><span class="sxs-lookup"><span data-stu-id="cb706-142">System.String</span></span>

## <span data-ttu-id="cb706-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cb706-143">OUTPUTS</span></span>

### <span data-ttu-id="cb706-144">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cb706-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="cb706-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="cb706-145">NOTES</span></span>

## <span data-ttu-id="cb706-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cb706-146">RELATED LINKS</span></span>

[<span data-ttu-id="cb706-147">Neu – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="cb706-147">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
