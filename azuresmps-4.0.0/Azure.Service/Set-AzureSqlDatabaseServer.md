---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B5A2F2A8-5D20-47E4-AFC5-44F687142A08
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e40d833125725f0ae1baff920a283112db24cdc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006070"
---
# <span data-ttu-id="b4899-101">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="b4899-101">Set-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="b4899-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4899-102">SYNOPSIS</span></span>
<span data-ttu-id="b4899-103">Ändert die Eigenschaften eines Azure SQL-Datenbankservers.</span><span class="sxs-lookup"><span data-stu-id="b4899-103">Modifies the properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="b4899-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4899-104">SYNTAX</span></span>

```
Set-AzureSqlDatabaseServer -ServerName <String> -AdminPassword <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4899-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4899-105">DESCRIPTION</span></span>
<span data-ttu-id="b4899-106">Das Cmdlet " **Satz-AzureSqlDatabaseServer** " ändert die Eigenschaften der angegebenen Instanz des Azure SQL-Datenbankservers.</span><span class="sxs-lookup"><span data-stu-id="b4899-106">The **Set-AzureSqlDatabaseServer** cmdlet modifies the properties of the specified instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="b4899-107">In der aktuellen Version können Sie nur das Kennwort für das Administratorkonto für einen Server aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b4899-107">In the current release, you can only update the administrator account password for a server.</span></span>

## <span data-ttu-id="b4899-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4899-108">EXAMPLES</span></span>

### <span data-ttu-id="b4899-109">Beispiel 1: Ändern des Kennworts für einen Server</span><span class="sxs-lookup"><span data-stu-id="b4899-109">Example 1: Change the password for a server</span></span>
```
PS C:\>Set-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y" -AdminPassword "NewPassword"
```

<span data-ttu-id="b4899-110">Mit diesem Befehl wird das Kennwort des Administratorkontos für den Azure SQL-Datenbankserver mit dem Namen lpqd0zbr8y geändert.</span><span class="sxs-lookup"><span data-stu-id="b4899-110">This command changes the administrator account password for the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="b4899-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4899-111">PARAMETERS</span></span>

### <span data-ttu-id="b4899-112">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="b4899-112">-AdminPassword</span></span>
<span data-ttu-id="b4899-113">Gibt das Kennwort des Administratorkontos für den Azure SQL-Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="b4899-113">Specifies the administrator account password for the Azure SQL Database server.</span></span>
<span data-ttu-id="b4899-114">Sie müssen ein sicheres Kennwort angeben.</span><span class="sxs-lookup"><span data-stu-id="b4899-114">You must specify a strong password.</span></span>
<span data-ttu-id="b4899-115">Weitere Informationen finden Sie unter [sichere Kennwörter](https://go.microsoft.com/fwlink/p/?LinkId=154152) ( https://go.microsoft.com/fwlink/p/?LinkId=154152) im Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="b4899-115">For more information, see [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152) (https://go.microsoft.com/fwlink/p/?LinkId=154152) at the Microsoft Developer Network.</span></span>

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

### <span data-ttu-id="b4899-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b4899-116">-Force</span></span>
<span data-ttu-id="b4899-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="b4899-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4899-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="b4899-118">-Profile</span></span>
<span data-ttu-id="b4899-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b4899-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b4899-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b4899-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b4899-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="b4899-121">-ServerName</span></span>
<span data-ttu-id="b4899-122">Gibt den Namen des Servers an, der vom Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="b4899-122">Specifies the name of the server that this cmdlet modifies.</span></span>
<span data-ttu-id="b4899-123">Geben Sie den Servernamen und nicht den vollqualifizierten DNS-Namen an.</span><span class="sxs-lookup"><span data-stu-id="b4899-123">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="b4899-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b4899-124">-Confirm</span></span>
<span data-ttu-id="b4899-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4899-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4899-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4899-126">-WhatIf</span></span>
<span data-ttu-id="b4899-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4899-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4899-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4899-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4899-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4899-129">CommonParameters</span></span>
<span data-ttu-id="b4899-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4899-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4899-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4899-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4899-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4899-132">INPUTS</span></span>

### <span data-ttu-id="b4899-133">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="b4899-133">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="b4899-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4899-134">OUTPUTS</span></span>

## <span data-ttu-id="b4899-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4899-135">NOTES</span></span>

## <span data-ttu-id="b4899-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4899-136">RELATED LINKS</span></span>

[<span data-ttu-id="b4899-137">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="b4899-137">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="b4899-138">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="b4899-138">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="b4899-139">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="b4899-139">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="b4899-140">Neu – AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="b4899-140">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="b4899-141">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="b4899-141">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)


