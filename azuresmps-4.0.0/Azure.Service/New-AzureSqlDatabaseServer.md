---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A0C674FC-A1D8-4068-8CAB-2EE0AECB8E68
online version: ''
schema: 2.0.0
ms.openlocfilehash: 069b96809c0659028135e8c9a28e7e3c0ab8b3ae
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006177"
---
# <span data-ttu-id="f52a7-101">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="f52a7-101">New-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="f52a7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f52a7-102">SYNOPSIS</span></span>
<span data-ttu-id="f52a7-103">Erstellt einen Azure SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="f52a7-103">Creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="f52a7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f52a7-104">SYNTAX</span></span>

```
New-AzureSqlDatabaseServer -AdministratorLogin <String> -AdministratorLoginPassword <String> -Location <String>
 [-Version <Single>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f52a7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f52a7-105">DESCRIPTION</span></span>
<span data-ttu-id="f52a7-106">Das Cmdlet **New-AzureSqlDatabaseServer** erstellt eine Instanz des Azure SQL-Datenbankservers im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f52a7-106">The **New-AzureSqlDatabaseServer** cmdlet creates an instance of Azure SQL Database Server in the current subscription.</span></span>

## <span data-ttu-id="f52a7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f52a7-107">EXAMPLES</span></span>

### <span data-ttu-id="f52a7-108">Beispiel 1: Erstellen eines Servers</span><span class="sxs-lookup"><span data-stu-id="f52a7-108">Example 1: Create a server</span></span>
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword"
```

<span data-ttu-id="f52a7-109">Mit diesem Befehl wird ein Azure SQL-Datenbankserver der Version 11 erstellt.</span><span class="sxs-lookup"><span data-stu-id="f52a7-109">This command creates a version 11 Azure SQL Database server.</span></span>

### <span data-ttu-id="f52a7-110">Beispiel 2: Erstellen eines Servers der Version 12</span><span class="sxs-lookup"><span data-stu-id="f52a7-110">Example 2: Create a version 12 server</span></span>
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword" -Version "12.0"
```

<span data-ttu-id="f52a7-111">Dieser Befehl erstellt einen Server der Version 12.</span><span class="sxs-lookup"><span data-stu-id="f52a7-111">This command creates a version 12 server.</span></span>

## <span data-ttu-id="f52a7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f52a7-112">PARAMETERS</span></span>

### <span data-ttu-id="f52a7-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="f52a7-113">-AdministratorLogin</span></span>
<span data-ttu-id="f52a7-114">Gibt den Namen des Administratorkontos für den neuen Azure SQL-Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="f52a7-114">Specifies the administrator account name for the new Azure SQL Database server.</span></span>

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

### <span data-ttu-id="f52a7-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="f52a7-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="f52a7-116">Gibt das Kennwort des Administratorkontos für den Azure SQL-Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="f52a7-116">Specifies the administrator account password for the Azure SQL Database server.</span></span>
<span data-ttu-id="f52a7-117">Sie müssen ein sicheres Kennwort angeben.</span><span class="sxs-lookup"><span data-stu-id="f52a7-117">You must specify a strong password.</span></span>
<span data-ttu-id="f52a7-118">Weitere Informationen finden Sie unter [sichere Kennwörter](https://go.microsoft.com/fwlink/p/?LinkId=154152) ( https://go.microsoft.com/fwlink/p/?LinkId=154152) im Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="f52a7-118">For more information, see [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152) (https://go.microsoft.com/fwlink/p/?LinkId=154152) at the Microsoft Developer Network.</span></span>

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

### <span data-ttu-id="f52a7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f52a7-119">-Force</span></span>
<span data-ttu-id="f52a7-120">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f52a7-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f52a7-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="f52a7-121">-Location</span></span>
<span data-ttu-id="f52a7-122">Gibt den Speicherort des Rechenzentrums an, in dem dieses Cmdlet den Server erstellt.</span><span class="sxs-lookup"><span data-stu-id="f52a7-122">Specifies the location of the data center where this cmdlet creates the server.</span></span>
<span data-ttu-id="f52a7-123">Weitere Informationen finden Sie unter [Azure-Bereiche](https://azure.microsoft.com/regions/) ( https://azure.microsoft.com/regions/#services) in der Azure-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="f52a7-123">For more information, see [Azure Regions](https://azure.microsoft.com/regions/) (https://azure.microsoft.com/regions/#services) in the Azure library.</span></span>

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

### <span data-ttu-id="f52a7-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="f52a7-124">-Profile</span></span>
<span data-ttu-id="f52a7-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="f52a7-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f52a7-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="f52a7-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f52a7-127">-Version</span><span class="sxs-lookup"><span data-stu-id="f52a7-127">-Version</span></span>
<span data-ttu-id="f52a7-128">Gibt die Version des neuen Servers an.</span><span class="sxs-lookup"><span data-stu-id="f52a7-128">Specifies the version of the new server.</span></span>
<span data-ttu-id="f52a7-129">Gültige Werte sind: 2,0 und 12,0.</span><span class="sxs-lookup"><span data-stu-id="f52a7-129">Valid values are: 2.0 and 12.0.</span></span>

```yaml
Type: Single
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f52a7-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f52a7-130">-Confirm</span></span>
<span data-ttu-id="f52a7-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f52a7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f52a7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f52a7-132">-WhatIf</span></span>
<span data-ttu-id="f52a7-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f52a7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f52a7-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f52a7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f52a7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f52a7-135">CommonParameters</span></span>
<span data-ttu-id="f52a7-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f52a7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f52a7-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f52a7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f52a7-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f52a7-138">INPUTS</span></span>

## <span data-ttu-id="f52a7-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f52a7-139">OUTPUTS</span></span>

### <span data-ttu-id="f52a7-140">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="f52a7-140">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="f52a7-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="f52a7-141">NOTES</span></span>

## <span data-ttu-id="f52a7-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f52a7-142">RELATED LINKS</span></span>

[<span data-ttu-id="f52a7-143">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="f52a7-143">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="f52a7-144">Server erstellen</span><span class="sxs-lookup"><span data-stu-id="f52a7-144">Create Server</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505699.aspx)

[<span data-ttu-id="f52a7-145">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="f52a7-145">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="f52a7-146">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="f52a7-146">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="f52a7-147">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="f52a7-147">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)

[<span data-ttu-id="f52a7-148">Satz-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="f52a7-148">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


