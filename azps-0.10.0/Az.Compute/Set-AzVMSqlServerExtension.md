---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 1795216cbc18da2d503a1e0056d614337cd12785
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398239"
---
# <span data-ttu-id="7f700-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="7f700-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="7f700-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f700-102">SYNOPSIS</span></span>
<span data-ttu-id="7f700-103">Legt die Azure SQL Server erweiterung auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="7f700-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="7f700-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f700-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f700-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f700-105">DESCRIPTION</span></span>
<span data-ttu-id="7f700-106">Das **Cmdlet "Set-AzVMSqlServerExtension"** legt die AzureSQL -Servererweiterung auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="7f700-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="7f700-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7f700-107">EXAMPLES</span></span>

### <span data-ttu-id="7f700-108">Beispiel 1: Festlegen der Einstellungen für automatisches Patchen auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="7f700-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="7f700-109">Der erste Befehl erstellt ein Konfigurationsobjekt mithilfe des **Cmdlets "New-AzureVMSqlServerAutoPatchingConfig".**</span><span class="sxs-lookup"><span data-stu-id="7f700-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="7f700-110">Der Befehl speichert die Konfiguration in der $AutoPatchingConfig Variable.</span><span class="sxs-lookup"><span data-stu-id="7f700-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>

<span data-ttu-id="7f700-111">Der zweite Befehl ruft den virtuellen Computer mit dem Namen "VirtualMachine11" für den Dienst "Service02" mit dem cmdlet Get-AzVM ab.</span><span class="sxs-lookup"><span data-stu-id="7f700-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="7f700-112">Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f700-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="7f700-113">Das aktuelle Cmdlet legt die Einstellungen für automatisches Patchen in $AutoPatchingConfig für den virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="7f700-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="7f700-114">Der Befehl übergibt den virtuellen Computer an das Update-AzVM Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f700-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="7f700-115">Beispiel 2: Festlegen von Einstellungen für die automatische Sicherung auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="7f700-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="7f700-116">Der erste Befehl erstellt ein Konfigurationsobjekt mithilfe des **Cmdlets "New-AzureVMSqlServerAutoBackupConfig".**</span><span class="sxs-lookup"><span data-stu-id="7f700-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="7f700-117">Der Befehl speichert die Konfiguration in der $AutoBackupConfig Variable.</span><span class="sxs-lookup"><span data-stu-id="7f700-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>

<span data-ttu-id="7f700-118">Der zweite Befehl ruft den virtuellen Computer namens "VirtualMachine11" für den Dienst "Service02" ab und übergibt ihn dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f700-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>

<span data-ttu-id="7f700-119">Das aktuelle Cmdlet legt die Einstellungen für die automatische Sicherung in $AutoBackupConfig für den virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="7f700-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="7f700-120">Der Befehl übergibt den virtuellen Computer an das Update-AzVM Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f700-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="7f700-121">Beispiel 3: Deaktivieren SQL Server Erweiterung auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="7f700-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="7f700-122">Dieser Befehl ruft einen virtuellen Computer namens "VirtualMachine08" auf Service03 ab und übergibt ihn dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f700-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="7f700-123">Der Befehl deaktiviert die SQL Server des virtuellen Computers auf diesem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="7f700-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="7f700-124">Beispiel 4: Deinstallieren SQL Server Erweiterung auf einem bestimmten virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="7f700-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="7f700-125">Dieser Befehl ruft einen virtuellen Computer namens "VirtualMachine08" auf Service03 ab und übergibt ihn dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f700-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="7f700-126">Mit dem Befehl wird eine SQL Server virtuellen Computererweiterung auf diesem virtuellen Computer deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="7f700-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="7f700-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f700-127">PARAMETERS</span></span>

### <span data-ttu-id="7f700-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="7f700-128">-AutoBackupSettings</span></span>
<span data-ttu-id="7f700-129">Gibt die einstellungen für die automatische SQL Server an.</span><span class="sxs-lookup"><span data-stu-id="7f700-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="7f700-130">Verwenden Sie zum **Erstellen eines AutoBackupSettings-Objekts** das New-AzureVMSqlServerAutoBackupConfig Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f700-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="7f700-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="7f700-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="7f700-132">Gibt die Einstellungen für das automatische SQL Server patchen an.</span><span class="sxs-lookup"><span data-stu-id="7f700-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="7f700-133">Verwenden Sie zum **Erstellen eines AutoPatchingSettings-Objekts** das New-AzureVMSqlServerAutoPatchingConfig Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f700-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="7f700-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f700-134">-DefaultProfile</span></span>
<span data-ttu-id="7f700-135">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f700-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f700-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="7f700-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="7f700-137">-Location</span><span class="sxs-lookup"><span data-stu-id="7f700-137">-Location</span></span>
<span data-ttu-id="7f700-138">Gibt den Speicherort des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="7f700-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="7f700-139">-Name</span><span class="sxs-lookup"><span data-stu-id="7f700-139">-Name</span></span>
<span data-ttu-id="7f700-140">Gibt den Namen des Namens der SQL Server Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="7f700-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="7f700-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f700-141">-ResourceGroupName</span></span>
<span data-ttu-id="7f700-142">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="7f700-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7f700-143">-Version</span><span class="sxs-lookup"><span data-stu-id="7f700-143">-Version</span></span>
<span data-ttu-id="7f700-144">Gibt die Version der Erweiterung SQL Server an.</span><span class="sxs-lookup"><span data-stu-id="7f700-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="7f700-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="7f700-145">-VMName</span></span>
<span data-ttu-id="7f700-146">Gibt den Namen des virtuellen Computers an, auf dem dieses Cmdlet die SQL Server legt.</span><span class="sxs-lookup"><span data-stu-id="7f700-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="7f700-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f700-147">CommonParameters</span></span>
<span data-ttu-id="7f700-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f700-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f700-149">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f700-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f700-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7f700-150">INPUTS</span></span>

### <span data-ttu-id="7f700-151">Keine</span><span class="sxs-lookup"><span data-stu-id="7f700-151">None</span></span>
<span data-ttu-id="7f700-152">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="7f700-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7f700-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7f700-153">OUTPUTS</span></span>

### <span data-ttu-id="7f700-154">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7f700-154">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7f700-155">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7f700-155">NOTES</span></span>

## <span data-ttu-id="7f700-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7f700-156">RELATED LINKS</span></span>

[<span data-ttu-id="7f700-157">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="7f700-157">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="7f700-158">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="7f700-158">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="7f700-159">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="7f700-159">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="7f700-160">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="7f700-160">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="7f700-161">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="7f700-161">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="7f700-162">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="7f700-162">Update-AzVM</span></span>](./Update-AzVM.md)


