---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
ms.openlocfilehash: 38f510602259ca799c6df947b9d74984dff178ba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844732"
---
# <span data-ttu-id="6cea2-101">Add-AzVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="6cea2-101">Add-AzVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="6cea2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6cea2-102">SYNOPSIS</span></span>
<span data-ttu-id="6cea2-103">Fügt der Antwortdatei für das unbeaufsichtigte Windows Setup Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="6cea2-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="6cea2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cea2-104">SYNTAX</span></span>

```
Add-AzVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cea2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6cea2-105">DESCRIPTION</span></span>
<span data-ttu-id="6cea2-106">Das Cmdlet **Add-AzVmssAdditionalUnattendContent** fügt der Antwortdatei für das unbeaufsichtigte Windows Setup Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="6cea2-106">The **Add-AzVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="6cea2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6cea2-107">EXAMPLES</span></span>

### <span data-ttu-id="6cea2-108">Beispiel 1: Hinzufügen von Informationen zur Antwortdatei für das unbeaufsichtigte Windows-Setup</span><span class="sxs-lookup"><span data-stu-id="6cea2-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="6cea2-109">Dieser Befehl fügt der Antwortdatei für das unbeaufsichtigte Windows Setup Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="6cea2-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="6cea2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cea2-110">PARAMETERS</span></span>

### <span data-ttu-id="6cea2-111">-Komponentenname</span><span class="sxs-lookup"><span data-stu-id="6cea2-111">-ComponentName</span></span>
<span data-ttu-id="6cea2-112">Gibt den Namen der Komponente an, die mit dem hinzugefügten Inhalt konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6cea2-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="6cea2-113">Der einzige zulässige Wert ist Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="6cea2-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

```yaml
Type: ComponentNames
Parameter Sets: (All)
Aliases: 
Accepted values: MicrosoftWindowsShellSetup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cea2-114">– Inhalt</span><span class="sxs-lookup"><span data-stu-id="6cea2-114">-Content</span></span>
<span data-ttu-id="6cea2-115">Gibt den XML-formatierten Inhalt an, der der unattend.xml-Datei für den angegebenen Pfad und die angegebene Komponente hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="6cea2-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cea2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cea2-116">-DefaultProfile</span></span>
<span data-ttu-id="6cea2-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6cea2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cea2-118">-Passname</span><span class="sxs-lookup"><span data-stu-id="6cea2-118">-PassName</span></span>
<span data-ttu-id="6cea2-119">Gibt den Namen des Passes an, auf den sich der Inhalt bezieht.</span><span class="sxs-lookup"><span data-stu-id="6cea2-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="6cea2-120">Der einzige zulässige Wert ist oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="6cea2-120">The only allowable value is oobeSystem.</span></span>

```yaml
Type: PassNames
Parameter Sets: (All)
Aliases: 
Accepted values: OobeSystem

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cea2-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="6cea2-121">-SettingName</span></span>
<span data-ttu-id="6cea2-122">Gibt den Namen der Einstellung an, auf die der Inhalt angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="6cea2-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="6cea2-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6cea2-123">The acceptable values for this parameter are::</span></span>

- <span data-ttu-id="6cea2-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="6cea2-124">FirstLogonCommands</span></span>
- <span data-ttu-id="6cea2-125">Autologon</span><span class="sxs-lookup"><span data-stu-id="6cea2-125">AutoLogon</span></span>

```yaml
Type: SettingNames
Parameter Sets: (All)
Aliases: 
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cea2-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6cea2-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6cea2-127">Geben Sie das **Scale** -Objekt für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="6cea2-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="6cea2-128">Sie können das Cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6cea2-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cea2-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6cea2-129">-Confirm</span></span>
<span data-ttu-id="6cea2-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6cea2-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cea2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cea2-131">-WhatIf</span></span>
<span data-ttu-id="6cea2-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6cea2-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6cea2-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6cea2-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cea2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cea2-134">CommonParameters</span></span>
<span data-ttu-id="6cea2-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cea2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cea2-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cea2-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cea2-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6cea2-137">INPUTS</span></span>

### <span data-ttu-id="6cea2-138">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6cea2-138">VirtualMachineScaleSet</span></span>
<span data-ttu-id="6cea2-139">Der Parameter "VirtualMachineScaleSet" akzeptiert den Wert vom Typ "VirtualMachineScaleSet" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="6cea2-139">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="6cea2-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6cea2-140">OUTPUTS</span></span>

### <span data-ttu-id="6cea2-141">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6cea2-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="6cea2-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="6cea2-142">NOTES</span></span>

## <span data-ttu-id="6cea2-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6cea2-143">RELATED LINKS</span></span>

[<span data-ttu-id="6cea2-144">Neu – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6cea2-144">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
