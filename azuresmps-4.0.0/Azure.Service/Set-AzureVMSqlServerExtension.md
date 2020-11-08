---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 56C7B6F5-C2AC-4C5A-8930-645374694CC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 053bb1bfb31b90a91d69e50b77ac6411321014f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005996"
---
# <span data-ttu-id="1023d-101">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="1023d-101">Set-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="1023d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1023d-102">SYNOPSIS</span></span>
<span data-ttu-id="1023d-103">Legt die Azure SQL Server-Erweiterung auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="1023d-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="1023d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1023d-104">SYNTAX</span></span>

### <span data-ttu-id="1023d-105">EnableSqlServerExtension (Standard)</span><span class="sxs-lookup"><span data-stu-id="1023d-105">EnableSqlServerExtension (Default)</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>]
 [[-AutoPatchingSettings] <AutoPatchingSettings>] [[-AutoBackupSettings] <AutoBackupSettings>]
 [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1023d-106">DisableSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="1023d-106">DisableSqlServerExtension</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Disable] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1023d-107">UninstallSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="1023d-107">UninstallSqlServerExtension</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Uninstall]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1023d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1023d-108">DESCRIPTION</span></span>
<span data-ttu-id="1023d-109">Das Cmdlet " **Set-AzureVMSqlServerExtension** " legt die Azure SQL Server-Erweiterung auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="1023d-109">The **Set-AzureVMSqlServerExtension** cmdlet sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="1023d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1023d-110">EXAMPLES</span></span>

### <span data-ttu-id="1023d-111">Beispiel 1: Festlegen von Einstellungen für das automatische Patchen auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="1023d-111">Example 1: Set auto-patching settings on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ServiceName" -Name "VMName" | Set-AzureVMSqlServerExtension -AutoPatchingSettings $APS | Update-AzureVM
```

<span data-ttu-id="1023d-112">Dieser Befehl legt die Einstellungen für das automatische Patchen auf einem virtuellen Azure-Computer fest.</span><span class="sxs-lookup"><span data-stu-id="1023d-112">This command sets auto-patching settings on an Azure virtual machine.</span></span>

### <span data-ttu-id="1023d-113">Beispiel 2: Festlegen der Einstellungen für die automatische Sicherung auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="1023d-113">Example 2: Set auto-backup settings on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ServiceName" -Name "VMName" | Set-AzureVMSqlServerExtension -AutoBackupSettings $ABS | Update-AzureVM
```

<span data-ttu-id="1023d-114">Dieser Befehl legt Einstellungen für die automatische Sicherung auf Azure Virtual Machine fest.</span><span class="sxs-lookup"><span data-stu-id="1023d-114">This command sets auto-backup settings on Azure virtual machine.</span></span>

### <span data-ttu-id="1023d-115">Beispiel 3: Deaktivieren einer SQL Server-Erweiterung auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="1023d-115">Example 3: Disable an SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Set-AzureVMSqlServerExtension -Disable
```

<span data-ttu-id="1023d-116">Mit diesem Befehl wird die SQL Server Virtual Machine-Erweiterung auf einem bestimmten virtuellen Computer deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1023d-116">This command disables SQL Server virtual machine extension on a given virtual machine.</span></span>

### <span data-ttu-id="1023d-117">Beispiel 4: Deinstallieren einer SQL Server-Erweiterung auf einem bestimmten virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="1023d-117">Example 4: Uninstall an SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Set-AzureVMSqlServerExtension -Uninstall
```

<span data-ttu-id="1023d-118">Dieser Befehl deinstalliert eine SQL Server Virtual Machine-Erweiterung auf dem virtuellen Computer mit dem Namen VMName.</span><span class="sxs-lookup"><span data-stu-id="1023d-118">This command uninstalls a SQL Server virtual machine extension on the virtual machine named VMName.</span></span>

## <span data-ttu-id="1023d-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="1023d-119">PARAMETERS</span></span>

### <span data-ttu-id="1023d-120">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="1023d-120">-AutoBackupSettings</span></span>
<span data-ttu-id="1023d-121">Gibt die automatischen SQL Server-Sicherungseinstellungen an.</span><span class="sxs-lookup"><span data-stu-id="1023d-121">Specifies the automatic SQL Server backup settings.</span></span>

