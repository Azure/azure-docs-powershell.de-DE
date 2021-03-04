---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/powershell/module/az.sql/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8c9f8bfad95a7bbefd6e685701813d0c383f2b8a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932227"
---
# <span data-ttu-id="f014b-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="f014b-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="f014b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f014b-102">SYNOPSIS</span></span>
<span data-ttu-id="f014b-103">Entfernt die erweiterten Bedrohungsschutzeinstellungen aus einer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f014b-103">Removes the advanced threat protection settings from a database.</span></span>

## <span data-ttu-id="f014b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f014b-104">SYNTAX</span></span>

```
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f014b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f014b-105">DESCRIPTION</span></span>
<span data-ttu-id="f014b-106">Das **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting-Cmdlet** entfernt die erweiterten Bedrohungsschutzeinstellungen aus einer AzureAzure-SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f014b-106">The **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an AzureAzure SQL database.</span></span>
<span data-ttu-id="f014b-107">Um dieses Cmdlet zu verwenden, geben Sie die *Parameter ResourceGroupName* und *ServerName* an, um die Datenbank zu identifizieren, aus der dieses Cmdlet die Einstellungen entfernt.</span><span class="sxs-lookup"><span data-stu-id="f014b-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="f014b-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f014b-108">EXAMPLES</span></span>

### <span data-ttu-id="f014b-109">Beispiel 1: Entfernen erweiterter Bedrohungsschutzeinstellungen für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="f014b-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\>Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="f014b-110">Mit diesem Befehl werden die erweiterten Einstellungen für den Bedrohungsschutz aus einer Datenbank mit dem Namen Datenbank01 auf dem Server mit dem Namen Server01 entfernt.</span><span class="sxs-lookup"><span data-stu-id="f014b-110">This command removes the advanced threat protection settings from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="f014b-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f014b-111">PARAMETERS</span></span>

### <span data-ttu-id="f014b-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f014b-112">-DatabaseName</span></span>
<span data-ttu-id="f014b-113">Gibt den Namen einer Datenbank an, in der die erweiterten Bedrohungsschutzeinstellungen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f014b-113">Specifies the name of a database where the advanced threat protection settings should be removed.</span></span>

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

### <span data-ttu-id="f014b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f014b-114">-DefaultProfile</span></span>
<span data-ttu-id="f014b-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f014b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f014b-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f014b-116">-PassThru</span></span>
<span data-ttu-id="f014b-117">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f014b-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f014b-118">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="f014b-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f014b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f014b-119">-ResourceGroupName</span></span>
<span data-ttu-id="f014b-120">Gibt den Namen der Ressourcengruppe an, zu der der Server gehört.</span><span class="sxs-lookup"><span data-stu-id="f014b-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="f014b-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="f014b-121">-ServerName</span></span>
<span data-ttu-id="f014b-122">Gibt den Namen eines Servers an, auf dem die Datenbank ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f014b-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="f014b-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f014b-123">-Confirm</span></span>
<span data-ttu-id="f014b-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f014b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f014b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f014b-125">-WhatIf</span></span>
<span data-ttu-id="f014b-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f014b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f014b-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f014b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f014b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f014b-128">CommonParameters</span></span>
<span data-ttu-id="f014b-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f014b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f014b-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f014b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f014b-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f014b-131">INPUTS</span></span>

### <span data-ttu-id="f014b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f014b-132">System.String</span></span>

## <span data-ttu-id="f014b-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f014b-133">OUTPUTS</span></span>

### <span data-ttu-id="f014b-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="f014b-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="f014b-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f014b-135">NOTES</span></span>

## <span data-ttu-id="f014b-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f014b-136">RELATED LINKS</span></span>

[<span data-ttu-id="f014b-137">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="f014b-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


