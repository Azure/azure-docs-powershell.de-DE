---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
ms.openlocfilehash: 9d1b34314c3c620e73a077b77f3935880d6621d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825376"
---
# <span data-ttu-id="6a97e-101">Remove-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="6a97e-101">Remove-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="6a97e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6a97e-102">SYNOPSIS</span></span>
<span data-ttu-id="6a97e-103">Entfernt den Azure SQL Server-DNS-Alias.</span><span class="sxs-lookup"><span data-stu-id="6a97e-103">Removes Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="6a97e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a97e-104">SYNTAX</span></span>

### <span data-ttu-id="6a97e-105">Entfernen eines Server-DNS-Alias aus Cmdlet-Eingabeparametern</span><span class="sxs-lookup"><span data-stu-id="6a97e-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a97e-106">Entfernen eines Server-DNS-Alias aus der AzureSqlServerDnsAliasModel-Instanzen Definition</span><span class="sxs-lookup"><span data-stu-id="6a97e-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a97e-107">Entfernen eines Server-DNS-Alias aus einer Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="6a97e-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a97e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a97e-108">DESCRIPTION</span></span>
<span data-ttu-id="6a97e-109">Mit diesen Befehlen wird der Azure SQL Server-DNS-Alias vom Server entfernt, der den Server intakt lässt.</span><span class="sxs-lookup"><span data-stu-id="6a97e-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="6a97e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6a97e-110">EXAMPLES</span></span>

### <span data-ttu-id="6a97e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6a97e-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="6a97e-112">Entfernt Azure SQL Server-DNS-Alias mit dem Namen "Aliasname" vom Server mit dem Namen "Servername"</span><span class="sxs-lookup"><span data-stu-id="6a97e-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="6a97e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a97e-113">PARAMETERS</span></span>

### <span data-ttu-id="6a97e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a97e-114">-AsJob</span></span>
<span data-ttu-id="6a97e-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6a97e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a97e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a97e-116">-DefaultProfile</span></span>
<span data-ttu-id="6a97e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6a97e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a97e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6a97e-118">-Force</span></span>
<span data-ttu-id="6a97e-119">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="6a97e-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="6a97e-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6a97e-120">-InputObject</span></span>
<span data-ttu-id="6a97e-121">Das zu entfernende Server-DNS-Alias Objekt</span><span class="sxs-lookup"><span data-stu-id="6a97e-121">The Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="6a97e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6a97e-122">-Name</span></span>
<span data-ttu-id="6a97e-123">Azure SQL Server-DNS-Alias Name</span><span class="sxs-lookup"><span data-stu-id="6a97e-123">Azure Sql Server Dns Alias name</span></span>

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

### <span data-ttu-id="6a97e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a97e-124">-ResourceGroupName</span></span>
<span data-ttu-id="6a97e-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6a97e-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="6a97e-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6a97e-126">-ResourceId</span></span>
<span data-ttu-id="6a97e-127">Die Ressourcen-ID des zu entfernenden Server-DNS-Alias Objekts</span><span class="sxs-lookup"><span data-stu-id="6a97e-127">The resource id of Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="6a97e-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="6a97e-128">-ServerName</span></span>
<span data-ttu-id="6a97e-129">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="6a97e-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="6a97e-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6a97e-130">-Confirm</span></span>
<span data-ttu-id="6a97e-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6a97e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a97e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a97e-132">-WhatIf</span></span>
<span data-ttu-id="6a97e-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6a97e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a97e-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6a97e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a97e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a97e-135">CommonParameters</span></span>
<span data-ttu-id="6a97e-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a97e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a97e-137">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a97e-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a97e-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6a97e-138">INPUTS</span></span>

### <span data-ttu-id="6a97e-139">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="6a97e-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

### <span data-ttu-id="6a97e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6a97e-140">System.String</span></span>

## <span data-ttu-id="6a97e-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6a97e-141">OUTPUTS</span></span>

### <span data-ttu-id="6a97e-142">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="6a97e-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="6a97e-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="6a97e-143">NOTES</span></span>

## <span data-ttu-id="6a97e-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6a97e-144">RELATED LINKS</span></span>
