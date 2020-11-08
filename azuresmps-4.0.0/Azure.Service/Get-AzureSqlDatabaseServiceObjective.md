---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A2C22A8A-EF50-4BE3-82DF-5ED6F69C00CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 457775a74fb7921a3c8b6b5e635bd7df7e704faa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005774"
---
# <span data-ttu-id="43d2b-101">Get-AzureSqlDatabaseServiceObjective</span><span class="sxs-lookup"><span data-stu-id="43d2b-101">Get-AzureSqlDatabaseServiceObjective</span></span>

## <span data-ttu-id="43d2b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43d2b-102">SYNOPSIS</span></span>
<span data-ttu-id="43d2b-103">Ruft Dienst Ziele für einen Azure SQL-Datenbankserver ab.</span><span class="sxs-lookup"><span data-stu-id="43d2b-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="43d2b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43d2b-104">SYNTAX</span></span>

### <span data-ttu-id="43d2b-105">ByConnectionContext (Standard)</span><span class="sxs-lookup"><span data-stu-id="43d2b-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabaseServiceObjective -Context <IServerDataServiceContext>
 [-ServiceObjective <ServiceObjective>] [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="43d2b-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="43d2b-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseServiceObjective -ServerName <String> [-ServiceObjective <ServiceObjective>]
 [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="43d2b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43d2b-107">DESCRIPTION</span></span>
<span data-ttu-id="43d2b-108">Das Cmdlet " **Get-AzureSqlDatabaseServiceObjective** " ruft Dienst Ziele für einen Azure SQL-Datenbankserver ab.</span><span class="sxs-lookup"><span data-stu-id="43d2b-108">The **Get-AzureSqlDatabaseServiceObjective** cmdlet gets service objectives for an Azure SQL Database server.</span></span>
<span data-ttu-id="43d2b-109">Dienst Ziele werden als Leistungsstufen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="43d2b-109">Service objectives are referred to as performance levels.</span></span>
<span data-ttu-id="43d2b-110">Wenn Sie kein Dienst Ziel angeben, gibt dieses Cmdlet alle gültigen Dienst Ziele für den angegebenen Server zurück.</span><span class="sxs-lookup"><span data-stu-id="43d2b-110">If you do not specify a service objective, this cmdlet returns all valid service objectives for the specified server.</span></span>

<span data-ttu-id="43d2b-111">Dieses Cmdlet gilt für Basic-, Standard-und Premium-Dienstebenen.</span><span class="sxs-lookup"><span data-stu-id="43d2b-111">This cmdlet applies to Basic, Standard, and Premium service tiers.</span></span>

## <span data-ttu-id="43d2b-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43d2b-112">EXAMPLES</span></span>

### <span data-ttu-id="43d2b-113">Beispiel 1: Abrufen aller Dienst Ziele mithilfe eines Verbindungskontexts</span><span class="sxs-lookup"><span data-stu-id="43d2b-113">Example 1: Get all the service objectives by using a connection context</span></span>
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -Context $Context
```

<span data-ttu-id="43d2b-114">Dieser Befehl ruft alle Dienst Ziele für den Server ab, die vom Verbindungskontext $Context angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="43d2b-114">This command gets all the service objectives for the server that the connection context $Context specifies.</span></span>

### <span data-ttu-id="43d2b-115">Beispiel 2: Abrufen aller Dienst Ziele mithilfe eines Server namens</span><span class="sxs-lookup"><span data-stu-id="43d2b-115">Example 2: Get all the service objectives by using a server name</span></span>
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -ServerName "Server01"
```

<span data-ttu-id="43d2b-116">Dieser Befehl ruft alle Dienst Ziele für den Server mit dem Namen SERVER01 ab.</span><span class="sxs-lookup"><span data-stu-id="43d2b-116">This command gets all the service objectives for the server named Server01.</span></span>

## <span data-ttu-id="43d2b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="43d2b-117">PARAMETERS</span></span>

### <span data-ttu-id="43d2b-118">-Context</span><span class="sxs-lookup"><span data-stu-id="43d2b-118">-Context</span></span>
<span data-ttu-id="43d2b-119">Gibt den Verbindungskontext eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="43d2b-119">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43d2b-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="43d2b-120">-Profile</span></span>
<span data-ttu-id="43d2b-121">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="43d2b-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="43d2b-122">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="43d2b-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="43d2b-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="43d2b-123">-ServerName</span></span>
<span data-ttu-id="43d2b-124">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="43d2b-124">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="43d2b-125">-ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="43d2b-125">-ServiceObjective</span></span>
<span data-ttu-id="43d2b-126">Gibt ein Objekt an, das das Dienst Ziel darstellt, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="43d2b-126">Specifies an object that represents the service objective that this cmdlet gets.</span></span>
<span data-ttu-id="43d2b-127">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="43d2b-127">Valid values are:</span></span> 

- <span data-ttu-id="43d2b-128">Standard: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span><span class="sxs-lookup"><span data-stu-id="43d2b-128">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span></span>
- <span data-ttu-id="43d2b-129">Standard (S0): f1173c43-91bd-4AAA-973c-54e79e15235b</span><span class="sxs-lookup"><span data-stu-id="43d2b-129">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span></span>
- <span data-ttu-id="43d2b-130">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span><span class="sxs-lookup"><span data-stu-id="43d2b-130">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span></span>
- <span data-ttu-id="43d2b-131">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span><span class="sxs-lookup"><span data-stu-id="43d2b-131">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span></span>
- <span data-ttu-id="43d2b-132">\* Standard (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40</span><span class="sxs-lookup"><span data-stu-id="43d2b-132">\*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span></span>
- <span data-ttu-id="43d2b-133">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="43d2b-133">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="43d2b-134">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="43d2b-134">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="43d2b-135">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span><span class="sxs-lookup"><span data-stu-id="43d2b-135">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span></span>
- <span data-ttu-id="43d2b-136">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="43d2b-136">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="43d2b-137">\* Standard (S3) ist Teil des neuesten SQL-Datenbankupdates V12 (Preview).</span><span class="sxs-lookup"><span data-stu-id="43d2b-137">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="43d2b-138">Weitere Informationen finden Sie unter [Neuerungen in der Azure SQL Database V12 Preview](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) ( `https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/` ) in der Azure-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="43d2b-138">For more information, see [What's New in the Azure SQL Database V12 Preview](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) (`https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/`) in the Azure library.</span></span>

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43d2b-139">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="43d2b-139">-ServiceObjectiveName</span></span>
<span data-ttu-id="43d2b-140">Gibt den Namen des abzurufenden Dienst Ziels an.</span><span class="sxs-lookup"><span data-stu-id="43d2b-140">Specifies the name of a service objective to get.</span></span>
<span data-ttu-id="43d2b-141">Gültige Werte sind: Basic, S0, S1, S2, S3, P1, P2 und P3.</span><span class="sxs-lookup"><span data-stu-id="43d2b-141">Valid values are: Basic, S0, S1, S2, S3, P1, P2, and P3.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d2b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d2b-142">CommonParameters</span></span>
<span data-ttu-id="43d2b-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43d2b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d2b-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43d2b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d2b-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43d2b-145">INPUTS</span></span>

### <span data-ttu-id="43d2b-146">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="43d2b-146">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective</span></span>

## <span data-ttu-id="43d2b-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43d2b-147">OUTPUTS</span></span>

### <span data-ttu-id="43d2b-148">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\></span><span class="sxs-lookup"><span data-stu-id="43d2b-148">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\></span></span>

## <span data-ttu-id="43d2b-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="43d2b-149">NOTES</span></span>

## <span data-ttu-id="43d2b-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43d2b-150">RELATED LINKS</span></span>

[<span data-ttu-id="43d2b-151">Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="43d2b-151">Azure SQL Database</span></span>](https://msdn.microsoft.com/library/ee336279.aspx)

[<span data-ttu-id="43d2b-152">Abrufen des Service Level-Ziels</span><span class="sxs-lookup"><span data-stu-id="43d2b-152">Get Service Level Objective</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505709.aspx)

[<span data-ttu-id="43d2b-153">Vorgänge für Azure SQL-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="43d2b-153">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="43d2b-154">Neu – AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="43d2b-154">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


