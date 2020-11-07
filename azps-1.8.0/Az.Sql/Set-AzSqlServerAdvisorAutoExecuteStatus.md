---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveradvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: aa3aff9a1e471445c49cbfb23b5799a97c54025d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658965"
---
# <span data-ttu-id="45484-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="45484-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="45484-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="45484-102">SYNOPSIS</span></span>
<span data-ttu-id="45484-103">Aktualisiert den automatischen Ausführungsstatus eines Azure SQL Server-Ratgebers.</span><span class="sxs-lookup"><span data-stu-id="45484-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="45484-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="45484-104">SYNTAX</span></span>

```
Set-AzSqlServerAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45484-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45484-105">DESCRIPTION</span></span>
<span data-ttu-id="45484-106">Das Cmdlet " **Set-AzSqlServerAdvisorAutoExecuteStatus** " legt die Auto Execute-Eigenschaft für einen Azure SQL Server Advisor fest.</span><span class="sxs-lookup"><span data-stu-id="45484-106">The **Set-AzSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="45484-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45484-107">EXAMPLES</span></span>

### <span data-ttu-id="45484-108">Beispiel 1: Aktivieren der automatischen Ausführung für einen Ratgeber</span><span class="sxs-lookup"><span data-stu-id="45484-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
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

<span data-ttu-id="45484-109">Dieser Befehl aktiviert den automatischen Ausführungsstatus eines Ratgebers mit dem Namen CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="45484-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="45484-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="45484-110">PARAMETERS</span></span>

### <span data-ttu-id="45484-111">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="45484-111">-AdvisorName</span></span>
<span data-ttu-id="45484-112">Gibt den Namen des Beraters an, für den das Cmdlet den automatischen Ausführungsstatus aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="45484-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="45484-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="45484-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="45484-114">Gibt den Wert an, mit dem dieses Cmdlet den Status der automatischen Ausführung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="45484-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="45484-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="45484-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="45484-116">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="45484-116">Enabled</span></span>
- <span data-ttu-id="45484-117">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="45484-117">Disabled</span></span>
- <span data-ttu-id="45484-118">Standard</span><span class="sxs-lookup"><span data-stu-id="45484-118">Default</span></span>

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

### <span data-ttu-id="45484-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45484-119">-DefaultProfile</span></span>
<span data-ttu-id="45484-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="45484-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45484-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45484-121">-ResourceGroupName</span></span>
<span data-ttu-id="45484-122">Gibt den Namen der Ressourcengruppe des Servers an.</span><span class="sxs-lookup"><span data-stu-id="45484-122">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="45484-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="45484-123">-ServerName</span></span>
<span data-ttu-id="45484-124">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="45484-124">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="45484-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="45484-125">-Confirm</span></span>
<span data-ttu-id="45484-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="45484-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45484-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45484-127">-WhatIf</span></span>
<span data-ttu-id="45484-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="45484-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45484-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="45484-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45484-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45484-130">CommonParameters</span></span>
<span data-ttu-id="45484-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45484-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45484-132">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45484-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45484-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="45484-133">INPUTS</span></span>

### <span data-ttu-id="45484-134">System. String</span><span class="sxs-lookup"><span data-stu-id="45484-134">System.String</span></span>

### <span data-ttu-id="45484-135">Microsoft. Azure. Commands. SQL. Advisor. Cmdlet. AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="45484-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="45484-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="45484-136">OUTPUTS</span></span>

### <span data-ttu-id="45484-137">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="45484-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="45484-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="45484-138">NOTES</span></span>
* <span data-ttu-id="45484-139">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Server, MSSQL, Ratgeber</span><span class="sxs-lookup"><span data-stu-id="45484-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="45484-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="45484-140">RELATED LINKS</span></span>

[<span data-ttu-id="45484-141">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="45484-141">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="45484-142">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="45484-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
