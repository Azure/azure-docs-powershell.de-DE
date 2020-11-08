---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 83E8DAD8-151A-408D-819F-274CB813ABDA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6f9a5753fdf4f87afc6baacbe9fc4c33c9be08ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006765"
---
# <span data-ttu-id="5265f-101">Get-AzureSqlRecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="5265f-101">Get-AzureSqlRecoverableDatabase</span></span>

## <span data-ttu-id="5265f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5265f-102">SYNOPSIS</span></span>
<span data-ttu-id="5265f-103">Ruft wiederherstellbare Datenbanken von einem angegebenen Server ab.</span><span class="sxs-lookup"><span data-stu-id="5265f-103">Gets recoverable databases from a specified server.</span></span>

## <span data-ttu-id="5265f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5265f-104">SYNTAX</span></span>

### <span data-ttu-id="5265f-105">AllDatabasesOnGivenServer (Standard)</span><span class="sxs-lookup"><span data-stu-id="5265f-105">AllDatabasesOnGivenServer (Default)</span></span>
```
Get-AzureSqlRecoverableDatabase -ServerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5265f-106">GivenDatabaseOnGivenServer</span><span class="sxs-lookup"><span data-stu-id="5265f-106">GivenDatabaseOnGivenServer</span></span>
```
Get-AzureSqlRecoverableDatabase -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="5265f-107">GivenDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="5265f-107">GivenDatabaseObject</span></span>
```
Get-AzureSqlRecoverableDatabase -Database <RecoverableDatabase> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5265f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5265f-108">DESCRIPTION</span></span>
<span data-ttu-id="5265f-109">Das Cmdlet " **Get-AzureSqlRecoverableDatabase** " ruft wiederherstellbare Datenbanken von einem angegebenen Server ab.</span><span class="sxs-lookup"><span data-stu-id="5265f-109">The **Get-AzureSqlRecoverableDatabase** cmdlet gets recoverable databases from a specified server.</span></span>
<span data-ttu-id="5265f-110">Dieses Cmdlet ruft eine bestimmte wiederherstellbare Datenbank oder alle wiederherstellbaren Datenbanken auf einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="5265f-110">This cmdlet gets a specific recoverable database or all recoverable databases on a server.</span></span>

## <span data-ttu-id="5265f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5265f-111">EXAMPLES</span></span>

### <span data-ttu-id="5265f-112">Beispiel 1: Abrufen aller wiederherstellbaren Datenbanken</span><span class="sxs-lookup"><span data-stu-id="5265f-112">Example 1: Get all recoverable databases</span></span>
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01"
```

<span data-ttu-id="5265f-113">Dieser Befehl ruft alle wiederherstellbaren Datenbanken auf dem Server mit dem Namen SERVER01 ab.</span><span class="sxs-lookup"><span data-stu-id="5265f-113">This command gets all recoverable databases on the server named Server01.</span></span>

### <span data-ttu-id="5265f-114">Beispiel 2: Abrufen einer bestimmten wiederherstellbaren Datenbank</span><span class="sxs-lookup"><span data-stu-id="5265f-114">Example 2: Get a specific recoverable database</span></span>
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17"
```

<span data-ttu-id="5265f-115">Dieser Befehl ruft die Datenbank mit dem Namen Database17 auf dem Server mit dem Namen SERVER01 ab.</span><span class="sxs-lookup"><span data-stu-id="5265f-115">This command gets retrieves the database named Database17 on the server named Server01.</span></span>

## <span data-ttu-id="5265f-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="5265f-116">PARAMETERS</span></span>

### <span data-ttu-id="5265f-117">-Datenbank</span><span class="sxs-lookup"><span data-stu-id="5265f-117">-Database</span></span>
<span data-ttu-id="5265f-118">Gibt ein Objekt an, das die wiederherstellbare Datenbank darstellt, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5265f-118">Specifies an object that represents the recoverable database that this cmdlet gets.</span></span>

```yaml
Type: RecoverableDatabase
Parameter Sets: GivenDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5265f-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5265f-119">-DatabaseName</span></span>
<span data-ttu-id="5265f-120">Gibt den Namen der wiederherstellbaren Datenbank an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5265f-120">Specifies the name of the recoverable database that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GivenDatabaseOnGivenServer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5265f-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="5265f-121">-Profile</span></span>
<span data-ttu-id="5265f-122">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="5265f-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5265f-123">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="5265f-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5265f-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="5265f-124">-ServerName</span></span>
<span data-ttu-id="5265f-125">Gibt den Namen des Servers an, von dem dieses Cmdlet wiederherstellbare Datenbanken erhält.</span><span class="sxs-lookup"><span data-stu-id="5265f-125">Specifies the name of the server from which this cmdlet gets recoverable databases.</span></span>

```yaml
Type: String
Parameter Sets: AllDatabasesOnGivenServer, GivenDatabaseOnGivenServer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5265f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5265f-126">CommonParameters</span></span>
<span data-ttu-id="5265f-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5265f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5265f-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5265f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5265f-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5265f-129">INPUTS</span></span>

### <span data-ttu-id="5265f-130">Microsoft. WindowsAzure. Management. SQL. Models. RecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="5265f-130">Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase</span></span>

## <span data-ttu-id="5265f-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5265f-131">OUTPUTS</span></span>

### <span data-ttu-id="5265f-132">IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\></span><span class="sxs-lookup"><span data-stu-id="5265f-132">IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\></span></span>

## <span data-ttu-id="5265f-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="5265f-133">NOTES</span></span>
* <span data-ttu-id="5265f-134">Sie müssen dieses Cmdlet mithilfe der zertifikatbasierten Authentifizierung ausführen.</span><span class="sxs-lookup"><span data-stu-id="5265f-134">You must use certificate-based authentication to run this cmdlet.</span></span> <span data-ttu-id="5265f-135">Führen Sie die folgenden Befehle auf dem Computer aus, auf dem dieses Cmdlet ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="5265f-135">Run the following commands on the computer where run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="5265f-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5265f-136">RELATED LINKS</span></span>

[<span data-ttu-id="5265f-137">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="5265f-137">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="5265f-138">Abrufen einer wiederherstellbaren Datenbank</span><span class="sxs-lookup"><span data-stu-id="5265f-138">Get Recoverable Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn800985.aspx)

[<span data-ttu-id="5265f-139">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="5265f-139">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="5265f-140">Anfang-AzureSqlDatabaseRecovery</span><span class="sxs-lookup"><span data-stu-id="5265f-140">Start-AzureSqlDatabaseRecovery</span></span>](./Start-AzureSqlDatabaseRecovery.md)


