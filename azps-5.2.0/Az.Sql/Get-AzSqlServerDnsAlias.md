---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 417bab5679da4607cc42468fc4620cf392323919
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304491"
---
# <span data-ttu-id="71398-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="71398-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="71398-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71398-102">SYNOPSIS</span></span>
<span data-ttu-id="71398-103">Ruft den Azure SQL Server-DNS-Alias ab oder listet diese auf.</span><span class="sxs-lookup"><span data-stu-id="71398-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="71398-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71398-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71398-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71398-105">DESCRIPTION</span></span>
<span data-ttu-id="71398-106">Den spezifischen Azure SQL Server-DNS-Alias erhalten oder alle Server-DNS-Aliase für den Server auflisten</span><span class="sxs-lookup"><span data-stu-id="71398-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="71398-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="71398-107">EXAMPLES</span></span>

### <span data-ttu-id="71398-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="71398-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="71398-109">Listet alle Server-DNS-Aliase für den jeweiligen Server auf.</span><span class="sxs-lookup"><span data-stu-id="71398-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="71398-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="71398-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="71398-111">Erhält Server-DNS-Alias, der durch den Server- und Aliasnamen angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="71398-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="71398-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="71398-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="71398-113">Listet alle Server-DNS-Aliase für den jeweiligen Server auf, die mit "dnsaliasname" beginnen.</span><span class="sxs-lookup"><span data-stu-id="71398-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="71398-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71398-114">PARAMETERS</span></span>

### <span data-ttu-id="71398-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71398-115">-DefaultProfile</span></span>
<span data-ttu-id="71398-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="71398-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71398-117">-Name</span><span class="sxs-lookup"><span data-stu-id="71398-117">-Name</span></span>
<span data-ttu-id="71398-118">Der Azure Sql Server-DNS-Aliasname.</span><span class="sxs-lookup"><span data-stu-id="71398-118">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71398-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71398-119">-ResourceGroupName</span></span>
<span data-ttu-id="71398-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="71398-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="71398-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="71398-121">-ServerName</span></span>
<span data-ttu-id="71398-122">Der Azure Sql Server-Name.</span><span class="sxs-lookup"><span data-stu-id="71398-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="71398-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71398-123">-Confirm</span></span>
<span data-ttu-id="71398-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="71398-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71398-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="71398-125">-WhatIf</span></span>
<span data-ttu-id="71398-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71398-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71398-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71398-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71398-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71398-128">CommonParameters</span></span>
<span data-ttu-id="71398-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71398-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71398-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71398-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71398-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="71398-131">INPUTS</span></span>

### <span data-ttu-id="71398-132">System.String</span><span class="sxs-lookup"><span data-stu-id="71398-132">System.String</span></span>

## <span data-ttu-id="71398-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="71398-133">OUTPUTS</span></span>

### <span data-ttu-id="71398-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="71398-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="71398-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="71398-135">NOTES</span></span>

## <span data-ttu-id="71398-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="71398-136">RELATED LINKS</span></span>
