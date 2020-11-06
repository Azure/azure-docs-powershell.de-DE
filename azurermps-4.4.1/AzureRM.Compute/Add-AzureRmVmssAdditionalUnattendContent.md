---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
ms.openlocfilehash: d99e54439b2e8b4474c4b0123634ddd7c286ea9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477358"
---
# <span data-ttu-id="987d8-101">Add-AzureRmVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="987d8-101">Add-AzureRmVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="987d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="987d8-102">SYNOPSIS</span></span>
<span data-ttu-id="987d8-103">Fügt der Antwortdatei für das unbeaufsichtigte Windows Setup Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="987d8-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="987d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="987d8-104">SYNTAX</span></span>

```
Add-AzureRmVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="987d8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="987d8-105">DESCRIPTION</span></span>
<span data-ttu-id="987d8-106">Das Cmdlet **Add-AzureRmVmssAdditionalUnattendContent** fügt der Antwortdatei für das unbeaufsichtigte Windows Setup Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="987d8-106">The **Add-AzureRmVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="987d8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="987d8-107">EXAMPLES</span></span>

### <span data-ttu-id="987d8-108">Beispiel 1: Hinzufügen von Informationen zur Antwortdatei für das unbeaufsichtigte Windows-Setup</span><span class="sxs-lookup"><span data-stu-id="987d8-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzureRmVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="987d8-109">Dieser Befehl fügt der Antwortdatei für das unbeaufsichtigte Windows Setup Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="987d8-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="987d8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="987d8-110">PARAMETERS</span></span>

### <span data-ttu-id="987d8-111">-Komponentenname</span><span class="sxs-lookup"><span data-stu-id="987d8-111">-ComponentName</span></span>
<span data-ttu-id="987d8-112">Gibt den Namen der Komponente an, die mit dem hinzugefügten Inhalt konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="987d8-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="987d8-113">Der einzige zulässige Wert ist Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="987d8-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

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

### <span data-ttu-id="987d8-114">– Inhalt</span><span class="sxs-lookup"><span data-stu-id="987d8-114">-Content</span></span>
<span data-ttu-id="987d8-115">Gibt den XML-formatierten Inhalt an, der der unattend.xml-Datei für den angegebenen Pfad und die angegebene Komponente hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="987d8-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

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

### <span data-ttu-id="987d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="987d8-116">-DefaultProfile</span></span>
<span data-ttu-id="987d8-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="987d8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="987d8-118">-Passname</span><span class="sxs-lookup"><span data-stu-id="987d8-118">-PassName</span></span>
<span data-ttu-id="987d8-119">Gibt den Namen des Passes an, auf den sich der Inhalt bezieht.</span><span class="sxs-lookup"><span data-stu-id="987d8-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="987d8-120">Der einzige zulässige Wert ist oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="987d8-120">The only allowable value is oobeSystem.</span></span>

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

### <span data-ttu-id="987d8-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="987d8-121">-SettingName</span></span>
<span data-ttu-id="987d8-122">Gibt den Namen der Einstellung an, auf die der Inhalt angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="987d8-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="987d8-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="987d8-123">The acceptable values for this parameter are::</span></span>

- <span data-ttu-id="987d8-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="987d8-124">FirstLogonCommands</span></span>
- <span data-ttu-id="987d8-125">Autologon</span><span class="sxs-lookup"><span data-stu-id="987d8-125">AutoLogon</span></span>

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

### <span data-ttu-id="987d8-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="987d8-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="987d8-127">Geben Sie das **Scale** -Objekt für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="987d8-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="987d8-128">Sie können das Cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="987d8-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="987d8-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="987d8-129">-Confirm</span></span>
<span data-ttu-id="987d8-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="987d8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="987d8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="987d8-131">-WhatIf</span></span>
<span data-ttu-id="987d8-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="987d8-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="987d8-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="987d8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="987d8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="987d8-134">CommonParameters</span></span>
<span data-ttu-id="987d8-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="987d8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="987d8-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="987d8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="987d8-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="987d8-137">INPUTS</span></span>

## <span data-ttu-id="987d8-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="987d8-138">OUTPUTS</span></span>

## <span data-ttu-id="987d8-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="987d8-139">NOTES</span></span>

## <span data-ttu-id="987d8-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="987d8-140">RELATED LINKS</span></span>

[<span data-ttu-id="987d8-141">Neu – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="987d8-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
