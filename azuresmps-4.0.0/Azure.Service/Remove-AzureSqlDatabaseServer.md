---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F73A078E-F9F2-4520-BF55-DFFE82BE4466
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a8127a77ecfdc5aa36659060cb5469206a9988d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006313"
---
# <span data-ttu-id="75853-101">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="75853-101">Remove-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="75853-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75853-102">SYNOPSIS</span></span>
<span data-ttu-id="75853-103">Entfernt einen Azure SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="75853-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="75853-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75853-104">SYNTAX</span></span>

```
Remove-AzureSqlDatabaseServer -ServerName <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75853-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75853-105">DESCRIPTION</span></span>
<span data-ttu-id="75853-106">Das Cmdlet **Remove-AzureSqlDatabaseServer** entfernt die angegebene Instanz des Azure SQL-Datenbankservers aus dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="75853-106">The **Remove-AzureSqlDatabaseServer** cmdlet removes the specified instance of Azure SQL Database Server from the current subscription.</span></span>
<span data-ttu-id="75853-107">Mit diesem Cmdlet werden alle Datenbanken auf dem Server gelöscht.</span><span class="sxs-lookup"><span data-stu-id="75853-107">This cmdlet deletes all databases on the server.</span></span>

## <span data-ttu-id="75853-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75853-108">EXAMPLES</span></span>

### <span data-ttu-id="75853-109">Beispiel 1: Entfernen eines Datenbankservers</span><span class="sxs-lookup"><span data-stu-id="75853-109">Example 1: Remove a database server</span></span>
```
PS C:\>Remove-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="75853-110">Dieser Befehl entfernt den Azure SQL-Datenbankserver mit dem Namen lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="75853-110">This command removes the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="75853-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="75853-111">PARAMETERS</span></span>

### <span data-ttu-id="75853-112">-Force</span><span class="sxs-lookup"><span data-stu-id="75853-112">-Force</span></span>
<span data-ttu-id="75853-113">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="75853-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75853-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="75853-114">-Profile</span></span>
<span data-ttu-id="75853-115">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="75853-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="75853-116">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="75853-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="75853-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="75853-117">-ServerName</span></span>
<span data-ttu-id="75853-118">Gibt den Namen des Servers an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="75853-118">Specifies the name of the server that this cmdlet removes.</span></span>
<span data-ttu-id="75853-119">Geben Sie den Servernamen und nicht den vollqualifizierten DNS-Namen an.</span><span class="sxs-lookup"><span data-stu-id="75853-119">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75853-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="75853-120">-Confirm</span></span>
<span data-ttu-id="75853-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75853-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75853-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75853-122">-WhatIf</span></span>
<span data-ttu-id="75853-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75853-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75853-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75853-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75853-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75853-125">CommonParameters</span></span>
<span data-ttu-id="75853-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75853-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75853-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75853-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75853-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75853-128">INPUTS</span></span>

### <span data-ttu-id="75853-129">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="75853-129">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="75853-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75853-130">OUTPUTS</span></span>

## <span data-ttu-id="75853-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="75853-131">NOTES</span></span>

## <span data-ttu-id="75853-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75853-132">RELATED LINKS</span></span>

[<span data-ttu-id="75853-133">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="75853-133">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="75853-134">Server löschen</span><span class="sxs-lookup"><span data-stu-id="75853-134">Delete Server</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505695.aspx)

[<span data-ttu-id="75853-135">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="75853-135">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="75853-136">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="75853-136">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="75853-137">Neu – AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="75853-137">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="75853-138">Satz-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="75853-138">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


