---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
ms.openlocfilehash: e53857533770d6de0040d2d777020f1a2f9f320a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995482"
---
# <span data-ttu-id="77d45-101">Get-AzSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="77d45-101">Get-AzSqlServerServiceObjective</span></span>

## <span data-ttu-id="77d45-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="77d45-102">SYNOPSIS</span></span>
<span data-ttu-id="77d45-103">Ruft Dienst Ziele für einen Azure SQL-Datenbankserver ab.</span><span class="sxs-lookup"><span data-stu-id="77d45-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="77d45-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="77d45-104">SYNTAX</span></span>

### <span data-ttu-id="77d45-105">ByLocation (Standard)</span><span class="sxs-lookup"><span data-stu-id="77d45-105">ByLocation (Default)</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77d45-106">ByServer</span><span class="sxs-lookup"><span data-stu-id="77d45-106">ByServer</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ResourceGroupName] <String>
 [-ServerName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77d45-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77d45-107">DESCRIPTION</span></span>
<span data-ttu-id="77d45-108">Das Cmdlet " **Get-AzSqlServerServiceObjective** " Ruft die verfügbaren Dienst Ziele für einen Azure SQL-Datenbankserver ab.</span><span class="sxs-lookup"><span data-stu-id="77d45-108">The **Get-AzSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="77d45-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77d45-109">EXAMPLES</span></span>

### <span data-ttu-id="77d45-110">Beispiel 1: Abrufen von Dienst Zielen</span><span class="sxs-lookup"><span data-stu-id="77d45-110">Example 1: Get service objectives</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="77d45-111">Dieser Befehl ruft die Dienst Ziele für den Server mit dem Namen SERVER01 ab.</span><span class="sxs-lookup"><span data-stu-id="77d45-111">This command gets the service objectives for the server named Server01.</span></span>

### <span data-ttu-id="77d45-112">Beispiel 2: Abrufen von Dienst Zielen mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="77d45-112">Example 2: Get service objectives using filtering</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServiceObjectiveName "P*"
ServiceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
```

<span data-ttu-id="77d45-113">Dieser Befehl ruft die Dienst Ziele für den Server mit dem Namen "Server01" ab, die mit "System" beginnen.</span><span class="sxs-lookup"><span data-stu-id="77d45-113">This command gets the service objectives for the server named Server01 that start with "System".</span></span>

### <span data-ttu-id="77d45-114">Beispiel 3: Abrufen von Dienst Zielen für einen Standort</span><span class="sxs-lookup"><span data-stu-id="77d45-114">Example 3: Get service objectives for a location</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -Location "west us"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="77d45-115">Dieser Befehl ruft die Dienst Ziele für einen angegebenen Azure-Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="77d45-115">This command gets the service objectives for a specified Azure region.</span></span>

## <span data-ttu-id="77d45-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="77d45-116">PARAMETERS</span></span>

### <span data-ttu-id="77d45-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77d45-117">-DefaultProfile</span></span>
<span data-ttu-id="77d45-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="77d45-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77d45-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="77d45-119">-Location</span></span>
<span data-ttu-id="77d45-120">Der Name des Speicherorts, für den die Dienst Ziele abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="77d45-120">The name of the Location for which to get the service objectives.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77d45-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77d45-121">-ResourceGroupName</span></span>
<span data-ttu-id="77d45-122">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="77d45-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="77d45-123">Dieses Cmdlet ruft Dienst Ziele für einen SQL-Datenbankserver ab, der dieser Ressource zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="77d45-123">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77d45-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="77d45-124">-ServerName</span></span>
<span data-ttu-id="77d45-125">Gibt den Namen eines SQL-Datenbank-SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="77d45-125">Specifies the name of a SQL Database SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77d45-126">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="77d45-126">-ServiceObjectiveName</span></span>
<span data-ttu-id="77d45-127">Gibt den Namen eines Dienst Ziels für einen Azure SQL-Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="77d45-127">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="77d45-128">Die zulässigen Werte für diesen Parameter sind: Basic, S0, S1, S2, P1, P2 und P3.</span><span class="sxs-lookup"><span data-stu-id="77d45-128">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77d45-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="77d45-129">-Confirm</span></span>
<span data-ttu-id="77d45-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="77d45-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77d45-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77d45-131">-WhatIf</span></span>
<span data-ttu-id="77d45-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77d45-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77d45-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="77d45-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77d45-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77d45-134">CommonParameters</span></span>
<span data-ttu-id="77d45-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77d45-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77d45-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77d45-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77d45-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="77d45-137">INPUTS</span></span>

### <span data-ttu-id="77d45-138">System. String</span><span class="sxs-lookup"><span data-stu-id="77d45-138">System.String</span></span>

## <span data-ttu-id="77d45-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="77d45-139">OUTPUTS</span></span>

### <span data-ttu-id="77d45-140">Microsoft. Azure. Commands. SQL. ServiceObjective. Model. AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="77d45-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="77d45-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="77d45-141">NOTES</span></span>

## <span data-ttu-id="77d45-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="77d45-142">RELATED LINKS</span></span>

[<span data-ttu-id="77d45-143">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="77d45-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


