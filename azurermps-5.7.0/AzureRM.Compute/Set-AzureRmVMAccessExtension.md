---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
ms.openlocfilehash: 6c24c01ebff1d0a74835b968640caea6b5d2b308
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476926"
---
# <span data-ttu-id="82db8-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="82db8-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="82db8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="82db8-102">SYNOPSIS</span></span>
<span data-ttu-id="82db8-103">Fügt die VMAccess-Erweiterung zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="82db8-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82db8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="82db8-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-UserName <String>] [-Password <String>] [-ResourceGroupName] <String>
 [-VMName] <String> [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82db8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="82db8-105">DESCRIPTION</span></span>
<span data-ttu-id="82db8-106">Mit dem Cmdlet " **AzureRmVMAccessExtension** " wird der Virtual Machine Access-VMAccess-VMAccess-Erweiterung zu einem virtuellen Computer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="82db8-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="82db8-107">VMAccess Extension kann verwendet werden, um ein temporäres Kennwort festzulegen, das nach der Anmeldung am Computer sofort geändert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="82db8-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="82db8-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="82db8-108">EXAMPLES</span></span>

### <span data-ttu-id="82db8-109">Beispiel 1: Hinzufügen einer VMAccess-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="82db8-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="82db8-110">Mit diesem Befehl wird eine VMAccess-Erweiterung für den virtuellen Computer mit dem Namen VirtualMachine07 in ResrouceGroup11 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="82db8-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="82db8-111">Der Befehl gibt die Version für Name und Typ des Handlers für VMAccess an.</span><span class="sxs-lookup"><span data-stu-id="82db8-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="82db8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="82db8-112">PARAMETERS</span></span>

### <span data-ttu-id="82db8-113">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="82db8-113">-DisableAutoUpgradeMinorVersion</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82db8-114">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="82db8-114">-ForceRerun</span></span>
<span data-ttu-id="82db8-115">Gibt an, dass dieses Cmdlet eine erneute Ausführung derselben Erweiterungskonfiguration auf dem virtuellen Computer erzwingt, ohne die Erweiterung zu deinstallieren und erneut zu installieren.</span><span class="sxs-lookup"><span data-stu-id="82db8-115">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="82db8-116">Der Wert kann eine beliebige Zeichenfolge sein, die vom aktuellen Wert abweicht.</span><span class="sxs-lookup"><span data-stu-id="82db8-116">The value can be any string different from the current value.</span></span>

<span data-ttu-id="82db8-117">Wenn forceUpdateTag nicht geändert wird, werden Updates für öffentliche oder geschützte Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="82db8-117">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82db8-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="82db8-118">-Location</span></span>
<span data-ttu-id="82db8-119">Gibt den Speicherort der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="82db8-119">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82db8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="82db8-120">-Name</span></span>
<span data-ttu-id="82db8-121">Gibt den Namen der Erweiterung an, die von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="82db8-121">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82db8-122">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="82db8-122">-Password</span></span>
<span data-ttu-id="82db8-123">Gibt das neue Kennwort des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="82db8-123">Specifies the new password of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82db8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82db8-124">-ResourceGroupName</span></span>
<span data-ttu-id="82db8-125">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="82db8-125">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82db8-126">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="82db8-126">-TypeHandlerVersion</span></span>
<span data-ttu-id="82db8-127">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="82db8-127">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="82db8-128">Führen Sie zum Abrufen der Version das Get-AzureRmVMExtensionImage-Cmdlet mit dem Wert Microsoft. Compute für den *PublisherName* -Parameter und VMAccessAgent für den *Type* -Parameter aus.</span><span class="sxs-lookup"><span data-stu-id="82db8-128">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82db8-129">-UserName</span><span class="sxs-lookup"><span data-stu-id="82db8-129">-UserName</span></span>
<span data-ttu-id="82db8-130">Gibt den neuen Benutzernamen für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="82db8-130">Specifies the new user name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82db8-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="82db8-131">-VMName</span></span>
<span data-ttu-id="82db8-132">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="82db8-132">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="82db8-133">Dieses Cmdlet fügt dem virtuellen Computer, den dieser Parameter angibt, VMAccess hinzu.</span><span class="sxs-lookup"><span data-stu-id="82db8-133">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82db8-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="82db8-134">-Confirm</span></span>
<span data-ttu-id="82db8-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="82db8-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82db8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82db8-136">-WhatIf</span></span>
<span data-ttu-id="82db8-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="82db8-137">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="82db8-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="82db8-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82db8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82db8-139">CommonParameters</span></span>
<span data-ttu-id="82db8-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82db8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82db8-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82db8-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82db8-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="82db8-142">INPUTS</span></span>

### <span data-ttu-id="82db8-143">Keine</span><span class="sxs-lookup"><span data-stu-id="82db8-143">None</span></span>
<span data-ttu-id="82db8-144">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="82db8-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="82db8-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="82db8-145">OUTPUTS</span></span>

## <span data-ttu-id="82db8-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="82db8-146">NOTES</span></span>

## <span data-ttu-id="82db8-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="82db8-147">RELATED LINKS</span></span>

[<span data-ttu-id="82db8-148">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="82db8-148">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="82db8-149">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="82db8-149">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="82db8-150">Satz-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="82db8-150">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="82db8-151">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="82db8-151">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


