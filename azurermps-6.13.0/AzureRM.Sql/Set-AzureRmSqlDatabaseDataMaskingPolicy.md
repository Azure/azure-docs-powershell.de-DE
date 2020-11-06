---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d59891980c11b90ee73275dbccb6a98b65c89613
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479425"
---
# <span data-ttu-id="b1163-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="b1163-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="b1163-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1163-102">SYNOPSIS</span></span>
<span data-ttu-id="b1163-103">Legt die Daten Maskierung für eine Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="b1163-103">Sets data masking for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1163-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1163-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedLogins <String>] [-PrivilegedUsers <String>]
 [-DataMaskingState <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1163-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1163-105">DESCRIPTION</span></span>
<span data-ttu-id="b1163-106">Das Cmdlet " **Set-AzureRmSqlDatabaseDataMaskingPolicy** " legt die Daten Maskierungs Richtlinie für eine Azure SQL-Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="b1163-106">The **Set-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="b1163-107">Um dieses Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b1163-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="b1163-108">Sie können den *DataMaskingState* -Parameter festlegen, um anzugeben, ob Daten Maskierungs Vorgänge aktiviert oder deaktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b1163-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="b1163-109">Sie können auch den *PrivilegedLogins* -Parameter festlegen, um anzugeben, welche Benutzer die nicht maskierten Daten anzeigen dürfen.</span><span class="sxs-lookup"><span data-stu-id="b1163-109">You can also set the *PrivilegedLogins* parameter to specify which users are allowed to see the unmasked data.</span></span>
<span data-ttu-id="b1163-110">Wenn das Cmdlet erfolgreich ausgeführt wird und der *passthru* -Parameter verwendet wird, gibt es zusätzlich zu den Datenbankbezeichnern ein Objekt zurück, das die aktuelle Daten Maskierungs Richtlinie beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b1163-110">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="b1163-111">Zu den Datenbankbezeichnern gehören **ResourceGroupName** , **Servername** und **DatabaseName** , sind aber nicht darauf limitiert.</span><span class="sxs-lookup"><span data-stu-id="b1163-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="b1163-112">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b1163-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b1163-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1163-113">EXAMPLES</span></span>

### <span data-ttu-id="b1163-114">Beispiel 1: Festlegen der Daten Maskierungs Richtlinie für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="b1163-114">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="b1163-115">Mit diesem Befehl wird die Daten Maskierungs Richtlinie für eine Datenbank mit dem Namen "database01" auf dem Server mit dem Namen "Server01" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1163-115">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="b1163-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1163-116">PARAMETERS</span></span>

### <span data-ttu-id="b1163-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b1163-117">-DatabaseName</span></span>
<span data-ttu-id="b1163-118">Gibt den Namen der Datenbank an, in der die Richtlinie festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b1163-118">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="b1163-119">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="b1163-119">-DataMaskingState</span></span>
<span data-ttu-id="b1163-120">Gibt an, ob der Daten Maskierungs Vorgang aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b1163-120">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="b1163-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b1163-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b1163-122">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="b1163-122">Enabled</span></span>
- <span data-ttu-id="b1163-123">Deaktiviert der Standardwert ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b1163-123">Disabled The default value is Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1163-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1163-124">-DefaultProfile</span></span>
<span data-ttu-id="b1163-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b1163-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1163-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1163-126">-PassThru</span></span>
<span data-ttu-id="b1163-127">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="b1163-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b1163-128">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="b1163-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b1163-129">-PrivilegedLogins</span><span class="sxs-lookup"><span data-stu-id="b1163-129">-PrivilegedLogins</span></span>
<span data-ttu-id="b1163-130">Gibt an, welche SQL-Benutzer von der Maskierung ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="b1163-130">Specifies which SQL users are excluded from masking.</span></span>
<span data-ttu-id="b1163-131">Dieser Parameter ist veraltet und wird aus zukünftigen Versionen entfernt.</span><span class="sxs-lookup"><span data-stu-id="b1163-131">This parameter is deprecated and will be removed from future releases.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1163-132">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="b1163-132">-PrivilegedUsers</span></span>
<span data-ttu-id="b1163-133">Gibt eine durch Semikolons getrennte Liste mit privilegierten Benutzer-IDs an.</span><span class="sxs-lookup"><span data-stu-id="b1163-133">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="b1163-134">Diesen Benutzern ist es gestattet, die Maskierungs Daten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b1163-134">These users are allowed to view the masking data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1163-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1163-135">-ResourceGroupName</span></span>
<span data-ttu-id="b1163-136">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="b1163-136">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="b1163-137">-Servername</span><span class="sxs-lookup"><span data-stu-id="b1163-137">-ServerName</span></span>
<span data-ttu-id="b1163-138">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="b1163-138">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="b1163-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b1163-139">-Confirm</span></span>
<span data-ttu-id="b1163-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1163-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1163-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1163-141">-WhatIf</span></span>
<span data-ttu-id="b1163-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1163-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1163-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1163-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1163-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1163-144">CommonParameters</span></span>
<span data-ttu-id="b1163-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1163-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1163-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1163-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1163-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1163-147">INPUTS</span></span>

### <span data-ttu-id="b1163-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b1163-148">System.String</span></span>

## <span data-ttu-id="b1163-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1163-149">OUTPUTS</span></span>

### <span data-ttu-id="b1163-150">Microsoft. Azure. Commands. SQL. datamasking. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b1163-150">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="b1163-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1163-151">NOTES</span></span>

## <span data-ttu-id="b1163-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1163-152">RELATED LINKS</span></span>

[<span data-ttu-id="b1163-153">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="b1163-153">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="b1163-154">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b1163-154">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b1163-155">Neu – AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b1163-155">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b1163-156">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b1163-156">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b1163-157">Satz-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b1163-157">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b1163-158">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="b1163-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


