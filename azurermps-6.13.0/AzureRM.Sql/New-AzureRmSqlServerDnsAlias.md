---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 3ce18369645705f78722f7505c8dd1e46f2514b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477650"
---
# <span data-ttu-id="22307-101">New-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="22307-101">New-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="22307-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="22307-102">SYNOPSIS</span></span>
<span data-ttu-id="22307-103">Dieser Befehl erstellt einen neuen Azure SQL Server-DNS-Alias.</span><span class="sxs-lookup"><span data-stu-id="22307-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22307-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="22307-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22307-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22307-105">DESCRIPTION</span></span>
<span data-ttu-id="22307-106">Erstellt einen neuen Azure SQL Server-DNS-Alias, der auf den angegebenen Server verweist.</span><span class="sxs-lookup"><span data-stu-id="22307-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="22307-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22307-107">EXAMPLES</span></span>

### <span data-ttu-id="22307-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="22307-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzureRmSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="22307-109">Dieser Befehl erstellt einen Azure SQL Server-DNS-Alias mit dem Namen Aliasname, der auf Server Name verweist.</span><span class="sxs-lookup"><span data-stu-id="22307-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="22307-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="22307-110">PARAMETERS</span></span>

### <span data-ttu-id="22307-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22307-111">-AsJob</span></span>
<span data-ttu-id="22307-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="22307-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22307-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22307-113">-DefaultProfile</span></span>
<span data-ttu-id="22307-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="22307-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22307-115">-Name</span><span class="sxs-lookup"><span data-stu-id="22307-115">-Name</span></span>
<span data-ttu-id="22307-116">Der Azure SQL Server-DNS-Alias Name.</span><span class="sxs-lookup"><span data-stu-id="22307-116">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="22307-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22307-117">-ResourceGroupName</span></span>
<span data-ttu-id="22307-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="22307-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="22307-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="22307-119">-ServerName</span></span>
<span data-ttu-id="22307-120">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="22307-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="22307-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="22307-121">-Confirm</span></span>
<span data-ttu-id="22307-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="22307-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22307-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22307-123">-WhatIf</span></span>
<span data-ttu-id="22307-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="22307-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22307-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="22307-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22307-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22307-126">CommonParameters</span></span>
<span data-ttu-id="22307-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22307-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22307-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22307-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22307-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="22307-129">INPUTS</span></span>

### <span data-ttu-id="22307-130">System. String</span><span class="sxs-lookup"><span data-stu-id="22307-130">System.String</span></span>

## <span data-ttu-id="22307-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="22307-131">OUTPUTS</span></span>

### <span data-ttu-id="22307-132">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="22307-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="22307-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="22307-133">NOTES</span></span>

## <span data-ttu-id="22307-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="22307-134">RELATED LINKS</span></span>
