---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 9677f45e772cbcb48190f5792df97e96051180c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939315"
---
# <span data-ttu-id="266fe-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="266fe-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="266fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="266fe-102">SYNOPSIS</span></span>
<span data-ttu-id="266fe-103">Legt eine erweiterte Bedrohungsschutzeinstellung für eine Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="266fe-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="266fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="266fe-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="266fe-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="266fe-105">DESCRIPTION</span></span>
<span data-ttu-id="266fe-106">Das **Cmdlet Update-AzSqlDatabaseAdvancedThreatProtectionSetting** legt eine erweiterte Bedrohungsschutzeinstellungen für eine Azure-SQL fest.</span><span class="sxs-lookup"><span data-stu-id="266fe-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="266fe-107">Um erweiterten Bedrohungsschutz für eine Datenbank zu aktivieren, müssen überwachungseinstellungen für diese Datenbank aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="266fe-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="266fe-108">Um dieses Cmdlet zu verwenden, geben Sie die *Parameter ResourceGroupName,* *ServerName* und *DatabaseName* an, um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="266fe-108">To use this cmdlet, specify the *ResourceGroupName*, *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="266fe-109">Dieses Cmdlet wird auch vom SQL Server Stretch Database Service in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="266fe-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="266fe-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="266fe-110">EXAMPLES</span></span>

### <span data-ttu-id="266fe-111">Beispiel 1: Festlegen der erweiterten Bedrohungsschutzeinstellungen für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="266fe-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="266fe-112">Mit diesem Befehl werden die erweiterten Bedrohungsschutzeinstellungen für eine Datenbank mit dem Namen Datenbank01 auf dem Server mit dem Namen Server01 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="266fe-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="266fe-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="266fe-113">PARAMETERS</span></span>

### <span data-ttu-id="266fe-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="266fe-114">-DatabaseName</span></span>
<span data-ttu-id="266fe-115">Gibt den Namen der Datenbank an, in der die Einstellungen festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="266fe-115">Specifies the name of the database where the settings is set.</span></span>

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

### <span data-ttu-id="266fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="266fe-116">-DefaultProfile</span></span>
<span data-ttu-id="266fe-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="266fe-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="266fe-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="266fe-118">-EmailAdmins</span></span>
<span data-ttu-id="266fe-119">Gibt an, ob die erweiterten Einstellungen für den Bedrohungsschutz mithilfe von E-Mail kontaktiert werden.</span><span class="sxs-lookup"><span data-stu-id="266fe-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="266fe-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="266fe-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="266fe-121">Gibt ein Array von Erkennungstypen an, das von den Einstellungen ausgeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="266fe-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="266fe-122">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="266fe-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="266fe-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="266fe-123">Sql_Injection</span></span> 
- <span data-ttu-id="266fe-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="266fe-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="266fe-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="266fe-125">Access_Anomaly</span></span> 
- <span data-ttu-id="266fe-126">Keine</span><span class="sxs-lookup"><span data-stu-id="266fe-126">None</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="266fe-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="266fe-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="266fe-128">Gibt eine semikolon getrennte Liste der E-Mail-Adressen an, an die die Einstellungen Benachrichtigungen senden.</span><span class="sxs-lookup"><span data-stu-id="266fe-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="266fe-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="266fe-129">-PassThru</span></span>
<span data-ttu-id="266fe-130">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="266fe-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="266fe-131">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="266fe-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="266fe-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="266fe-132">-ResourceGroupName</span></span>
<span data-ttu-id="266fe-133">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="266fe-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="266fe-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="266fe-134">-RetentionInDays</span></span>
<span data-ttu-id="266fe-135">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle</span><span class="sxs-lookup"><span data-stu-id="266fe-135">The number of retention days for the audit logs</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="266fe-136">-Servername</span><span class="sxs-lookup"><span data-stu-id="266fe-136">-ServerName</span></span>
<span data-ttu-id="266fe-137">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="266fe-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="266fe-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="266fe-138">-StorageAccountName</span></span>
<span data-ttu-id="266fe-139">Gibt den Namen des zu verwendenden Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="266fe-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="266fe-140">Platzhalter sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="266fe-140">Wildcards are not permitted.</span></span> <span data-ttu-id="266fe-141">Dieser Parameter ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="266fe-141">This parameter is not required.</span></span> <span data-ttu-id="266fe-142">Wenn dieser Parameter nicht bereitgestellt wird, verwendet das Cmdlet das Speicherkonto, das zuvor als Teil der erweiterten Bedrohungsschutzeinstellungen der Datenbank definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="266fe-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="266fe-143">Wenn dies das erste Mal ist, dass eine erweiterte Bedrohungsschutzeinstellung einer Datenbank definiert wird und dieser Parameter nicht bereitgestellt wird, kann das Cmdlet fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="266fe-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="266fe-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="266fe-144">-Confirm</span></span>
<span data-ttu-id="266fe-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="266fe-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="266fe-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="266fe-146">-WhatIf</span></span>
<span data-ttu-id="266fe-147">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="266fe-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="266fe-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="266fe-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="266fe-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="266fe-149">CommonParameters</span></span>
<span data-ttu-id="266fe-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="266fe-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="266fe-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="266fe-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="266fe-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="266fe-152">INPUTS</span></span>

### <span data-ttu-id="266fe-153">System.String</span><span class="sxs-lookup"><span data-stu-id="266fe-153">System.String</span></span>

### <span data-ttu-id="266fe-154">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="266fe-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="266fe-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="266fe-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="266fe-156">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="266fe-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="266fe-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="266fe-157">OUTPUTS</span></span>

### <span data-ttu-id="266fe-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="266fe-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="266fe-159">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="266fe-159">NOTES</span></span>

## <span data-ttu-id="266fe-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="266fe-160">RELATED LINKS</span></span>

[<span data-ttu-id="266fe-161">Get-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="266fe-161">Get-AzSqlDatabaseThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="266fe-162">Remove-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="266fe-162">Remove-AzSqlDatabaseThreatDetectionsettings</span></span>](./Remove-AzSqlDatabaseThreatDetectionsettings.md)

[<span data-ttu-id="266fe-163">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="266fe-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


