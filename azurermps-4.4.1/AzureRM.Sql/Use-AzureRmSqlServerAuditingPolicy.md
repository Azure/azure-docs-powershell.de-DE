---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 381F5B34-983C-4733-B384-35D6579B79A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: 9e3e94109904bc14f22e2ca2c08936316ed597db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499930"
---
# <span data-ttu-id="c4a0f-101">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="c4a0f-101">Use-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="c4a0f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4a0f-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a0f-103">Gibt an, dass eine Datenbank die Überwachungsrichtlinie Ihres Hostservers verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4a0f-103">Specifies that a database uses the auditing policy of its host server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4a0f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4a0f-104">SYNTAX</span></span>

```
Use-AzureRmSqlServerAuditingPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4a0f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4a0f-105">DESCRIPTION</span></span>
<span data-ttu-id="c4a0f-106">Das Cmdlet **use-AzureRmSqlServerAuditingPolicy** gibt an, dass eine Datenbank die Überwachungsrichtlinie Ihres Hostservers verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4a0f-106">The **Use-AzureRmSqlServerAuditingPolicy** cmdlet specifies that a database uses the auditing policy of its host server.</span></span>
<span data-ttu-id="c4a0f-107">Geben Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* an, um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c4a0f-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="c4a0f-108">Wenn für den Datenbankserver keine Überwachungsrichtlinie definiert ist, schlägt dieses Cmdlet fehl.</span><span class="sxs-lookup"><span data-stu-id="c4a0f-108">If no auditing policy is defined for the database server, this cmdlet fails.</span></span>

<span data-ttu-id="c4a0f-109">Wenn der Host die Überwachung auf Serverebene verwendet, wird die Bedrohungserkennung entfernt.</span><span class="sxs-lookup"><span data-stu-id="c4a0f-109">If the host uses server level auditing, threat detection is removed.</span></span>

## <span data-ttu-id="c4a0f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4a0f-110">EXAMPLES</span></span>

### <span data-ttu-id="c4a0f-111">Beispiel 1: Konfigurieren einer Datenbank für die Verwendung der Überwachungsrichtlinie Ihres Servers</span><span class="sxs-lookup"><span data-stu-id="c4a0f-111">Example 1: Configure a database to use the auditing policy of its server</span></span>
```
PS C:\>Use-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server02" -DatabaseName "Database01"
```

<span data-ttu-id="c4a0f-112">Dieser Befehl gibt an, dass die Datenbank mit dem Namen database01 in Server02 die Überwachungsrichtlinie des Servers verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4a0f-112">This command specifies that the database named Database01 on Server02 uses the auditing policy of the server.</span></span>

## <span data-ttu-id="c4a0f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4a0f-113">PARAMETERS</span></span>

### <span data-ttu-id="c4a0f-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c4a0f-114">-DatabaseName</span></span>
<span data-ttu-id="c4a0f-115">Gibt den Namen der Datenbank an, in der die Überwachungsrichtlinie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4a0f-115">Specifies the name of the database that will use the auditing policy.</span></span>

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

### <span data-ttu-id="c4a0f-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4a0f-116">-PassThru</span></span>
<span data-ttu-id="c4a0f-117">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c4a0f-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c4a0f-118">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="c4a0f-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a0f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4a0f-119">-ResourceGroupName</span></span>
<span data-ttu-id="c4a0f-120">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c4a0f-120">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="c4a0f-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="c4a0f-121">-ServerName</span></span>
<span data-ttu-id="c4a0f-122">Gibt den Namen des Servers an, der die Datenbank hostet, die die Überwachungsrichtlinie verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4a0f-122">Specifies the name of the server that hosts the database that uses the auditing policy.</span></span>

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

### <span data-ttu-id="c4a0f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a0f-123">-DefaultProfile</span></span>
<span data-ttu-id="c4a0f-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4a0f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4a0f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a0f-125">CommonParameters</span></span>
<span data-ttu-id="c4a0f-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4a0f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a0f-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4a0f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a0f-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4a0f-128">INPUTS</span></span>

## <span data-ttu-id="c4a0f-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4a0f-129">OUTPUTS</span></span>

### <span data-ttu-id="c4a0f-130">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c4a0f-130">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="c4a0f-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4a0f-131">NOTES</span></span>

## <span data-ttu-id="c4a0f-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4a0f-132">RELATED LINKS</span></span>

[<span data-ttu-id="c4a0f-133">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="c4a0f-133">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="c4a0f-134">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="c4a0f-134">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="c4a0f-135">Satz-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="c4a0f-135">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="c4a0f-136">Satz-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="c4a0f-136">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="c4a0f-137">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="c4a0f-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


