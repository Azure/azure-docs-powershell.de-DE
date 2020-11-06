---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 7c71e9390ca28b48127a2f977e04eba645ae962f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505566"
---
# <span data-ttu-id="9c7a2-101">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9c7a2-101">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="9c7a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9c7a2-102">SYNOPSIS</span></span>
<span data-ttu-id="9c7a2-103">Legt eine Bedrohungs Erkennungsrichtlinie auf einem Server fest.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-103">Sets a threat detection policy on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c7a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c7a2-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c7a2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c7a2-105">DESCRIPTION</span></span>
<span data-ttu-id="9c7a2-106">Das Cmdlet " **Set-AzureRmSqlServerThreatDetectionPolicy** " legt eine Bedrohungs Erkennungsrichtlinie auf einem Azure SQL Server fest.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-106">The **Set-AzureRmSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="9c7a2-107">Um die Bedrohungserkennung auf einem Server zu aktivieren, muss auf diesem Server eine Überwachungsrichtlinie aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="9c7a2-108">Um dieses Cmdlet zu verwenden, geben Sie die Parameter *ResourceGroupName* und Servername an, um den Server zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="9c7a2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c7a2-109">EXAMPLES</span></span>

### <span data-ttu-id="9c7a2-110">Beispiel 1: Festlegen der Bedrohungs Erkennungsrichtlinie für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="9c7a2-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="9c7a2-111">Mit diesem Befehl wird die Richtlinie für die Bedrohungserkennung für einen Server namens "Server01" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="9c7a2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c7a2-112">PARAMETERS</span></span>

### <span data-ttu-id="9c7a2-113">-Emailadmins</span><span class="sxs-lookup"><span data-stu-id="9c7a2-113">-EmailAdmins</span></span>
<span data-ttu-id="9c7a2-114">Gibt an, ob die Richtlinie für die Bedrohungserkennung Kontakte mit Administratoren per e-Mail kontaktiert.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-114">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="9c7a2-115">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="9c7a2-115">-ExcludedDetectionType</span></span>
<span data-ttu-id="9c7a2-116">Gibt ein Array von Erkennungstypen an, die aus der Richtlinie ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-116">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="9c7a2-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9c7a2-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9c7a2-118">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="9c7a2-118">Sql_Injection</span></span>
- <span data-ttu-id="9c7a2-119">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="9c7a2-119">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="9c7a2-120">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="9c7a2-120">Access_Anomaly</span></span>
- <span data-ttu-id="9c7a2-121">Keine</span><span class="sxs-lookup"><span data-stu-id="9c7a2-121">None</span></span>

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

### <span data-ttu-id="9c7a2-122">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="9c7a2-122">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="9c7a2-123">Gibt eine durch Semikolons getrennte Liste der e-Mail-Adressen an, an die die Richtlinie Benachrichtigungen sendet.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-123">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="9c7a2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c7a2-124">-PassThru</span></span>
<span data-ttu-id="9c7a2-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9c7a2-126">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9c7a2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c7a2-127">-ResourceGroupName</span></span>
<span data-ttu-id="9c7a2-128">Gibt den Namen der Ressourcengruppe an, zu der der Server gehört.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-128">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="9c7a2-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="9c7a2-129">-RetentionInDays</span></span>
<span data-ttu-id="9c7a2-130">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle</span><span class="sxs-lookup"><span data-stu-id="9c7a2-130">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="9c7a2-131">-Servername</span><span class="sxs-lookup"><span data-stu-id="9c7a2-131">-ServerName</span></span>
<span data-ttu-id="9c7a2-132">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-132">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7a2-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9c7a2-133">-StorageAccountName</span></span>
<span data-ttu-id="9c7a2-134">Gibt den Namen des zu verwendenden speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-134">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="9c7a2-135">Platzhalter sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-135">Wildcards are not permitted.</span></span> <span data-ttu-id="9c7a2-136">Dieser Parameter ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-136">This parameter is not required.</span></span> <span data-ttu-id="9c7a2-137">Wenn dieser Parameter nicht angegeben wird, verwendet das Cmdlet das Speicherkonto, das zuvor als Teil der Bedrohungs Erkennungsrichtlinie der Datenbank definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-137">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="9c7a2-138">Wenn dies das erste Mal ist, dass eine Datenbank Theat-Erkennungsrichtlinie definiert ist und dieser Parameter nicht angegeben wird, schlägt das Cmdlet fehl.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-138">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="9c7a2-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9c7a2-139">-Confirm</span></span>
<span data-ttu-id="9c7a2-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c7a2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c7a2-141">-WhatIf</span></span>
<span data-ttu-id="9c7a2-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c7a2-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c7a2-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c7a2-144">-DefaultProfile</span></span>
<span data-ttu-id="9c7a2-145">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c7a2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c7a2-146">CommonParameters</span></span>
<span data-ttu-id="9c7a2-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c7a2-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c7a2-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c7a2-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9c7a2-149">INPUTS</span></span>

###  
<span data-ttu-id="9c7a2-150">Sie können keine Eingabe an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-150">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="9c7a2-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9c7a2-151">OUTPUTS</span></span>

### <span data-ttu-id="9c7a2-152">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="9c7a2-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="9c7a2-153">Dieses Cmdlet gibt ein **ServerThreatDetectionPolicyModel** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="9c7a2-153">This cmdlet returns a **ServerThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="9c7a2-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c7a2-154">NOTES</span></span>

## <span data-ttu-id="9c7a2-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9c7a2-155">RELATED LINKS</span></span>

[<span data-ttu-id="9c7a2-156">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9c7a2-156">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="9c7a2-157">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9c7a2-157">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="9c7a2-158">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="9c7a2-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
