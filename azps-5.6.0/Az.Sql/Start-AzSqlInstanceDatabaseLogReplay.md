---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Start-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: ce937cc6f7e4bc68592ed089a3028e2919fde29f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924408"
---
# <span data-ttu-id="e0849-101">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="e0849-101">Start-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="e0849-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0849-102">SYNOPSIS</span></span>
<span data-ttu-id="e0849-103">Startet einen Protokollwiedergabedienst mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="e0849-103">Starts a Log Replay service with the given parameters.</span></span>

## <span data-ttu-id="e0849-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0849-104">SYNTAX</span></span>

### <span data-ttu-id="e0849-105">LogReplayInstanceDatabaseFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="e0849-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-AsJob] [-Name] <String>
 [-InstanceName] <String> [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0849-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="e0849-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-AsJob] [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0849-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0849-107">DESCRIPTION</span></span>
<span data-ttu-id="e0849-108">Das **Cmdlet Start-AzSqlInstanceDatabaseLogReplay** initiiert den Start des Protokollwiedergabediensts.</span><span class="sxs-lookup"><span data-stu-id="e0849-108">The **Start-AzSqlInstanceDatabaseLogReplay** cmdlet initiate start of the log replay service.</span></span>

## <span data-ttu-id="e0849-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e0849-109">EXAMPLES</span></span>

### <span data-ttu-id="e0849-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e0849-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
    -AutoComplete -LastBackupName "last_backup.bak"
```

<span data-ttu-id="e0849-111">Mit diesem Befehl wird eine neue verwaltete Datenbank erstellt und die Wiederherstellung von Sicherungen aus dem angegebenen Container gestartet, bis last_backup.bak wiederhergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e0849-111">This command will create new managed database and will start restoring backups from the given container until last_backup.bak is restored.</span></span>

### <span data-ttu-id="e0849-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e0849-112">Example 2</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
```

<span data-ttu-id="e0849-113">Mit diesem Befehl wird eine neue verwaltete Datenbank erstellt und die Wiederherstellung von Sicherungen aus dem angegebenen Container gestartet, bis Complete-AzSqlInstanceDatabaseLogReplay mit der letzten gesuchten Sicherung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e0849-113">This command will create new managed database and will start restoring backups from the given container until Complete-AzSqlInstanceDatabaseLogReplay is called with the last backup wanted.</span></span>

## <span data-ttu-id="e0849-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e0849-114">PARAMETERS</span></span>

### <span data-ttu-id="e0849-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0849-115">-AsJob</span></span>
<span data-ttu-id="e0849-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e0849-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0849-117">-AutoCompleteRestore</span><span class="sxs-lookup"><span data-stu-id="e0849-117">-AutoCompleteRestore</span></span>
<span data-ttu-id="e0849-118">Der Indikator, ob die Wiederherstellung nach Abschluss automatisch abgeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e0849-118">The indicator whether or not to auto-complete restore upon completion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0849-119">-Sortierung</span><span class="sxs-lookup"><span data-stu-id="e0849-119">-Collation</span></span>
<span data-ttu-id="e0849-120">Die Sortierung der zu verwendende Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="e0849-120">The collation of the instance database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0849-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0849-121">-DefaultProfile</span></span>
<span data-ttu-id="e0849-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0849-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0849-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0849-123">-InputObject</span></span>
<span data-ttu-id="e0849-124">Das Instanzdatenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="e0849-124">The instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0849-125">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e0849-125">-InstanceName</span></span>
<span data-ttu-id="e0849-126">Der Name der -Instanz.</span><span class="sxs-lookup"><span data-stu-id="e0849-126">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0849-127">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="e0849-127">-LastBackupName</span></span>
<span data-ttu-id="e0849-128">Der Name der letzten sicherungsdatei, die wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e0849-128">The name of the last backup file to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0849-129">-Name</span><span class="sxs-lookup"><span data-stu-id="e0849-129">-Name</span></span>
<span data-ttu-id="e0849-130">Der Name der Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="e0849-130">The name of the instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0849-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0849-131">-PassThru</span></span>
<span data-ttu-id="e0849-132">Definiert, ob die Synchronisierungsgruppe zurückgeben wird.</span><span class="sxs-lookup"><span data-stu-id="e0849-132">Defines Whether return the sync group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0849-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0849-133">-ResourceGroupName</span></span>
<span data-ttu-id="e0849-134">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e0849-134">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0849-135">-StorageContainerSasToken</span><span class="sxs-lookup"><span data-stu-id="e0849-135">-StorageContainerSasToken</span></span>
<span data-ttu-id="e0849-136">Das Sas-Token für den Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="e0849-136">The storage container Sas token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasToken

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0849-137">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="e0849-137">-StorageContainerUri</span></span>
<span data-ttu-id="e0849-138">Der Speichercontainer-URI.</span><span class="sxs-lookup"><span data-stu-id="e0849-138">The storage container URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Storage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0849-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e0849-139">-Confirm</span></span>
<span data-ttu-id="e0849-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e0849-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0849-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0849-141">-WhatIf</span></span>
<span data-ttu-id="e0849-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0849-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0849-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0849-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0849-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0849-144">CommonParameters</span></span>
<span data-ttu-id="e0849-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0849-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0849-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0849-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0849-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e0849-147">INPUTS</span></span>

### <span data-ttu-id="e0849-148">System.String</span><span class="sxs-lookup"><span data-stu-id="e0849-148">System.String</span></span>

### <span data-ttu-id="e0849-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e0849-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="e0849-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e0849-150">OUTPUTS</span></span>

### <span data-ttu-id="e0849-151">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e0849-151">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="e0849-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e0849-152">NOTES</span></span>

## <span data-ttu-id="e0849-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e0849-153">RELATED LINKS</span></span>
