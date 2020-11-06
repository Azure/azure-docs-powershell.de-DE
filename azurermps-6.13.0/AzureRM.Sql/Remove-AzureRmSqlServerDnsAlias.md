---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 5afd12ac027b19f888eb6a5110db2179dd6df24d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504281"
---
# <span data-ttu-id="f7be8-101">Remove-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="f7be8-101">Remove-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="f7be8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7be8-102">SYNOPSIS</span></span>
<span data-ttu-id="f7be8-103">Entfernt den Azure SQL Server-DNS-Alias.</span><span class="sxs-lookup"><span data-stu-id="f7be8-103">Removes Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7be8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7be8-104">SYNTAX</span></span>

### <span data-ttu-id="f7be8-105">Entfernen eines Server-DNS-Alias aus Cmdlet-Eingabeparametern</span><span class="sxs-lookup"><span data-stu-id="f7be8-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzureRmSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7be8-106">Entfernen eines Server-DNS-Alias aus der AzureSqlServerDnsAliasModel-Instanzen Definition</span><span class="sxs-lookup"><span data-stu-id="f7be8-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzureRmSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7be8-107">Entfernen eines Server-DNS-Alias aus einer Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="f7be8-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzureRmSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7be8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7be8-108">DESCRIPTION</span></span>
<span data-ttu-id="f7be8-109">Mit diesen Befehlen wird der Azure SQL Server-DNS-Alias vom Server entfernt, der den Server intakt lässt.</span><span class="sxs-lookup"><span data-stu-id="f7be8-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="f7be8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7be8-110">EXAMPLES</span></span>

### <span data-ttu-id="f7be8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f7be8-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="f7be8-112">Entfernt Azure SQL Server-DNS-Alias mit dem Namen "Aliasname" vom Server mit dem Namen "Servername"</span><span class="sxs-lookup"><span data-stu-id="f7be8-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="f7be8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7be8-113">PARAMETERS</span></span>

### <span data-ttu-id="f7be8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7be8-114">-AsJob</span></span>
<span data-ttu-id="f7be8-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f7be8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7be8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7be8-116">-DefaultProfile</span></span>
<span data-ttu-id="f7be8-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f7be8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7be8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f7be8-118">-Force</span></span>
<span data-ttu-id="f7be8-119">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="f7be8-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="f7be8-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f7be8-120">-InputObject</span></span>
<span data-ttu-id="f7be8-121">Das zu entfernende Server-DNS-Alias Objekt</span><span class="sxs-lookup"><span data-stu-id="f7be8-121">The Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="f7be8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f7be8-122">-Name</span></span>
<span data-ttu-id="f7be8-123">Azure SQL Server-DNS-Alias Name</span><span class="sxs-lookup"><span data-stu-id="f7be8-123">Azure Sql Server Dns Alias name</span></span>

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

### <span data-ttu-id="f7be8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7be8-124">-ResourceGroupName</span></span>
<span data-ttu-id="f7be8-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f7be8-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="f7be8-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f7be8-126">-ResourceId</span></span>
<span data-ttu-id="f7be8-127">Die Ressourcen-ID des zu entfernenden Server-DNS-Alias Objekts</span><span class="sxs-lookup"><span data-stu-id="f7be8-127">The resource id of Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="f7be8-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="f7be8-128">-ServerName</span></span>
<span data-ttu-id="f7be8-129">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="f7be8-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="f7be8-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f7be8-130">-Confirm</span></span>
<span data-ttu-id="f7be8-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7be8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7be8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7be8-132">-WhatIf</span></span>
<span data-ttu-id="f7be8-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7be8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7be8-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7be8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7be8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7be8-135">CommonParameters</span></span>
<span data-ttu-id="f7be8-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7be8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7be8-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7be8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7be8-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7be8-138">INPUTS</span></span>

### <span data-ttu-id="f7be8-139">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="f7be8-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>
<span data-ttu-id="f7be8-140">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f7be8-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="f7be8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f7be8-141">System.String</span></span>

## <span data-ttu-id="f7be8-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7be8-142">OUTPUTS</span></span>

### <span data-ttu-id="f7be8-143">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="f7be8-143">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="f7be8-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7be8-144">NOTES</span></span>

## <span data-ttu-id="f7be8-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7be8-145">RELATED LINKS</span></span>
