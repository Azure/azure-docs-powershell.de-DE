---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 94963c8c5d61c91e2d53cdf7b12cc333acc566a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166058"
---
# <span data-ttu-id="1d910-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="1d910-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="1d910-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1d910-102">SYNOPSIS</span></span>
<span data-ttu-id="1d910-103">Ruft die erweiterten Bedrohungsschutz Einstellungen für einen Server ab.</span><span class="sxs-lookup"><span data-stu-id="1d910-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="1d910-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d910-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSetting -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d910-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d910-105">DESCRIPTION</span></span>
<span data-ttu-id="1d910-106">Das Cmdlet " **Get-AzSqlServerAdvancedThreatProtectionSetting** " Ruft die erweiterten Bedrohungsschutz Einstellungen eines Azure SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="1d910-106">The **Get-AzSqlServerAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="1d910-107">Um dieses Cmdlet zu verwenden, geben Sie die Parameter *ResourceGroupName* und Server *Name* an, um den Server zu identifizieren, für den dieses Cmdlet die Einstellungen erhält.</span><span class="sxs-lookup"><span data-stu-id="1d910-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="1d910-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1d910-108">EXAMPLES</span></span>

### <span data-ttu-id="1d910-109">Beispiel 1: Abrufen der erweiterten Bedrohungsschutz Einstellungen für einen Server</span><span class="sxs-lookup"><span data-stu-id="1d910-109">Example 1: Get the advanced threat protection settings for a server</span></span>
```
PS C:\>Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="1d910-110">Dieser Befehl ruft die erweiterten Bedrohungsschutz Einstellungen für einen Server mit dem Namen "Server01" ab.</span><span class="sxs-lookup"><span data-stu-id="1d910-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="1d910-111">Der Server ist der Ressourcengruppe ResourceGroup11 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1d910-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="1d910-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d910-112">PARAMETERS</span></span>

### <span data-ttu-id="1d910-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d910-113">-DefaultProfile</span></span>
<span data-ttu-id="1d910-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1d910-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d910-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d910-115">-ResourceGroupName</span></span>
<span data-ttu-id="1d910-116">Gibt den Namen der Ressourcengruppe an, zu der der Server gehört.</span><span class="sxs-lookup"><span data-stu-id="1d910-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="1d910-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="1d910-117">-ServerName</span></span>
<span data-ttu-id="1d910-118">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="1d910-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="1d910-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1d910-119">-Confirm</span></span>
<span data-ttu-id="1d910-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1d910-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d910-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d910-121">-WhatIf</span></span>
<span data-ttu-id="1d910-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d910-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d910-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d910-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d910-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d910-124">CommonParameters</span></span>
<span data-ttu-id="1d910-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d910-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d910-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d910-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d910-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1d910-127">INPUTS</span></span>

### <span data-ttu-id="1d910-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1d910-128">System.String</span></span>

## <span data-ttu-id="1d910-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1d910-129">OUTPUTS</span></span>

### <span data-ttu-id="1d910-130">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="1d910-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="1d910-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="1d910-131">NOTES</span></span>

## <span data-ttu-id="1d910-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1d910-132">RELATED LINKS</span></span>

[<span data-ttu-id="1d910-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="1d910-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)

[<span data-ttu-id="1d910-134">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="1d910-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


