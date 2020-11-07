---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: fe8a76ed0851393462ba94937d2ab92914b503b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663993"
---
# <span data-ttu-id="c0671-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c0671-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="c0671-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c0671-102">SYNOPSIS</span></span>
<span data-ttu-id="c0671-103">Legt eine Bedrohungs Erkennungsrichtlinie für eine Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="c0671-103">Sets a threat detection policy on a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0671-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0671-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0671-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0671-105">DESCRIPTION</span></span>
<span data-ttu-id="c0671-106">Das Cmdlet " **Set-AzureRmSqlDatabaseThreatDetectionPolicy** " legt eine Bedrohungs Erkennungsrichtlinie für eine Azure SQL-Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="c0671-106">The **Set-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL database.</span></span>
<span data-ttu-id="c0671-107">Um die Bedrohungserkennung für eine Datenbank zu aktivieren, muss in dieser Datenbank eine Überwachungsrichtlinie aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="c0671-107">In order to enable threat detection on a database an auditing policy must be enabled on that database.</span></span>
<span data-ttu-id="c0671-108">Um dieses Cmdlet zu verwenden, geben Sie die *ResourceGroupName* -, *Servername* -und *DatabaseName* -Parameter an, um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c0671-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="c0671-109">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c0671-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c0671-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0671-110">EXAMPLES</span></span>

### <span data-ttu-id="c0671-111">Beispiel 1: Festlegen der Bedrohungs Erkennungsrichtlinie für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="c0671-111">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="c0671-112">Dieser Befehl legt die Richtlinie für die Bedrohungserkennung für eine Datenbank mit dem Namen Database01 auf dem Server mit dem Namen Server01 fest.</span><span class="sxs-lookup"><span data-stu-id="c0671-112">This command sets the threat detection policy for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="c0671-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0671-113">PARAMETERS</span></span>

### <span data-ttu-id="c0671-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c0671-114">-DatabaseName</span></span>
<span data-ttu-id="c0671-115">Gibt den Namen der Datenbank an, in der die Richtlinie festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c0671-115">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="c0671-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0671-116">-DefaultProfile</span></span>
<span data-ttu-id="c0671-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c0671-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0671-118">-Emailadmins</span><span class="sxs-lookup"><span data-stu-id="c0671-118">-EmailAdmins</span></span>
<span data-ttu-id="c0671-119">Gibt an, ob die Richtlinie für die Bedrohungserkennung Kontakte mit Administratoren per e-Mail kontaktiert.</span><span class="sxs-lookup"><span data-stu-id="c0671-119">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="c0671-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="c0671-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="c0671-121">Gibt ein Array von Erkennungstypen an, die aus der Richtlinie ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c0671-121">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="c0671-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c0671-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c0671-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="c0671-123">Sql_Injection</span></span> 
- <span data-ttu-id="c0671-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="c0671-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="c0671-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="c0671-125">Access_Anomaly</span></span> 
- <span data-ttu-id="c0671-126">Keine</span><span class="sxs-lookup"><span data-stu-id="c0671-126">None</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]
Parameter Sets: (All)
Aliases:
Accepted values: Sql_Injection, Sql_Injection_Vulnerability, Access_Anomaly, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0671-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="c0671-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="c0671-128">Gibt eine durch Semikolons getrennte Liste der e-Mail-Adressen an, an die die Richtlinie Benachrichtigungen sendet.</span><span class="sxs-lookup"><span data-stu-id="c0671-128">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="c0671-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0671-129">-PassThru</span></span>
<span data-ttu-id="c0671-130">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c0671-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c0671-131">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="c0671-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c0671-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0671-132">-ResourceGroupName</span></span>
<span data-ttu-id="c0671-133">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c0671-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="c0671-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="c0671-134">-RetentionInDays</span></span>
<span data-ttu-id="c0671-135">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle</span><span class="sxs-lookup"><span data-stu-id="c0671-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="c0671-136">-Servername</span><span class="sxs-lookup"><span data-stu-id="c0671-136">-ServerName</span></span>
<span data-ttu-id="c0671-137">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="c0671-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="c0671-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c0671-138">-StorageAccountName</span></span>
<span data-ttu-id="c0671-139">Gibt den Namen des zu verwendenden speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="c0671-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="c0671-140">Platzhalter sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="c0671-140">Wildcards are not permitted.</span></span> <span data-ttu-id="c0671-141">Dieser Parameter ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c0671-141">This parameter is not required.</span></span> <span data-ttu-id="c0671-142">Wenn dieser Parameter nicht angegeben wird, verwendet das Cmdlet das Speicherkonto, das zuvor als Teil der Bedrohungs Erkennungsrichtlinie der Datenbank definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c0671-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="c0671-143">Wenn dies das erste Mal ist, dass eine Datenbank-Bedrohungs Erkennungsrichtlinie definiert ist und dieser Parameter nicht angegeben wird, schlägt das Cmdlet fehl.</span><span class="sxs-lookup"><span data-stu-id="c0671-143">If this is the first time a database threat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="c0671-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c0671-144">-Confirm</span></span>
<span data-ttu-id="c0671-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0671-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0671-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0671-146">-WhatIf</span></span>
<span data-ttu-id="c0671-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0671-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0671-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0671-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0671-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0671-149">CommonParameters</span></span>
<span data-ttu-id="c0671-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0671-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0671-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0671-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0671-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c0671-152">INPUTS</span></span>

### <span data-ttu-id="c0671-153">System. String</span><span class="sxs-lookup"><span data-stu-id="c0671-153">System.String</span></span>

### <span data-ttu-id="c0671-154">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c0671-154">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="c0671-155">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. detectiontype []</span><span class="sxs-lookup"><span data-stu-id="c0671-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="c0671-156">System. Nullable ' 1 [[System. UInt32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c0671-156">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="c0671-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c0671-157">OUTPUTS</span></span>

### <span data-ttu-id="c0671-158">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c0671-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="c0671-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="c0671-159">NOTES</span></span>

## <span data-ttu-id="c0671-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c0671-160">RELATED LINKS</span></span>

[<span data-ttu-id="c0671-161">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c0671-161">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="c0671-162">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c0671-162">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="c0671-163">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="c0671-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


