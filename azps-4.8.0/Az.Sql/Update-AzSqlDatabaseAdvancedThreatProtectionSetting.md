---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 1bd5906ac4736fc2aace122070edfebe1e59fe3f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165990"
---
# <span data-ttu-id="295c2-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="295c2-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="295c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="295c2-102">SYNOPSIS</span></span>
<span data-ttu-id="295c2-103">Legt eine erweiterte Bedrohungsschutz Einstellungen für eine Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="295c2-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="295c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="295c2-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="295c2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="295c2-105">DESCRIPTION</span></span>
<span data-ttu-id="295c2-106">Das Cmdlet **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** legt eine erweiterte Bedrohungsschutz Einstellungen für eine Azure SQL-Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="295c2-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="295c2-107">Um erweiterten Bedrohungsschutz für eine Datenbank zu aktivieren, müssen Überwachungseinstellungen für diese Datenbank aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="295c2-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="295c2-108">Um dieses Cmdlet zu verwenden, geben Sie die *ResourceGroupName* -, *Servername* -und *DatabaseName* -Parameter an, um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="295c2-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="295c2-109">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="295c2-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="295c2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="295c2-110">EXAMPLES</span></span>

### <span data-ttu-id="295c2-111">Beispiel 1: Festlegen der erweiterten Bedrohungsschutz Einstellungen für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="295c2-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="295c2-112">Mit diesem Befehl werden die erweiterten Bedrohungsschutz Einstellungen für eine Datenbank mit dem Namen "database01" auf dem Server "Server01" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="295c2-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="295c2-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="295c2-113">PARAMETERS</span></span>

### <span data-ttu-id="295c2-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="295c2-114">-DatabaseName</span></span>
<span data-ttu-id="295c2-115">Gibt den Namen der Datenbank an, in der die Einstellungen festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="295c2-115">Specifies the name of the database where the settings is set.</span></span>

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

### <span data-ttu-id="295c2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="295c2-116">-DefaultProfile</span></span>
<span data-ttu-id="295c2-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="295c2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="295c2-118">-Emailadmins</span><span class="sxs-lookup"><span data-stu-id="295c2-118">-EmailAdmins</span></span>
<span data-ttu-id="295c2-119">Gibt an, ob die erweiterten Bedrohungsschutz Einstellungen mithilfe von e-Mail mit Administratoren Kontakt aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="295c2-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="295c2-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="295c2-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="295c2-121">Gibt ein Array von Erkennungstypen an, die aus den Einstellungen ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="295c2-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="295c2-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="295c2-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="295c2-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="295c2-123">Sql_Injection</span></span> 
- <span data-ttu-id="295c2-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="295c2-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="295c2-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="295c2-125">Access_Anomaly</span></span> 
- <span data-ttu-id="295c2-126">Keine</span><span class="sxs-lookup"><span data-stu-id="295c2-126">None</span></span>

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

### <span data-ttu-id="295c2-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="295c2-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="295c2-128">Gibt eine durch Semikolons getrennte Liste der e-Mail-Adressen an, an die die Einstellungen Benachrichtigungen senden.</span><span class="sxs-lookup"><span data-stu-id="295c2-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="295c2-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="295c2-129">-PassThru</span></span>
<span data-ttu-id="295c2-130">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="295c2-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="295c2-131">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="295c2-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="295c2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="295c2-132">-ResourceGroupName</span></span>
<span data-ttu-id="295c2-133">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="295c2-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="295c2-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="295c2-134">-RetentionInDays</span></span>
<span data-ttu-id="295c2-135">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle</span><span class="sxs-lookup"><span data-stu-id="295c2-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="295c2-136">-Servername</span><span class="sxs-lookup"><span data-stu-id="295c2-136">-ServerName</span></span>
<span data-ttu-id="295c2-137">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="295c2-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="295c2-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="295c2-138">-StorageAccountName</span></span>
<span data-ttu-id="295c2-139">Gibt den Namen des zu verwendenden speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="295c2-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="295c2-140">Platzhalter sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="295c2-140">Wildcards are not permitted.</span></span> <span data-ttu-id="295c2-141">Dieser Parameter ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="295c2-141">This parameter is not required.</span></span> <span data-ttu-id="295c2-142">Wenn dieser Parameter nicht angegeben wird, verwendet das Cmdlet das Speicherkonto, das zuvor als Teil der erweiterten Bedrohungsschutz Einstellungen der Datenbank definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="295c2-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="295c2-143">Wenn dies das erste Mal ist, dass eine Datenbank erweiterte Bedrohungsschutz Einstellungen definiert ist und dieser Parameter nicht angegeben wird, schlägt das Cmdlet fehl.</span><span class="sxs-lookup"><span data-stu-id="295c2-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="295c2-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="295c2-144">-Confirm</span></span>
<span data-ttu-id="295c2-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="295c2-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="295c2-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="295c2-146">-WhatIf</span></span>
<span data-ttu-id="295c2-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="295c2-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="295c2-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="295c2-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="295c2-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="295c2-149">CommonParameters</span></span>
<span data-ttu-id="295c2-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="295c2-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="295c2-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="295c2-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="295c2-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="295c2-152">INPUTS</span></span>

### <span data-ttu-id="295c2-153">System. String</span><span class="sxs-lookup"><span data-stu-id="295c2-153">System.String</span></span>

### <span data-ttu-id="295c2-154">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="295c2-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="295c2-155">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. detectiontype []</span><span class="sxs-lookup"><span data-stu-id="295c2-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="295c2-156">System. Nullable ' 1 [[System. UInt32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="295c2-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="295c2-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="295c2-157">OUTPUTS</span></span>

### <span data-ttu-id="295c2-158">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="295c2-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="295c2-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="295c2-159">NOTES</span></span>

## <span data-ttu-id="295c2-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="295c2-160">RELATED LINKS</span></span>

[<span data-ttu-id="295c2-161">Get-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="295c2-161">Get-AzSqlDatabaseThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="295c2-162">Remove-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="295c2-162">Remove-AzSqlDatabaseThreatDetectionsettings</span></span>](./Remove-AzSqlDatabaseThreatDetectionsettings.md)

[<span data-ttu-id="295c2-163">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="295c2-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


