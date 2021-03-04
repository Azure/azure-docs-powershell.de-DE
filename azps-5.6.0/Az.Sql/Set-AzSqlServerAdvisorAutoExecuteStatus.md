---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserveradvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: a80656e0a85401c4a98b62823b2b19ec2294d2f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949856"
---
# <span data-ttu-id="f4470-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f4470-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="f4470-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4470-102">SYNOPSIS</span></span>
<span data-ttu-id="f4470-103">Aktualisiert den Status der automatischen Ausführung eines Azure SQL Server Advisors.</span><span class="sxs-lookup"><span data-stu-id="f4470-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="f4470-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4470-104">SYNTAX</span></span>

```
Set-AzSqlServerAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4470-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4470-105">DESCRIPTION</span></span>
<span data-ttu-id="f4470-106">Das **Cmdlet Set-AzSqlServerAdvisorAutoExecuteStatus** legt die Eigenschaft für die automatische Ausführung für einen Azure SQL Server-Berater fest.</span><span class="sxs-lookup"><span data-stu-id="f4470-106">The **Set-AzSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="f4470-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f4470-107">EXAMPLES</span></span>

### <span data-ttu-id="f4470-108">Beispiel 1: Aktivieren der automatischen Ausführung für einen Berater</span><span class="sxs-lookup"><span data-stu-id="f4470-108">Example 1: Enable auto execute for an Advisor</span></span>
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

<span data-ttu-id="f4470-109">Mit diesem Befehl wird der Status der automatischen Ausführung eines Advisors namens CreateIndex aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f4470-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="f4470-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f4470-110">PARAMETERS</span></span>

### <span data-ttu-id="f4470-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="f4470-111">-AdvisorName</span></span>
<span data-ttu-id="f4470-112">Gibt den Namen des Beraters an, für den dieses Cmdlet den Status der automatischen Ausführung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f4470-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="f4470-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f4470-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="f4470-114">Gibt den Wert an, auf den dieses Cmdlet den Status der automatischen Ausführung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f4470-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="f4470-115">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="f4470-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f4470-116">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="f4470-116">Enabled</span></span>
- <span data-ttu-id="f4470-117">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="f4470-117">Disabled</span></span>
- <span data-ttu-id="f4470-118">Standard</span><span class="sxs-lookup"><span data-stu-id="f4470-118">Default</span></span>

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

### <span data-ttu-id="f4470-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4470-119">-DefaultProfile</span></span>
<span data-ttu-id="f4470-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f4470-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4470-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4470-121">-ResourceGroupName</span></span>
<span data-ttu-id="f4470-122">Gibt den Namen der Ressourcengruppe des Servers an.</span><span class="sxs-lookup"><span data-stu-id="f4470-122">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="f4470-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="f4470-123">-ServerName</span></span>
<span data-ttu-id="f4470-124">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="f4470-124">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="f4470-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f4470-125">-Confirm</span></span>
<span data-ttu-id="f4470-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4470-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4470-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4470-127">-WhatIf</span></span>
<span data-ttu-id="f4470-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4470-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4470-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4470-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4470-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4470-130">CommonParameters</span></span>
<span data-ttu-id="f4470-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4470-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4470-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4470-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4470-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f4470-133">INPUTS</span></span>

### <span data-ttu-id="f4470-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f4470-134">System.String</span></span>

### <span data-ttu-id="f4470-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f4470-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="f4470-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f4470-136">OUTPUTS</span></span>

### <span data-ttu-id="f4470-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="f4470-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="f4470-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f4470-138">NOTES</span></span>
* <span data-ttu-id="f4470-139">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="f4470-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="f4470-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f4470-140">RELATED LINKS</span></span>

[<span data-ttu-id="f4470-141">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="f4470-141">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="f4470-142">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="f4470-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
