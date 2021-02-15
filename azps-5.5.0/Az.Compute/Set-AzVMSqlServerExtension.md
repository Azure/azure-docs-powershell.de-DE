---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 753c1de5b2f967ad321334231c77e379e11bc2ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164196"
---
# <span data-ttu-id="6edcd-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="6edcd-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="6edcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6edcd-102">SYNOPSIS</span></span>
<span data-ttu-id="6edcd-103">Legt die Azure SQL Server erweiterung auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="6edcd-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="6edcd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6edcd-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6edcd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6edcd-105">DESCRIPTION</span></span>
<span data-ttu-id="6edcd-106">Das **Cmdlet "Set-AzVMSqlServerExtension"** legt die AzureSQL -Servererweiterung auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="6edcd-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="6edcd-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6edcd-107">EXAMPLES</span></span>

### <span data-ttu-id="6edcd-108">Beispiel 1: Festlegen der Einstellungen für automatisches Patchen auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="6edcd-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="6edcd-109">Der erste Befehl erstellt ein Konfigurationsobjekt mithilfe des **Cmdlets "New-AzVMSqlServerAutoPatchingConfig".**</span><span class="sxs-lookup"><span data-stu-id="6edcd-109">The first command creates a configuration object by using the **New-AzVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="6edcd-110">Der Befehl speichert die Konfiguration in der $AutoPatchingConfig Variable.</span><span class="sxs-lookup"><span data-stu-id="6edcd-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>
<span data-ttu-id="6edcd-111">Der zweite Befehl ruft den virtuellen Computer mit dem Namen "VirtualMachine11" für den Dienst "Service02" mit dem cmdlet Get-AzVM ab.</span><span class="sxs-lookup"><span data-stu-id="6edcd-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="6edcd-112">Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6edcd-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6edcd-113">Das aktuelle Cmdlet legt die Einstellungen für automatisches Patchen in $AutoPatchingConfig für den virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="6edcd-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="6edcd-114">Der Befehl übergibt den virtuellen Computer an das Update-AzVM Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6edcd-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="6edcd-115">Beispiel 2: Festlegen von Einstellungen für die automatische Sicherung auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="6edcd-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="6edcd-116">Der erste Befehl erstellt ein Konfigurationsobjekt mithilfe des **Cmdlets "New-AzVMSqlServerAutoBackupConfig".**</span><span class="sxs-lookup"><span data-stu-id="6edcd-116">The first command creates a configuration object by using the **New-AzVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="6edcd-117">Der Befehl speichert die Konfiguration in der $AutoBackupConfig Variable.</span><span class="sxs-lookup"><span data-stu-id="6edcd-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="6edcd-118">Der zweite Befehl ruft den virtuellen Computer namens "VirtualMachine11" für den Dienst "Service02" ab und übergibt ihn dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6edcd-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="6edcd-119">Das aktuelle Cmdlet legt die Einstellungen für die automatische Sicherung in $AutoBackupConfig für den virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="6edcd-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="6edcd-120">Der Befehl übergibt den virtuellen Computer an das Update-AzVM Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6edcd-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="6edcd-121">Beispiel 3: Deaktivieren SQL Server Erweiterung auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="6edcd-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="6edcd-122">Dieser Befehl ruft einen virtuellen Computer namens "VirtualMachine08" auf Service03 ab und übergibt ihn dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6edcd-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="6edcd-123">Der Befehl deaktiviert die SQL Server des virtuellen Computers auf diesem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="6edcd-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="6edcd-124">Beispiel 4: Deinstallieren SQL Server Erweiterung auf einem bestimmten virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="6edcd-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="6edcd-125">Dieser Befehl ruft einen virtuellen Computer namens "VirtualMachine08" auf Service03 ab und übergibt ihn dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6edcd-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="6edcd-126">Mit dem Befehl wird eine SQL Server virtuellen Computererweiterung auf diesem virtuellen Computer deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="6edcd-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="6edcd-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6edcd-127">PARAMETERS</span></span>

### <span data-ttu-id="6edcd-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="6edcd-128">-AutoBackupSettings</span></span>
<span data-ttu-id="6edcd-129">Gibt die einstellungen für die automatische SQL Server an.</span><span class="sxs-lookup"><span data-stu-id="6edcd-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="6edcd-130">Verwenden Sie zum **Erstellen eines AutoBackupSettings-Objekts** das New-AzVMSqlServerAutoBackupConfig Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6edcd-130">To create an **AutoBackupSettings** object , use the New-AzVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="6edcd-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="6edcd-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="6edcd-132">Gibt die Einstellungen für das automatische SQL Server patchen an.</span><span class="sxs-lookup"><span data-stu-id="6edcd-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="6edcd-133">Zum Erstellen eines **AutoPatchingSettings-Objekts** verwenden Sie das New-AzVMSqlServerAutoPatchingConfig Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6edcd-133">To create an **AutoPatchingSettings** object , use the New-AzVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="6edcd-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6edcd-134">-DefaultProfile</span></span>
<span data-ttu-id="6edcd-135">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6edcd-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6edcd-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="6edcd-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="6edcd-137">-Location</span><span class="sxs-lookup"><span data-stu-id="6edcd-137">-Location</span></span>
<span data-ttu-id="6edcd-138">Gibt den Speicherort des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="6edcd-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="6edcd-139">-Name</span><span class="sxs-lookup"><span data-stu-id="6edcd-139">-Name</span></span>
<span data-ttu-id="6edcd-140">Gibt den Namen des Namens der SQL Server Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="6edcd-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="6edcd-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6edcd-141">-ResourceGroupName</span></span>
<span data-ttu-id="6edcd-142">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="6edcd-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6edcd-143">-Version</span><span class="sxs-lookup"><span data-stu-id="6edcd-143">-Version</span></span>
<span data-ttu-id="6edcd-144">Gibt die Version der Erweiterung SQL Server an.</span><span class="sxs-lookup"><span data-stu-id="6edcd-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="6edcd-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="6edcd-145">-VMName</span></span>
<span data-ttu-id="6edcd-146">Gibt den Namen des virtuellen Computers an, auf dem dieses Cmdlet die SQL Server legt.</span><span class="sxs-lookup"><span data-stu-id="6edcd-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="6edcd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6edcd-147">CommonParameters</span></span>
<span data-ttu-id="6edcd-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6edcd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6edcd-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6edcd-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6edcd-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6edcd-150">INPUTS</span></span>

### <span data-ttu-id="6edcd-151">System.String</span><span class="sxs-lookup"><span data-stu-id="6edcd-151">System.String</span></span>

### <span data-ttu-id="6edcd-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="6edcd-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

### <span data-ttu-id="6edcd-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="6edcd-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

### <span data-ttu-id="6edcd-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="6edcd-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="6edcd-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6edcd-155">OUTPUTS</span></span>

### <span data-ttu-id="6edcd-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6edcd-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6edcd-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6edcd-157">NOTES</span></span>

## <span data-ttu-id="6edcd-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6edcd-158">RELATED LINKS</span></span>

[<span data-ttu-id="6edcd-159">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="6edcd-159">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="6edcd-160">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="6edcd-160">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="6edcd-161">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="6edcd-161">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="6edcd-162">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="6edcd-162">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="6edcd-163">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="6edcd-163">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="6edcd-164">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="6edcd-164">Update-AzVM</span></span>](./Update-AzVM.md)


