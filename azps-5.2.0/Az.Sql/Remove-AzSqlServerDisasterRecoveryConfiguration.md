---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: df3ed9faa96a98b4e94df370bf90161e7baf2b99
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289606"
---
# <span data-ttu-id="07442-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="07442-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="07442-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07442-102">SYNOPSIS</span></span>
<span data-ttu-id="07442-103">Entfernt eine wiederherstellungskonfiguration SQL Datenbankserversystems.</span><span class="sxs-lookup"><span data-stu-id="07442-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="07442-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07442-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07442-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07442-105">DESCRIPTION</span></span>
<span data-ttu-id="07442-106">Das **Cmdlet "Remove-AzSqlServerDisasterRecoveryConfiguration"** entfernt eine SQL Datenbankserversystemwiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="07442-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="07442-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="07442-107">EXAMPLES</span></span>

## <span data-ttu-id="07442-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07442-108">PARAMETERS</span></span>

### <span data-ttu-id="07442-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07442-109">-DefaultProfile</span></span>
<span data-ttu-id="07442-110">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="07442-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07442-111">-Force</span><span class="sxs-lookup"><span data-stu-id="07442-111">-Force</span></span>
<span data-ttu-id="07442-112">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="07442-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07442-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07442-113">-ResourceGroupName</span></span>
<span data-ttu-id="07442-114">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="07442-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="07442-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="07442-115">-ServerName</span></span>
<span data-ttu-id="07442-116">Gibt den Namen eines SQL Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="07442-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="07442-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="07442-117">-VirtualEndpointName</span></span>
<span data-ttu-id="07442-118">Gibt den Namen eines virtuellen Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="07442-118">Specifies the name of a virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07442-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07442-119">-Confirm</span></span>
<span data-ttu-id="07442-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="07442-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07442-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="07442-121">-WhatIf</span></span>
<span data-ttu-id="07442-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07442-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07442-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07442-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07442-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07442-124">CommonParameters</span></span>
<span data-ttu-id="07442-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07442-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07442-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07442-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07442-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="07442-127">INPUTS</span></span>

### <span data-ttu-id="07442-128">System.String</span><span class="sxs-lookup"><span data-stu-id="07442-128">System.String</span></span>

## <span data-ttu-id="07442-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="07442-129">OUTPUTS</span></span>

### <span data-ttu-id="07442-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="07442-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="07442-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="07442-131">NOTES</span></span>

## <span data-ttu-id="07442-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="07442-132">RELATED LINKS</span></span>

[<span data-ttu-id="07442-133">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="07442-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="07442-134">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="07442-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="07442-135">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="07442-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="07442-136">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="07442-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
