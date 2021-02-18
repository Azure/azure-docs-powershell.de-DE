---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8ff7e7df12bc1415cfe6e4b14dc673e93d8d8791
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173852"
---
# <span data-ttu-id="8aa04-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="8aa04-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="8aa04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8aa04-102">SYNOPSIS</span></span>
<span data-ttu-id="8aa04-103">Entfernt die erweiterten Threat Protection-Einstellungen von einem Server.</span><span class="sxs-lookup"><span data-stu-id="8aa04-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="8aa04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8aa04-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8aa04-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8aa04-105">DESCRIPTION</span></span>
<span data-ttu-id="8aa04-106">Das Clear-AzSqlServerAdvancedThreatProtectionSetting entfernt die erweiterten Threat Protection-Einstellungen von einem Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8aa04-106">The Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="8aa04-107">Um dieses Cmdlet zu verwenden, geben Sie die Parameter "ResourceGroupName" und "ServerName" an, um den Server zu identifizieren, von dem dieses Cmdlet die Einstellungen entfernt.</span><span class="sxs-lookup"><span data-stu-id="8aa04-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="8aa04-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8aa04-108">EXAMPLES</span></span>

### <span data-ttu-id="8aa04-109">Beispiel 1: Entfernen erweiterter Threat Protection-Einstellungen für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="8aa04-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="8aa04-110">Mit diesem Befehl werden die erweiterten Threat Protection-Einstellungen von einem Server namens Server01 entfernt.</span><span class="sxs-lookup"><span data-stu-id="8aa04-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="8aa04-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8aa04-111">PARAMETERS</span></span>

### <span data-ttu-id="8aa04-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aa04-112">-DefaultProfile</span></span>
<span data-ttu-id="8aa04-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8aa04-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8aa04-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8aa04-114">-PassThru</span></span>
<span data-ttu-id="8aa04-115">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="8aa04-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8aa04-116">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="8aa04-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8aa04-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aa04-117">-ResourceGroupName</span></span>
<span data-ttu-id="8aa04-118">Gibt den Namen der Ressourcengruppe an, der der Server zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8aa04-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="8aa04-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8aa04-119">-ServerName</span></span>
<span data-ttu-id="8aa04-120">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="8aa04-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="8aa04-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8aa04-121">-Confirm</span></span>
<span data-ttu-id="8aa04-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8aa04-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aa04-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8aa04-123">-WhatIf</span></span>
<span data-ttu-id="8aa04-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8aa04-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8aa04-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8aa04-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aa04-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aa04-126">CommonParameters</span></span>
<span data-ttu-id="8aa04-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aa04-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aa04-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8aa04-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aa04-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8aa04-129">INPUTS</span></span>

### <span data-ttu-id="8aa04-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8aa04-130">System.String</span></span>

## <span data-ttu-id="8aa04-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8aa04-131">OUTPUTS</span></span>

### <span data-ttu-id="8aa04-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="8aa04-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="8aa04-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8aa04-133">NOTES</span></span>

## <span data-ttu-id="8aa04-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8aa04-134">RELATED LINKS</span></span>

[<span data-ttu-id="8aa04-135">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="8aa04-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

