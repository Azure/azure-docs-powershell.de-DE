---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8090ee9cf6ec251668dbeadba6b18a7cde4898c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176902"
---
# <span data-ttu-id="dfd04-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="dfd04-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="dfd04-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dfd04-102">SYNOPSIS</span></span>
<span data-ttu-id="dfd04-103">Ruft die erweiterten Bedrohungsschutz Einstellungen für eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="dfd04-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="dfd04-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfd04-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSetting [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dfd04-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dfd04-105">DESCRIPTION</span></span>
<span data-ttu-id="dfd04-106">Das Cmdlet " **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** " Ruft die erweiterten Bedrohungsschutz Einstellungen einer Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="dfd04-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="dfd04-107">Um dieses Cmdlet zu verwenden, geben Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* an, um die Datenbank zu identifizieren, für die dieses Cmdlet die Einstellungen erhält.</span><span class="sxs-lookup"><span data-stu-id="dfd04-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="dfd04-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dfd04-108">EXAMPLES</span></span>

### <span data-ttu-id="dfd04-109">Beispiel 1: Abrufen der erweiterten Bedrohungsschutz Einstellungen für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="dfd04-109">Example 1: Get the advanced threat protection settings for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="dfd04-110">Dieser Befehl ruft die erweiterten Bedrohungsschutz Einstellungen für eine Datenbank mit dem Namen database01 ab.</span><span class="sxs-lookup"><span data-stu-id="dfd04-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="dfd04-111">Die Datenbank befindet sich auf dem Server mit dem Namen Server01, der der Ressourcengruppe ResourceGroup11 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="dfd04-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="dfd04-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfd04-112">PARAMETERS</span></span>

### <span data-ttu-id="dfd04-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dfd04-113">-DatabaseName</span></span>
<span data-ttu-id="dfd04-114">Gibt den Namen einer Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="dfd04-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="dfd04-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfd04-115">-DefaultProfile</span></span>
<span data-ttu-id="dfd04-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="dfd04-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfd04-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfd04-117">-ResourceGroupName</span></span>
<span data-ttu-id="dfd04-118">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="dfd04-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="dfd04-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="dfd04-119">-ServerName</span></span>
<span data-ttu-id="dfd04-120">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="dfd04-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="dfd04-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dfd04-121">-Confirm</span></span>
<span data-ttu-id="dfd04-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dfd04-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfd04-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfd04-123">-WhatIf</span></span>
<span data-ttu-id="dfd04-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dfd04-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfd04-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dfd04-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfd04-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfd04-126">CommonParameters</span></span>
<span data-ttu-id="dfd04-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfd04-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfd04-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfd04-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfd04-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dfd04-129">INPUTS</span></span>

### <span data-ttu-id="dfd04-130">System. String</span><span class="sxs-lookup"><span data-stu-id="dfd04-130">System.String</span></span>

## <span data-ttu-id="dfd04-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dfd04-131">OUTPUTS</span></span>

### <span data-ttu-id="dfd04-132">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="dfd04-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="dfd04-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="dfd04-133">NOTES</span></span>

## <span data-ttu-id="dfd04-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dfd04-134">RELATED LINKS</span></span>

[<span data-ttu-id="dfd04-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="dfd04-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)



