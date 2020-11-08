---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 6723557D-8052-4BFA-872C-384B1423B3AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185ad06375fe9bbd11cb25c26b25704baeaa1dfe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005776"
---
# <span data-ttu-id="5fceb-101">Get-AzureSqlDatabaseServerQuota</span><span class="sxs-lookup"><span data-stu-id="5fceb-101">Get-AzureSqlDatabaseServerQuota</span></span>

## <span data-ttu-id="5fceb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5fceb-102">SYNOPSIS</span></span>
<span data-ttu-id="5fceb-103">Ruft Kontingentinformationen für einen Azure SQL-Datenbankserver ab.</span><span class="sxs-lookup"><span data-stu-id="5fceb-103">Gets quota information for an Azure SQL Database server.</span></span>

## <span data-ttu-id="5fceb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fceb-104">SYNTAX</span></span>

### <span data-ttu-id="5fceb-105">ByConnectionContext</span><span class="sxs-lookup"><span data-stu-id="5fceb-105">ByConnectionContext</span></span>
```
Get-AzureSqlDatabaseServerQuota -ConnectionContext <IServerDataServiceContext> [-QuotaName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5fceb-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="5fceb-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseServerQuota -ServerName <String> [-QuotaName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5fceb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5fceb-107">DESCRIPTION</span></span>
<span data-ttu-id="5fceb-108">Das Cmdlet " **Get-AzureSqlDatabaseServerQuota** " Ruft die Kontingentinformationen für eine angegebene Instanz des Azure SQL-Datenbankservers ab.</span><span class="sxs-lookup"><span data-stu-id="5fceb-108">The **Get-AzureSqlDatabaseServerQuota** cmdlet gets the quota information for a specified instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="5fceb-109">Geben Sie einen Verbindungskontext oder den Servernamen an.</span><span class="sxs-lookup"><span data-stu-id="5fceb-109">Specify a connection context or the server name.</span></span>
<span data-ttu-id="5fceb-110">Wenn Sie keinen Kontingent Namen angeben, ruft dieses Cmdlet alle Kontingentinformationen für den Server ab.</span><span class="sxs-lookup"><span data-stu-id="5fceb-110">If you do not specify a quota name, this cmdlet gets all the quota information for the server.</span></span>

## <span data-ttu-id="5fceb-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5fceb-111">EXAMPLES</span></span>

### <span data-ttu-id="5fceb-112">Beispiel 1: Abrufen von Informationen zu einem bestimmten Kontingent</span><span class="sxs-lookup"><span data-stu-id="5fceb-112">Example 1: Get information for a specific quota</span></span>
```
PS C:\> $QuotaPremium = GetAzureSqlDatabaseServerQuota $Context -QuotaName "Premium_Databases"
```

<span data-ttu-id="5fceb-113">Dieser Befehl ruft das Kontingent mit dem Namen Premium_Databases aus dem Azure SQL-Datenbankserver ab, der durch die in der $Context-Variable gespeicherte Verbindung angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5fceb-113">This command gets the quota named Premium_Databases from the Azure SQL Database server specified by the connection stored in the $Context variable.</span></span>

### <span data-ttu-id="5fceb-114">Beispiel 2: Abrufen von Informationen für alle Kontingente</span><span class="sxs-lookup"><span data-stu-id="5fceb-114">Example 2: Get information for all quotas</span></span>
```
PS C:\> $QuotaList = GetAzureSqlDatabaseServerQuota $Context
```

<span data-ttu-id="5fceb-115">Dieser Befehl ruft alle Kontingentwerte vom Server ab, der durch die Verbindungs $Context angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5fceb-115">This command gets all quota values from the server specified by the connection $Context.</span></span>

## <span data-ttu-id="5fceb-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="5fceb-116">PARAMETERS</span></span>

### <span data-ttu-id="5fceb-117">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="5fceb-117">-ConnectionContext</span></span>
<span data-ttu-id="5fceb-118">Gibt den Verbindungskontext eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="5fceb-118">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5fceb-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="5fceb-119">-Profile</span></span>
<span data-ttu-id="5fceb-120">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="5fceb-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5fceb-121">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="5fceb-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5fceb-122">-Kontingentname</span><span class="sxs-lookup"><span data-stu-id="5fceb-122">-QuotaName</span></span>
<span data-ttu-id="5fceb-123">Gibt den Namen des Kontingentwerts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5fceb-123">Specifies the name of the quota value that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fceb-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="5fceb-124">-ServerName</span></span>
<span data-ttu-id="5fceb-125">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="5fceb-125">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fceb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fceb-126">CommonParameters</span></span>
<span data-ttu-id="5fceb-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fceb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fceb-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fceb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fceb-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5fceb-129">INPUTS</span></span>

## <span data-ttu-id="5fceb-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5fceb-130">OUTPUTS</span></span>

### <span data-ttu-id="5fceb-131">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. ServerQuota []</span><span class="sxs-lookup"><span data-stu-id="5fceb-131">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServerQuota[]</span></span>

## <span data-ttu-id="5fceb-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="5fceb-132">NOTES</span></span>
* <span data-ttu-id="5fceb-133">Authentifizierung: Dieses Cmdlet kann entweder die SQL Server-Authentifizierung oder die zertifikatbasierte Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="5fceb-133">Authentication: This cmdlet can use either SQL Server authentication or certificate-based authentication.</span></span> <span data-ttu-id="5fceb-134">Beispiele für das Einrichten der Authentifizierung finden Sie unter New-AzureSqlDatabaseServerContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fceb-134">For examples of setting up authentication, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="5fceb-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5fceb-135">RELATED LINKS</span></span>

[<span data-ttu-id="5fceb-136">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="5fceb-136">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="5fceb-137">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="5fceb-137">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="5fceb-138">Neu – AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="5fceb-138">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


