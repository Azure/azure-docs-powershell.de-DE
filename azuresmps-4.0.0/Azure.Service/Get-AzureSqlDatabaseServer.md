---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 0ACEDE22-1C2B-4846-A949-710AF6C148D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d513d6d019c84984923541624063e657e2250b61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005777"
---
# <span data-ttu-id="254d2-101">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="254d2-101">Get-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="254d2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="254d2-102">SYNOPSIS</span></span>
<span data-ttu-id="254d2-103">Ruft Informationen zu Azure SQL-Datenbankservern ab.</span><span class="sxs-lookup"><span data-stu-id="254d2-103">Gets information about Azure SQL Database servers.</span></span>

## <span data-ttu-id="254d2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="254d2-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseServer [-ServerName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="254d2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="254d2-105">DESCRIPTION</span></span>
<span data-ttu-id="254d2-106">Das Cmdlet " **Get-AzureSqlDatabaseServer** " Ruft Informationen zu den Instanzen des Azure SQL-Datenbankservers im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="254d2-106">The **Get-AzureSqlDatabaseServer** cmdlet gets information about the instances of Azure SQL Database Server in the current subscription.</span></span>
<span data-ttu-id="254d2-107">Wenn Sie einen Server nach Namen angeben, gibt dieses Cmdlet ein Objekt zurück, das Informationen zu diesem Server enthält.</span><span class="sxs-lookup"><span data-stu-id="254d2-107">If you specify a server by name, this cmdlet returns an object that contains information about that server.</span></span>
<span data-ttu-id="254d2-108">Andernfalls gibt das Cmdlet Informationen zu allen Servern zurück.</span><span class="sxs-lookup"><span data-stu-id="254d2-108">Otherwise, the cmdlet returns information about all the servers.</span></span>

## <span data-ttu-id="254d2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="254d2-109">EXAMPLES</span></span>

### <span data-ttu-id="254d2-110">Beispiel 1: Abrufen von Informationen zu allen Servern</span><span class="sxs-lookup"><span data-stu-id="254d2-110">Example 1: Get information about all servers</span></span>
```
PS C:\> Get-AzureSqlDatabaseServer
```

<span data-ttu-id="254d2-111">Dieser Befehl gibt Informationen zu allen Instanzen des Azure SQL-Datenbankservers im aktuellen Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="254d2-111">This command returns information about all instances of Azure SQL Database Server in the current subscription.</span></span>

### <span data-ttu-id="254d2-112">Beispiel 2: Abrufen von Informationen zu einem bestimmten Server</span><span class="sxs-lookup"><span data-stu-id="254d2-112">Example 2: Get information about a specific server</span></span>
```
PS C:\> Get-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="254d2-113">Dieser Befehl gibt Informationen zum Server mit dem Namen lpqd0zbr8y zurück.</span><span class="sxs-lookup"><span data-stu-id="254d2-113">This command returns information about the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="254d2-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="254d2-114">PARAMETERS</span></span>

### <span data-ttu-id="254d2-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="254d2-115">-Profile</span></span>
<span data-ttu-id="254d2-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="254d2-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="254d2-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="254d2-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="254d2-118">-Servername</span><span class="sxs-lookup"><span data-stu-id="254d2-118">-ServerName</span></span>
<span data-ttu-id="254d2-119">Gibt den Namen des Servers an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="254d2-119">Specifies the name of the server that this cmdlet removes.</span></span>
<span data-ttu-id="254d2-120">Geben Sie den Servernamen und nicht den vollqualifizierten DNS-Namen an.</span><span class="sxs-lookup"><span data-stu-id="254d2-120">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="254d2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="254d2-121">CommonParameters</span></span>
<span data-ttu-id="254d2-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="254d2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="254d2-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="254d2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="254d2-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="254d2-124">INPUTS</span></span>

### <span data-ttu-id="254d2-125">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="254d2-125">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="254d2-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="254d2-126">OUTPUTS</span></span>

### <span data-ttu-id="254d2-127">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\></span><span class="sxs-lookup"><span data-stu-id="254d2-127">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\></span></span>

## <span data-ttu-id="254d2-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="254d2-128">NOTES</span></span>

## <span data-ttu-id="254d2-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="254d2-129">RELATED LINKS</span></span>

[<span data-ttu-id="254d2-130">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="254d2-130">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="254d2-131">Listenserver</span><span class="sxs-lookup"><span data-stu-id="254d2-131">List Servers</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505702.aspx)

[<span data-ttu-id="254d2-132">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="254d2-132">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="254d2-133">Neu – AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="254d2-133">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="254d2-134">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="254d2-134">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)

[<span data-ttu-id="254d2-135">Satz-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="254d2-135">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


