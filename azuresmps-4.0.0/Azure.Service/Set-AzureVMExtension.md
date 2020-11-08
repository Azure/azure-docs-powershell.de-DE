---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 97E9FB22-43A8-4D07-AF48-5884E4593CA9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35f3baea7440d58812056999ea4f271acf80b8d4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005652"
---
# <span data-ttu-id="451b0-101">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="451b0-101">Set-AzureVMExtension</span></span>

## <span data-ttu-id="451b0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="451b0-102">SYNOPSIS</span></span>
<span data-ttu-id="451b0-103">Legt Ressourcenerweiterungen für virtuelle Computer fest.</span><span class="sxs-lookup"><span data-stu-id="451b0-103">Sets resource extensions for virtual machines.</span></span>

## <span data-ttu-id="451b0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="451b0-104">SYNTAX</span></span>

### <span data-ttu-id="451b0-105">SetByExtensionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="451b0-105">SetByExtensionName (Default)</span></span>
```
Set-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [[-ReferenceName] <String>] [[-PublicConfiguration] <String>] [[-PrivateConfiguration] <String>] [-Disable]
 [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="451b0-106">SetByExtensionNameAndConfigFile</span><span class="sxs-lookup"><span data-stu-id="451b0-106">SetByExtensionNameAndConfigFile</span></span>
```
Set-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [[-ReferenceName] <String>] [[-PublicConfigPath] <String>] [[-PrivateConfigPath] <String>] [-Disable]
 [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="451b0-107">SetByReferenceName</span><span class="sxs-lookup"><span data-stu-id="451b0-107">SetByReferenceName</span></span>
```
Set-AzureVMExtension [-ReferenceName] <String> [[-PublicConfiguration] <String>]
 [[-PrivateConfiguration] <String>] [-Disable] [-Uninstall] [[-PublicConfigKey] <String>]
 [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="451b0-108">SetByReferenceNameAndConfigFile</span><span class="sxs-lookup"><span data-stu-id="451b0-108">SetByReferenceNameAndConfigFile</span></span>
```
Set-AzureVMExtension [-ReferenceName] <String> [[-PublicConfigPath] <String>] [[-PrivateConfigPath] <String>]
 [-Disable] [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="451b0-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="451b0-109">DESCRIPTION</span></span>
<span data-ttu-id="451b0-110">Das Cmdlet " **Set-AzureVMExtension** " legt Ressourcenerweiterungen für virtuelle Computer fest.</span><span class="sxs-lookup"><span data-stu-id="451b0-110">The **Set-AzureVMExtension** cmdlet sets resource extensions for virtual machines.</span></span>

## <span data-ttu-id="451b0-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="451b0-111">EXAMPLES</span></span>

### <span data-ttu-id="451b0-112">Beispiel 1: Erstellen eines virtuellen Computers mit angewendeten Ressourcenerweiterungen</span><span class="sxs-lookup"><span data-stu-id="451b0-112">Example 1: Create a virtual machine with resource extensions applied</span></span>
```
PS C:\> $X = New-AzureVMConfig -Name $VM -InstanceSize Small -ImageName $IMG;$X = Add-AzureProvisioningConfig -VM $X -Password $PWD -AdminUsername $USR -Windows;$X = Set-AzureVMExtension -VM $X -ExtensionName $Ext1 -Publisher $Publisher -Version $VER -PublicConfiguration $P1 -PrivateConfiguration $P2;$X = Set-AzureVMExtension -VM $X -ExtensionName $Ext2 -Publisher $Publisher -Version $VER -PublicConfiguration $P3 -PrivateConfiguration $P4;New-AzureVM -Location $LOC -ServiceName $SVC -VM $X;
```

<span data-ttu-id="451b0-113">Dieser Befehl erstellt einen virtuellen Computer mit angewendeten Ressourcenerweiterungen.</span><span class="sxs-lookup"><span data-stu-id="451b0-113">This command creates a virtual machine with resource extensions applied.</span></span>

## <span data-ttu-id="451b0-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="451b0-114">PARAMETERS</span></span>

### <span data-ttu-id="451b0-115">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="451b0-115">-Disable</span></span>
<span data-ttu-id="451b0-116">Gibt an, dass dieses Cmdlet den Erweiterungszustand deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="451b0-116">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="451b0-117">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="451b0-117">-ExtensionName</span></span>
<span data-ttu-id="451b0-118">Gibt den Namen der Erweiterung des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="451b0-118">Specifies the extension name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="451b0-119">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="451b0-119">-ForceUpdate</span></span>
<span data-ttu-id="451b0-120">Gibt an, dass dieses Cmdlet eine Konfiguration erneut auf eine Erweiterung anwendet, wenn die Konfiguration nicht aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="451b0-120">Indicates that this cmdlet re-applies a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="451b0-121">-Information</span><span class="sxs-lookup"><span data-stu-id="451b0-121">-InformationAction</span></span>
<span data-ttu-id="451b0-122">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="451b0-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="451b0-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="451b0-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="451b0-124">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="451b0-124">Continue</span></span>
- <span data-ttu-id="451b0-125">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="451b0-125">Ignore</span></span>
- <span data-ttu-id="451b0-126">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="451b0-126">Inquire</span></span>
- <span data-ttu-id="451b0-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="451b0-127">SilentlyContinue</span></span>
- <span data-ttu-id="451b0-128">Beenden</span><span class="sxs-lookup"><span data-stu-id="451b0-128">Stop</span></span>
- <span data-ttu-id="451b0-129">Anhalten</span><span class="sxs-lookup"><span data-stu-id="451b0-129">Suspend</span></span>

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

### <span data-ttu-id="451b0-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="451b0-130">-InformationVariable</span></span>
<span data-ttu-id="451b0-131">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="451b0-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="451b0-132">-PrivateConfigKey</span><span class="sxs-lookup"><span data-stu-id="451b0-132">-PrivateConfigKey</span></span>
<span data-ttu-id="451b0-133">Gibt einen privaten Konfigurationsschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="451b0-133">Specifies a private configuration key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="451b0-134">-PrivateConfigPath</span><span class="sxs-lookup"><span data-stu-id="451b0-134">-PrivateConfigPath</span></span>
<span data-ttu-id="451b0-135">Gibt den privaten Konfigurationspfad an.</span><span class="sxs-lookup"><span data-stu-id="451b0-135">Specifies the private configuration path.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionNameAndConfigFile, SetByReferenceNameAndConfigFile
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="451b0-136">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="451b0-136">-PrivateConfiguration</span></span>
<span data-ttu-id="451b0-137">Gibt den privaten Konfigurations Text an.</span><span class="sxs-lookup"><span data-stu-id="451b0-137">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByReferenceName
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="451b0-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="451b0-138">-Profile</span></span>
<span data-ttu-id="451b0-139">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="451b0-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="451b0-140">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="451b0-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="451b0-141">-PublicConfigKey</span><span class="sxs-lookup"><span data-stu-id="451b0-141">-PublicConfigKey</span></span>
<span data-ttu-id="451b0-142">Gibt den öffentlichen Konfigurationsschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="451b0-142">Specifies the public configuration key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="451b0-143">-PublicConfigPath</span><span class="sxs-lookup"><span data-stu-id="451b0-143">-PublicConfigPath</span></span>
<span data-ttu-id="451b0-144">Gibt den öffentlichen Konfigurationspfad an.</span><span class="sxs-lookup"><span data-stu-id="451b0-144">Specifies the public configuration path.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionNameAndConfigFile, SetByReferenceNameAndConfigFile
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="451b0-145">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="451b0-145">-PublicConfiguration</span></span>
<span data-ttu-id="451b0-146">Gibt den öffentlichen Konfigurations Text an.</span><span class="sxs-lookup"><span data-stu-id="451b0-146">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByReferenceName
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="451b0-147">-Publisher</span><span class="sxs-lookup"><span data-stu-id="451b0-147">-Publisher</span></span>
<span data-ttu-id="451b0-148">Gibt den Herausgeber der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="451b0-148">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="451b0-149">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="451b0-149">-ReferenceName</span></span>
<span data-ttu-id="451b0-150">Gibt den Verweisnamen der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="451b0-150">Specifies the reference name of the extension.</span></span>

<span data-ttu-id="451b0-151">Hierbei handelt es sich um eine benutzerdefinierte Zeichenfolge, die verwendet werden kann, um auf eine Erweiterung zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="451b0-151">This is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="451b0-152">Sie müssen Sie angeben, wenn die Erweiterung zum ersten Mal dem virtuellen Computer hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="451b0-152">You need to specify it when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="451b0-153">Für nachfolgende Updates müssen Sie beim Aktualisieren der Erweiterung den zuvor verwendeten Verweisnamen angeben.</span><span class="sxs-lookup"><span data-stu-id="451b0-153">For subsequent updates, you need to specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="451b0-154">Der Verweisname, der einer Erweiterung zugewiesen ist, wird mit dem Cmdlet **Get-AzureVM** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="451b0-154">The ReferenceName assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByReferenceName, SetByReferenceNameAndConfigFile
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="451b0-155">-Deinstallieren</span><span class="sxs-lookup"><span data-stu-id="451b0-155">-Uninstall</span></span>
<span data-ttu-id="451b0-156">Gibt an, dass dieses Cmdlet die Ressourcenerweiterung vom virtuellen Computer deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="451b0-156">Indicates that this cmdlet uninstalls the resource extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="451b0-157">-Version</span><span class="sxs-lookup"><span data-stu-id="451b0-157">-Version</span></span>
<span data-ttu-id="451b0-158">Gibt die Erweiterungsversion an.</span><span class="sxs-lookup"><span data-stu-id="451b0-158">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="451b0-159">-VM</span><span class="sxs-lookup"><span data-stu-id="451b0-159">-VM</span></span>
<span data-ttu-id="451b0-160">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="451b0-160">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="451b0-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="451b0-161">CommonParameters</span></span>
<span data-ttu-id="451b0-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="451b0-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="451b0-163">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="451b0-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="451b0-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="451b0-164">INPUTS</span></span>

## <span data-ttu-id="451b0-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="451b0-165">OUTPUTS</span></span>

## <span data-ttu-id="451b0-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="451b0-166">NOTES</span></span>

## <span data-ttu-id="451b0-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="451b0-167">RELATED LINKS</span></span>

[<span data-ttu-id="451b0-168">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="451b0-168">Get-AzureVMExtension</span></span>](./Get-AzureVMExtension.md)

[<span data-ttu-id="451b0-169">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="451b0-169">Remove-AzureVMExtension</span></span>](./Remove-AzureVMExtension.md)

[<span data-ttu-id="451b0-170">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="451b0-170">Get-AzureVM</span></span>](./Get-AzureVM.md)


