---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D3BA6534-CAAC-41E2-8442-0606B712E2B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 3fb40be93a1591e0337ec438e5eb3a317a08009b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480834"
---
# <span data-ttu-id="ae5bf-101">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="ae5bf-101">Remove-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="ae5bf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ae5bf-102">SYNOPSIS</span></span>
<span data-ttu-id="ae5bf-103">Entfernt die Überwachung einer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-103">Removes the auditing of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae5bf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae5bf-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseAuditing [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae5bf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae5bf-105">DESCRIPTION</span></span>
<span data-ttu-id="ae5bf-106">Das Cmdlet **Remove-AzureRmSqlDatabaseAuditing** entfernt die Überwachung einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-106">The **Remove-AzureRmSqlDatabaseAuditing** cmdlet removes the auditing of an Azure SQL database.</span></span>
<span data-ttu-id="ae5bf-107">Um dieses Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="ae5bf-108">Nachdem Sie dieses Cmdlet ausgeführt haben, wird die Überwachung der Datenbank nicht durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-108">After you run this cmdlet, auditing of the database is not performed.</span></span>
<span data-ttu-id="ae5bf-109">Wenn der Befehl erfolgreich ausgeführt wird und Sie den *passthru* -Parameter verwendet haben, gibt das Cmdlet zusätzlich zu den Datenbankbezeichnern ein Objekt zurück, das die aktuelle Überwachungsrichtlinie beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-109">If the command succeeds and you have used the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy, in addition to the database identifiers.</span></span>
<span data-ttu-id="ae5bf-110">Zu den Datenbankbezeichnern gehören die **ResourceGroupName** , **Servername** und **DatabaseName** , sind aber nicht darauf limitiert.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-110">Database identifiers include, but are not limited to, the **ResourceGroupName** , **ServerName** and **DatabaseName**.</span></span>

<span data-ttu-id="ae5bf-111">Wenn Sie die Überwachung einer Azure SQL-Datenbank entfernen, wird die Bedrohungserkennung ebenfalls entfernt.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-111">If you remove auditing of an Azure SQL database, threat detection is also removed.</span></span>

<span data-ttu-id="ae5bf-112">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ae5bf-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae5bf-113">EXAMPLES</span></span>

### <span data-ttu-id="ae5bf-114">Beispiel 1: Entfernen der Überwachung einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="ae5bf-114">Example 1: Remove the auditing of an Azure SQL database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="ae5bf-115">Dieser Befehl entfernt die Überwachung der Datenbank mit dem Namen database01.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-115">This command removes the auditing of database named Database01.</span></span>
<span data-ttu-id="ae5bf-116">Diese Datenbank befindet sich auf Server01, die der Ressourcengruppe mit dem Namen ResourceGroup01 zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-116">That database is located on Server01, which is assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="ae5bf-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae5bf-117">PARAMETERS</span></span>

### <span data-ttu-id="ae5bf-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ae5bf-118">-DatabaseName</span></span>
<span data-ttu-id="ae5bf-119">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-119">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="ae5bf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae5bf-120">-DefaultProfile</span></span>
<span data-ttu-id="ae5bf-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ae5bf-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae5bf-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae5bf-122">-PassThru</span></span>
<span data-ttu-id="ae5bf-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-123">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="ae5bf-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ae5bf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae5bf-125">-ResourceGroupName</span></span>
<span data-ttu-id="ae5bf-126">Gibt den Namen der Ressourcengruppe an, die die Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-126">Specifies the name of the resource group containing the database.</span></span>

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

### <span data-ttu-id="ae5bf-127">-Servername</span><span class="sxs-lookup"><span data-stu-id="ae5bf-127">-ServerName</span></span>
<span data-ttu-id="ae5bf-128">Gibt den Namen des Servers an, der die Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-128">Specifies the name of the server containing the database.</span></span>

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

### <span data-ttu-id="ae5bf-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ae5bf-129">-Confirm</span></span>
<span data-ttu-id="ae5bf-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae5bf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae5bf-131">-WhatIf</span></span>
<span data-ttu-id="ae5bf-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae5bf-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae5bf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae5bf-134">CommonParameters</span></span>
<span data-ttu-id="ae5bf-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae5bf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae5bf-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae5bf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae5bf-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ae5bf-137">INPUTS</span></span>

### <span data-ttu-id="ae5bf-138">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="ae5bf-138">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="ae5bf-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ae5bf-139">OUTPUTS</span></span>

### <span data-ttu-id="ae5bf-140">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="ae5bf-140">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="ae5bf-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="ae5bf-141">NOTES</span></span>

## <span data-ttu-id="ae5bf-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ae5bf-142">RELATED LINKS</span></span>

[<span data-ttu-id="ae5bf-143">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="ae5bf-143">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="ae5bf-144">Satz-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="ae5bf-144">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="ae5bf-145">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="ae5bf-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


