---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8090ee9cf6ec251668dbeadba6b18a7cde4898c4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361877"
---
# <span data-ttu-id="0b5fe-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="0b5fe-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="0b5fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b5fe-102">SYNOPSIS</span></span>
<span data-ttu-id="0b5fe-103">Ruft die erweiterten Threat Protection-Einstellungen für eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="0b5fe-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="0b5fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b5fe-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSetting [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b5fe-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b5fe-105">DESCRIPTION</span></span>
<span data-ttu-id="0b5fe-106">Das **Cmdlet "Get-AzSqlDatabaseAdvancedThreatProtectionSetting"** ruft die erweiterten Threat Protection-Einstellungen einer Azure SQL ab.</span><span class="sxs-lookup"><span data-stu-id="0b5fe-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="0b5fe-107">Um dieses Cmdlet zu verwenden, geben Sie die Parameter *"ResourceGroupName",* *"ServerName"* und *"DatabaseName"* an, um die Datenbank zu identifizieren, für die dieses Cmdlet die Einstellungen erhält.</span><span class="sxs-lookup"><span data-stu-id="0b5fe-107">To use this cmdlet, specify the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="0b5fe-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0b5fe-108">EXAMPLES</span></span>

### <span data-ttu-id="0b5fe-109">Beispiel 1: Erhalten der erweiterten Threat Protection-Einstellungen für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="0b5fe-109">Example 1: Get the advanced threat protection settings for a database</span></span>
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

<span data-ttu-id="0b5fe-110">Dieser Befehl ruft die erweiterten Threat Protection-Einstellungen für eine Datenbank mit dem Namen "Database01" ab.</span><span class="sxs-lookup"><span data-stu-id="0b5fe-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="0b5fe-111">Die Datenbank befindet sich auf dem Server mit dem Namen Server01, der der Ressourcengruppe "ResourceGroup11" zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="0b5fe-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="0b5fe-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b5fe-112">PARAMETERS</span></span>

### <span data-ttu-id="0b5fe-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0b5fe-113">-DatabaseName</span></span>
<span data-ttu-id="0b5fe-114">Gibt den Namen einer Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="0b5fe-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="0b5fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b5fe-115">-DefaultProfile</span></span>
<span data-ttu-id="0b5fe-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0b5fe-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b5fe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b5fe-117">-ResourceGroupName</span></span>
<span data-ttu-id="0b5fe-118">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="0b5fe-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="0b5fe-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0b5fe-119">-ServerName</span></span>
<span data-ttu-id="0b5fe-120">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="0b5fe-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="0b5fe-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b5fe-121">-Confirm</span></span>
<span data-ttu-id="0b5fe-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b5fe-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b5fe-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0b5fe-123">-WhatIf</span></span>
<span data-ttu-id="0b5fe-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b5fe-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b5fe-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b5fe-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b5fe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b5fe-126">CommonParameters</span></span>
<span data-ttu-id="0b5fe-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b5fe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b5fe-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b5fe-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b5fe-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0b5fe-129">INPUTS</span></span>

### <span data-ttu-id="0b5fe-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0b5fe-130">System.String</span></span>

## <span data-ttu-id="0b5fe-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0b5fe-131">OUTPUTS</span></span>

### <span data-ttu-id="0b5fe-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="0b5fe-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="0b5fe-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0b5fe-133">NOTES</span></span>

## <span data-ttu-id="0b5fe-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0b5fe-134">RELATED LINKS</span></span>

[<span data-ttu-id="0b5fe-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="0b5fe-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)



