---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 68e81a7f51ca385d5671698ad8624f523ae98c53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923928"
---
# <span data-ttu-id="41138-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="41138-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="41138-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41138-102">SYNOPSIS</span></span>
<span data-ttu-id="41138-103">Ruft Aktivitäten für eine Datenbankserversystemwiederherstellungskonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="41138-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="41138-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41138-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41138-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41138-105">DESCRIPTION</span></span>
<span data-ttu-id="41138-106">Das **Cmdlet Get-AzSqlServerDisasterRecoveryConfigurationActivity** ruft Aktivitäten für eine SQL Datenbankserversystemwiederherstellungskonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="41138-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="41138-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="41138-107">EXAMPLES</span></span>

## <span data-ttu-id="41138-108">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="41138-108">PARAMETERS</span></span>

### <span data-ttu-id="41138-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41138-109">-DefaultProfile</span></span>
<span data-ttu-id="41138-110">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="41138-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41138-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="41138-111">-OperationId</span></span>
<span data-ttu-id="41138-112">Gibt die Vorgangs-ID an.</span><span class="sxs-lookup"><span data-stu-id="41138-112">Specifies the operation ID.</span></span>

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

### <span data-ttu-id="41138-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41138-113">-ResourceGroupName</span></span>
<span data-ttu-id="41138-114">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="41138-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="41138-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="41138-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="41138-116">Gibt den Namen der Serversystemwiederherstellungskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="41138-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="41138-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="41138-117">-ServerName</span></span>
<span data-ttu-id="41138-118">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="41138-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="41138-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="41138-119">-Confirm</span></span>
<span data-ttu-id="41138-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="41138-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41138-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41138-121">-WhatIf</span></span>
<span data-ttu-id="41138-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="41138-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41138-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="41138-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41138-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41138-124">CommonParameters</span></span>
<span data-ttu-id="41138-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41138-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41138-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41138-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41138-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="41138-127">INPUTS</span></span>

### <span data-ttu-id="41138-128">System.String</span><span class="sxs-lookup"><span data-stu-id="41138-128">System.String</span></span>

### <span data-ttu-id="41138-129">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="41138-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="41138-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="41138-130">OUTPUTS</span></span>

### <span data-ttu-id="41138-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="41138-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="41138-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="41138-132">NOTES</span></span>

## <span data-ttu-id="41138-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="41138-133">RELATED LINKS</span></span>

[<span data-ttu-id="41138-134">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="41138-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
