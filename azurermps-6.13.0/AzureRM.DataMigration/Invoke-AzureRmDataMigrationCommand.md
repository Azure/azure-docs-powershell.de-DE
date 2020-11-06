---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Invoke-AzureRmDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Invoke-AzureRmDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Invoke-AzureRmDataMigrationCommand.md
ms.openlocfilehash: 882d7eb0b005478850addda2d066c7266e6c2ad0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499541"
---
# <span data-ttu-id="fad1b-101">Invoke-AzureRmDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="fad1b-101">Invoke-AzureRmDataMigrationCommand</span></span>

## <span data-ttu-id="fad1b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fad1b-102">SYNOPSIS</span></span>
<span data-ttu-id="fad1b-103">Erstellt einen neuen Befehl, der für eine vorhandene DMS-Aufgabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fad1b-103">Creates a new command to be executed on an existing DMS task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fad1b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fad1b-104">SYNTAX</span></span>

```
Invoke-AzureRmDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fad1b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fad1b-105">DESCRIPTION</span></span>
<span data-ttu-id="fad1b-106">Das New-AzureRmDataMigrationCommand-Cmdlet erstellt eine neue Befehls Aufgabe, die für eine vorhandene Migrationsaufgabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fad1b-106">The New-AzureRmDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="fad1b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fad1b-107">EXAMPLES</span></span>

### <span data-ttu-id="fad1b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fad1b-108">Example 1</span></span>
```
PS C:\> $command = New-AzureRmDmsCommand -CommandType Complete -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="fad1b-109">In den obigen Beispielen wird das New-AzureRmDmsCommand-Cmdlet verwendet, um einen Befehl für einen vorhandenen Dienst, ein Projekt und eine Aufgabe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fad1b-109">The above examples uses the New-AzureRmDmsCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="fad1b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fad1b-110">PARAMETERS</span></span>

### <span data-ttu-id="fad1b-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="fad1b-111">-CommandType</span></span>
<span data-ttu-id="fad1b-112">Befehlstyp</span><span class="sxs-lookup"><span data-stu-id="fad1b-112">Command Type.</span></span>

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

### <span data-ttu-id="fad1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fad1b-113">-DefaultProfile</span></span>
<span data-ttu-id="fad1b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fad1b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fad1b-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="fad1b-115">-ProjectName</span></span>
<span data-ttu-id="fad1b-116">Der Name des Projekts.</span><span class="sxs-lookup"><span data-stu-id="fad1b-116">The name of the project.</span></span>

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

### <span data-ttu-id="fad1b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fad1b-117">-ResourceGroupName</span></span>
<span data-ttu-id="fad1b-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fad1b-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="fad1b-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fad1b-119">-ServiceName</span></span>
<span data-ttu-id="fad1b-120">Name des Daten Bank Migrations Diensts.</span><span class="sxs-lookup"><span data-stu-id="fad1b-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="fad1b-121">-Taskname</span><span class="sxs-lookup"><span data-stu-id="fad1b-121">-TaskName</span></span>
<span data-ttu-id="fad1b-122">Der Name der Aufgabe, auf der der Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fad1b-122">The name of the task the command is run on.</span></span>

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

### <span data-ttu-id="fad1b-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fad1b-123">-Confirm</span></span>
<span data-ttu-id="fad1b-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fad1b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fad1b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fad1b-125">-WhatIf</span></span>
<span data-ttu-id="fad1b-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fad1b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fad1b-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fad1b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fad1b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fad1b-128">CommonParameters</span></span>
<span data-ttu-id="fad1b-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fad1b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fad1b-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fad1b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fad1b-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fad1b-131">INPUTS</span></span>

### <span data-ttu-id="fad1b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fad1b-132">System.String</span></span>

## <span data-ttu-id="fad1b-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fad1b-133">OUTPUTS</span></span>

### <span data-ttu-id="fad1b-134">Microsoft. Azure. Management. datamigration. Models. CommandProperties</span><span class="sxs-lookup"><span data-stu-id="fad1b-134">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="fad1b-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="fad1b-135">NOTES</span></span>

## <span data-ttu-id="fad1b-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fad1b-136">RELATED LINKS</span></span>
