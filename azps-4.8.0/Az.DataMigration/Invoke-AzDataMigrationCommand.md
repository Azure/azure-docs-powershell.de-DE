---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: ebfc974fdf268225c6c572756f7c5567b691ec04
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166996"
---
# <span data-ttu-id="c7c81-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="c7c81-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="c7c81-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7c81-102">SYNOPSIS</span></span>
<span data-ttu-id="c7c81-103">Erstellt einen neuen Befehl, der für eine vorhandene DMS-Aufgabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7c81-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="c7c81-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7c81-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="c7c81-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7c81-105">DESCRIPTION</span></span>
<span data-ttu-id="c7c81-106">Das Invoke-AzDataMigrationCommand-Cmdlet erstellt eine neue Befehls Aufgabe, die für eine vorhandene Migrationsaufgabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7c81-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="c7c81-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7c81-107">EXAMPLES</span></span>

### <span data-ttu-id="c7c81-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c7c81-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="c7c81-109">In den obigen Beispielen wird das Invoke-AzDataMigrationCommand-Cmdlet verwendet, um einen Befehl für einen vorhandenen Dienst, ein Projekt und eine Aufgabe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c7c81-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="c7c81-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7c81-110">PARAMETERS</span></span>

### <span data-ttu-id="c7c81-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="c7c81-111">-CommandType</span></span>
<span data-ttu-id="c7c81-112">Befehlstyp</span><span class="sxs-lookup"><span data-stu-id="c7c81-112">Command Type.</span></span>

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

### <span data-ttu-id="c7c81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7c81-113">-DefaultProfile</span></span>
<span data-ttu-id="c7c81-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c7c81-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7c81-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="c7c81-115">-ProjectName</span></span>
<span data-ttu-id="c7c81-116">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="c7c81-116">The name of the project.</span></span>

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

### <span data-ttu-id="c7c81-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7c81-117">-ResourceGroupName</span></span>
<span data-ttu-id="c7c81-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c7c81-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="c7c81-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c7c81-119">-ServiceName</span></span>
<span data-ttu-id="c7c81-120">Name des Daten Bank Migrations Diensts.</span><span class="sxs-lookup"><span data-stu-id="c7c81-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="c7c81-121">-Taskname</span><span class="sxs-lookup"><span data-stu-id="c7c81-121">-TaskName</span></span>
<span data-ttu-id="c7c81-122">Der Name der Aufgabe, auf der der Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c7c81-122">The name of the task the command is run on.</span></span>

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
### <span data-ttu-id="c7c81-123">-Objektname</span><span class="sxs-lookup"><span data-stu-id="c7c81-123">-ObjectName</span></span>
<span data-ttu-id="c7c81-124">Der Name des Datenbankobjekts, für das der Befehl ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7c81-124">The name of the database object the command will run against.</span></span>

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

### <span data-ttu-id="c7c81-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c7c81-125">-Confirm</span></span>
<span data-ttu-id="c7c81-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c7c81-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7c81-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7c81-127">-WhatIf</span></span>
<span data-ttu-id="c7c81-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c7c81-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7c81-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7c81-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7c81-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7c81-130">CommonParameters</span></span>
<span data-ttu-id="c7c81-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7c81-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7c81-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7c81-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7c81-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7c81-133">INPUTS</span></span>

### <span data-ttu-id="c7c81-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c7c81-134">System.String</span></span>

## <span data-ttu-id="c7c81-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7c81-135">OUTPUTS</span></span>

### <span data-ttu-id="c7c81-136">Microsoft. Azure. Management. datamigration. Models. CommandProperties</span><span class="sxs-lookup"><span data-stu-id="c7c81-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="c7c81-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7c81-137">NOTES</span></span>

## <span data-ttu-id="c7c81-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7c81-138">RELATED LINKS</span></span>
