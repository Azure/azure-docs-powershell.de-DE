---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8ff7e7df12bc1415cfe6e4b14dc673e93d8d8791
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295156"
---
# <span data-ttu-id="c54a3-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="c54a3-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="c54a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c54a3-102">SYNOPSIS</span></span>
<span data-ttu-id="c54a3-103">Entfernt die erweiterten Threat Protection-Einstellungen von einem Server.</span><span class="sxs-lookup"><span data-stu-id="c54a3-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="c54a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c54a3-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c54a3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c54a3-105">DESCRIPTION</span></span>
<span data-ttu-id="c54a3-106">Das Clear-AzSqlServerAdvancedThreatProtectionSetting entfernt die erweiterten Threat Protection-Einstellungen von einem Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c54a3-106">The Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="c54a3-107">Um dieses Cmdlet zu verwenden, geben Sie die Parameter "ResourceGroupName" und "ServerName" an, um den Server zu identifizieren, von dem dieses Cmdlet die Einstellungen entfernt.</span><span class="sxs-lookup"><span data-stu-id="c54a3-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="c54a3-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c54a3-108">EXAMPLES</span></span>

### <span data-ttu-id="c54a3-109">Beispiel 1: Entfernen erweiterter Threat Protection-Einstellungen für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="c54a3-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="c54a3-110">Mit diesem Befehl werden die erweiterten Threat Protection-Einstellungen von einem Server namens Server01 entfernt.</span><span class="sxs-lookup"><span data-stu-id="c54a3-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="c54a3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c54a3-111">PARAMETERS</span></span>

### <span data-ttu-id="c54a3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c54a3-112">-DefaultProfile</span></span>
<span data-ttu-id="c54a3-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c54a3-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c54a3-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c54a3-114">-PassThru</span></span>
<span data-ttu-id="c54a3-115">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c54a3-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c54a3-116">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="c54a3-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c54a3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c54a3-117">-ResourceGroupName</span></span>
<span data-ttu-id="c54a3-118">Gibt den Namen der Ressourcengruppe an, der der Server zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c54a3-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="c54a3-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c54a3-119">-ServerName</span></span>
<span data-ttu-id="c54a3-120">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="c54a3-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="c54a3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c54a3-121">-Confirm</span></span>
<span data-ttu-id="c54a3-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c54a3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c54a3-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c54a3-123">-WhatIf</span></span>
<span data-ttu-id="c54a3-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c54a3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c54a3-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c54a3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c54a3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c54a3-126">CommonParameters</span></span>
<span data-ttu-id="c54a3-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c54a3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c54a3-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c54a3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c54a3-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c54a3-129">INPUTS</span></span>

### <span data-ttu-id="c54a3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c54a3-130">System.String</span></span>

## <span data-ttu-id="c54a3-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c54a3-131">OUTPUTS</span></span>

### <span data-ttu-id="c54a3-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="c54a3-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="c54a3-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c54a3-133">NOTES</span></span>

## <span data-ttu-id="c54a3-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c54a3-134">RELATED LINKS</span></span>

[<span data-ttu-id="c54a3-135">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="c54a3-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

