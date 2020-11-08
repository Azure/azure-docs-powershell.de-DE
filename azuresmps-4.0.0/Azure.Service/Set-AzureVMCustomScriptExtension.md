---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6A8F07D1-AC20-4950-9019-BDFB4FD3CF69
online version: ''
schema: 2.0.0
ms.openlocfilehash: a7569e203369bf1177b4eecc2bd689f3e20dcd48
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006243"
---
# <span data-ttu-id="028e0-101">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="028e0-101">Set-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="028e0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="028e0-102">SYNOPSIS</span></span>
<span data-ttu-id="028e0-103">Legt Informationen für eine benutzerdefinierte Skripterweiterung Azure Virtual Machine fest.</span><span class="sxs-lookup"><span data-stu-id="028e0-103">Sets information for an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="028e0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="028e0-104">SYNTAX</span></span>

### <span data-ttu-id="028e0-105">SetCustomScriptExtensionByContainerAndFileNames (Standard)</span><span class="sxs-lookup"><span data-stu-id="028e0-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-ContainerName] <String>
 [-FileName] <String[]> [[-StorageAccountName] <String>] [[-StorageEndpointSuffix] <String>]
 [[-StorageAccountKey] <String>] [[-Run] <String>] [[-Argument] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="028e0-106">DisableCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="028e0-106">DisableCustomScriptExtension</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Disable] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="028e0-107">UninstalleCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="028e0-107">UninstalleCustomScriptExtension</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Uninstall] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="028e0-108">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="028e0-108">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [[-FileUri] <String[]>]
 [-Run] <String> [[-Argument] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="028e0-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="028e0-109">DESCRIPTION</span></span>
<span data-ttu-id="028e0-110">Das Cmdlet " **Set-AzureVMCustomScriptExtension** " legt Informationen für eine benutzerdefinierte Skripterweiterung Azure Virtual Machine fest.</span><span class="sxs-lookup"><span data-stu-id="028e0-110">The **Set-AzureVMCustomScriptExtension** cmdlet sets information for an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="028e0-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="028e0-111">EXAMPLES</span></span>

### <span data-ttu-id="028e0-112">Beispiel 1: Einrichten von Informationen für eine benutzerdefinierte Skripterweiterung für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="028e0-112">Example 1: Set information for a virtual machine custom script extension</span></span>
```
PS C:\> $VM = Set-AzureVMCustomScriptExtension -VM $VM -ContainerName "Container01" -FileName "script1.ps1","script2.ps1" -Run "script1.ps1" -Argument "arg1 arg2";
PS C:\> New-AzureVM -Location "West US" -ServiceName $SVC -VM $VM;
```

<span data-ttu-id="028e0-113">Dieser Befehl legt Informationen für eine benutzerdefinierte Skripterweiterung für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="028e0-113">This command sets information for a virtual machine custom script extension.</span></span>

### <span data-ttu-id="028e0-114">Beispiel 2: Einrichten von Informationen für eine benutzerdefinierte Skripterweiterung für einen virtuellen Computer mithilfe eines Dateipfad</span><span class="sxs-lookup"><span data-stu-id="028e0-114">Example 2: Set information for a virtual machine custom script extension using a file path</span></span>
```
PS C:\> Set-AzureVMCustomScriptExtension -VM $VM -FileUri "http://www.blob.core.contoso.net/bar/script1.ps1","http://www.blob.core.contoso.net/baz/script2.ps1" -Run "script1.ps1" -Argument "arg1 arg2";
PS C:\> Update-AzureVM -ServiceName $SVC -Name $Name -VM VM;
```

<span data-ttu-id="028e0-115">Dieser Befehl legt Informationen für eine benutzerdefinierte Skripterweiterung für einen virtuellen Computer unter Verwendung mehrerer Datei-URLs fest.</span><span class="sxs-lookup"><span data-stu-id="028e0-115">This command sets information for a virtual machine custom script extension using multiple file URLs.</span></span>

## <span data-ttu-id="028e0-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="028e0-116">PARAMETERS</span></span>

### <span data-ttu-id="028e0-117">-Argument</span><span class="sxs-lookup"><span data-stu-id="028e0-117">-Argument</span></span>
<span data-ttu-id="028e0-118">Gibt eine Zeichenfolge an, die ein Argument bereitstellt, das dieses Cmdlet auf dem virtuellen Computer ausführt.</span><span class="sxs-lookup"><span data-stu-id="028e0-118">Specifies a string that supplies an argument that this cmdlet runs on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames, SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028e0-119">-Containername</span><span class="sxs-lookup"><span data-stu-id="028e0-119">-ContainerName</span></span>
<span data-ttu-id="028e0-120">Gibt den Containernamen im Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="028e0-120">Specifies the container name within the storage account.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028e0-121">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="028e0-121">-Disable</span></span>
<span data-ttu-id="028e0-122">Gibt an, dass dieses Cmdlet den Erweiterungszustand deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="028e0-122">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableCustomScriptExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028e0-123">-FileName</span><span class="sxs-lookup"><span data-stu-id="028e0-123">-FileName</span></span>
<span data-ttu-id="028e0-124">Gibt ein Zeichenfolgenarray an, das die Namen der BLOB-Dateien im angegebenen Container enthält.</span><span class="sxs-lookup"><span data-stu-id="028e0-124">Specifies a string array that contains the names of the blob files in the specified container.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028e0-125">-FileUri</span><span class="sxs-lookup"><span data-stu-id="028e0-125">-FileUri</span></span>
<span data-ttu-id="028e0-126">Gibt ein Zeichenfolgenarray an, das die URLs der BLOB-Dateien enthält.</span><span class="sxs-lookup"><span data-stu-id="028e0-126">Specifies a string array that contains the URLs of the blob files.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028e0-127">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="028e0-127">-ForceUpdate</span></span>
<span data-ttu-id="028e0-128">Gibt an, dass dieses Cmdlet eine Konfiguration erneut auf eine Erweiterung anwendet, wenn die Konfiguration nicht aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="028e0-128">Indicates that this cmdlet re-apply a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028e0-129">-Information</span><span class="sxs-lookup"><span data-stu-id="028e0-129">-InformationAction</span></span>
<span data-ttu-id="028e0-130">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="028e0-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="028e0-131">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="028e0-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="028e0-132">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="028e0-132">Continue</span></span>
- <span data-ttu-id="028e0-133">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="028e0-133">Ignore</span></span>
- <span data-ttu-id="028e0-134">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="028e0-134">Inquire</span></span>
- <span data-ttu-id="028e0-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="028e0-135">SilentlyContinue</span></span>
- <span data-ttu-id="028e0-136">Beenden</span><span class="sxs-lookup"><span data-stu-id="028e0-136">Stop</span></span>
- <span data-ttu-id="028e0-137">Anhalten</span><span class="sxs-lookup"><span data-stu-id="028e0-137">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028e0-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="028e0-138">-InformationVariable</span></span>
<span data-ttu-id="028e0-139">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="028e0-139">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028e0-140">-Profil</span><span class="sxs-lookup"><span data-stu-id="028e0-140">-Profile</span></span>
<span data-ttu-id="028e0-141">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="028e0-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="028e0-142">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="028e0-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028e0-143">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="028e0-143">-ReferenceName</span></span>
<span data-ttu-id="028e0-144">Gibt den Verweisnamen für die Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="028e0-144">Specifies the reference name for the extension.</span></span>

<span data-ttu-id="028e0-145">Dieser Parameter ist eine benutzerdefinierte Zeichenfolge, die verwendet werden kann, um auf eine Erweiterung zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="028e0-145">This parameter is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="028e0-146">Sie wird angegeben, wenn die Erweiterung zum ersten Mal dem virtuellen Computer hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="028e0-146">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="028e0-147">Für nachfolgende Updates müssen Sie beim Aktualisieren der Erweiterung den zuvor verwendeten Verweisnamen angeben.</span><span class="sxs-lookup"><span data-stu-id="028e0-147">For subsequent updates, you need to specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="028e0-148">Der *Verweisname* , der einer Erweiterung zugewiesen ist, wird mit dem Cmdlet **Get-AzureVM** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="028e0-148">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028e0-149">-Run</span><span class="sxs-lookup"><span data-stu-id="028e0-149">-Run</span></span>
<span data-ttu-id="028e0-150">Gibt den Befehl an, der von der Erweiterung auf dem virtuellen Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="028e0-150">Specifies the command this cmdlet runs by the extension on the virtual machine.</span></span>
<span data-ttu-id="028e0-151">Nur "powershell.exe" wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="028e0-151">Only "powershell.exe" is supported.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: RunFile, Command

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: RunFile, Command

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028e0-152">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="028e0-152">-StorageAccountKey</span></span>
<span data-ttu-id="028e0-153">Gibt den speicherkontoschlüssel an</span><span class="sxs-lookup"><span data-stu-id="028e0-153">Specifies the storage account key</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028e0-154">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="028e0-154">-StorageAccountName</span></span>
<span data-ttu-id="028e0-155">Gibt den Namen des speicherkontos im aktuellen Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="028e0-155">Specifies the storage account name in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028e0-156">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="028e0-156">-StorageEndpointSuffix</span></span>
<span data-ttu-id="028e0-157">Gibt den Speicherdienst Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="028e0-157">Specifies the storage service endpoint.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028e0-158">-Deinstallieren</span><span class="sxs-lookup"><span data-stu-id="028e0-158">-Uninstall</span></span>
<span data-ttu-id="028e0-159">Gibt an, dass dieses Cmdlet die benutzerdefinierte Skripterweiterung vom virtuellen Computer deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="028e0-159">Indicates that this cmdlet uninstalls the custom script extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstalleCustomScriptExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028e0-160">-Version</span><span class="sxs-lookup"><span data-stu-id="028e0-160">-Version</span></span>
<span data-ttu-id="028e0-161">Gibt die Version der benutzerdefinierten Skripterweiterung an.</span><span class="sxs-lookup"><span data-stu-id="028e0-161">Specifies the version of the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028e0-162">-VM</span><span class="sxs-lookup"><span data-stu-id="028e0-162">-VM</span></span>
<span data-ttu-id="028e0-163">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="028e0-163">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="028e0-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="028e0-164">CommonParameters</span></span>
<span data-ttu-id="028e0-165">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="028e0-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="028e0-166">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="028e0-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="028e0-167">Eingaben</span><span class="sxs-lookup"><span data-stu-id="028e0-167">INPUTS</span></span>

## <span data-ttu-id="028e0-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="028e0-168">OUTPUTS</span></span>

## <span data-ttu-id="028e0-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="028e0-169">NOTES</span></span>

## <span data-ttu-id="028e0-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="028e0-170">RELATED LINKS</span></span>

[<span data-ttu-id="028e0-171">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="028e0-171">Get-AzureVMCustomScriptExtension</span></span>](./Get-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="028e0-172">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="028e0-172">Remove-AzureVMCustomScriptExtension</span></span>](./Remove-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="028e0-173">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="028e0-173">Get-AzureVM</span></span>](./Get-AzureVM.md)


