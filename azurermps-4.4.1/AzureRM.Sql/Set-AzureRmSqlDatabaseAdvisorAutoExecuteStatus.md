---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 149579bb6bbcd4ee5fe5fa192ad040e6e4c68b28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505574"
---
# <span data-ttu-id="370c2-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="370c2-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="370c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="370c2-102">SYNOPSIS</span></span>
<span data-ttu-id="370c2-103">Ändert den automatischen Ausführungsstatus eines Azure SQL-Daten Bank Beraters.</span><span class="sxs-lookup"><span data-stu-id="370c2-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="370c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="370c2-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -DatabaseName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="370c2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="370c2-105">DESCRIPTION</span></span>
<span data-ttu-id="370c2-106">Das Cmdlet " **festlegen-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** " ändert die Auto Execute-Eigenschaft für einen Azure SQL-Daten Bank Ratgeber.</span><span class="sxs-lookup"><span data-stu-id="370c2-106">The **Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="370c2-107">Derzeit unterstützt dieses Cmdlet die aktivierten, deaktivierten und Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="370c2-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="370c2-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="370c2-108">EXAMPLES</span></span>

### <span data-ttu-id="370c2-109">Beispiel 1: Aktivieren der automatischen Ausführung für einen Ratgeber</span><span class="sxs-lookup"><span data-stu-id="370c2-109">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -ResourceGroupName "ContosoRunnersProd" -ServerName "runner-australia-east" -DatabaseName "ContosoRunner" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
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

<span data-ttu-id="370c2-110">Mit diesem Befehl wird der automatische Ausführungsstatus eines Ratgebers mit dem Namen CreateIndex in Enabled geändert.</span><span class="sxs-lookup"><span data-stu-id="370c2-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="370c2-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="370c2-111">PARAMETERS</span></span>

### <span data-ttu-id="370c2-112">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="370c2-112">-AdvisorName</span></span>
<span data-ttu-id="370c2-113">Gibt den Namen des Beraters an, für den das Cmdlet den Status ändert.</span><span class="sxs-lookup"><span data-stu-id="370c2-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="370c2-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="370c2-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="370c2-115">Gibt den Wert für den Status an.</span><span class="sxs-lookup"><span data-stu-id="370c2-115">Specifies the value for the status.</span></span>
<span data-ttu-id="370c2-116">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="370c2-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="370c2-117">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="370c2-117">Enabled</span></span> 
- <span data-ttu-id="370c2-118">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="370c2-118">Disabled</span></span> 
- <span data-ttu-id="370c2-119">Standard</span><span class="sxs-lookup"><span data-stu-id="370c2-119">Default</span></span>

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

### <span data-ttu-id="370c2-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="370c2-120">-DatabaseName</span></span>
<span data-ttu-id="370c2-121">Gibt den Namen der Datenbank an, für die dieses Cmdlet den Status ändert.</span><span class="sxs-lookup"><span data-stu-id="370c2-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="370c2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="370c2-122">-ResourceGroupName</span></span>
<span data-ttu-id="370c2-123">Gibt den Namen der Ressourcengruppe des Servers an, der diese Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="370c2-123">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="370c2-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="370c2-124">-ServerName</span></span>
<span data-ttu-id="370c2-125">Gibt den Namen des Servers für die Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="370c2-125">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="370c2-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="370c2-126">-Confirm</span></span>
<span data-ttu-id="370c2-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="370c2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="370c2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="370c2-128">-WhatIf</span></span>
<span data-ttu-id="370c2-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="370c2-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="370c2-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="370c2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="370c2-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="370c2-131">-DefaultProfile</span></span>
<span data-ttu-id="370c2-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="370c2-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="370c2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="370c2-133">CommonParameters</span></span>
<span data-ttu-id="370c2-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="370c2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="370c2-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="370c2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="370c2-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="370c2-136">INPUTS</span></span>

## <span data-ttu-id="370c2-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="370c2-137">OUTPUTS</span></span>

### <span data-ttu-id="370c2-138">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="370c2-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>
<span data-ttu-id="370c2-139">Dieses Cmdlet gibt ein **AzureSqlDatabaseAdvisorModel** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="370c2-139">This cmdlet returns an **AzureSqlDatabaseAdvisorModel** object.</span></span>

## <span data-ttu-id="370c2-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="370c2-140">NOTES</span></span>

## <span data-ttu-id="370c2-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="370c2-141">RELATED LINKS</span></span>

[<span data-ttu-id="370c2-142">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="370c2-142">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="370c2-143">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="370c2-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

