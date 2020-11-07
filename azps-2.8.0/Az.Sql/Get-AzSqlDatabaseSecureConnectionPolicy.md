---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F22E14D6-B18B-4136-B1DF-710DA34372C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesecureconnectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
ms.openlocfilehash: d160e6cf954240495a9f9b3969d87dab6d880e54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825636"
---
# <span data-ttu-id="a7c31-101">Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7c31-101">Get-AzSqlDatabaseSecureConnectionPolicy</span></span>

## <span data-ttu-id="a7c31-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a7c31-102">SYNOPSIS</span></span>
<span data-ttu-id="a7c31-103">Ruft die sichere Verbindungsrichtlinie für eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="a7c31-103">Gets the secure connection policy for a database.</span></span> <span data-ttu-id="a7c31-104">Sichere Verbindung ist veraltet, und dieser Befehl wird in einer zukünftigen Version entfernt.</span><span class="sxs-lookup"><span data-stu-id="a7c31-104">Secure connection is deprecated and this command will be removed in a future release.</span></span> <span data-ttu-id="a7c31-105">Verwenden Sie das SQL-Datenbank-Blade im Azure-Portal, um die Verbindungszeichenfolgen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a7c31-105">Please use the SQL database blade in the Azure portal to view the connection strings</span></span>

## <span data-ttu-id="a7c31-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7c31-106">SYNTAX</span></span>

```
Get-AzSqlDatabaseSecureConnectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7c31-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7c31-107">DESCRIPTION</span></span>
<span data-ttu-id="a7c31-108">Das Cmdlet " **Get-AzSqlDatabaseSecureConnectionPolicy** " Ruft die verschlüsselte Kanal Richtlinie einer Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="a7c31-108">The **Get-AzSqlDatabaseSecureConnectionPolicy** cmdlet gets the encrypted channel policy of an Azure SQL database.</span></span>
<span data-ttu-id="a7c31-109">Um das Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a7c31-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="a7c31-110">Nachdem dieses Cmdlet erfolgreich ausgeführt wurde, gibt es ein Objekt zurück, das die aktuelle verschlüsselte Kanal Richtlinie und auch die Datenbankbezeichner beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a7c31-110">After this cmdlet runs successfully, it returns an object that describes the current encrypted channel policy and also the database identifiers.</span></span>
<span data-ttu-id="a7c31-111">Zu den Datenbankbezeichnern gehören **ResourceGroupName** , **Servername** und **DatabaseName** , sind aber nicht darauf limitiert.</span><span class="sxs-lookup"><span data-stu-id="a7c31-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="a7c31-112">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a7c31-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a7c31-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7c31-113">EXAMPLES</span></span>

### <span data-ttu-id="a7c31-114">Beispiel 1: Abrufen der verschlüsselten Kanal Richtlinie einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="a7c31-114">Example 1: Get the encrypted channel policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseSecureConnectionPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database01"
DatabaseName          : database01
ConnectionStrings     : Microsoft.Azure.Commands.Sql.SecureConnection.Model.ConnectionStrings
ResourceGroupName     : resourcegroup01
ServerName            : server01
ProxyDnsName          : server01.database.secure.windows.net
ProxyPort             : 1433
SecureConnectionState : Optional
```

<span data-ttu-id="a7c31-115">Dieser Befehl ruft die verschlüsselte Kanal Richtlinie einer Azure SQL-Datenbank mit dem Namen database01 ab, die sich auf dem Server Server01 befindet.</span><span class="sxs-lookup"><span data-stu-id="a7c31-115">This command gets the encrypted channel policy of an Azure SQL database named database01 located on server server01.</span></span>

## <span data-ttu-id="a7c31-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7c31-116">PARAMETERS</span></span>

### <span data-ttu-id="a7c31-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a7c31-117">-DatabaseName</span></span>
<span data-ttu-id="a7c31-118">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="a7c31-118">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7c31-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7c31-119">-DefaultProfile</span></span>
<span data-ttu-id="a7c31-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a7c31-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7c31-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7c31-121">-ResourceGroupName</span></span>
<span data-ttu-id="a7c31-122">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="a7c31-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a7c31-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="a7c31-123">-ServerName</span></span>
<span data-ttu-id="a7c31-124">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="a7c31-124">Specifies the name of server that hosts the database.</span></span>

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

### <span data-ttu-id="a7c31-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a7c31-125">-Confirm</span></span>
<span data-ttu-id="a7c31-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a7c31-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7c31-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7c31-127">-WhatIf</span></span>
<span data-ttu-id="a7c31-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a7c31-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7c31-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7c31-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7c31-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7c31-130">CommonParameters</span></span>
<span data-ttu-id="a7c31-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7c31-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7c31-132">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7c31-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7c31-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a7c31-133">INPUTS</span></span>

### <span data-ttu-id="a7c31-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a7c31-134">System.String</span></span>

## <span data-ttu-id="a7c31-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a7c31-135">OUTPUTS</span></span>

### <span data-ttu-id="a7c31-136">Microsoft. Azure. Commands. SQL. SecureConnection. Model. DatabaseSecureConnectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a7c31-136">Microsoft.Azure.Commands.Sql.SecureConnection.Model.DatabaseSecureConnectionPolicyModel</span></span>

## <span data-ttu-id="a7c31-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7c31-137">NOTES</span></span>

## <span data-ttu-id="a7c31-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a7c31-138">RELATED LINKS</span></span>