```yaml
Type: AutoBackupSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1023d-122">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="1023d-122">-AutoPatchingSettings</span></span>
<span data-ttu-id="1023d-123">Gibt die automatischen Updateeinstellungen für SQL Server an.</span><span class="sxs-lookup"><span data-stu-id="1023d-123">Specifies the automatic SQL Server patching settings.</span></span>

```yaml
Type: AutoPatchingSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1023d-124">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="1023d-124">-Disable</span></span>
<span data-ttu-id="1023d-125">Gibt an, dass dieses Cmdlet den Erweiterungszustand deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1023d-125">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableSqlServerExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1023d-126">-Information</span><span class="sxs-lookup"><span data-stu-id="1023d-126">-InformationAction</span></span>
<span data-ttu-id="1023d-127">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="1023d-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1023d-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1023d-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1023d-129">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="1023d-129">Continue</span></span>
- <span data-ttu-id="1023d-130">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="1023d-130">Ignore</span></span>
- <span data-ttu-id="1023d-131">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="1023d-131">Inquire</span></span>
- <span data-ttu-id="1023d-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1023d-132">SilentlyContinue</span></span>
- <span data-ttu-id="1023d-133">Beenden</span><span class="sxs-lookup"><span data-stu-id="1023d-133">Stop</span></span>
- <span data-ttu-id="1023d-134">Anhalten</span><span class="sxs-lookup"><span data-stu-id="1023d-134">Suspend</span></span>

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

### <span data-ttu-id="1023d-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1023d-135">-InformationVariable</span></span>
<span data-ttu-id="1023d-136">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="1023d-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1023d-137">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="1023d-137">-KeyVaultCredentialSettings</span></span>
<span data-ttu-id="1023d-138">Gibt die Einstellungen für die Key Vault-Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="1023d-138">Specifies key vault credential settings.</span></span>

```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1023d-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="1023d-139">-Profile</span></span>
<span data-ttu-id="1023d-140">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="1023d-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1023d-141">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="1023d-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1023d-142">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="1023d-142">-ReferenceName</span></span>
<span data-ttu-id="1023d-143">Gibt den Verweisnamen der SQL Server-Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="1023d-143">Specifies the reference name of the SQL Server extension.</span></span>

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

### <span data-ttu-id="1023d-144">-Deinstallieren</span><span class="sxs-lookup"><span data-stu-id="1023d-144">-Uninstall</span></span>
<span data-ttu-id="1023d-145">Gibt an, dass dieses Cmdlet die SQL Server-Erweiterung vom virtuellen Computer deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="1023d-145">Indicates that this cmdlet uninstalls the SQL Server extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallSqlServerExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1023d-146">-Version</span><span class="sxs-lookup"><span data-stu-id="1023d-146">-Version</span></span>
<span data-ttu-id="1023d-147">Gibt die Version der SQL Server-Erweiterung an, aus der Get-AzureVMSqlServerExtension Einstellungen abruft.</span><span class="sxs-lookup"><span data-stu-id="1023d-147">Specifies the version of the SQL Server extension that Get-AzureVMSqlServerExtension retrieves settings from.</span></span>

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

### <span data-ttu-id="1023d-148">-VM</span><span class="sxs-lookup"><span data-stu-id="1023d-148">-VM</span></span>
<span data-ttu-id="1023d-149">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="1023d-149">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="1023d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1023d-150">CommonParameters</span></span>
<span data-ttu-id="1023d-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1023d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1023d-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1023d-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1023d-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1023d-153">INPUTS</span></span>

## <span data-ttu-id="1023d-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1023d-154">OUTPUTS</span></span>

## <span data-ttu-id="1023d-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="1023d-155">NOTES</span></span>

## <span data-ttu-id="1023d-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1023d-156">RELATED LINKS</span></span>

[<span data-ttu-id="1023d-157">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="1023d-157">Get-AzureVMSqlServerExtension</span></span>](./Get-AzureVMSqlServerExtension.md)

[<span data-ttu-id="1023d-158">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="1023d-158">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)


