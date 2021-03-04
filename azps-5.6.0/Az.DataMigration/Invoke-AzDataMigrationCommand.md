---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: e99e2e6a8c0b2c8a0fc0b2d2143d2b4301520ab0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918939"
---
# <span data-ttu-id="1e0ce-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="1e0ce-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="1e0ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e0ce-102">SYNOPSIS</span></span>
<span data-ttu-id="1e0ce-103">Erstellt einen neuen Befehl, der für eine vorhandene DMS-Aufgabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1e0ce-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="1e0ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e0ce-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="1e0ce-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e0ce-105">DESCRIPTION</span></span>
<span data-ttu-id="1e0ce-106">Das Invoke-AzDataMigrationCommand-Cmdlet erstellt eine neue Befehlsaufgabe, die für eine vorhandene Migrationsaufgabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1e0ce-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="1e0ce-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1e0ce-107">EXAMPLES</span></span>

### <span data-ttu-id="1e0ce-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1e0ce-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="1e0ce-109">In den vorstehenden Beispielen wird das cmdlet Invoke-AzDataMigrationCommand verwendet, um einen Befehl für einen vorhandenen Dienst, ein Projekt und einen Vorgang zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1e0ce-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="1e0ce-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1e0ce-110">PARAMETERS</span></span>

### <span data-ttu-id="1e0ce-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="1e0ce-111">-CommandType</span></span>
<span data-ttu-id="1e0ce-112">Befehlstyp.</span><span class="sxs-lookup"><span data-stu-id="1e0ce-112">Command Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.CommandTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: CompleteSqlDBSync, CancelMongoDB, RestartMongoDB, FinishMongoDB, CompleteSqlMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e0ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e0ce-113">-DefaultProfile</span></span>
<span data-ttu-id="1e0ce-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1e0ce-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e0ce-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="1e0ce-115">-ProjectName</span></span>
<span data-ttu-id="1e0ce-116">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="1e0ce-116">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0ce-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e0ce-117">-ResourceGroupName</span></span>
<span data-ttu-id="1e0ce-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1e0ce-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0ce-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1e0ce-119">-ServiceName</span></span>
<span data-ttu-id="1e0ce-120">Name des Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="1e0ce-120">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0ce-121">-TaskName</span><span class="sxs-lookup"><span data-stu-id="1e0ce-121">-TaskName</span></span>
<span data-ttu-id="1e0ce-122">Der Name der Aufgabe, für die der Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e0ce-122">The name of the task the command is run on.</span></span>

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
### <span data-ttu-id="1e0ce-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="1e0ce-123">-ObjectName</span></span>
<span data-ttu-id="1e0ce-124">Der Name des Datenbankobjekts, für das der Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e0ce-124">The name of the database object the command will run against.</span></span>

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

### <span data-ttu-id="1e0ce-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1e0ce-125">-Confirm</span></span>
<span data-ttu-id="1e0ce-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e0ce-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e0ce-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e0ce-127">-WhatIf</span></span>
<span data-ttu-id="1e0ce-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e0ce-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e0ce-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e0ce-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e0ce-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e0ce-130">CommonParameters</span></span>
<span data-ttu-id="1e0ce-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e0ce-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e0ce-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e0ce-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e0ce-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1e0ce-133">INPUTS</span></span>

### <span data-ttu-id="1e0ce-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1e0ce-134">System.String</span></span>

## <span data-ttu-id="1e0ce-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1e0ce-135">OUTPUTS</span></span>

### <span data-ttu-id="1e0ce-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span><span class="sxs-lookup"><span data-stu-id="1e0ce-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="1e0ce-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1e0ce-137">NOTES</span></span>

## <span data-ttu-id="1e0ce-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1e0ce-138">RELATED LINKS</span></span>
