---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 1895fe45f51782cc1a3a54d8b2d0f2da752c2990
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825519"
---
# <span data-ttu-id="98ea8-101">Get-AzSqlServerAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="98ea8-101">Get-AzSqlServerAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="98ea8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="98ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="98ea8-103">Ruft die erweiterten Bedrohungsschutz Einstellungen für einen Server ab.</span><span class="sxs-lookup"><span data-stu-id="98ea8-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="98ea8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="98ea8-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSettings -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98ea8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="98ea8-105">DESCRIPTION</span></span>
<span data-ttu-id="98ea8-106">Das Cmdlet " **Get-AzSqlServerAdvancedThreatProtectionSettings** " Ruft die erweiterten Bedrohungsschutz Einstellungen eines Azure SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="98ea8-106">The **Get-AzSqlServerAdvancedThreatProtectionSettings** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="98ea8-107">Um dieses Cmdlet zu verwenden, geben Sie die Parameter *ResourceGroupName* und Server *Name* an, um den Server zu identifizieren, für den dieses Cmdlet die Einstellungen erhält.</span><span class="sxs-lookup"><span data-stu-id="98ea8-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="98ea8-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="98ea8-108">EXAMPLES</span></span>

### <span data-ttu-id="98ea8-109">Beispiel 1: Abrufen der erweiterten Bedrohungsschutz Einstellungen für einen Server</span><span class="sxs-lookup"><span data-stu-id="98ea8-109">Example 1: Get the advanced threat protection settings for a server</span></span>
```
PS C:\>Get-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="98ea8-110">Dieser Befehl ruft die erweiterten Bedrohungsschutz Einstellungen für einen Server mit dem Namen "Server01" ab.</span><span class="sxs-lookup"><span data-stu-id="98ea8-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="98ea8-111">Der Server ist der Ressourcengruppe ResourceGroup11 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="98ea8-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="98ea8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="98ea8-112">PARAMETERS</span></span>

### <span data-ttu-id="98ea8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98ea8-113">-DefaultProfile</span></span>
<span data-ttu-id="98ea8-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="98ea8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98ea8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98ea8-115">-ResourceGroupName</span></span>
<span data-ttu-id="98ea8-116">Gibt den Namen der Ressourcengruppe an, zu der der Server gehört.</span><span class="sxs-lookup"><span data-stu-id="98ea8-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="98ea8-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="98ea8-117">-ServerName</span></span>
<span data-ttu-id="98ea8-118">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="98ea8-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="98ea8-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="98ea8-119">-Confirm</span></span>
<span data-ttu-id="98ea8-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="98ea8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98ea8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98ea8-121">-WhatIf</span></span>
<span data-ttu-id="98ea8-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="98ea8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98ea8-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="98ea8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98ea8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98ea8-124">CommonParameters</span></span>
<span data-ttu-id="98ea8-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98ea8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98ea8-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98ea8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98ea8-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="98ea8-127">INPUTS</span></span>

### <span data-ttu-id="98ea8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="98ea8-128">System.String</span></span>

## <span data-ttu-id="98ea8-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="98ea8-129">OUTPUTS</span></span>

### <span data-ttu-id="98ea8-130">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="98ea8-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="98ea8-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="98ea8-131">NOTES</span></span>

## <span data-ttu-id="98ea8-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="98ea8-132">RELATED LINKS</span></span>

[<span data-ttu-id="98ea8-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="98ea8-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSettings.md)

[<span data-ttu-id="98ea8-134">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="98ea8-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


