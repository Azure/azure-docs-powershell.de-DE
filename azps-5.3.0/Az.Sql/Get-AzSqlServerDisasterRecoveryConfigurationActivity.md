---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: ad3c257366513a5cc9998b4e4edea8879dc38545
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470332"
---
# <span data-ttu-id="42600-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="42600-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="42600-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42600-102">SYNOPSIS</span></span>
<span data-ttu-id="42600-103">Ruft Die Aktivität für eine Datenbankserversystemwiederherstellungskonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="42600-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="42600-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42600-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42600-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42600-105">DESCRIPTION</span></span>
<span data-ttu-id="42600-106">Das **Cmdlet "Get-AzSqlServerDisasterRecoveryConfigurationActivity"** ruft Aktivitäten für eine SQL Wiederherstellungskonfiguration des Datenbankserversystems ab.</span><span class="sxs-lookup"><span data-stu-id="42600-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="42600-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="42600-107">EXAMPLES</span></span>

## <span data-ttu-id="42600-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42600-108">PARAMETERS</span></span>

### <span data-ttu-id="42600-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42600-109">-DefaultProfile</span></span>
<span data-ttu-id="42600-110">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="42600-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42600-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="42600-111">-OperationId</span></span>
<span data-ttu-id="42600-112">Gibt die Vorgangs-ID an.</span><span class="sxs-lookup"><span data-stu-id="42600-112">Specifies the operation ID.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42600-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42600-113">-ResourceGroupName</span></span>
<span data-ttu-id="42600-114">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="42600-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="42600-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="42600-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="42600-116">Gibt den Namen der Wiederherstellungskonfiguration des Serversystems an.</span><span class="sxs-lookup"><span data-stu-id="42600-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="42600-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="42600-117">-ServerName</span></span>
<span data-ttu-id="42600-118">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="42600-118">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42600-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42600-119">-Confirm</span></span>
<span data-ttu-id="42600-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="42600-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42600-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="42600-121">-WhatIf</span></span>
<span data-ttu-id="42600-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42600-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42600-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42600-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42600-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42600-124">CommonParameters</span></span>
<span data-ttu-id="42600-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42600-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42600-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42600-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42600-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="42600-127">INPUTS</span></span>

### <span data-ttu-id="42600-128">System.String</span><span class="sxs-lookup"><span data-stu-id="42600-128">System.String</span></span>

### <span data-ttu-id="42600-129">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="42600-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="42600-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="42600-130">OUTPUTS</span></span>

### <span data-ttu-id="42600-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="42600-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="42600-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="42600-132">NOTES</span></span>

## <span data-ttu-id="42600-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="42600-133">RELATED LINKS</span></span>

[<span data-ttu-id="42600-134">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="42600-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
