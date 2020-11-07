---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: 61aa9673121f53f36d5c2994db348160eac55cd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664095"
---
# <span data-ttu-id="d58cb-101">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d58cb-101">Set-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="d58cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d58cb-102">SYNOPSIS</span></span>
<span data-ttu-id="d58cb-103">Legt die Azure SQL Server-Erweiterung auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="d58cb-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d58cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d58cb-104">SYNTAX</span></span>

```
Set-AzureRmVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d58cb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d58cb-105">DESCRIPTION</span></span>
<span data-ttu-id="d58cb-106">Das Cmdlet " **Set-AzureRmVMSqlServerExtension** " legt die AzureSQL-Server Erweiterung auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="d58cb-106">The **Set-AzureRmVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="d58cb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d58cb-107">EXAMPLES</span></span>

### <span data-ttu-id="d58cb-108">Beispiel 1: Festlegen der Einstellungen für automatische Patches auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="d58cb-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzureRmVM
```

<span data-ttu-id="d58cb-109">Mit dem ersten Befehl wird mithilfe des Cmdlets **New-AzureVMSqlServerAutoPatchingConfig** ein Configuration-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="d58cb-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="d58cb-110">Der Befehl speichert die Konfiguration in der $AutoPatchingConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d58cb-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>
<span data-ttu-id="d58cb-111">Der zweite Befehl ruft den virtuellen Computer mit dem Namen "VirtualMachine11" auf dem Dienst mit dem Namen Service02 mithilfe des Get-AzureRmVM-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="d58cb-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="d58cb-112">Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d58cb-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d58cb-113">Das aktuelle Cmdlet legt die Einstellungen für das automatische Patchen in $AutoPatchingConfig für den virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="d58cb-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="d58cb-114">Der Befehl übergibt den virtuellen Computer an das Update-AzureRmVM-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d58cb-114">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="d58cb-115">Beispiel 2: Festlegen automatischer Sicherungseinstellungen auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="d58cb-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzureRmVM
```

<span data-ttu-id="d58cb-116">Mit dem ersten Befehl wird mithilfe des Cmdlets **New-AzureVMSqlServerAutoBackupConfig** ein Configuration-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="d58cb-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="d58cb-117">Der Befehl speichert die Konfiguration in der $AutoBackupConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d58cb-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="d58cb-118">Der zweite Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine11 auf dem Dienst mit dem Namen Service02 ab und übergibt ihn dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d58cb-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="d58cb-119">Das aktuelle Cmdlet legt die Einstellungen für automatische Sicherungskopien in $AutoBackupConfig für den virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="d58cb-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="d58cb-120">Der Befehl übergibt den virtuellen Computer an das Update-AzureRmVM-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d58cb-120">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="d58cb-121">Beispiel 3: Deaktivieren einer SQL Server-Erweiterung auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="d58cb-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Disable
```

<span data-ttu-id="d58cb-122">Dieser Befehl ruft einen virtuellen Computer mit dem Namen VirtualMachine08 in Service03 ab und übergibt ihn dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d58cb-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="d58cb-123">Der Befehl deaktiviert die Erweiterung SQL Server Virtual Machine auf diesem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="d58cb-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="d58cb-124">Beispiel 4: Deinstallieren einer SQL Server-Erweiterung auf einem bestimmten virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="d58cb-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Uninstall
```

<span data-ttu-id="d58cb-125">Dieser Befehl ruft einen virtuellen Computer mit dem Namen VirtualMachine08 in Service03 ab und übergibt ihn dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d58cb-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="d58cb-126">Der Befehl deinstalliert eine SQL Server Virtual Machine-Erweiterung auf diesem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="d58cb-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="d58cb-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="d58cb-127">PARAMETERS</span></span>

### <span data-ttu-id="d58cb-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="d58cb-128">-AutoBackupSettings</span></span>
<span data-ttu-id="d58cb-129">Gibt die automatischen SQL Server-Sicherungseinstellungen an.</span><span class="sxs-lookup"><span data-stu-id="d58cb-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="d58cb-130">Verwenden Sie das New-AzureVMSqlServerAutoBackupConfig-Cmdlet, um ein **AutoBackupSettings** -Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d58cb-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="d58cb-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="d58cb-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="d58cb-132">Gibt die automatischen Updateeinstellungen für SQL Server an.</span><span class="sxs-lookup"><span data-stu-id="d58cb-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="d58cb-133">Verwenden Sie das New-AzureVMSqlServerAutoPatchingConfig-Cmdlet, um ein **AutoPatchingSettings** -Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d58cb-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="d58cb-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d58cb-134">-DefaultProfile</span></span>
<span data-ttu-id="d58cb-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d58cb-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d58cb-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="d58cb-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="d58cb-137">-Standort</span><span class="sxs-lookup"><span data-stu-id="d58cb-137">-Location</span></span>
<span data-ttu-id="d58cb-138">Gibt den Speicherort der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="d58cb-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="d58cb-139">-Name</span><span class="sxs-lookup"><span data-stu-id="d58cb-139">-Name</span></span>
<span data-ttu-id="d58cb-140">Gibt den Namen der SQL Server-Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="d58cb-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="d58cb-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d58cb-141">-ResourceGroupName</span></span>
<span data-ttu-id="d58cb-142">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="d58cb-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d58cb-143">-Version</span><span class="sxs-lookup"><span data-stu-id="d58cb-143">-Version</span></span>
<span data-ttu-id="d58cb-144">Gibt die Version der SQL Server-Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="d58cb-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="d58cb-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="d58cb-145">-VMName</span></span>
<span data-ttu-id="d58cb-146">Gibt den Namen des virtuellen Computers an, auf dem dieses Cmdlet die SQL Server-Erweiterung festlegt.</span><span class="sxs-lookup"><span data-stu-id="d58cb-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="d58cb-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d58cb-147">CommonParameters</span></span>
<span data-ttu-id="d58cb-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d58cb-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d58cb-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d58cb-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d58cb-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d58cb-150">INPUTS</span></span>

### <span data-ttu-id="d58cb-151">System. String</span><span class="sxs-lookup"><span data-stu-id="d58cb-151">System.String</span></span>

### <span data-ttu-id="d58cb-152">Microsoft. Azure. Commands. Compute. AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="d58cb-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

### <span data-ttu-id="d58cb-153">Microsoft. Azure. Commands. Compute. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="d58cb-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

### <span data-ttu-id="d58cb-154">Microsoft. Azure. Commands. Compute. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="d58cb-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="d58cb-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d58cb-155">OUTPUTS</span></span>

### <span data-ttu-id="d58cb-156">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d58cb-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d58cb-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="d58cb-157">NOTES</span></span>

## <span data-ttu-id="d58cb-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d58cb-158">RELATED LINKS</span></span>

[<span data-ttu-id="d58cb-159">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d58cb-159">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="d58cb-160">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d58cb-160">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="d58cb-161">Neu – AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="d58cb-161">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="d58cb-162">Neu – AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="d58cb-162">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="d58cb-163">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d58cb-163">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="d58cb-164">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d58cb-164">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


