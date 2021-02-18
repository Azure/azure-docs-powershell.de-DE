---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: a9d2d82ae9b35b79701d071fa7598cf40b185cd5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409816"
---
# <span data-ttu-id="1a249-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="1a249-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="1a249-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a249-102">SYNOPSIS</span></span>
<span data-ttu-id="1a249-103">Ruft die erweiterten Threat Protection-Einstellungen für einen Server ab.</span><span class="sxs-lookup"><span data-stu-id="1a249-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="1a249-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a249-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSetting -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a249-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a249-105">DESCRIPTION</span></span>
<span data-ttu-id="1a249-106">Das **Cmdlet "Get-AzSqlServerAdvancedThreatProtectionSetting"** ruft die erweiterten Threat Protection-Einstellungen eines Azure SQL ab.</span><span class="sxs-lookup"><span data-stu-id="1a249-106">The **Get-AzSqlServerAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="1a249-107">Um dieses Cmdlet zu verwenden, geben Sie die *Parameter "ResourceGroupName"* und *"ServerName"* an, um den Server zu identifizieren, für den dieses Cmdlet die Einstellungen erhält.</span><span class="sxs-lookup"><span data-stu-id="1a249-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="1a249-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1a249-108">EXAMPLES</span></span>

### <span data-ttu-id="1a249-109">Beispiel 1: Erhalten der erweiterten Threat Protection-Einstellungen für einen Server</span><span class="sxs-lookup"><span data-stu-id="1a249-109">Example 1: Get the advanced threat protection settings for a server</span></span>
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

<span data-ttu-id="1a249-110">Dieser Befehl ruft die erweiterten Threat Protection-Einstellungen für einen Server mit dem Namen Server01 ab.</span><span class="sxs-lookup"><span data-stu-id="1a249-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="1a249-111">Der Server ist der Ressourcengruppe "ResourceGroup11" zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="1a249-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="1a249-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a249-112">PARAMETERS</span></span>

### <span data-ttu-id="1a249-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a249-113">-DefaultProfile</span></span>
<span data-ttu-id="1a249-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1a249-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a249-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a249-115">-ResourceGroupName</span></span>
<span data-ttu-id="1a249-116">Gibt den Namen der Ressourcengruppe an, zu der der Server gehört.</span><span class="sxs-lookup"><span data-stu-id="1a249-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="1a249-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1a249-117">-ServerName</span></span>
<span data-ttu-id="1a249-118">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="1a249-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="1a249-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a249-119">-Confirm</span></span>
<span data-ttu-id="1a249-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1a249-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a249-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1a249-121">-WhatIf</span></span>
<span data-ttu-id="1a249-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a249-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a249-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a249-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a249-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a249-124">CommonParameters</span></span>
<span data-ttu-id="1a249-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a249-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a249-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a249-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a249-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1a249-127">INPUTS</span></span>

### <span data-ttu-id="1a249-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1a249-128">System.String</span></span>

## <span data-ttu-id="1a249-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1a249-129">OUTPUTS</span></span>

### <span data-ttu-id="1a249-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="1a249-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="1a249-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1a249-131">NOTES</span></span>

## <span data-ttu-id="1a249-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1a249-132">RELATED LINKS</span></span>


[<span data-ttu-id="1a249-133">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="1a249-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


