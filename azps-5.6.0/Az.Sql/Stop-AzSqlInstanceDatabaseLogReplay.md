---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Stop-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 42c2fa289eef04734c0619ca7bf2a46ece19606e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946816"
---
# <span data-ttu-id="5e0cc-101">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="5e0cc-101">Stop-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="5e0cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e0cc-102">SYNOPSIS</span></span>
<span data-ttu-id="5e0cc-103">Bricht den Protokollwiedergabedienst ab, indem die Datenbank gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="5e0cc-103">Cancels the Log Replay service by dropping the database.</span></span>

## <span data-ttu-id="5e0cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e0cc-104">SYNTAX</span></span>

### <span data-ttu-id="5e0cc-105">LogReplayInstanceDatabaseFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e0cc-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e0cc-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="5e0cc-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-PassThru] [-InputObject] <AzureSqlManagedDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e0cc-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e0cc-107">DESCRIPTION</span></span>
<span data-ttu-id="5e0cc-108">Das **Cmdlet Stop-AzSqlInstanceDatabaseLogReplay** löscht die Datenbank und bricht daher den Protokollwiederholungsdienst ab.</span><span class="sxs-lookup"><span data-stu-id="5e0cc-108">The **Stop-AzSqlInstanceDatabaseLogReplay** cmdlet drops the database and thus cancel Log Replay service.</span></span>

## <span data-ttu-id="5e0cc-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5e0cc-109">EXAMPLES</span></span>

### <span data-ttu-id="5e0cc-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5e0cc-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="5e0cc-111">Mit diesem Befehl wird der Protokollwiedergabedienst in der angegebenen Datenbank abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="5e0cc-111">This command will cancel log replay service on the given database.</span></span>

## <span data-ttu-id="5e0cc-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5e0cc-112">PARAMETERS</span></span>

### <span data-ttu-id="5e0cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e0cc-113">-DefaultProfile</span></span>
<span data-ttu-id="5e0cc-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e0cc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e0cc-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="5e0cc-115">-Force</span></span>
<span data-ttu-id="5e0cc-116">Bestätigungsmeldung überspringen zum Ausführen der Aktion</span><span class="sxs-lookup"><span data-stu-id="5e0cc-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="5e0cc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e0cc-117">-InputObject</span></span>
<span data-ttu-id="5e0cc-118">Das Instanzdatenbankobjekt.</span><span class="sxs-lookup"><span data-stu-id="5e0cc-118">The instance database object.</span></span>

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

### <span data-ttu-id="5e0cc-119">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="5e0cc-119">-InstanceName</span></span>
<span data-ttu-id="5e0cc-120">Der Name der -Instanz.</span><span class="sxs-lookup"><span data-stu-id="5e0cc-120">The name of the instance.</span></span>

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

### <span data-ttu-id="5e0cc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5e0cc-121">-Name</span></span>
<span data-ttu-id="5e0cc-122">Der Name der Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="5e0cc-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="5e0cc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e0cc-123">-PassThru</span></span>
<span data-ttu-id="5e0cc-124">Definiert, ob die Synchronisierungsgruppe zurückgeben wird.</span><span class="sxs-lookup"><span data-stu-id="5e0cc-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="5e0cc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e0cc-125">-ResourceGroupName</span></span>
<span data-ttu-id="5e0cc-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5e0cc-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="5e0cc-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e0cc-127">-Confirm</span></span>
<span data-ttu-id="5e0cc-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e0cc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e0cc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e0cc-129">-WhatIf</span></span>
<span data-ttu-id="5e0cc-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e0cc-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e0cc-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e0cc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e0cc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e0cc-132">CommonParameters</span></span>
<span data-ttu-id="5e0cc-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e0cc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e0cc-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e0cc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e0cc-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5e0cc-135">INPUTS</span></span>

### <span data-ttu-id="5e0cc-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5e0cc-136">System.String</span></span>

### <span data-ttu-id="5e0cc-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5e0cc-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="5e0cc-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5e0cc-138">OUTPUTS</span></span>

### <span data-ttu-id="5e0cc-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5e0cc-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="5e0cc-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5e0cc-140">NOTES</span></span>

## <span data-ttu-id="5e0cc-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5e0cc-141">RELATED LINKS</span></span>
