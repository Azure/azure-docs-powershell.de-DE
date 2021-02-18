---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Stop-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 2a7c74c4c8fef61e01ccbbb512ff428b9e885f06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175097"
---
# <span data-ttu-id="1755f-101">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="1755f-101">Stop-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="1755f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1755f-102">SYNOPSIS</span></span>
<span data-ttu-id="1755f-103">Bricht den Protokollwiedergabedienst ab, indem die Datenbank gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="1755f-103">Cancels the Log Replay service by dropping the database.</span></span>

## <span data-ttu-id="1755f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1755f-104">SYNTAX</span></span>

### <span data-ttu-id="1755f-105">LogReplayInstanceDatabaseFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="1755f-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1755f-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="1755f-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-PassThru] [-InputObject] <AzureSqlManagedDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1755f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1755f-107">DESCRIPTION</span></span>
<span data-ttu-id="1755f-108">Das **Cmdlet "Stop-AzSqlInstanceDatabaseLogReplay"** löscht die Datenbank und bricht daher den Log Replay-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="1755f-108">The **Stop-AzSqlInstanceDatabaseLogReplay** cmdlet drops the database and thus cancel Log Replay service.</span></span>

## <span data-ttu-id="1755f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1755f-109">EXAMPLES</span></span>

### <span data-ttu-id="1755f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1755f-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="1755f-111">Mit diesem Befehl wird der Wiedergabedienst für das Protokoll in der angegebenen Datenbank abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="1755f-111">This command will cancel log replay service on the given database.</span></span>

## <span data-ttu-id="1755f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1755f-112">PARAMETERS</span></span>

### <span data-ttu-id="1755f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1755f-113">-DefaultProfile</span></span>
<span data-ttu-id="1755f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1755f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1755f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1755f-115">-Force</span></span>
<span data-ttu-id="1755f-116">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="1755f-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1755f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1755f-117">-InputObject</span></span>
<span data-ttu-id="1755f-118">Das Instanzdatenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="1755f-118">The instance database object.</span></span>

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

### <span data-ttu-id="1755f-119">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="1755f-119">-InstanceName</span></span>
<span data-ttu-id="1755f-120">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="1755f-120">The name of the instance.</span></span>

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

### <span data-ttu-id="1755f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1755f-121">-Name</span></span>
<span data-ttu-id="1755f-122">Der Name der Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="1755f-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="1755f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1755f-123">-PassThru</span></span>
<span data-ttu-id="1755f-124">Definiert, ob die Synchronisierungsgruppe zurückgeben wird.</span><span class="sxs-lookup"><span data-stu-id="1755f-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="1755f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1755f-125">-ResourceGroupName</span></span>
<span data-ttu-id="1755f-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1755f-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="1755f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1755f-127">-Confirm</span></span>
<span data-ttu-id="1755f-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1755f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1755f-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1755f-129">-WhatIf</span></span>
<span data-ttu-id="1755f-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1755f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1755f-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1755f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1755f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1755f-132">CommonParameters</span></span>
<span data-ttu-id="1755f-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1755f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1755f-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1755f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1755f-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1755f-135">INPUTS</span></span>

### <span data-ttu-id="1755f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1755f-136">System.String</span></span>

### <span data-ttu-id="1755f-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="1755f-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="1755f-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1755f-138">OUTPUTS</span></span>

### <span data-ttu-id="1755f-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="1755f-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="1755f-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1755f-140">NOTES</span></span>

## <span data-ttu-id="1755f-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1755f-141">RELATED LINKS</span></span>
