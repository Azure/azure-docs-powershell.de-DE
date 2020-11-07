---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmsqlserverextension
schema: 2.0.0
ms.openlocfilehash: 2a1dbf5eea7f772a7819ed341a681adc24134225
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849724"
---
# <span data-ttu-id="72fcc-101">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="72fcc-101">Set-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="72fcc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="72fcc-103">Legt die Azure SQL Server-Erweiterung auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="72fcc-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72fcc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72fcc-104">SYNTAX</span></span>

```
Set-AzureRmVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72fcc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72fcc-105">DESCRIPTION</span></span>
<span data-ttu-id="72fcc-106">Das Cmdlet " **Set-AzureRmVMSqlServerExtension** " legt die AzureSQL-Server Erweiterung auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="72fcc-106">The **Set-AzureRmVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="72fcc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72fcc-107">EXAMPLES</span></span>

### <span data-ttu-id="72fcc-108">Beispiel 1: Festlegen der Einstellungen für automatische Patches auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="72fcc-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzureRmVM
```

<span data-ttu-id="72fcc-109">Mit dem ersten Befehl wird mithilfe des Cmdlets **New-AzureVMSqlServerAutoPatchingConfig** ein Configuration-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="72fcc-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="72fcc-110">Der Befehl speichert die Konfiguration in der $AutoPatchingConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="72fcc-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>

<span data-ttu-id="72fcc-111">Der zweite Befehl ruft den virtuellen Computer mit dem Namen "VirtualMachine11" auf dem Dienst mit dem Namen Service02 mithilfe des Get-AzureRmVM-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="72fcc-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="72fcc-112">Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72fcc-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="72fcc-113">Das aktuelle Cmdlet legt die Einstellungen für das automatische Patchen in $AutoPatchingConfig für den virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="72fcc-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="72fcc-114">Der Befehl übergibt den virtuellen Computer an das Update-AzureRmVM-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72fcc-114">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="72fcc-115">Beispiel 2: Festlegen automatischer Sicherungseinstellungen auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="72fcc-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzureRmVM
```

<span data-ttu-id="72fcc-116">Mit dem ersten Befehl wird mithilfe des Cmdlets **New-AzureVMSqlServerAutoBackupConfig** ein Configuration-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="72fcc-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="72fcc-117">Der Befehl speichert die Konfiguration in der $AutoBackupConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="72fcc-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>

<span data-ttu-id="72fcc-118">Der zweite Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine11 auf dem Dienst mit dem Namen Service02 ab und übergibt ihn dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72fcc-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>

<span data-ttu-id="72fcc-119">Das aktuelle Cmdlet legt die Einstellungen für automatische Sicherungskopien in $AutoBackupConfig für den virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="72fcc-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="72fcc-120">Der Befehl übergibt den virtuellen Computer an das Update-AzureRmVM-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72fcc-120">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="72fcc-121">Beispiel 3: Deaktivieren einer SQL Server-Erweiterung auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="72fcc-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Disable
```

<span data-ttu-id="72fcc-122">Dieser Befehl ruft einen virtuellen Computer mit dem Namen VirtualMachine08 in Service03 ab und übergibt ihn dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72fcc-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="72fcc-123">Der Befehl deaktiviert die Erweiterung SQL Server Virtual Machine auf diesem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="72fcc-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="72fcc-124">Beispiel 4: Deinstallieren einer SQL Server-Erweiterung auf einem bestimmten virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="72fcc-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Uninstall
```

<span data-ttu-id="72fcc-125">Dieser Befehl ruft einen virtuellen Computer mit dem Namen VirtualMachine08 in Service03 ab und übergibt ihn dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72fcc-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="72fcc-126">Der Befehl deinstalliert eine SQL Server Virtual Machine-Erweiterung auf diesem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="72fcc-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="72fcc-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="72fcc-127">PARAMETERS</span></span>

### <span data-ttu-id="72fcc-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="72fcc-128">-AutoBackupSettings</span></span>
<span data-ttu-id="72fcc-129">Gibt die automatischen SQL Server-Sicherungseinstellungen an.</span><span class="sxs-lookup"><span data-stu-id="72fcc-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="72fcc-130">Verwenden Sie das New-AzureVMSqlServerAutoBackupConfig-Cmdlet, um ein **AutoBackupSettings** -Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="72fcc-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

```yaml
Type: AutoBackupSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72fcc-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="72fcc-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="72fcc-132">Gibt die automatischen Updateeinstellungen für SQL Server an.</span><span class="sxs-lookup"><span data-stu-id="72fcc-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="72fcc-133">Verwenden Sie das New-AzureVMSqlServerAutoPatchingConfig-Cmdlet, um ein **AutoPatchingSettings** -Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="72fcc-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

```yaml
Type: AutoPatchingSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72fcc-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72fcc-134">-DefaultProfile</span></span>
<span data-ttu-id="72fcc-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="72fcc-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72fcc-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="72fcc-136">-KeyVaultCredentialSettings</span></span>
```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72fcc-137">-Standort</span><span class="sxs-lookup"><span data-stu-id="72fcc-137">-Location</span></span>
<span data-ttu-id="72fcc-138">Gibt den Speicherort der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="72fcc-138">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72fcc-139">-Name</span><span class="sxs-lookup"><span data-stu-id="72fcc-139">-Name</span></span>
<span data-ttu-id="72fcc-140">Gibt den Namen der SQL Server-Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="72fcc-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="72fcc-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72fcc-141">-ResourceGroupName</span></span>
<span data-ttu-id="72fcc-142">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="72fcc-142">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72fcc-143">-Version</span><span class="sxs-lookup"><span data-stu-id="72fcc-143">-Version</span></span>
<span data-ttu-id="72fcc-144">Gibt die Version der SQL Server-Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="72fcc-144">Specifies the version of the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72fcc-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="72fcc-145">-VMName</span></span>
<span data-ttu-id="72fcc-146">Gibt den Namen des virtuellen Computers an, auf dem dieses Cmdlet die SQL Server-Erweiterung festlegt.</span><span class="sxs-lookup"><span data-stu-id="72fcc-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72fcc-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72fcc-147">CommonParameters</span></span>
<span data-ttu-id="72fcc-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72fcc-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72fcc-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72fcc-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72fcc-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72fcc-150">INPUTS</span></span>

### <span data-ttu-id="72fcc-151">Keine</span><span class="sxs-lookup"><span data-stu-id="72fcc-151">None</span></span>
<span data-ttu-id="72fcc-152">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="72fcc-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72fcc-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72fcc-153">OUTPUTS</span></span>

### <span data-ttu-id="72fcc-154">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="72fcc-154">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="72fcc-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="72fcc-155">NOTES</span></span>

## <span data-ttu-id="72fcc-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72fcc-156">RELATED LINKS</span></span>

[<span data-ttu-id="72fcc-157">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="72fcc-157">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="72fcc-158">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="72fcc-158">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)





[<span data-ttu-id="72fcc-159">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="72fcc-159">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="72fcc-160">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="72fcc-160">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


