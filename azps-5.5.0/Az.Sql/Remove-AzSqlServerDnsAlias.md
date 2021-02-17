---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
ms.openlocfilehash: d611f0bc14d657f47881cbdfbb1326111873114a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164908"
---
# <span data-ttu-id="71c9a-101">Remove-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="71c9a-101">Remove-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="71c9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71c9a-102">SYNOPSIS</span></span>
<span data-ttu-id="71c9a-103">Entfernt den Azure SQL Server-DNS-Alias.</span><span class="sxs-lookup"><span data-stu-id="71c9a-103">Removes Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="71c9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71c9a-104">SYNTAX</span></span>

### <span data-ttu-id="71c9a-105">Entfernen eines Server-DNS-Alias aus Eingabeparametern für Cmdlets</span><span class="sxs-lookup"><span data-stu-id="71c9a-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71c9a-106">Entfernen eines Server-Dns-Alias aus der AzureSqlServerDnsAliasModel-Instanzdefinition</span><span class="sxs-lookup"><span data-stu-id="71c9a-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71c9a-107">Entfernen eines Server-DNS-Alias aus einer Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="71c9a-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71c9a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71c9a-108">DESCRIPTION</span></span>
<span data-ttu-id="71c9a-109">Mit diesen Befehlen wird der Azure SQL Server-DNS-Alias vom Server entfernt, und der Server bleibt intakt.</span><span class="sxs-lookup"><span data-stu-id="71c9a-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="71c9a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="71c9a-110">EXAMPLES</span></span>

### <span data-ttu-id="71c9a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="71c9a-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="71c9a-112">Entfernt den Azure SQL Server-DNS-Alias mit dem Namen "aliasName" vom Server mit dem Namenservername.</span><span class="sxs-lookup"><span data-stu-id="71c9a-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="71c9a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71c9a-113">PARAMETERS</span></span>

### <span data-ttu-id="71c9a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71c9a-114">-AsJob</span></span>
<span data-ttu-id="71c9a-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="71c9a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71c9a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71c9a-116">-DefaultProfile</span></span>
<span data-ttu-id="71c9a-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="71c9a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71c9a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="71c9a-118">-Force</span></span>
<span data-ttu-id="71c9a-119">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="71c9a-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="71c9a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71c9a-120">-InputObject</span></span>
<span data-ttu-id="71c9a-121">Das zu entfernende Server-DNS-Aliasobjekt</span><span class="sxs-lookup"><span data-stu-id="71c9a-121">The Server Dns Alias object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel
Parameter Sets: Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71c9a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="71c9a-122">-Name</span></span>
<span data-ttu-id="71c9a-123">Azure Sql Server-Dns-Aliasname</span><span class="sxs-lookup"><span data-stu-id="71c9a-123">Azure Sql Server Dns Alias name</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c9a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71c9a-124">-ResourceGroupName</span></span>
<span data-ttu-id="71c9a-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="71c9a-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c9a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71c9a-126">-ResourceId</span></span>
<span data-ttu-id="71c9a-127">Die Ressourcen-ID des zu entfernende Server-Dns-Aliasobjekts</span><span class="sxs-lookup"><span data-stu-id="71c9a-127">The resource id of Server Dns Alias object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from an Azure resource id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71c9a-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="71c9a-128">-ServerName</span></span>
<span data-ttu-id="71c9a-129">Der Azure Sql Server-Name.</span><span class="sxs-lookup"><span data-stu-id="71c9a-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c9a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71c9a-130">-Confirm</span></span>
<span data-ttu-id="71c9a-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="71c9a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71c9a-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="71c9a-132">-WhatIf</span></span>
<span data-ttu-id="71c9a-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71c9a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71c9a-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71c9a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71c9a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71c9a-135">CommonParameters</span></span>
<span data-ttu-id="71c9a-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71c9a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71c9a-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71c9a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71c9a-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="71c9a-138">INPUTS</span></span>

### <span data-ttu-id="71c9a-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="71c9a-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

### <span data-ttu-id="71c9a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="71c9a-140">System.String</span></span>

## <span data-ttu-id="71c9a-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="71c9a-141">OUTPUTS</span></span>

### <span data-ttu-id="71c9a-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="71c9a-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="71c9a-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="71c9a-143">NOTES</span></span>

## <span data-ttu-id="71c9a-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="71c9a-144">RELATED LINKS</span></span>
