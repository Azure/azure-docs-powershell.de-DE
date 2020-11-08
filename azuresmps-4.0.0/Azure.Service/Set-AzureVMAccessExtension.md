---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8F881112-3603-4EE7-88A4-ED45040A60AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: ecc71708c0dff8e359813bb01db0f09f2c91a0cb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006017"
---
# <span data-ttu-id="affbf-101">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="affbf-101">Set-AzureVMAccessExtension</span></span>

## <span data-ttu-id="affbf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="affbf-102">SYNOPSIS</span></span>
<span data-ttu-id="affbf-103">Legt die VMAccess-Erweiterung für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="affbf-103">Sets the VMAccess extension for a virtual machine.</span></span>

## <span data-ttu-id="affbf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="affbf-104">SYNTAX</span></span>

### <span data-ttu-id="affbf-105">EnableAccessExtension (Standard)</span><span class="sxs-lookup"><span data-stu-id="affbf-105">EnableAccessExtension (Default)</span></span>
```
Set-AzureVMAccessExtension [[-UserName] <String>] [[-Password] <String>] [[-ReferenceName] <String>]
 [[-Version] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="affbf-106">DisableAccessExtension</span><span class="sxs-lookup"><span data-stu-id="affbf-106">DisableAccessExtension</span></span>
```
Set-AzureVMAccessExtension [-Disable] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="affbf-107">UninstallAccessExtension</span><span class="sxs-lookup"><span data-stu-id="affbf-107">UninstallAccessExtension</span></span>
```
Set-AzureVMAccessExtension [-Uninstall] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="affbf-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="affbf-108">DESCRIPTION</span></span>
<span data-ttu-id="affbf-109">Das Cmdlet " **Satz-AzureVMAccessExtension** " fügt die VMAccess-Erweiterung des virtuellen Computers zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="affbf-109">The **Set-AzureVMAccessExtension** cmdlet adds the Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="affbf-110">VMAccess Extension kann verwendet werden, um ein temporäres Kennwort festzulegen, das nach der Anmeldung am Computer sofort geändert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="affbf-110">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="affbf-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="affbf-111">EXAMPLES</span></span>

### <span data-ttu-id="affbf-112">Beispiel 1: Festlegung der auf einen angegebenen virtuellen Computer angewendeten VMAccess-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="affbf-112">Example 1: Set the VMAccess extension applied to a specified virtual machine</span></span>
```
PS C:\> Set-AzureVMAccessExtension -VM $VM -UserName $User -Password $PWD;
```

<span data-ttu-id="affbf-113">Mit diesem Befehl wird die auf den angegebenen virtuellen Computer angewendete VMAccess-Erweiterung so festgelegt, wie Sie in der Variablen $VM gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="affbf-113">This command sets the VMAccess extension applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="affbf-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="affbf-114">PARAMETERS</span></span>

### <span data-ttu-id="affbf-115">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="affbf-115">-Disable</span></span>
<span data-ttu-id="affbf-116">Gibt an, dass das Cmdlet den Erweiterungszustand auf Disable festlegt.</span><span class="sxs-lookup"><span data-stu-id="affbf-116">Indicates that this cmdlet sets the Extension State to Disable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="affbf-117">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="affbf-117">-ForceUpdate</span></span>
<span data-ttu-id="affbf-118">Gibt an, dass dieses Cmdlet eine Konfiguration erneut auf eine Erweiterung anwendet, wenn die Konfiguration nicht aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="affbf-118">Indicates that this cmdlet reapplies a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="affbf-119">-Information</span><span class="sxs-lookup"><span data-stu-id="affbf-119">-InformationAction</span></span>
<span data-ttu-id="affbf-120">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="affbf-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="affbf-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="affbf-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="affbf-122">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="affbf-122">Continue</span></span>
- <span data-ttu-id="affbf-123">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="affbf-123">Ignore</span></span>
- <span data-ttu-id="affbf-124">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="affbf-124">Inquire</span></span>
- <span data-ttu-id="affbf-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="affbf-125">SilentlyContinue</span></span>
- <span data-ttu-id="affbf-126">Beenden</span><span class="sxs-lookup"><span data-stu-id="affbf-126">Stop</span></span>
- <span data-ttu-id="affbf-127">Anhalten</span><span class="sxs-lookup"><span data-stu-id="affbf-127">Suspend</span></span>

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

### <span data-ttu-id="affbf-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="affbf-128">-InformationVariable</span></span>
<span data-ttu-id="affbf-129">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="affbf-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="affbf-130">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="affbf-130">-Password</span></span>
<span data-ttu-id="affbf-131">Gibt das Kennwort für das Zurücksetzen der Anmeldeinformationen für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="affbf-131">Specifies the password for resetting the virtual machine's credential.</span></span>

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="affbf-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="affbf-132">-Profile</span></span>
<span data-ttu-id="affbf-133">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="affbf-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="affbf-134">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="affbf-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="affbf-135">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="affbf-135">-ReferenceName</span></span>
<span data-ttu-id="affbf-136">Gibt den Verweisnamen der Access-Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="affbf-136">Specifies the reference name of the access extension.</span></span>

<span data-ttu-id="affbf-137">Hierbei handelt es sich um eine benutzerdefinierte Zeichenfolge, die verwendet wird, um auf eine Erweiterung zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="affbf-137">This is a user-defined string that is used to refer to an extension.</span></span>
<span data-ttu-id="affbf-138">Sie wird angegeben, wenn die Erweiterung zum ersten Mal dem virtuellen Computer hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="affbf-138">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="affbf-139">Bei nachfolgenden Updates sollten Sie beim Aktualisieren der Erweiterung den zuvor verwendeten Verweisnamen angeben.</span><span class="sxs-lookup"><span data-stu-id="affbf-139">For subsequent updates, you should specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="affbf-140">Der *Verweisname* , der einer Erweiterung zugewiesen ist, wird mit dem Cmdlet **Get-AzureVM** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="affbf-140">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="affbf-141">-Deinstallieren</span><span class="sxs-lookup"><span data-stu-id="affbf-141">-Uninstall</span></span>
<span data-ttu-id="affbf-142">Gibt an, ob dieses Cmdlet die Access-Erweiterung deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="affbf-142">Indicates whether this cmdlet uninstalls the access extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="affbf-143">-UserName</span><span class="sxs-lookup"><span data-stu-id="affbf-143">-UserName</span></span>
<span data-ttu-id="affbf-144">Gibt den Benutzernamen an, den dieses Cmdlet verwendet, um die Anmeldeinformationen des virtuellen Computers zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="affbf-144">Specifies the user name that this cmdlet uses to reset the virtual machine's credential.</span></span>

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="affbf-145">-Version</span><span class="sxs-lookup"><span data-stu-id="affbf-145">-Version</span></span>
<span data-ttu-id="affbf-146">Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="affbf-146">Specifies the version of the extension.</span></span>

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

### <span data-ttu-id="affbf-147">-VM</span><span class="sxs-lookup"><span data-stu-id="affbf-147">-VM</span></span>
<span data-ttu-id="affbf-148">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="affbf-148">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="affbf-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="affbf-149">CommonParameters</span></span>
<span data-ttu-id="affbf-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="affbf-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="affbf-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="affbf-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="affbf-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="affbf-152">INPUTS</span></span>

## <span data-ttu-id="affbf-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="affbf-153">OUTPUTS</span></span>

## <span data-ttu-id="affbf-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="affbf-154">NOTES</span></span>

## <span data-ttu-id="affbf-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="affbf-155">RELATED LINKS</span></span>

[<span data-ttu-id="affbf-156">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="affbf-156">Get-AzureVMAccessExtension</span></span>](./Get-AzureVMAccessExtension.md)

[<span data-ttu-id="affbf-157">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="affbf-157">Remove-AzureVMAccessExtension</span></span>](./Remove-AzureVMAccessExtension.md)


