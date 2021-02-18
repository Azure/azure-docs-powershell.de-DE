---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 85a45c1a5f7c4d88adaf4e9b9da35b415b7a2093
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405804"
---
# <span data-ttu-id="fed0f-101">Get-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="fed0f-101">Get-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="fed0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fed0f-102">SYNOPSIS</span></span>
<span data-ttu-id="fed0f-103">Ruft die erweiterten Threat Protection-Einstellungen für eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="fed0f-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="fed0f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fed0f-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSettings [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fed0f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fed0f-105">DESCRIPTION</span></span>
<span data-ttu-id="fed0f-106">Das **Cmdlet "Get-AzSqlDatabaseAdvancedThreatProtectionSettings"** ruft die erweiterten Threat Protection-Einstellungen einer Azure SQL ab.</span><span class="sxs-lookup"><span data-stu-id="fed0f-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSettings** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="fed0f-107">Um dieses Cmdlet zu verwenden, geben Sie die Parameter *"ResourceGroupName",* *"ServerName"* und *"DatabaseName"* an, um die Datenbank zu identifizieren, für die dieses Cmdlet die Einstellungen erhält.</span><span class="sxs-lookup"><span data-stu-id="fed0f-107">To use this cmdlet, specify the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="fed0f-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fed0f-108">EXAMPLES</span></span>

### <span data-ttu-id="fed0f-109">Beispiel 1: Erhalten der erweiterten Threat Protection-Einstellungen für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="fed0f-109">Example 1: Get the advanced threat protection settings for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="fed0f-110">Dieser Befehl ruft die erweiterten Threat Protection-Einstellungen für eine Datenbank mit dem Namen "Database01" ab.</span><span class="sxs-lookup"><span data-stu-id="fed0f-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="fed0f-111">Die Datenbank befindet sich auf dem Server mit dem Namen Server01, der der Ressourcengruppe "ResourceGroup11" zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="fed0f-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="fed0f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fed0f-112">PARAMETERS</span></span>

### <span data-ttu-id="fed0f-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fed0f-113">-DatabaseName</span></span>
<span data-ttu-id="fed0f-114">Gibt den Namen einer Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="fed0f-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="fed0f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fed0f-115">-DefaultProfile</span></span>
<span data-ttu-id="fed0f-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fed0f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fed0f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fed0f-117">-ResourceGroupName</span></span>
<span data-ttu-id="fed0f-118">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="fed0f-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="fed0f-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fed0f-119">-ServerName</span></span>
<span data-ttu-id="fed0f-120">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="fed0f-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="fed0f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fed0f-121">-Confirm</span></span>
<span data-ttu-id="fed0f-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fed0f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fed0f-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fed0f-123">-WhatIf</span></span>
<span data-ttu-id="fed0f-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fed0f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fed0f-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fed0f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fed0f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fed0f-126">CommonParameters</span></span>
<span data-ttu-id="fed0f-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fed0f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fed0f-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fed0f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fed0f-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fed0f-129">INPUTS</span></span>

### <span data-ttu-id="fed0f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fed0f-130">System.String</span></span>

## <span data-ttu-id="fed0f-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fed0f-131">OUTPUTS</span></span>

### <span data-ttu-id="fed0f-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="fed0f-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="fed0f-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fed0f-133">NOTES</span></span>

## <span data-ttu-id="fed0f-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fed0f-134">RELATED LINKS</span></span>




