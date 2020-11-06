---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 381F5B34-983C-4733-B384-35D6579B79A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/use-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: f74abc2daab0c79c9d070d206a82b33fb15f23f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501333"
---
# <span data-ttu-id="d51d3-101">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d51d3-101">Use-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="d51d3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d51d3-102">SYNOPSIS</span></span>
<span data-ttu-id="d51d3-103">Gibt an, dass eine Datenbank die Überwachungsrichtlinie Ihres Hostservers verwendet.</span><span class="sxs-lookup"><span data-stu-id="d51d3-103">Specifies that a database uses the auditing policy of its host server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d51d3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d51d3-104">SYNTAX</span></span>

```
Use-AzureRmSqlServerAuditingPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d51d3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d51d3-105">DESCRIPTION</span></span>
<span data-ttu-id="d51d3-106">Das Cmdlet **use-AzureRmSqlServerAuditingPolicy** gibt an, dass eine Datenbank die Überwachungsrichtlinie Ihres Hostservers verwendet.</span><span class="sxs-lookup"><span data-stu-id="d51d3-106">The **Use-AzureRmSqlServerAuditingPolicy** cmdlet specifies that a database uses the auditing policy of its host server.</span></span>
<span data-ttu-id="d51d3-107">Geben Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* an, um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d51d3-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="d51d3-108">Wenn für den Datenbankserver keine Überwachungsrichtlinie definiert ist, schlägt dieses Cmdlet fehl.</span><span class="sxs-lookup"><span data-stu-id="d51d3-108">If no auditing policy is defined for the database server, this cmdlet fails.</span></span>

<span data-ttu-id="d51d3-109">Wenn der Host die Überwachung auf Serverebene verwendet, wird die Bedrohungserkennung entfernt.</span><span class="sxs-lookup"><span data-stu-id="d51d3-109">If the host uses server level auditing, threat detection is removed.</span></span>

## <span data-ttu-id="d51d3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d51d3-110">EXAMPLES</span></span>

### <span data-ttu-id="d51d3-111">Beispiel 1: Konfigurieren einer Datenbank für die Verwendung der Überwachungsrichtlinie Ihres Servers</span><span class="sxs-lookup"><span data-stu-id="d51d3-111">Example 1: Configure a database to use the auditing policy of its server</span></span>
```
PS C:\>Use-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server02" -DatabaseName "Database01"
```

<span data-ttu-id="d51d3-112">Dieser Befehl gibt an, dass die Datenbank mit dem Namen database01 in Server02 die Überwachungsrichtlinie des Servers verwendet.</span><span class="sxs-lookup"><span data-stu-id="d51d3-112">This command specifies that the database named Database01 on Server02 uses the auditing policy of the server.</span></span>

## <span data-ttu-id="d51d3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d51d3-113">PARAMETERS</span></span>

### <span data-ttu-id="d51d3-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d51d3-114">-DatabaseName</span></span>
<span data-ttu-id="d51d3-115">Gibt den Namen der Datenbank an, in der die Überwachungsrichtlinie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d51d3-115">Specifies the name of the database that will use the auditing policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d51d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d51d3-116">-DefaultProfile</span></span>
<span data-ttu-id="d51d3-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d51d3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d51d3-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d51d3-118">-PassThru</span></span>
<span data-ttu-id="d51d3-119">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d51d3-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d51d3-120">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="d51d3-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d51d3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d51d3-121">-ResourceGroupName</span></span>
<span data-ttu-id="d51d3-122">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d51d3-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="d51d3-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="d51d3-123">-ServerName</span></span>
<span data-ttu-id="d51d3-124">Gibt den Namen des Servers an, der die Datenbank hostet, die die Überwachungsrichtlinie verwendet.</span><span class="sxs-lookup"><span data-stu-id="d51d3-124">Specifies the name of the server that hosts the database that uses the auditing policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d51d3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d51d3-125">CommonParameters</span></span>
<span data-ttu-id="d51d3-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d51d3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d51d3-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d51d3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d51d3-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d51d3-128">INPUTS</span></span>

### <span data-ttu-id="d51d3-129">Keine</span><span class="sxs-lookup"><span data-stu-id="d51d3-129">None</span></span>
<span data-ttu-id="d51d3-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d51d3-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d51d3-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d51d3-131">OUTPUTS</span></span>

### <span data-ttu-id="d51d3-132">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d51d3-132">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="d51d3-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="d51d3-133">NOTES</span></span>

## <span data-ttu-id="d51d3-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d51d3-134">RELATED LINKS</span></span>

[<span data-ttu-id="d51d3-135">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d51d3-135">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="d51d3-136">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d51d3-136">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="d51d3-137">Satz-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d51d3-137">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="d51d3-138">Satz-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d51d3-138">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="d51d3-139">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="d51d3-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


