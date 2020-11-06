---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 7b4d445ede7bae59431707f3ff6bc587effde21c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498694"
---
# <span data-ttu-id="165a2-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="165a2-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="165a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="165a2-102">SYNOPSIS</span></span>
<span data-ttu-id="165a2-103">Aktualisiert den automatischen Ausführungsstatus eines Azure SQL Elastic Pool Advisor.</span><span class="sxs-lookup"><span data-stu-id="165a2-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="165a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="165a2-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="165a2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="165a2-105">DESCRIPTION</span></span>
<span data-ttu-id="165a2-106">Das Cmdlet " **Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** " legt die Auto Execute-Eigenschaft für einen Azure SQL Elastic Pool Advisor fest.</span><span class="sxs-lookup"><span data-stu-id="165a2-106">The **Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="165a2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="165a2-107">EXAMPLES</span></span>

### <span data-ttu-id="165a2-108">Beispiel 1: Aktivieren der automatischen Ausführung für einen Ratgeber</span><span class="sxs-lookup"><span data-stu-id="165a2-108">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
'Enabled'ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : ElasticPool
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="165a2-109">Dieser Befehl legt den automatischen Ausführungsstatus eines Ratgebers mit dem Namen CreateIndex auf Enabled fest.</span><span class="sxs-lookup"><span data-stu-id="165a2-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="165a2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="165a2-110">PARAMETERS</span></span>

### <span data-ttu-id="165a2-111">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="165a2-111">-AdvisorName</span></span>
<span data-ttu-id="165a2-112">Gibt den Namen des Beraters an, für den das Cmdlet den automatischen Ausführungsstatus aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="165a2-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="165a2-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="165a2-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="165a2-114">Gibt einen neuen Wert an, mit dem dieses Cmdlet den automatischen Ausführungsstatus aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="165a2-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>

<span data-ttu-id="165a2-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="165a2-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="165a2-116">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="165a2-116">Enabled</span></span>
- <span data-ttu-id="165a2-117">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="165a2-117">Disabled</span></span>
- <span data-ttu-id="165a2-118">Standard</span><span class="sxs-lookup"><span data-stu-id="165a2-118">Default</span></span>

```yaml
Type: AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="165a2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="165a2-119">-DefaultProfile</span></span>
<span data-ttu-id="165a2-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="165a2-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165a2-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="165a2-121">-ElasticPoolName</span></span>
<span data-ttu-id="165a2-122">Gibt den Namen des elastischen Pools an.</span><span class="sxs-lookup"><span data-stu-id="165a2-122">Specifies the name of the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="165a2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="165a2-123">-ResourceGroupName</span></span>
<span data-ttu-id="165a2-124">Gibt den Namen der Ressourcengruppe des Servers an, der diesen elastischen Pool enthält.</span><span class="sxs-lookup"><span data-stu-id="165a2-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="165a2-125">-Servername</span><span class="sxs-lookup"><span data-stu-id="165a2-125">-ServerName</span></span>
<span data-ttu-id="165a2-126">Gibt den Namen des Servers an, in dem sich der elastische Pool befindet.</span><span class="sxs-lookup"><span data-stu-id="165a2-126">Specifies the name of the server the elastic pool is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="165a2-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="165a2-127">-Confirm</span></span>
<span data-ttu-id="165a2-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="165a2-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165a2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="165a2-129">-WhatIf</span></span>
<span data-ttu-id="165a2-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="165a2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="165a2-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="165a2-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165a2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="165a2-132">CommonParameters</span></span>
<span data-ttu-id="165a2-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="165a2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="165a2-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="165a2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="165a2-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="165a2-135">INPUTS</span></span>

### <span data-ttu-id="165a2-136">Keine</span><span class="sxs-lookup"><span data-stu-id="165a2-136">None</span></span>
<span data-ttu-id="165a2-137">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="165a2-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="165a2-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="165a2-138">OUTPUTS</span></span>

### <span data-ttu-id="165a2-139">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="165a2-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="165a2-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="165a2-140">NOTES</span></span>
* <span data-ttu-id="165a2-141">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Elastic Pool, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="165a2-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="165a2-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="165a2-142">RELATED LINKS</span></span>

[<span data-ttu-id="165a2-143">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="165a2-143">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="165a2-144">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="165a2-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
