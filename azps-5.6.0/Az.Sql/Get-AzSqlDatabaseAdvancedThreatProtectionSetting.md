---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/powershell/module/az.sql/get-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 570b56ab98e8679a47bcb26b36f1bea4d24bd275
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939864"
---
# <span data-ttu-id="b74b4-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="b74b4-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="b74b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b74b4-102">SYNOPSIS</span></span>
<span data-ttu-id="b74b4-103">Ruft die erweiterten Einstellungen für den Bedrohungsschutz für eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="b74b4-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="b74b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b74b4-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSetting [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b74b4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b74b4-105">DESCRIPTION</span></span>
<span data-ttu-id="b74b4-106">Das **Get-AzSqlDatabaseAdvancedThreatProtectionSetting-Cmdlet** ruft die erweiterten Bedrohungsschutzeinstellungen einer Azure SQL ab.</span><span class="sxs-lookup"><span data-stu-id="b74b4-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="b74b4-107">Um dieses Cmdlet zu verwenden, geben Sie die *Parameter ResourceGroupName,* *ServerName* und *DatabaseName* an, um die Datenbank zu identifizieren, für die dieses Cmdlet die Einstellungen erhält.</span><span class="sxs-lookup"><span data-stu-id="b74b4-107">To use this cmdlet, specify the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="b74b4-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b74b4-108">EXAMPLES</span></span>

### <span data-ttu-id="b74b4-109">Beispiel 1: Erhalten der erweiterten Einstellungen für den Bedrohungsschutz für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="b74b4-109">Example 1: Get the advanced threat protection settings for a database</span></span>
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

<span data-ttu-id="b74b4-110">Dieser Befehl ruft die erweiterten Bedrohungsschutzeinstellungen für eine Datenbank mit dem Namen Datenbank01 ab.</span><span class="sxs-lookup"><span data-stu-id="b74b4-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="b74b4-111">Die Datenbank befindet sich auf dem Server mit dem Namen Server01, der der Ressourcengruppe ResourceGroup11 zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="b74b4-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="b74b4-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b74b4-112">PARAMETERS</span></span>

### <span data-ttu-id="b74b4-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b74b4-113">-DatabaseName</span></span>
<span data-ttu-id="b74b4-114">Gibt den Namen einer Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="b74b4-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="b74b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b74b4-115">-DefaultProfile</span></span>
<span data-ttu-id="b74b4-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b74b4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b74b4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b74b4-117">-ResourceGroupName</span></span>
<span data-ttu-id="b74b4-118">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="b74b4-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="b74b4-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="b74b4-119">-ServerName</span></span>
<span data-ttu-id="b74b4-120">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="b74b4-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="b74b4-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b74b4-121">-Confirm</span></span>
<span data-ttu-id="b74b4-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b74b4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b74b4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b74b4-123">-WhatIf</span></span>
<span data-ttu-id="b74b4-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b74b4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b74b4-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b74b4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b74b4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b74b4-126">CommonParameters</span></span>
<span data-ttu-id="b74b4-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b74b4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b74b4-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b74b4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b74b4-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b74b4-129">INPUTS</span></span>

### <span data-ttu-id="b74b4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b74b4-130">System.String</span></span>

## <span data-ttu-id="b74b4-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b74b4-131">OUTPUTS</span></span>

### <span data-ttu-id="b74b4-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="b74b4-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="b74b4-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b74b4-133">NOTES</span></span>

## <span data-ttu-id="b74b4-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b74b4-134">RELATED LINKS</span></span>

[<span data-ttu-id="b74b4-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="b74b4-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)



