---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 746a9a9908865047d5b904b5b47b71ca9c30fbd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481433"
---
# <span data-ttu-id="59785-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="59785-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="59785-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59785-102">SYNOPSIS</span></span>
<span data-ttu-id="59785-103">Legt eine Bedrohungs Erkennungsrichtlinie für eine Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="59785-103">Sets a threat detection policy on a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59785-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59785-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59785-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59785-105">DESCRIPTION</span></span>
<span data-ttu-id="59785-106">Das Cmdlet " **Set-AzureRmSqlDatabaseThreatDetectionPolicy** " legt eine Bedrohungs Erkennungsrichtlinie für eine Azure SQL-Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="59785-106">The **Set-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL database.</span></span>
<span data-ttu-id="59785-107">Um die Bedrohungserkennung für eine Datenbank zu aktivieren, muss in dieser Datenbank eine Überwachungsrichtlinie aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="59785-107">In order to enable threat detection on a database an auditing policy must be enabled on that database.</span></span>

<span data-ttu-id="59785-108">Um dieses Cmdlet zu verwenden, geben Sie die *ResourceGroupName* -, *Servername* -und *DatabaseName* -Parameter an, um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="59785-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>

<span data-ttu-id="59785-109">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="59785-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="59785-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59785-110">EXAMPLES</span></span>

### <span data-ttu-id="59785-111">Beispiel 1: Festlegen der Bedrohungs Erkennungsrichtlinie für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="59785-111">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="59785-112">Dieser Befehl legt die Richtlinie für die Bedrohungserkennung für eine Datenbank mit dem Namen Database01 auf dem Server mit dem Namen Server01 fest.</span><span class="sxs-lookup"><span data-stu-id="59785-112">This command sets the threat detection policy for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="59785-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="59785-113">PARAMETERS</span></span>

### <span data-ttu-id="59785-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="59785-114">-DatabaseName</span></span>
<span data-ttu-id="59785-115">Gibt den Namen der Datenbank an, in der die Richtlinie festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="59785-115">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="59785-116">-Emailadmins</span><span class="sxs-lookup"><span data-stu-id="59785-116">-EmailAdmins</span></span>
<span data-ttu-id="59785-117">Gibt an, ob die Richtlinie für die Bedrohungserkennung Kontakte mit Administratoren per e-Mail kontaktiert.</span><span class="sxs-lookup"><span data-stu-id="59785-117">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="59785-118">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="59785-118">-ExcludedDetectionType</span></span>
<span data-ttu-id="59785-119">Gibt ein Array von Erkennungstypen an, die aus der Richtlinie ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="59785-119">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="59785-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="59785-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="59785-121">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="59785-121">Sql_Injection</span></span> 
- <span data-ttu-id="59785-122">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="59785-122">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="59785-123">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="59785-123">Access_Anomaly</span></span> 
- <span data-ttu-id="59785-124">Keine</span><span class="sxs-lookup"><span data-stu-id="59785-124">None</span></span>

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

### <span data-ttu-id="59785-125">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="59785-125">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="59785-126">Gibt eine durch Semikolons getrennte Liste der e-Mail-Adressen an, an die die Richtlinie Benachrichtigungen sendet.</span><span class="sxs-lookup"><span data-stu-id="59785-126">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="59785-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59785-127">-PassThru</span></span>
<span data-ttu-id="59785-128">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="59785-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="59785-129">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="59785-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="59785-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59785-130">-ResourceGroupName</span></span>
<span data-ttu-id="59785-131">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="59785-131">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="59785-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="59785-132">-RetentionInDays</span></span>
<span data-ttu-id="59785-133">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle</span><span class="sxs-lookup"><span data-stu-id="59785-133">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="59785-134">-Servername</span><span class="sxs-lookup"><span data-stu-id="59785-134">-ServerName</span></span>
<span data-ttu-id="59785-135">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="59785-135">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="59785-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="59785-136">-StorageAccountName</span></span>
<span data-ttu-id="59785-137">Gibt den Namen des zu verwendenden speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="59785-137">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="59785-138">Platzhalter sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="59785-138">Wildcards are not permitted.</span></span> <span data-ttu-id="59785-139">Dieser Parameter ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="59785-139">This parameter is not required.</span></span> <span data-ttu-id="59785-140">Wenn dieser Parameter nicht angegeben wird, verwendet das Cmdlet das Speicherkonto, das zuvor als Teil der Bedrohungs Erkennungsrichtlinie der Datenbank definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="59785-140">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="59785-141">Wenn dies das erste Mal ist, dass eine Datenbank-Bedrohungs Erkennungsrichtlinie definiert ist und dieser Parameter nicht angegeben wird, schlägt das Cmdlet fehl.</span><span class="sxs-lookup"><span data-stu-id="59785-141">If this is the first time a database threat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="59785-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="59785-142">-Confirm</span></span>
<span data-ttu-id="59785-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="59785-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59785-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59785-144">-WhatIf</span></span>
<span data-ttu-id="59785-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59785-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59785-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59785-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59785-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59785-147">-DefaultProfile</span></span>
<span data-ttu-id="59785-148">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="59785-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59785-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59785-149">CommonParameters</span></span>
<span data-ttu-id="59785-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59785-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59785-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59785-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59785-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59785-152">INPUTS</span></span>

###  
<span data-ttu-id="59785-153">Sie können keine Eingabe an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="59785-153">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="59785-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59785-154">OUTPUTS</span></span>

### <span data-ttu-id="59785-155">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="59785-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="59785-156">Dieses Cmdlet gibt ein **Model. DatabaseThreatDetectionPolicyModel** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="59785-156">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="59785-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="59785-157">NOTES</span></span>

## <span data-ttu-id="59785-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59785-158">RELATED LINKS</span></span>

[<span data-ttu-id="59785-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="59785-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="59785-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="59785-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="59785-161">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="59785-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


