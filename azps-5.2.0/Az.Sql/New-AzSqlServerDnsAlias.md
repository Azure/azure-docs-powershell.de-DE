---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 66f8c3acc178a922868177200e6d4f1f8f50931f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371242"
---
# <span data-ttu-id="5e28b-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="5e28b-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="5e28b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e28b-102">SYNOPSIS</span></span>
<span data-ttu-id="5e28b-103">Mit diesem Befehl wird ein neuer Azure SQL Server-DNS-Alias erstellt.</span><span class="sxs-lookup"><span data-stu-id="5e28b-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="5e28b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e28b-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e28b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e28b-105">DESCRIPTION</span></span>
<span data-ttu-id="5e28b-106">Erstellt einen neuen Azure SQL Server-DNS-Alias, der auf den angegebenen Server verweisen soll.</span><span class="sxs-lookup"><span data-stu-id="5e28b-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="5e28b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5e28b-107">EXAMPLES</span></span>

### <span data-ttu-id="5e28b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5e28b-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="5e28b-109">Mit diesem Befehl wird ein Azure SQL Server-DNS-Alias mit dem Namen "aliasName" erstellt, der auf den Serverservernamen verweisen soll.</span><span class="sxs-lookup"><span data-stu-id="5e28b-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="5e28b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e28b-110">PARAMETERS</span></span>

### <span data-ttu-id="5e28b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e28b-111">-AsJob</span></span>
<span data-ttu-id="5e28b-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5e28b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e28b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e28b-113">-DefaultProfile</span></span>
<span data-ttu-id="5e28b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e28b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e28b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5e28b-115">-Name</span></span>
<span data-ttu-id="5e28b-116">Der Azure Sql Server-Dns-Aliasname.</span><span class="sxs-lookup"><span data-stu-id="5e28b-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e28b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e28b-117">-ResourceGroupName</span></span>
<span data-ttu-id="5e28b-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5e28b-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="5e28b-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5e28b-119">-ServerName</span></span>
<span data-ttu-id="5e28b-120">Der Azure Sql Server-Name.</span><span class="sxs-lookup"><span data-stu-id="5e28b-120">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e28b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e28b-121">-Confirm</span></span>
<span data-ttu-id="5e28b-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e28b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e28b-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5e28b-123">-WhatIf</span></span>
<span data-ttu-id="5e28b-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e28b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e28b-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e28b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e28b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e28b-126">CommonParameters</span></span>
<span data-ttu-id="5e28b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e28b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e28b-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e28b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e28b-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5e28b-129">INPUTS</span></span>

### <span data-ttu-id="5e28b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5e28b-130">System.String</span></span>

## <span data-ttu-id="5e28b-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5e28b-131">OUTPUTS</span></span>

### <span data-ttu-id="5e28b-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="5e28b-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="5e28b-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5e28b-133">NOTES</span></span>

## <span data-ttu-id="5e28b-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5e28b-134">RELATED LINKS</span></span>
