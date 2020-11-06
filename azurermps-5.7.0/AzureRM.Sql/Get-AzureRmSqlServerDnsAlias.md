---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 4a2b7de83036e274b9d53b701615e3c348c5f4df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476494"
---
# <span data-ttu-id="1bb28-101">Get-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="1bb28-101">Get-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="1bb28-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1bb28-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb28-103">Ruft den Azure SQL Server-DNS-Alias ab oder listet ihn auf.</span><span class="sxs-lookup"><span data-stu-id="1bb28-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bb28-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bb28-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bb28-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1bb28-105">DESCRIPTION</span></span>
<span data-ttu-id="1bb28-106">Abrufen des bestimmten Azure SQL Server-DNS-Alias oder Auflisten aller Server-DNS-Aliase für den Server</span><span class="sxs-lookup"><span data-stu-id="1bb28-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="1bb28-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1bb28-107">EXAMPLES</span></span>

### <span data-ttu-id="1bb28-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1bb28-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzureRmSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="1bb28-109">Listet alle Server-DNS-Aliase für den jeweiligen Server auf</span><span class="sxs-lookup"><span data-stu-id="1bb28-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="1bb28-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1bb28-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzureRmSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="1bb28-111">Ruft den Server-DNS-Alias ab, der vom Server und Aliasnamen angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1bb28-111">Gets Server DNS Alias specified by server and alias name</span></span>

## <span data-ttu-id="1bb28-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bb28-112">PARAMETERS</span></span>

### <span data-ttu-id="1bb28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bb28-113">-DefaultProfile</span></span>
<span data-ttu-id="1bb28-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1bb28-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb28-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1bb28-115">-Name</span></span>
<span data-ttu-id="1bb28-116">Der Azure SQL Server-DNS-Alias Name.</span><span class="sxs-lookup"><span data-stu-id="1bb28-116">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb28-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bb28-117">-ResourceGroupName</span></span>
<span data-ttu-id="1bb28-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1bb28-118">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb28-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="1bb28-119">-ServerName</span></span>
<span data-ttu-id="1bb28-120">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="1bb28-120">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb28-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1bb28-121">-Confirm</span></span>
<span data-ttu-id="1bb28-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1bb28-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb28-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bb28-123">-WhatIf</span></span>
<span data-ttu-id="1bb28-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1bb28-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bb28-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1bb28-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb28-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb28-126">CommonParameters</span></span>
<span data-ttu-id="1bb28-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bb28-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb28-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bb28-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb28-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1bb28-129">INPUTS</span></span>

### <span data-ttu-id="1bb28-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1bb28-130">System.String</span></span>

## <span data-ttu-id="1bb28-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1bb28-131">OUTPUTS</span></span>

### <span data-ttu-id="1bb28-132">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="1bb28-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="1bb28-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="1bb28-133">NOTES</span></span>

## <span data-ttu-id="1bb28-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1bb28-134">RELATED LINKS</span></span>
