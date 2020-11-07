---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: f00c1499e7f7e8a5a6d6b14bcbd8289b35ae2ced
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651482"
---
# <span data-ttu-id="ac87a-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="ac87a-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="ac87a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac87a-102">SYNOPSIS</span></span>
<span data-ttu-id="ac87a-103">Erstellt einen neuen Befehl, der für eine vorhandene DMS-Aufgabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac87a-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="ac87a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac87a-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="ac87a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac87a-105">DESCRIPTION</span></span>
<span data-ttu-id="ac87a-106">Das Invoke-AzDataMigrationCommand-Cmdlet erstellt eine neue Befehls Aufgabe, die für eine vorhandene Migrationsaufgabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac87a-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="ac87a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac87a-107">EXAMPLES</span></span>

### <span data-ttu-id="ac87a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ac87a-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="ac87a-109">In den obigen Beispielen wird das Invoke-AzDataMigrationCommand-Cmdlet verwendet, um einen Befehl für einen vorhandenen Dienst, ein Projekt und eine Aufgabe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ac87a-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="ac87a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac87a-110">PARAMETERS</span></span>

### <span data-ttu-id="ac87a-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="ac87a-111">-CommandType</span></span>
<span data-ttu-id="ac87a-112">Befehlstyp</span><span class="sxs-lookup"><span data-stu-id="ac87a-112">Command Type.</span></span>

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

### <span data-ttu-id="ac87a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac87a-113">-DefaultProfile</span></span>
<span data-ttu-id="ac87a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ac87a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac87a-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="ac87a-115">-ProjectName</span></span>
<span data-ttu-id="ac87a-116">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="ac87a-116">The name of the project.</span></span>

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

### <span data-ttu-id="ac87a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac87a-117">-ResourceGroupName</span></span>
<span data-ttu-id="ac87a-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ac87a-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="ac87a-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ac87a-119">-ServiceName</span></span>
<span data-ttu-id="ac87a-120">Name des Daten Bank Migrations Diensts.</span><span class="sxs-lookup"><span data-stu-id="ac87a-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="ac87a-121">-Taskname</span><span class="sxs-lookup"><span data-stu-id="ac87a-121">-TaskName</span></span>
<span data-ttu-id="ac87a-122">Der Name der Aufgabe, auf der der Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac87a-122">The name of the task the command is run on.</span></span>

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
### <span data-ttu-id="ac87a-123">-Objektname</span><span class="sxs-lookup"><span data-stu-id="ac87a-123">-ObjectName</span></span>
<span data-ttu-id="ac87a-124">Der Name des Datenbankobjekts, für das der Befehl ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac87a-124">The name of the database object the command will run against.</span></span>

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

### <span data-ttu-id="ac87a-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ac87a-125">-Confirm</span></span>
<span data-ttu-id="ac87a-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac87a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac87a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac87a-127">-WhatIf</span></span>
<span data-ttu-id="ac87a-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac87a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac87a-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac87a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac87a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac87a-130">CommonParameters</span></span>
<span data-ttu-id="ac87a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac87a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac87a-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac87a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac87a-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac87a-133">INPUTS</span></span>

### <span data-ttu-id="ac87a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ac87a-134">System.String</span></span>

## <span data-ttu-id="ac87a-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac87a-135">OUTPUTS</span></span>

### <span data-ttu-id="ac87a-136">Microsoft. Azure. Management. datamigration. Models. CommandProperties</span><span class="sxs-lookup"><span data-stu-id="ac87a-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="ac87a-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac87a-137">NOTES</span></span>

## <span data-ttu-id="ac87a-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac87a-138">RELATED LINKS</span></span>
