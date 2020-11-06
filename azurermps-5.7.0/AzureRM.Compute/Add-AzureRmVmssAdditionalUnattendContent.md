---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
ms.openlocfilehash: de61efcbabb2e5acd7d82bf7a1cec8341fe06433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481338"
---
# <span data-ttu-id="73e3a-101">Add-AzureRmVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="73e3a-101">Add-AzureRmVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="73e3a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="73e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="73e3a-103">Fügt der Antwortdatei für das unbeaufsichtigte Windows Setup Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="73e3a-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73e3a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="73e3a-104">SYNTAX</span></span>

```
Add-AzureRmVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73e3a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73e3a-105">DESCRIPTION</span></span>
<span data-ttu-id="73e3a-106">Das Cmdlet **Add-AzureRmVmssAdditionalUnattendContent** fügt der Antwortdatei für das unbeaufsichtigte Windows Setup Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="73e3a-106">The **Add-AzureRmVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="73e3a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="73e3a-107">EXAMPLES</span></span>

### <span data-ttu-id="73e3a-108">Beispiel 1: Hinzufügen von Informationen zur Antwortdatei für das unbeaufsichtigte Windows-Setup</span><span class="sxs-lookup"><span data-stu-id="73e3a-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzureRmVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="73e3a-109">Dieser Befehl fügt der Antwortdatei für das unbeaufsichtigte Windows Setup Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="73e3a-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="73e3a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="73e3a-110">PARAMETERS</span></span>

### <span data-ttu-id="73e3a-111">-Komponentenname</span><span class="sxs-lookup"><span data-stu-id="73e3a-111">-ComponentName</span></span>
<span data-ttu-id="73e3a-112">Gibt den Namen der Komponente an, die mit dem hinzugefügten Inhalt konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="73e3a-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="73e3a-113">Der einzige zulässige Wert ist Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="73e3a-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

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

### <span data-ttu-id="73e3a-114">– Inhalt</span><span class="sxs-lookup"><span data-stu-id="73e3a-114">-Content</span></span>
<span data-ttu-id="73e3a-115">Gibt den XML-formatierten Inhalt an, der der unattend.xml-Datei für den angegebenen Pfad und die angegebene Komponente hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="73e3a-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

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

### <span data-ttu-id="73e3a-116">-Passname</span><span class="sxs-lookup"><span data-stu-id="73e3a-116">-PassName</span></span>
<span data-ttu-id="73e3a-117">Gibt den Namen des Passes an, auf den sich der Inhalt bezieht.</span><span class="sxs-lookup"><span data-stu-id="73e3a-117">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="73e3a-118">Der einzige zulässige Wert ist oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="73e3a-118">The only allowable value is oobeSystem.</span></span>

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

### <span data-ttu-id="73e3a-119">-SettingName</span><span class="sxs-lookup"><span data-stu-id="73e3a-119">-SettingName</span></span>
<span data-ttu-id="73e3a-120">Gibt den Namen der Einstellung an, auf die der Inhalt angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="73e3a-120">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="73e3a-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="73e3a-121">The acceptable values for this parameter are::</span></span>

- <span data-ttu-id="73e3a-122">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="73e3a-122">FirstLogonCommands</span></span>
- <span data-ttu-id="73e3a-123">Autologon</span><span class="sxs-lookup"><span data-stu-id="73e3a-123">AutoLogon</span></span>

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

### <span data-ttu-id="73e3a-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="73e3a-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="73e3a-125">Geben Sie das **Scale** -Objekt für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="73e3a-125">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="73e3a-126">Sie können das Cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="73e3a-126">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="73e3a-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="73e3a-127">-Confirm</span></span>
<span data-ttu-id="73e3a-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="73e3a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73e3a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73e3a-129">-WhatIf</span></span>
<span data-ttu-id="73e3a-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73e3a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73e3a-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73e3a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73e3a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73e3a-132">CommonParameters</span></span>
<span data-ttu-id="73e3a-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73e3a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73e3a-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73e3a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73e3a-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="73e3a-135">INPUTS</span></span>

### <span data-ttu-id="73e3a-136">Keine</span><span class="sxs-lookup"><span data-stu-id="73e3a-136">None</span></span>
<span data-ttu-id="73e3a-137">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="73e3a-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="73e3a-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="73e3a-138">OUTPUTS</span></span>

## <span data-ttu-id="73e3a-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="73e3a-139">NOTES</span></span>

## <span data-ttu-id="73e3a-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="73e3a-140">RELATED LINKS</span></span>

[<span data-ttu-id="73e3a-141">Neu – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="73e3a-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
