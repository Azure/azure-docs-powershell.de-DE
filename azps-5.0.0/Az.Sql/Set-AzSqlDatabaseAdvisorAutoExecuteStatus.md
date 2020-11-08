---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 1d6348c5ede63dee1f76059277c8f7d142a2c327
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179009"
---
# <span data-ttu-id="80b38-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="80b38-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="80b38-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80b38-102">SYNOPSIS</span></span>
<span data-ttu-id="80b38-103">Ändert den automatischen Ausführungsstatus eines Azure SQL-Daten Bank Beraters.</span><span class="sxs-lookup"><span data-stu-id="80b38-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="80b38-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80b38-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80b38-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80b38-105">DESCRIPTION</span></span>
<span data-ttu-id="80b38-106">Das Cmdlet " **festlegen-AzSqlDatabaseAdvisorAutoExecuteStatus** " ändert die Auto Execute-Eigenschaft für einen Azure SQL-Daten Bank Ratgeber.</span><span class="sxs-lookup"><span data-stu-id="80b38-106">The **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="80b38-107">Derzeit unterstützt dieses Cmdlet die aktivierten, deaktivierten und Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="80b38-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="80b38-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80b38-108">EXAMPLES</span></span>

### <span data-ttu-id="80b38-109">Beispiel 1: Aktivieren der automatischen Ausführung für einen Ratgeber</span><span class="sxs-lookup"><span data-stu-id="80b38-109">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzSqlDatabaseAdvisorAutoExecuteStatus -ResourceGroupName "ContosoRunnersProd" -ServerName "runner-australia-east" -DatabaseName "ContosoRunner" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
DatabaseName                   : ContosoRunner
ResourceGroupName              : ContosoRunnersProd
ServerName                     : runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="80b38-110">Mit diesem Befehl wird der automatische Ausführungsstatus eines Ratgebers mit dem Namen CreateIndex in Enabled geändert.</span><span class="sxs-lookup"><span data-stu-id="80b38-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="80b38-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="80b38-111">PARAMETERS</span></span>

### <span data-ttu-id="80b38-112">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="80b38-112">-AdvisorName</span></span>
<span data-ttu-id="80b38-113">Gibt den Namen des Beraters an, für den das Cmdlet den Status ändert.</span><span class="sxs-lookup"><span data-stu-id="80b38-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="80b38-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="80b38-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="80b38-115">Gibt den Wert für den Status an.</span><span class="sxs-lookup"><span data-stu-id="80b38-115">Specifies the value for the status.</span></span>
<span data-ttu-id="80b38-116">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="80b38-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="80b38-117">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="80b38-117">Enabled</span></span> 
- <span data-ttu-id="80b38-118">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="80b38-118">Disabled</span></span> 
- <span data-ttu-id="80b38-119">Standard</span><span class="sxs-lookup"><span data-stu-id="80b38-119">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80b38-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="80b38-120">-DatabaseName</span></span>
<span data-ttu-id="80b38-121">Gibt den Namen der Datenbank an, für die dieses Cmdlet den Status ändert.</span><span class="sxs-lookup"><span data-stu-id="80b38-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="80b38-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80b38-122">-DefaultProfile</span></span>
<span data-ttu-id="80b38-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="80b38-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80b38-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80b38-124">-ResourceGroupName</span></span>
<span data-ttu-id="80b38-125">Gibt den Namen der Ressourcengruppe des Servers an, der diese Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="80b38-125">Specifies the name of the resource group of the server that contains this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80b38-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="80b38-126">-ServerName</span></span>
<span data-ttu-id="80b38-127">Gibt den Namen des Servers für die Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="80b38-127">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="80b38-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="80b38-128">-Confirm</span></span>
<span data-ttu-id="80b38-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="80b38-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80b38-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80b38-130">-WhatIf</span></span>
<span data-ttu-id="80b38-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80b38-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80b38-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="80b38-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80b38-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80b38-133">CommonParameters</span></span>
<span data-ttu-id="80b38-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80b38-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80b38-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80b38-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80b38-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80b38-136">INPUTS</span></span>

### <span data-ttu-id="80b38-137">System. String</span><span class="sxs-lookup"><span data-stu-id="80b38-137">System.String</span></span>

### <span data-ttu-id="80b38-138">Microsoft. Azure. Commands. SQL. Advisor. Cmdlet. AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="80b38-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="80b38-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80b38-139">OUTPUTS</span></span>

### <span data-ttu-id="80b38-140">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="80b38-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="80b38-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="80b38-141">NOTES</span></span>

## <span data-ttu-id="80b38-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80b38-142">RELATED LINKS</span></span>

[<span data-ttu-id="80b38-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="80b38-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="80b38-144">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="80b38-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

