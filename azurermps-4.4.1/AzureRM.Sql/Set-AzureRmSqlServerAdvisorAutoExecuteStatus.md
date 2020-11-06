---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: f483d3deb6c4e4ee6fb5c091dffc9b7969766d6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499125"
---
# <span data-ttu-id="b2d31-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b2d31-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="b2d31-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2d31-102">SYNOPSIS</span></span>
<span data-ttu-id="b2d31-103">Aktualisiert den automatischen Ausführungsstatus eines Azure SQL Server-Ratgebers.</span><span class="sxs-lookup"><span data-stu-id="b2d31-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2d31-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2d31-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2d31-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2d31-105">DESCRIPTION</span></span>
<span data-ttu-id="b2d31-106">Das Cmdlet " **Set-AzureRmSqlServerAdvisorAutoExecuteStatus** " legt die Auto Execute-Eigenschaft für einen Azure SQL Server Advisor fest.</span><span class="sxs-lookup"><span data-stu-id="b2d31-106">The **Set-AzureRmSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="b2d31-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2d31-107">EXAMPLES</span></span>

### <span data-ttu-id="b2d31-108">Beispiel 1: Aktivieren der automatischen Ausführung für einen Ratgeber</span><span class="sxs-lookup"><span data-stu-id="b2d31-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzureRmSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Server
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="b2d31-109">Dieser Befehl aktiviert den automatischen Ausführungsstatus eines Ratgebers mit dem Namen CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="b2d31-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="b2d31-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2d31-110">PARAMETERS</span></span>

### <span data-ttu-id="b2d31-111">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="b2d31-111">-AdvisorName</span></span>
<span data-ttu-id="b2d31-112">Gibt den Namen des Beraters an, für den das Cmdlet den automatischen Ausführungsstatus aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b2d31-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="b2d31-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b2d31-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="b2d31-114">Gibt den Wert an, mit dem dieses Cmdlet den Status der automatischen Ausführung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b2d31-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>

<span data-ttu-id="b2d31-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b2d31-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b2d31-116">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="b2d31-116">Enabled</span></span>
- <span data-ttu-id="b2d31-117">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="b2d31-117">Disabled</span></span>
- <span data-ttu-id="b2d31-118">Standard</span><span class="sxs-lookup"><span data-stu-id="b2d31-118">Default</span></span>

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

### <span data-ttu-id="b2d31-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2d31-119">-ResourceGroupName</span></span>
<span data-ttu-id="b2d31-120">Gibt den Namen der Ressourcengruppe des Servers an.</span><span class="sxs-lookup"><span data-stu-id="b2d31-120">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="b2d31-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="b2d31-121">-ServerName</span></span>
<span data-ttu-id="b2d31-122">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="b2d31-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="b2d31-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b2d31-123">-Confirm</span></span>
<span data-ttu-id="b2d31-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2d31-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2d31-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2d31-125">-WhatIf</span></span>
<span data-ttu-id="b2d31-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2d31-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2d31-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2d31-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2d31-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2d31-128">-DefaultProfile</span></span>
<span data-ttu-id="b2d31-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b2d31-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2d31-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2d31-130">CommonParameters</span></span>
<span data-ttu-id="b2d31-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2d31-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2d31-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2d31-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2d31-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2d31-133">INPUTS</span></span>

## <span data-ttu-id="b2d31-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2d31-134">OUTPUTS</span></span>

### <span data-ttu-id="b2d31-135">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="b2d31-135">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="b2d31-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2d31-136">NOTES</span></span>
* <span data-ttu-id="b2d31-137">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Server, MSSQL, Ratgeber</span><span class="sxs-lookup"><span data-stu-id="b2d31-137">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="b2d31-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2d31-138">RELATED LINKS</span></span>

[<span data-ttu-id="b2d31-139">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="b2d31-139">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="b2d31-140">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="b2d31-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
