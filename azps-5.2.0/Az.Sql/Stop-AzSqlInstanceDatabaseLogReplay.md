---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Stop-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 2a7c74c4c8fef61e01ccbbb512ff428b9e885f06
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301851"
---
# <span data-ttu-id="890b6-101">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="890b6-101">Stop-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="890b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="890b6-102">SYNOPSIS</span></span>
<span data-ttu-id="890b6-103">Bricht den Protokollwiedergabedienst ab, indem die Datenbank gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="890b6-103">Cancels the Log Replay service by dropping the database.</span></span>

## <span data-ttu-id="890b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="890b6-104">SYNTAX</span></span>

### <span data-ttu-id="890b6-105">LogReplayInstanceDatabaseFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="890b6-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="890b6-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="890b6-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-PassThru] [-InputObject] <AzureSqlManagedDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="890b6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="890b6-107">DESCRIPTION</span></span>
<span data-ttu-id="890b6-108">Das **Cmdlet "Stop-AzSqlInstanceDatabaseLogReplay"** löscht die Datenbank und bricht daher den Log Replay-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="890b6-108">The **Stop-AzSqlInstanceDatabaseLogReplay** cmdlet drops the database and thus cancel Log Replay service.</span></span>

## <span data-ttu-id="890b6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="890b6-109">EXAMPLES</span></span>

### <span data-ttu-id="890b6-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="890b6-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="890b6-111">Mit diesem Befehl wird der Wiedergabedienst für das Protokoll in der angegebenen Datenbank abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="890b6-111">This command will cancel log replay service on the given database.</span></span>

## <span data-ttu-id="890b6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="890b6-112">PARAMETERS</span></span>

### <span data-ttu-id="890b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="890b6-113">-DefaultProfile</span></span>
<span data-ttu-id="890b6-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="890b6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="890b6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="890b6-115">-Force</span></span>
<span data-ttu-id="890b6-116">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="890b6-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="890b6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="890b6-117">-InputObject</span></span>
<span data-ttu-id="890b6-118">Das Instanzdatenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="890b6-118">The instance database object.</span></span>

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

### <span data-ttu-id="890b6-119">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="890b6-119">-InstanceName</span></span>
<span data-ttu-id="890b6-120">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="890b6-120">The name of the instance.</span></span>

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

### <span data-ttu-id="890b6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="890b6-121">-Name</span></span>
<span data-ttu-id="890b6-122">Der Name der Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="890b6-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="890b6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="890b6-123">-PassThru</span></span>
<span data-ttu-id="890b6-124">Definiert, ob die Synchronisierungsgruppe zurückgeben wird.</span><span class="sxs-lookup"><span data-stu-id="890b6-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="890b6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="890b6-125">-ResourceGroupName</span></span>
<span data-ttu-id="890b6-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="890b6-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="890b6-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="890b6-127">-Confirm</span></span>
<span data-ttu-id="890b6-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="890b6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="890b6-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="890b6-129">-WhatIf</span></span>
<span data-ttu-id="890b6-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="890b6-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="890b6-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="890b6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="890b6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="890b6-132">CommonParameters</span></span>
<span data-ttu-id="890b6-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="890b6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="890b6-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="890b6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="890b6-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="890b6-135">INPUTS</span></span>

### <span data-ttu-id="890b6-136">System.String</span><span class="sxs-lookup"><span data-stu-id="890b6-136">System.String</span></span>

### <span data-ttu-id="890b6-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="890b6-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="890b6-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="890b6-138">OUTPUTS</span></span>

### <span data-ttu-id="890b6-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="890b6-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="890b6-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="890b6-140">NOTES</span></span>

## <span data-ttu-id="890b6-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="890b6-141">RELATED LINKS</span></span>
