---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 26d056b5ad9cdff22f0419f90fad17c3147e0e14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480777"
---
# <span data-ttu-id="618b9-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="618b9-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="618b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="618b9-102">SYNOPSIS</span></span>
<span data-ttu-id="618b9-103">Legt die Daten Maskierung für eine Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="618b9-103">Sets data masking for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="618b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="618b9-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedLogins <String>] [-PrivilegedUsers <String>]
 [-DataMaskingState <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="618b9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="618b9-105">DESCRIPTION</span></span>
<span data-ttu-id="618b9-106">Das Cmdlet " **Set-AzureRmSqlDatabaseDataMaskingPolicy** " legt die Daten Maskierungs Richtlinie für eine Azure SQL-Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="618b9-106">The **Set-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="618b9-107">Um dieses Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="618b9-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="618b9-108">Sie können den *DataMaskingState* -Parameter festlegen, um anzugeben, ob Daten Maskierungs Vorgänge aktiviert oder deaktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="618b9-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>

<span data-ttu-id="618b9-109">Sie können auch den *PrivilegedLogins* -Parameter festlegen, um anzugeben, welche Benutzer die nicht maskierten Daten anzeigen dürfen.</span><span class="sxs-lookup"><span data-stu-id="618b9-109">You can also set the *PrivilegedLogins* parameter to specify which users are allowed to see the unmasked data.</span></span>
<span data-ttu-id="618b9-110">Wenn das Cmdlet erfolgreich ausgeführt wird und der *passthru* -Parameter verwendet wird, gibt es zusätzlich zu den Datenbankbezeichnern ein Objekt zurück, das die aktuelle Daten Maskierungs Richtlinie beschreibt.</span><span class="sxs-lookup"><span data-stu-id="618b9-110">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="618b9-111">Zu den Datenbankbezeichnern gehören **ResourceGroupName** , **Servername** und **DatabaseName** , sind aber nicht darauf limitiert.</span><span class="sxs-lookup"><span data-stu-id="618b9-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="618b9-112">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="618b9-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="618b9-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="618b9-113">EXAMPLES</span></span>

### <span data-ttu-id="618b9-114">Beispiel 1: Festlegen der Daten Maskierungs Richtlinie für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="618b9-114">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="618b9-115">Mit diesem Befehl wird die Daten Maskierungs Richtlinie für eine Datenbank mit dem Namen "database01" auf dem Server mit dem Namen "Server01" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="618b9-115">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="618b9-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="618b9-116">PARAMETERS</span></span>

### <span data-ttu-id="618b9-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="618b9-117">-DatabaseName</span></span>
<span data-ttu-id="618b9-118">Gibt den Namen der Datenbank an, in der die Richtlinie festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="618b9-118">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="618b9-119">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="618b9-119">-DataMaskingState</span></span>
<span data-ttu-id="618b9-120">Gibt an, ob der Daten Maskierungs Vorgang aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="618b9-120">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="618b9-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="618b9-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="618b9-122">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="618b9-122">Enabled</span></span>
- <span data-ttu-id="618b9-123">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="618b9-123">Disabled</span></span>

<span data-ttu-id="618b9-124">Der Standardwert ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="618b9-124">The default value is Enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="618b9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="618b9-125">-DefaultProfile</span></span>
<span data-ttu-id="618b9-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="618b9-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="618b9-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="618b9-127">-PassThru</span></span>
<span data-ttu-id="618b9-128">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="618b9-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="618b9-129">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="618b9-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="618b9-130">-PrivilegedLogins</span><span class="sxs-lookup"><span data-stu-id="618b9-130">-PrivilegedLogins</span></span>
<span data-ttu-id="618b9-131">Gibt an, welche SQL-Benutzer von der Maskierung ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="618b9-131">Specifies which SQL users are excluded from masking.</span></span>

<span data-ttu-id="618b9-132">Dieser Parameter ist veraltet und wird aus zukünftigen Versionen entfernt.</span><span class="sxs-lookup"><span data-stu-id="618b9-132">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="618b9-133">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="618b9-133">-PrivilegedUsers</span></span>
<span data-ttu-id="618b9-134">Gibt eine durch Semikolons getrennte Liste mit privilegierten Benutzer-IDs an.</span><span class="sxs-lookup"><span data-stu-id="618b9-134">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="618b9-135">Diesen Benutzern ist es gestattet, die Maskierungs Daten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="618b9-135">These users are allowed to view the masking data.</span></span>

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

### <span data-ttu-id="618b9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="618b9-136">-ResourceGroupName</span></span>
<span data-ttu-id="618b9-137">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="618b9-137">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="618b9-138">-Servername</span><span class="sxs-lookup"><span data-stu-id="618b9-138">-ServerName</span></span>
<span data-ttu-id="618b9-139">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="618b9-139">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="618b9-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="618b9-140">-Confirm</span></span>
<span data-ttu-id="618b9-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="618b9-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="618b9-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="618b9-142">-WhatIf</span></span>
<span data-ttu-id="618b9-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="618b9-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="618b9-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="618b9-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="618b9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="618b9-145">CommonParameters</span></span>
<span data-ttu-id="618b9-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="618b9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="618b9-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="618b9-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="618b9-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="618b9-148">INPUTS</span></span>

### <span data-ttu-id="618b9-149">Keine</span><span class="sxs-lookup"><span data-stu-id="618b9-149">None</span></span>
<span data-ttu-id="618b9-150">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="618b9-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="618b9-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="618b9-151">OUTPUTS</span></span>

### <span data-ttu-id="618b9-152">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="618b9-152">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="618b9-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="618b9-153">NOTES</span></span>

## <span data-ttu-id="618b9-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="618b9-154">RELATED LINKS</span></span>

[<span data-ttu-id="618b9-155">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="618b9-155">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="618b9-156">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="618b9-156">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="618b9-157">Neu – AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="618b9-157">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="618b9-158">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="618b9-158">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="618b9-159">Satz-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="618b9-159">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="618b9-160">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="618b9-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


