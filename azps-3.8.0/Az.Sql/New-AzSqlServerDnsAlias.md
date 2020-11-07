---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 66f8c3acc178a922868177200e6d4f1f8f50931f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847388"
---
# <span data-ttu-id="bfbf9-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="bfbf9-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="bfbf9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bfbf9-102">SYNOPSIS</span></span>
<span data-ttu-id="bfbf9-103">Dieser Befehl erstellt einen neuen Azure SQL Server-DNS-Alias.</span><span class="sxs-lookup"><span data-stu-id="bfbf9-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="bfbf9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfbf9-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfbf9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfbf9-105">DESCRIPTION</span></span>
<span data-ttu-id="bfbf9-106">Erstellt einen neuen Azure SQL Server-DNS-Alias, der auf den angegebenen Server verweist.</span><span class="sxs-lookup"><span data-stu-id="bfbf9-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="bfbf9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bfbf9-107">EXAMPLES</span></span>

### <span data-ttu-id="bfbf9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bfbf9-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="bfbf9-109">Dieser Befehl erstellt einen Azure SQL Server-DNS-Alias mit dem Namen Aliasname, der auf Server Name verweist.</span><span class="sxs-lookup"><span data-stu-id="bfbf9-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="bfbf9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfbf9-110">PARAMETERS</span></span>

### <span data-ttu-id="bfbf9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bfbf9-111">-AsJob</span></span>
<span data-ttu-id="bfbf9-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="bfbf9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bfbf9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfbf9-113">-DefaultProfile</span></span>
<span data-ttu-id="bfbf9-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bfbf9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfbf9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="bfbf9-115">-Name</span></span>
<span data-ttu-id="bfbf9-116">Der Azure SQL Server-DNS-Alias Name.</span><span class="sxs-lookup"><span data-stu-id="bfbf9-116">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="bfbf9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfbf9-117">-ResourceGroupName</span></span>
<span data-ttu-id="bfbf9-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bfbf9-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="bfbf9-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="bfbf9-119">-ServerName</span></span>
<span data-ttu-id="bfbf9-120">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="bfbf9-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="bfbf9-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bfbf9-121">-Confirm</span></span>
<span data-ttu-id="bfbf9-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bfbf9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfbf9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfbf9-123">-WhatIf</span></span>
<span data-ttu-id="bfbf9-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bfbf9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfbf9-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bfbf9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfbf9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfbf9-126">CommonParameters</span></span>
<span data-ttu-id="bfbf9-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfbf9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfbf9-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfbf9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfbf9-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bfbf9-129">INPUTS</span></span>

### <span data-ttu-id="bfbf9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bfbf9-130">System.String</span></span>

## <span data-ttu-id="bfbf9-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bfbf9-131">OUTPUTS</span></span>

### <span data-ttu-id="bfbf9-132">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="bfbf9-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="bfbf9-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="bfbf9-133">NOTES</span></span>

## <span data-ttu-id="bfbf9-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bfbf9-134">RELATED LINKS</span></span>
