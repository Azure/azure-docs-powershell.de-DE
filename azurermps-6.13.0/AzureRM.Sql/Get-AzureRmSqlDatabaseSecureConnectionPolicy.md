---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F22E14D6-B18B-4136-B1DF-710DA34372C3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasesecureconnectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseSecureConnectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseSecureConnectionPolicy.md
ms.openlocfilehash: 92b75e55adb4e1107767c3c58394c9f344a5bd3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663640"
---
# <span data-ttu-id="fec20-101">Get-AzureRmSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fec20-101">Get-AzureRmSqlDatabaseSecureConnectionPolicy</span></span>

## <span data-ttu-id="fec20-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fec20-102">SYNOPSIS</span></span>
<span data-ttu-id="fec20-103">Ruft die sichere Verbindungsrichtlinie für eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="fec20-103">Gets the secure connection policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fec20-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fec20-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseSecureConnectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fec20-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fec20-105">DESCRIPTION</span></span>
<span data-ttu-id="fec20-106">Das Cmdlet " **Get-AzureRmSqlDatabaseSecureConnectionPolicy** " Ruft die verschlüsselte Kanal Richtlinie einer Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="fec20-106">The **Get-AzureRmSqlDatabaseSecureConnectionPolicy** cmdlet gets the encrypted channel policy of an Azure SQL database.</span></span>
<span data-ttu-id="fec20-107">Um das Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fec20-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="fec20-108">Nachdem dieses Cmdlet erfolgreich ausgeführt wurde, gibt es ein Objekt zurück, das die aktuelle verschlüsselte Kanal Richtlinie und auch die Datenbankbezeichner beschreibt.</span><span class="sxs-lookup"><span data-stu-id="fec20-108">After this cmdlet runs successfully, it returns an object that describes the current encrypted channel policy and also the database identifiers.</span></span>
<span data-ttu-id="fec20-109">Zu den Datenbankbezeichnern gehören **ResourceGroupName** , **Servername** und **DatabaseName** , sind aber nicht darauf limitiert.</span><span class="sxs-lookup"><span data-stu-id="fec20-109">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="fec20-110">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fec20-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="fec20-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fec20-111">EXAMPLES</span></span>

### <span data-ttu-id="fec20-112">Beispiel 1: Abrufen der verschlüsselten Kanal Richtlinie einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="fec20-112">Example 1: Get the encrypted channel policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseSecureConnectionPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database01"
DatabaseName          : database01
ConnectionStrings     : Microsoft.Azure.Commands.Sql.SecureConnection.Model.ConnectionStrings
ResourceGroupName     : resourcegroup01
ServerName            : server01
ProxyDnsName          : server01.database.secure.windows.net
ProxyPort             : 1433
SecureConnectionState : Optional
```

<span data-ttu-id="fec20-113">Dieser Befehl ruft die verschlüsselte Kanal Richtlinie einer Azure SQL-Datenbank mit dem Namen database01 ab, die sich auf dem Server Server01 befindet.</span><span class="sxs-lookup"><span data-stu-id="fec20-113">This command gets the encrypted channel policy of an Azure SQL database named database01 located on server server01.</span></span>

## <span data-ttu-id="fec20-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="fec20-114">PARAMETERS</span></span>

### <span data-ttu-id="fec20-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fec20-115">-DatabaseName</span></span>
<span data-ttu-id="fec20-116">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="fec20-116">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="fec20-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fec20-117">-DefaultProfile</span></span>
<span data-ttu-id="fec20-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="fec20-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fec20-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fec20-119">-ResourceGroupName</span></span>
<span data-ttu-id="fec20-120">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="fec20-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="fec20-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="fec20-121">-ServerName</span></span>
<span data-ttu-id="fec20-122">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="fec20-122">Specifies the name of server that hosts the database.</span></span>

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

### <span data-ttu-id="fec20-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fec20-123">-Confirm</span></span>
<span data-ttu-id="fec20-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fec20-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fec20-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fec20-125">-WhatIf</span></span>
<span data-ttu-id="fec20-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fec20-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fec20-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fec20-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fec20-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fec20-128">CommonParameters</span></span>
<span data-ttu-id="fec20-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fec20-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fec20-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fec20-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fec20-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fec20-131">INPUTS</span></span>

### <span data-ttu-id="fec20-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fec20-132">System.String</span></span>

## <span data-ttu-id="fec20-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fec20-133">OUTPUTS</span></span>

### <span data-ttu-id="fec20-134">Microsoft. Azure. Commands. SQL. SecureConnection. Model. DatabaseSecureConnectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="fec20-134">Microsoft.Azure.Commands.Sql.SecureConnection.Model.DatabaseSecureConnectionPolicyModel</span></span>

## <span data-ttu-id="fec20-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="fec20-135">NOTES</span></span>

## <span data-ttu-id="fec20-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fec20-136">RELATED LINKS</span></span>
