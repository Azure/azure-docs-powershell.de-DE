---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4a576c930d8ff1c53c6c9e92c7d87664aef4da4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948416"
---
# <span data-ttu-id="eeb2c-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="eeb2c-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="eeb2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eeb2c-102">SYNOPSIS</span></span>
<span data-ttu-id="eeb2c-103">Entfernt die erweiterten Bedrohungsschutzeinstellungen von einem Server.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="eeb2c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eeb2c-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeb2c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eeb2c-105">DESCRIPTION</span></span>
<span data-ttu-id="eeb2c-106">Das Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet entfernt die erweiterten Bedrohungsschutzeinstellungen von einem Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-106">The Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="eeb2c-107">Um dieses Cmdlet zu verwenden, geben Sie die Parameter ResourceGroupName und ServerName an, um den Server zu identifizieren, von dem dieses Cmdlet die Einstellungen entfernt.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="eeb2c-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eeb2c-108">EXAMPLES</span></span>

### <span data-ttu-id="eeb2c-109">Beispiel 1: Entfernen erweiterter Bedrohungsschutzeinstellungen für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="eeb2c-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="eeb2c-110">Mit diesem Befehl werden die erweiterten Bedrohungsschutzeinstellungen von einem Server namens Server01 entfernt.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="eeb2c-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="eeb2c-111">PARAMETERS</span></span>

### <span data-ttu-id="eeb2c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeb2c-112">-DefaultProfile</span></span>
<span data-ttu-id="eeb2c-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="eeb2c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eeb2c-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eeb2c-114">-PassThru</span></span>
<span data-ttu-id="eeb2c-115">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="eeb2c-116">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="eeb2c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeb2c-117">-ResourceGroupName</span></span>
<span data-ttu-id="eeb2c-118">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="eeb2c-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="eeb2c-119">-ServerName</span></span>
<span data-ttu-id="eeb2c-120">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="eeb2c-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eeb2c-121">-Confirm</span></span>
<span data-ttu-id="eeb2c-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeb2c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeb2c-123">-WhatIf</span></span>
<span data-ttu-id="eeb2c-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeb2c-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeb2c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeb2c-126">CommonParameters</span></span>
<span data-ttu-id="eeb2c-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeb2c-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eeb2c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeb2c-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eeb2c-129">INPUTS</span></span>

### <span data-ttu-id="eeb2c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="eeb2c-130">System.String</span></span>

## <span data-ttu-id="eeb2c-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eeb2c-131">OUTPUTS</span></span>

### <span data-ttu-id="eeb2c-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="eeb2c-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="eeb2c-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="eeb2c-133">NOTES</span></span>

## <span data-ttu-id="eeb2c-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="eeb2c-134">RELATED LINKS</span></span>

[<span data-ttu-id="eeb2c-135">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="eeb2c-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

