---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
ms.openlocfilehash: d611f0bc14d657f47881cbdfbb1326111873114a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173434"
---
# <span data-ttu-id="921bb-101">Remove-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="921bb-101">Remove-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="921bb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="921bb-102">SYNOPSIS</span></span>
<span data-ttu-id="921bb-103">Entfernt den Azure SQL Server-DNS-Alias.</span><span class="sxs-lookup"><span data-stu-id="921bb-103">Removes Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="921bb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="921bb-104">SYNTAX</span></span>

### <span data-ttu-id="921bb-105">Entfernen eines Server-DNS-Alias aus Cmdlet-Eingabeparametern</span><span class="sxs-lookup"><span data-stu-id="921bb-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="921bb-106">Entfernen eines Server-DNS-Alias aus der AzureSqlServerDnsAliasModel-Instanzen Definition</span><span class="sxs-lookup"><span data-stu-id="921bb-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="921bb-107">Entfernen eines Server-DNS-Alias aus einer Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="921bb-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="921bb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="921bb-108">DESCRIPTION</span></span>
<span data-ttu-id="921bb-109">Mit diesen Befehlen wird der Azure SQL Server-DNS-Alias vom Server entfernt, der den Server intakt lässt.</span><span class="sxs-lookup"><span data-stu-id="921bb-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="921bb-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="921bb-110">EXAMPLES</span></span>

### <span data-ttu-id="921bb-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="921bb-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="921bb-112">Entfernt Azure SQL Server-DNS-Alias mit dem Namen "Aliasname" vom Server mit dem Namen "Servername"</span><span class="sxs-lookup"><span data-stu-id="921bb-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="921bb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="921bb-113">PARAMETERS</span></span>

### <span data-ttu-id="921bb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="921bb-114">-AsJob</span></span>
<span data-ttu-id="921bb-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="921bb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="921bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="921bb-116">-DefaultProfile</span></span>
<span data-ttu-id="921bb-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="921bb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="921bb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="921bb-118">-Force</span></span>
<span data-ttu-id="921bb-119">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="921bb-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="921bb-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="921bb-120">-InputObject</span></span>
<span data-ttu-id="921bb-121">Das zu entfernende Server-DNS-Alias Objekt</span><span class="sxs-lookup"><span data-stu-id="921bb-121">The Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="921bb-122">-Name</span><span class="sxs-lookup"><span data-stu-id="921bb-122">-Name</span></span>
<span data-ttu-id="921bb-123">Azure SQL Server-DNS-Alias Name</span><span class="sxs-lookup"><span data-stu-id="921bb-123">Azure Sql Server Dns Alias name</span></span>

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

### <span data-ttu-id="921bb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="921bb-124">-ResourceGroupName</span></span>
<span data-ttu-id="921bb-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="921bb-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="921bb-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="921bb-126">-ResourceId</span></span>
<span data-ttu-id="921bb-127">Die Ressourcen-ID des zu entfernenden Server-DNS-Alias Objekts</span><span class="sxs-lookup"><span data-stu-id="921bb-127">The resource id of Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="921bb-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="921bb-128">-ServerName</span></span>
<span data-ttu-id="921bb-129">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="921bb-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="921bb-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="921bb-130">-Confirm</span></span>
<span data-ttu-id="921bb-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="921bb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="921bb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="921bb-132">-WhatIf</span></span>
<span data-ttu-id="921bb-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="921bb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="921bb-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="921bb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="921bb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="921bb-135">CommonParameters</span></span>
<span data-ttu-id="921bb-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="921bb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="921bb-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="921bb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="921bb-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="921bb-138">INPUTS</span></span>

### <span data-ttu-id="921bb-139">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="921bb-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

### <span data-ttu-id="921bb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="921bb-140">System.String</span></span>

## <span data-ttu-id="921bb-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="921bb-141">OUTPUTS</span></span>

### <span data-ttu-id="921bb-142">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="921bb-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="921bb-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="921bb-143">NOTES</span></span>

## <span data-ttu-id="921bb-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="921bb-144">RELATED LINKS</span></span>
