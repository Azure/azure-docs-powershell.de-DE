---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 753c1de5b2f967ad321334231c77e379e11bc2ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177696"
---
# <span data-ttu-id="ab67c-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="ab67c-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="ab67c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ab67c-102">SYNOPSIS</span></span>
<span data-ttu-id="ab67c-103">Legt die Azure SQL Server-Erweiterung auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="ab67c-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="ab67c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab67c-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab67c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab67c-105">DESCRIPTION</span></span>
<span data-ttu-id="ab67c-106">Das Cmdlet " **Set-AzVMSqlServerExtension** " legt die AzureSQL-Server Erweiterung auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="ab67c-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="ab67c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ab67c-107">EXAMPLES</span></span>

### <span data-ttu-id="ab67c-108">Beispiel 1: Festlegen der Einstellungen für automatische Patches auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="ab67c-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="ab67c-109">Mit dem ersten Befehl wird mithilfe des Cmdlets **New-AzVMSqlServerAutoPatchingConfig** ein Configuration-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="ab67c-109">The first command creates a configuration object by using the **New-AzVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="ab67c-110">Der Befehl speichert die Konfiguration in der $AutoPatchingConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ab67c-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>
<span data-ttu-id="ab67c-111">Der zweite Befehl ruft den virtuellen Computer mit dem Namen "VirtualMachine11" auf dem Dienst mit dem Namen Service02 mithilfe des Get-AzVM-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="ab67c-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="ab67c-112">Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab67c-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ab67c-113">Das aktuelle Cmdlet legt die Einstellungen für das automatische Patchen in $AutoPatchingConfig für den virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="ab67c-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="ab67c-114">Der Befehl übergibt den virtuellen Computer an das Update-AzVM-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab67c-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="ab67c-115">Beispiel 2: Festlegen automatischer Sicherungseinstellungen auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="ab67c-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="ab67c-116">Mit dem ersten Befehl wird mithilfe des Cmdlets **New-AzVMSqlServerAutoBackupConfig** ein Configuration-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="ab67c-116">The first command creates a configuration object by using the **New-AzVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="ab67c-117">Der Befehl speichert die Konfiguration in der $AutoBackupConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ab67c-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="ab67c-118">Der zweite Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine11 auf dem Dienst mit dem Namen Service02 ab und übergibt ihn dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab67c-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="ab67c-119">Das aktuelle Cmdlet legt die Einstellungen für automatische Sicherungskopien in $AutoBackupConfig für den virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="ab67c-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="ab67c-120">Der Befehl übergibt den virtuellen Computer an das Update-AzVM-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab67c-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="ab67c-121">Beispiel 3: Deaktivieren einer SQL Server-Erweiterung auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="ab67c-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="ab67c-122">Dieser Befehl ruft einen virtuellen Computer mit dem Namen VirtualMachine08 in Service03 ab und übergibt ihn dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab67c-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="ab67c-123">Der Befehl deaktiviert die Erweiterung SQL Server Virtual Machine auf diesem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="ab67c-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="ab67c-124">Beispiel 4: Deinstallieren einer SQL Server-Erweiterung auf einem bestimmten virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="ab67c-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="ab67c-125">Dieser Befehl ruft einen virtuellen Computer mit dem Namen VirtualMachine08 in Service03 ab und übergibt ihn dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab67c-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="ab67c-126">Der Befehl deinstalliert eine SQL Server Virtual Machine-Erweiterung auf diesem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="ab67c-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="ab67c-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab67c-127">PARAMETERS</span></span>

### <span data-ttu-id="ab67c-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="ab67c-128">-AutoBackupSettings</span></span>
<span data-ttu-id="ab67c-129">Gibt die automatischen SQL Server-Sicherungseinstellungen an.</span><span class="sxs-lookup"><span data-stu-id="ab67c-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="ab67c-130">Verwenden Sie das New-AzVMSqlServerAutoBackupConfig-Cmdlet, um ein **AutoBackupSettings** -Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ab67c-130">To create an **AutoBackupSettings** object , use the New-AzVMSqlServerAutoBackupConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoBackupSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab67c-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="ab67c-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="ab67c-132">Gibt die automatischen Updateeinstellungen für SQL Server an.</span><span class="sxs-lookup"><span data-stu-id="ab67c-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="ab67c-133">Verwenden Sie das New-AzVMSqlServerAutoPatchingConfig-Cmdlet, um ein **AutoPatchingSettings** -Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ab67c-133">To create an **AutoPatchingSettings** object , use the New-AzVMSqlServerAutoPatchingConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoPatchingSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab67c-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab67c-134">-DefaultProfile</span></span>
<span data-ttu-id="ab67c-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ab67c-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab67c-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="ab67c-136">-KeyVaultCredentialSettings</span></span>
```yaml
Type: Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab67c-137">-Standort</span><span class="sxs-lookup"><span data-stu-id="ab67c-137">-Location</span></span>
<span data-ttu-id="ab67c-138">Gibt den Speicherort der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="ab67c-138">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab67c-139">-Name</span><span class="sxs-lookup"><span data-stu-id="ab67c-139">-Name</span></span>
<span data-ttu-id="ab67c-140">Gibt den Namen der SQL Server-Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="ab67c-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="ab67c-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab67c-141">-ResourceGroupName</span></span>
<span data-ttu-id="ab67c-142">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="ab67c-142">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab67c-143">-Version</span><span class="sxs-lookup"><span data-stu-id="ab67c-143">-Version</span></span>
<span data-ttu-id="ab67c-144">Gibt die Version der SQL Server-Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="ab67c-144">Specifies the version of the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab67c-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="ab67c-145">-VMName</span></span>
<span data-ttu-id="ab67c-146">Gibt den Namen des virtuellen Computers an, auf dem dieses Cmdlet die SQL Server-Erweiterung festlegt.</span><span class="sxs-lookup"><span data-stu-id="ab67c-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab67c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab67c-147">CommonParameters</span></span>
<span data-ttu-id="ab67c-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab67c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab67c-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab67c-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab67c-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ab67c-150">INPUTS</span></span>

### <span data-ttu-id="ab67c-151">System. String</span><span class="sxs-lookup"><span data-stu-id="ab67c-151">System.String</span></span>

### <span data-ttu-id="ab67c-152">Microsoft. Azure. Commands. Compute. AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="ab67c-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

### <span data-ttu-id="ab67c-153">Microsoft. Azure. Commands. Compute. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="ab67c-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

### <span data-ttu-id="ab67c-154">Microsoft. Azure. Commands. Compute. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="ab67c-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="ab67c-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ab67c-155">OUTPUTS</span></span>

### <span data-ttu-id="ab67c-156">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ab67c-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ab67c-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="ab67c-157">NOTES</span></span>

## <span data-ttu-id="ab67c-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ab67c-158">RELATED LINKS</span></span>

[<span data-ttu-id="ab67c-159">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ab67c-159">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="ab67c-160">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="ab67c-160">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="ab67c-161">Neu – AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="ab67c-161">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="ab67c-162">Neu – AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="ab67c-162">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="ab67c-163">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="ab67c-163">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="ab67c-164">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="ab67c-164">Update-AzVM</span></span>](./Update-AzVM.md)


