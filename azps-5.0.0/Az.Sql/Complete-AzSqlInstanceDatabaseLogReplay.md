---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Complete-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: d1d7cead951520944199347ebdbb209c5474eb3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177206"
---
# <span data-ttu-id="7c867-101">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="7c867-101">Complete-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="7c867-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7c867-102">SYNOPSIS</span></span>
<span data-ttu-id="7c867-103">Schließt den Protokollwiedergabe Dienst für die angegebene Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="7c867-103">Completes Log Replay service for the given database.</span></span>

## <span data-ttu-id="7c867-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c867-104">SYNTAX</span></span>

### <span data-ttu-id="7c867-105">LogReplayInstanceDatabaseFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="7c867-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c867-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="7c867-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7c867-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c867-107">DESCRIPTION</span></span>
<span data-ttu-id="7c867-108">Das Cmdlet **Complete-AzSqlInstanceDatabaseLogReplay** rundet den Protokollwiedergabe Dienst in der angegebenen Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="7c867-108">The **Complete-AzSqlInstanceDatabaseLogReplay** cmdlet completes the Log Replay service on the given database.</span></span>

## <span data-ttu-id="7c867-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c867-109">EXAMPLES</span></span>

### <span data-ttu-id="7c867-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7c867-110">Example 1</span></span>
```powershell
PS C:\> Complete-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName" -LastBackupName "last_backup.bak"
```

<span data-ttu-id="7c867-111">Mit diesem Befehl wird der Protokollwiedergabe Dienst für die angegebene Datenbank abgeschlossen, nachdem die letzte Sicherung wiederhergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7c867-111">This command will complete Log Replay service for the given database after last backup gets restored.</span></span>

## <span data-ttu-id="7c867-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c867-112">PARAMETERS</span></span>

### <span data-ttu-id="7c867-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c867-113">-DefaultProfile</span></span>
<span data-ttu-id="7c867-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7c867-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c867-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7c867-115">-InputObject</span></span>
<span data-ttu-id="7c867-116">Das Instanzdatenbank-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7c867-116">The instance database object.</span></span>

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

### <span data-ttu-id="7c867-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7c867-117">-InstanceName</span></span>
<span data-ttu-id="7c867-118">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="7c867-118">The name of the instance.</span></span>

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

### <span data-ttu-id="7c867-119">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="7c867-119">-LastBackupName</span></span>
<span data-ttu-id="7c867-120">Der Name der letzten Sicherungsdatei, die wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c867-120">The name of the last backup file to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c867-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7c867-121">-Name</span></span>
<span data-ttu-id="7c867-122">Der Name der Instanzen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7c867-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="7c867-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c867-123">-PassThru</span></span>
<span data-ttu-id="7c867-124">Definiert, ob die Synchronisierungsgruppe zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7c867-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="7c867-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c867-125">-ResourceGroupName</span></span>
<span data-ttu-id="7c867-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7c867-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="7c867-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7c867-127">-Confirm</span></span>
<span data-ttu-id="7c867-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c867-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c867-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c867-129">-WhatIf</span></span>
<span data-ttu-id="7c867-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c867-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c867-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c867-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c867-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c867-132">CommonParameters</span></span>
<span data-ttu-id="7c867-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c867-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c867-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c867-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c867-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7c867-135">INPUTS</span></span>

### <span data-ttu-id="7c867-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7c867-136">System.String</span></span>

### <span data-ttu-id="7c867-137">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7c867-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="7c867-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7c867-138">OUTPUTS</span></span>

## <span data-ttu-id="7c867-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c867-139">NOTES</span></span>

## <span data-ttu-id="7c867-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7c867-140">RELATED LINKS</span></span>
