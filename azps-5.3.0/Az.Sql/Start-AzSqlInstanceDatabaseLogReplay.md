---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Start-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 61a87f61efaa889af830cc7bdaa44bcf0b7fc698
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468391"
---
# <span data-ttu-id="fa645-101">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="fa645-101">Start-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="fa645-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa645-102">SYNOPSIS</span></span>
<span data-ttu-id="fa645-103">Startet einen Protokollwiedergabedienst mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="fa645-103">Starts a Log Replay service with the given parameters.</span></span>

## <span data-ttu-id="fa645-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa645-104">SYNTAX</span></span>

### <span data-ttu-id="fa645-105">LogReplayInstanceDatabaseFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="fa645-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-Name] <String>
 [-InstanceName] <String> [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa645-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="fa645-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa645-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa645-107">DESCRIPTION</span></span>
<span data-ttu-id="fa645-108">Das **Cmdlet "Start-AzSqlInstanceDatabaseLogReplay"** initiiert den Start des Protokollwiedergabediensts.</span><span class="sxs-lookup"><span data-stu-id="fa645-108">The **Start-AzSqlInstanceDatabaseLogReplay** cmdlet initiate start of the log replay service.</span></span>

## <span data-ttu-id="fa645-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fa645-109">EXAMPLES</span></span>

### <span data-ttu-id="fa645-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fa645-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
    -AutoComplete -LastBackupName "last_backup.bak"
```

<span data-ttu-id="fa645-111">Dieser Befehl erstellt eine neue verwaltete Datenbank und startet die Wiederherstellung von Sicherungen aus dem angegebenen Container, bis last_backup.bak wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fa645-111">This command will create new managed database and will start restoring backups from the given container until last_backup.bak is restored.</span></span>

### <span data-ttu-id="fa645-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fa645-112">Example 2</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
```

<span data-ttu-id="fa645-113">Dieser Befehl erstellt eine neue verwaltete Datenbank und startet die Wiederherstellung von Sicherungen aus dem angegebenen Container, bis Complete-AzSqlInstanceDatabaseLogReplay mit der letzten gesuchten Sicherung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fa645-113">This command will create new managed database and will start restoring backups from the given container until Complete-AzSqlInstanceDatabaseLogReplay is called with the last backup wanted.</span></span>

## <span data-ttu-id="fa645-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa645-114">PARAMETERS</span></span>

### <span data-ttu-id="fa645-115">-AutoCompleteRestore</span><span class="sxs-lookup"><span data-stu-id="fa645-115">-AutoCompleteRestore</span></span>
<span data-ttu-id="fa645-116">Der Indikator gibt an, ob die Wiederherstellung nach Abschluss automatisch abgeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa645-116">The indicator whether or not to auto-complete restore upon completion.</span></span>

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

### <span data-ttu-id="fa645-117">-Collation</span><span class="sxs-lookup"><span data-stu-id="fa645-117">-Collation</span></span>
<span data-ttu-id="fa645-118">Die Sortierung der zu verwendende Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="fa645-118">The collation of the instance database to use.</span></span>

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

### <span data-ttu-id="fa645-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa645-119">-DefaultProfile</span></span>
<span data-ttu-id="fa645-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa645-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa645-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa645-121">-InputObject</span></span>
<span data-ttu-id="fa645-122">Das Instanzdatenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="fa645-122">The instance database object.</span></span>

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

### <span data-ttu-id="fa645-123">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="fa645-123">-InstanceName</span></span>
<span data-ttu-id="fa645-124">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="fa645-124">The name of the instance.</span></span>

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

### <span data-ttu-id="fa645-125">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="fa645-125">-LastBackupName</span></span>
<span data-ttu-id="fa645-126">Der Name der letzten wiederherzustellende Sicherungsdatei.</span><span class="sxs-lookup"><span data-stu-id="fa645-126">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="fa645-127">-Name</span><span class="sxs-lookup"><span data-stu-id="fa645-127">-Name</span></span>
<span data-ttu-id="fa645-128">Der Name der Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="fa645-128">The name of the instance database.</span></span>

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

### <span data-ttu-id="fa645-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa645-129">-PassThru</span></span>
<span data-ttu-id="fa645-130">Definiert, ob die Synchronisierungsgruppe zurückgeben wird.</span><span class="sxs-lookup"><span data-stu-id="fa645-130">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="fa645-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa645-131">-ResourceGroupName</span></span>
<span data-ttu-id="fa645-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fa645-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="fa645-133">-StorageContainerSasToken</span><span class="sxs-lookup"><span data-stu-id="fa645-133">-StorageContainerSasToken</span></span>
<span data-ttu-id="fa645-134">Das Speichercontainer-Sastoken.</span><span class="sxs-lookup"><span data-stu-id="fa645-134">The storage container Sas token.</span></span>

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

### <span data-ttu-id="fa645-135">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="fa645-135">-StorageContainerUri</span></span>
<span data-ttu-id="fa645-136">Der Speichercontainer-URI.</span><span class="sxs-lookup"><span data-stu-id="fa645-136">The storage container URI.</span></span>

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

### <span data-ttu-id="fa645-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa645-137">-Confirm</span></span>
<span data-ttu-id="fa645-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fa645-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa645-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fa645-139">-WhatIf</span></span>
<span data-ttu-id="fa645-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa645-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa645-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa645-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa645-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa645-142">CommonParameters</span></span>
<span data-ttu-id="fa645-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa645-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa645-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa645-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa645-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fa645-145">INPUTS</span></span>

### <span data-ttu-id="fa645-146">System.String</span><span class="sxs-lookup"><span data-stu-id="fa645-146">System.String</span></span>

### <span data-ttu-id="fa645-147">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="fa645-147">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="fa645-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fa645-148">OUTPUTS</span></span>

### <span data-ttu-id="fa645-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="fa645-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="fa645-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fa645-150">NOTES</span></span>

## <span data-ttu-id="fa645-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fa645-151">RELATED LINKS</span></span>
