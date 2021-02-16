---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: ebfc974fdf268225c6c572756f7c5567b691ec04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166036"
---
# <span data-ttu-id="3c77f-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="3c77f-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="3c77f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c77f-102">SYNOPSIS</span></span>
<span data-ttu-id="3c77f-103">Erstellt einen neuen Befehl, der für eine vorhandene Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c77f-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="3c77f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c77f-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="3c77f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c77f-105">DESCRIPTION</span></span>
<span data-ttu-id="3c77f-106">Das Invoke-AzDataMigrationCommand erstellt eine neue Befehlsaufgabe, die für eine vorhandene Migrationsaufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c77f-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="3c77f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3c77f-107">EXAMPLES</span></span>

### <span data-ttu-id="3c77f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3c77f-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="3c77f-109">In den vorstehenden Beispielen wird das cmdlet Invoke-AzDataMigrationCommand verwendet, um einen Befehl für einen vorhandenen Dienst, ein vorhandenes Projekt und eine vorhandene Aufgabe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3c77f-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="3c77f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c77f-110">PARAMETERS</span></span>

### <span data-ttu-id="3c77f-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="3c77f-111">-CommandType</span></span>
<span data-ttu-id="3c77f-112">Befehlstyp.</span><span class="sxs-lookup"><span data-stu-id="3c77f-112">Command Type.</span></span>

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

### <span data-ttu-id="3c77f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c77f-113">-DefaultProfile</span></span>
<span data-ttu-id="3c77f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3c77f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c77f-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="3c77f-115">-ProjectName</span></span>
<span data-ttu-id="3c77f-116">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="3c77f-116">The name of the project.</span></span>

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

### <span data-ttu-id="3c77f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c77f-117">-ResourceGroupName</span></span>
<span data-ttu-id="3c77f-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3c77f-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="3c77f-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3c77f-119">-ServiceName</span></span>
<span data-ttu-id="3c77f-120">Name des Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="3c77f-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="3c77f-121">-TaskName</span><span class="sxs-lookup"><span data-stu-id="3c77f-121">-TaskName</span></span>
<span data-ttu-id="3c77f-122">Der Name der Aufgabe, für die der Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c77f-122">The name of the task the command is run on.</span></span>

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
### <span data-ttu-id="3c77f-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="3c77f-123">-ObjectName</span></span>
<span data-ttu-id="3c77f-124">Der Name des Datenbankobjekts, für das der Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c77f-124">The name of the database object the command will run against.</span></span>

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

### <span data-ttu-id="3c77f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c77f-125">-Confirm</span></span>
<span data-ttu-id="3c77f-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3c77f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c77f-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3c77f-127">-WhatIf</span></span>
<span data-ttu-id="3c77f-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c77f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c77f-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3c77f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c77f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c77f-130">CommonParameters</span></span>
<span data-ttu-id="3c77f-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c77f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c77f-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c77f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c77f-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3c77f-133">INPUTS</span></span>

### <span data-ttu-id="3c77f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3c77f-134">System.String</span></span>

## <span data-ttu-id="3c77f-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3c77f-135">OUTPUTS</span></span>

### <span data-ttu-id="3c77f-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span><span class="sxs-lookup"><span data-stu-id="3c77f-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="3c77f-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3c77f-137">NOTES</span></span>

## <span data-ttu-id="3c77f-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3c77f-138">RELATED LINKS</span></span>
